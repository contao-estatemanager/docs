---
description: Zuordnung von Feldern für Immobiliendatensätze
---

# Feldzuordnungen

**Innerhalb jeder Schnittstelle** ist es möglich, jedes **Feld** einer **Import-XML** einem bestimmten Feld der im Contao EstateManager existierenden Objektfelder **zuzuordnen** und zu formatieren.

Die XML-Datei, welche die OpenImmo Felder beinhaltet, kann sich auch innerhalb eines importierten Archivs befinden.

Feldzuordnungen sind notwendig für das Speichern der Informationen von importierten Objekten.

{% hint style="danger" %}
Wenn **keine Feldzuordnungen** angelegt sind, können Objekte **nicht synchronisiert** werden!
{% endhint %}

### OpenImmo Feldzuordnungen erstellen

Nach der Erstellung einer neuen Schnittstelle **existieren noch keine Zuordnungen** für Felder des OpenImmo-Standards.

{% hint style="info" %}
Durch **Felder zurücksetzen** ![](../../../.gitbook/assets/sync.svg) kann eine Standardzuordnung erstellt werden.
{% endhint %}

### Neue Feldzuordnung erstellen

Neue Feldzuordnungen können über **Neue Feldzuordnung** ![](../../../.gitbook/assets/new.svg) erstellt werden.

### Typ

:small\_blue\_diamond:`Typ`

_Hier kann der Datentyp ausgewählt werden, auf den die Feldzuordnung verweisen soll:_

* Immobilie\
  _Bezieht sich auf die Tabelle **tl\_real\_estate** und somit auf einen Immobiliendatensatz._
* Kontaktperson\
  _Bezieht sich auf die Tabelle **tl\_contact\_person** und somit auf eine Kontaktperson (Innerhalb der Anbieterverwaltung)._

:small\_blue\_diamond:`Attribut`

_Attribute sind Informationen für den ausgewählten Typen, welche in der jeweiligen Datenbank gespeichert werden. Hier kann das Datenbankfeld für die Zuordnung ausgewählt werden._

### Feld-Einstellungen

Die Feldeinstellungen dienen dazu, die übertragenen Feldinformationen innerhalb einer Importdatei ermitteln zu können. Mithilfe dieser Einstellungen ist es möglich, verschiedene Importdateien einzulesen, um sie anschließend korrekt in das System zu überführen.

:small\_blue\_diamond:`OpenImmo-Feldgruppe`

_Feldgruppen dienen zur Identifizierung einer Kategorie. Innerhalb einer Feldgruppe können Felder gefunden werden._

#### Beispielhafte Ausschnitte aus einer Import.xml

{% tabs %}
{% tab title="Normale Feldgruppe" %}
Im nachfolgenden Beispiel ist `<geo>` die OpenImmo-Feldgruppe, die innen liegenden Informationen sind OpenImmo-Felder:

```
<geo>
    <plz>12345</plz>
    <ort>Musterstadt</ort>
    <strasse>Musterstrasse</strasse>
    <hausnummer>1</hausnummer>
</geo>
```

Die **OpenImmo-Feldgruppe** für die Postleitzahl einer Immobilie wäre somit:

> **geo**
{% endtab %}

{% tab title="Verschachtelte Feldgruppe" %}
Im nachfolgenden Beispiel ist die Information des OpenImmo-Feldes `<gueltis_bis>` innerhalb von `<energiepass>`, welches sich wiederum in `<zustand_angaben>`befindet.&#x20;

```
<zustand_angaben>
    <baujahr>1970</baujahr>
    <energiepass>
        <epart>BEDARF</epart>
        <gueltig_bis>01.01.1970</gueltig_bis>
        <endenergiebedarf>34.6</endenergiebedarf>
    </energiepass>
</zustand_angaben>
```

Der Zugriff auf das OpenImmo-Feld `<gueltig_bis>` wäre mit folgender Konfiguration der **OpenImmo-Feldgruppe** gegeben:

> **zustand\_angaben/energiepass**
{% endtab %}
{% endtabs %}



:small\_blue\_diamond:`OpenImmo-Feld`

_Innerhalb der OpenImmo-Felder befinden sich Werte . Auf diese kann über verschiedene Wege zugegriffen werden:_

#### Beispielhafte Ausschnitte aus einer Import.xml

{% tabs %}
{% tab title="Element-Werte" %}
Im nachfolgenden Beispiel wird der Wert **Mustermann** innerhalb von `<name>` ausgelesen.

```
<kontaktperson>
    <email_zentrale>info@estatemanager.com</email_zentrale>
    <tel_zentrale>02171/4015150</tel_zentrale>
    <name>Mustermann</name>
    <vorname>Max</vorname>
    <anrede>Herr</anrede>
</kontaktperson>
```

Hierfür ist folgende Konfiguration notwendig:

> **OpenImmo-Feldgruppe:** kontaktperson
>
> **OpenImmo-Feld:** name
{% endtab %}

{% tab title="Attribut-Werte" %}
Im nachfolgenden Beispiel wird der Wert **51.06995** des Attributs `breitengrad` innerhalb von `<geokoordinaten>` ausgelesen.\
\
Auf Attributwerte kann mithilfe von <mark style="color:blue;">`element@attribut`</mark> zugegriffen werden.

```
<geo>
    <plz>12345</plz>
    <ort>Musterstadt</ort>
    <geokoordinaten breitengrad="51.06995" laengengrad="6.99735"/>
    <strasse>Musterstr.</strasse>
    <hausnummer>123</hausnummer>
    <land iso_land="DEU"/>
</geo>
```

Hierfür ist folgende Konfiguration notwendig:

> **OpenImmo-Feldgruppe:** geo
>
> **OpenImmo-Feld:** geokoordinaten@breitengrad
{% endtab %}

{% tab title="Attribut-Namen" %}
In manchen Fällen enthält ein Element mehrere Attribute mit Wahrheitswerten (Boolean).\
Mit folgenden Konfigurationen lassen sich die nachfolgenden Beispiele auslesen:

\


**Beispiel 1**\
Jedes Objekt enthält **nur eine Nutzungsart**. In der XML werden jedoch alle Nutzungsarten als Attribute übertragen. **Nur eine** der Nutzungsarten **ist wahr**.\
In diesem Fall soll also der **Attributname** ausgegeben werden, dessen _Attributwert_ auf _true_ steht.\
\
Um **auf den einen Attributnamen** eines Elements **zuzugreifen**, der **wahr** ist, kann <mark style="color:blue;">`attribut@+`</mark> verwendet werden.

```
<objektkategorie>
    <nutzungsart WAZ="false" GEWERBE="false" ANLAGE="false" WOHNEN="true"/>
    <vermarktungsart KAUF="true" LEASING="false" ERBPACHT="false" MIETE_PACHT="false"/>
    <objektart>
        <grundstueck grundst_typ="WOHNEN"/>
    </objektart>
</objektkategorie>
```

Hierfür ist folgende Konfiguration notwendig:

> **OpenImmo-Feldgruppe:** objektkategorie
>
> **OpenImmo-Feld:** nutzungsart@+

Der Rückgabewert mit der oben genannten Konfiguration wäre `WOHNEN`.

\


**Beispiel 2**\
In diesem Beispiel sind **mehrere Attribute** innerhalb eines Elements von Wichtigkeit. Es sollen **alle Attributnamen ausgelesen** werden, in welchen der Wert **wahr** ist.\
\
Um auf **alle Attributnamen** eines Elements zuzugreifen, **die wahr sind**, kann <mark style="color:blue;">`attribut@#`</mark> verwendet werden.

```
<ausstattung>
    <boden FLIESEN="true" TEPPICH="true" PARKETT="true" LAMINAT="true" MARMOR="true"/>
    <heizungsart ZENTRAL="true"/>
    <befeuerung OEL="true"/>
</ausstattung>
```

Hierfür ist folgende Konfiguration notwendig:

> **OpenImmo-Feldgruppe:** ausstattung
>
> **OpenImmo-Feld:** boden@#

Der Rückgabewert mit der oben genannten Konfiguration wäre:\
`FLIESEN TEPPICH PARKETT LAMINAT MARMOR`.

\


**Beispiel 3**\
In diesem Beispiel sollen alle Attribute eines Elements unabhängig des Attributwerts zurückgegeben werden.\
\
Um auf **alle Attributnamen** eines Elements zuzugreifen, **unabhängig des Attributwerts**, kann <mark style="color:blue;">`attribut@*`</mark> verwendet werden.

```
<example>
    <element attribut1 attribut2 attribut3 attribut4/>
</example>
```

Hierfür ist folgende Konfiguration notwendig:

> **OpenImmo-Feldgruppe:** example
>
> **OpenImmo-Feld:** element@\*

Der Rückgabewert mit der oben genannten Konfiguration wäre:\
`attribut1 attribut2 attribut3 attribut4`.
{% endtab %}

{% tab title="Element-Namen" %}
Im nachfolgenden Beispiel wird der Name des Elements **buero\_praxen** innerhalb von `<objektart>` ausgelesen.\
\
Auf den **Namen des ersten Elements innerhalb eines Elternelements** kann mithilfe von <mark style="color:blue;">`elternelement@[1]`</mark> zugegriffen werden.

```
<objektkategorie>
    <objektart>
        <buero_praxen buero_typ="BUEROFLAECHE"/>
    </objektart>
</objektkategorie>
```

Hierfür ist folgende Konfiguration notwendig:

> **OpenImmo-Feldgruppe:** objektkategorie
>
> **OpenImmo-Feld:** objektart@\[1]

Sollte der Name des **zweiten** oder **dritten** Elementes von Bedeutung sein, kann man auch <mark style="color:blue;">`elternelement@[`</mark><mark style="color:blue;">**`2`**</mark><mark style="color:blue;">`]`</mark> oder <mark style="color:blue;">`elternelement@[`</mark><mark style="color:blue;">**`3`**</mark><mark style="color:blue;">`]`</mark> verwenden.
{% endtab %}
{% endtabs %}



:small\_blue\_diamond:`OpenImmo-Bedingungsfeld`

_Bedingungsfelder sind ähnlich der OpenImmo-Felder und dienen mithilfe des `OpenImmo-Bedingungswertes` der Überprüfung von Attributwerten._

#### Beispielhafter Ausschnitt aus einer Import.xml

{% tabs %}
{% tab title="Attributname" %}
Im nachfolgenden Beispiel sind `<infrastruktur>` und `<distanzen>` die OpenImmo-Feldgruppe, das Attribut **distanz\_zu** wäre das **OpenImmo-Bedingungsfeld**.\
\
Auf den Attributnamen kann mithilfe von <mark style="color:blue;">`@attributname`</mark> zugegriffen werden.

```
<infrastruktur>
    <distanzen distanz_zu="EINKAUFSMOEGLICHKEITEN">0.50</distanzen>
    <distanzen distanz_zu="FLUGHAFEN">25.00</distanzen>
    <distanzen distanz_zu="AUTOBAHN">2.00</distanzen>
    <distanzen distanz_zu="BUS">0.20</distanzen>
</infrastruktur>
```

Folgende Konfiguration ist für die Verwendung des Attributnamen als Bedingungsfeld von Nöten:

> **OpenImmo-Feldgruppe:**         infrastruktur/distanzen
>
> **OpenImmo-Feld:**                    &#x20;
>
> **OpenImmo-Bedingungsfeld:** @distanz\_zu

{% hint style="warning" %}
Ein Bedingungsfeld **benötigt immer einen Bedingungswert**, welcher überprüft werden muss.
{% endhint %}
{% endtab %}
{% endtabs %}



:small\_blue\_diamond:`OpenImmo-Bedingungswert`

_Der Bedingungswert ist der zu überprüfende **Attributwert** des Attributnamen, welcher im OpenImmo-Bedingungsfeld eingetragen wird._\
_Mithilfe eines Bedingungswertes kann ein Wert innerhalb mehrerer gleichnamiger Elemente ausgelesen werden._

#### Beispielhafte_r_ Ausschnitt aus einer Import.xml

{% tabs %}
{% tab title="Attributwert" %}
Im nachfolgenden Beispiel sind `<infrastruktur>` und `<distanzen>` die OpenImmo-Feldgruppe, das Attribut `distanz_zu` ist das OpenImmo-Bedingungsfeld.\
\
Es soll auf den Wert des Elements `<distanzen distanz_zu="FLUGHAFEN">25.00</distanzen>` zugegriffen werden.\
\
Das Attribut `distanz_zu` ist das _OpenImmo-Bedingungsfeld_.\
Der Wert **FLUGHAFEN** ist der **OpenImmo-Bedingungswert**.

```
<infrastruktur>
    <distanzen distanz_zu="EINKAUFSMOEGLICHKEITEN">0.50</distanzen>
    <distanzen distanz_zu="FLUGHAFEN">25.00</distanzen>
    <distanzen distanz_zu="AUTOBAHN">2.00</distanzen>
    <distanzen distanz_zu="BUS">0.20</distanzen>
</infrastruktur>
```

Folgende Konfiguration ist für die Überprüfung des Attributwertes von Nöten:

> **OpenImmo-Feldgruppe:**           infrastruktur/distanzen
>
> **OpenImmo-Feld:**                      &#x20;
>
> **OpenImmo-Bedingungsfeld:**   @distanz\_zu
>
> **OpenImmo-Bedingungswert:**  FLUGHAFEN

Der Rückgabewert mit der oben genannten Konfiguration wäre:\
`25.00`.
{% endtab %}
{% endtabs %}



:small\_blue\_diamond:`Werte serialisieren`

_Mit dieser Option lassen sich gefundene Werte serialisieren. Anwendung findet diese Option z. B. bei Bildern eines Objektes._

{% hint style="warning" %}
Diese Einstellung ist **notwendig für Felder**, welche **in Contao serialisiert** sind und als **ein Wert** in der **Datenbank gespeichert** werden. Ein Beispiel für einen serialisierten Wert in Contao wäre das Feld `multiSRC`.
{% endhint %}

#### Beispielhafter Ausschnitt aus einer Import.xml

{% tabs %}
{% tab title="Serialisierung" %}
Im nachfolgenden Beispiel sind:

* `<anhaenge>` und `<anhang>` die **OpenImmo-Feldgruppe**
* `<daten>` und `<pfad>` die **OpenImmo-Felder**
* `@gruppe` ist das **OpenImmo-Bedingungsfeld**
* `BILD` ist der zu überprüfende **OpenImmo-Bedingungswert**

\
Es sollen **alle Werte** innerhalb von **anhang/daten/pfad** ausgegeben werden, in welchem `<anhang>` das **Attribut** `gruppe` und den **Attributwert** `BILD` besitzt.

Da es sich um mehrere Werte handelt, welche dem System übergeben werden sollen, **kann hier serialisiert** werden.

```
<anhaenge>
    <anhang location="EXTERN" gruppe="TITELBILD">
        <anhangtitel>Immobilie 1</anhangtitel>
        <format>jpg</format>
        <daten>
            <pfad>Foto_1.jpg</pfad>
        </daten>
    </anhang>
    <anhang location="EXTERN" gruppe="BILD">
        <anhangtitel>Bild 1</anhangtitel>
        <format>jpg</format>
        <daten>
            <pfad>Bild_1.jpg</pfad>
        </daten>
    </anhang>
    <anhang location="EXTERN" gruppe="BILD">
        <anhangtitel>Bild 2</anhangtitel>
        <format>jpg</format>
        <daten>
            <pfad>Bild_2.jpg</pfad>
        </daten>
    </anhang>
    <anhang location="EXTERN" gruppe="BILD">
        <anhangtitel>Bild 3</anhangtitel>
        <format>jpg</format>
        <daten>
            <pfad>Bild_3.jpg</pfad>
        </daten>
    </anhang>
    <anhang location="EXTERN" gruppe="BILD">
        <anhangtitel>Bild 4</anhangtitel>
        <format>jpg</format>
        <daten>
            <pfad>Bild_3.jpg</pfad>
        </daten>
    </anhang>
</anhaenge>
```

Folgende Konfiguration dient der Serialisierung der Werte:

> **OpenImmo-Feldgruppe:**           anhaenge/anhang
>
> **OpenImmo-Feld:**                       daten/pfad
>
> **OpenImmo-Bedingungsfeld:**   @gruppe
>
> **OpenImmo-Bedingungswert:**  BILD\
> \
> **Werte Serialisieren:** ✅

Der Rückgabewert mit der oben genannten Konfiguration wäre:\
`{Bild1.jpg, Bild2.jpg, Bild3.jpg, Bild4.jpg}`
{% endtab %}
{% endtabs %}



:small\_blue\_diamond:`Leeren Wert mappen`

_Wenn importierte Objekte trotz **nicht-existenter Informationen in der Import.xml** einen **Standardwer**t erhalten sollen, kann hier bei Aktivierung der Checkbox, ein **gewünschter Standardwert** eingetragen werden._

### Formatierung

Durch Formatierungen können die eingelesenen Werte vor der Speicherung in die Datenbank in eine gewünschte Form umgewandelt werden.

:small\_blue\_diamond:`Formatierung`

_Hier kann ausgewählt werden, **welche Formatierung** angewendet werden soll. Folgende Optionen stehen zur Verfügung:_

* Keine
* Zahl
* Datum
* Text
* Boolescher Wert

#### Zahl (Formatierung)

Kürzt eine Zahl anhand der übergebenen Dezimalstellen.

> Beispiel:\
> **Anzahl an Dezimalstellen:** 2\
> \
> Aus `5000` wird `50.00`

{% hint style="info" %}
Nutzt die Funktion [**number\_format()**](https://www.php.net/manual/de/function.number-format.php)****
{% endhint %}

#### Datum (Formatierung)

Wandelt ein übertragenes Datum in einen Timestamp um. Optional kann ein Datumsformat angegeben werden.

> Beispiel:\
> Aus `1990-03-21` wird `638006400`

{% hint style="info" %}
Nutzt die Funktion [**strtotime()**](https://www.php.net/manual/de/function.strtotime.php)****
{% endhint %}

#### Text (Formatierung)

Mithilfe der Text-Formatierung können gefundene Strings formatiert werden. Folgende Auswahlmöglichkeiten stehen zur Verfügung:

* Keine
* Kleinschreibung
* Großschreibung
* Erstes Zeichen groß
* Sonderzeichen ersetzen

{% tabs %}
{% tab title="Kleinschreibung" %}
**Setzt einen String in Kleinbuchstaben um.**

> Beispiel:\
> Aus `GEWERBE` wird `gewerbe`

{% hint style="info" %}
Nutzt die Funktion [**strtolower()**](https://php.net/manual/de/function.strtolower.php)****
{% endhint %}
{% endtab %}

{% tab title="Großschreibung" %}
**Wandelt alle Zeichen eines Strings in Großbuchstaben um.**

> Beispiel:\
> Aus `beispiel` wird `BEISPIEL`

{% hint style="info" %}
Nutzt die Funktion [**strtoupper()**](https://php.net/manual/de/function.strtoupper.php)****
{% endhint %}
{% endtab %}

{% tab title="Erstes Zeichen groß" %}
**Verwandelt das erste Zeichen eines Strings in einen Großbuchstaben.**

> Beispiel:\
> Aus `beispiel` wird `Beispiel`

{% hint style="info" %}
Nutzt die Funktion [**ucfirst()**](https://php.net/manual/de/function.ucfirst.php)****
{% endhint %}
{% endtab %}

{% tab title="Sonderzeichen ersetzen" %}
**Ersetzt folgende Sonderzeichen innerhalb eines übertragenen Strings.**

| Original | Umwandlung |
| -------- | ---------- |
| ‘        | '          |
| ’        | '          |
| ”        | "          |
| “        | "          |
|         | "          |
|         | "          |
| –        | -          |
| —        | -          |
|         | -          |
| …        | \&#8230;   |
{% endtab %}
{% endtabs %}

#### Trimmen (Textformatierung)

Entfernt Zwischenraumzeichen (oder andere Zeichen) am Anfang und Ende eines Strings.

{% hint style="info" %}
Nutzt die Funktion [**trim()**](https://www.php.net/manual/de/function.trim.php)****
{% endhint %}

#### Boolescher Wert (Formatierung)

Wandelt übertragene Werte in boolsche Werte um (0 und 1). Kann mithilfe von **Vergleichswert** auch zur Überprüfung von vorgegebenen Werten genutzt werden.

### Experten-Einstellungen

:small\_blue\_diamond:`Datei speichern`

_Hier kann angegeben werden, ob eine **Datei bei einer Feldzuordnung gespeichert** werden soll. Diese Option ist **nötig**, um **übertragene Dateien** für ein Objekt zu **speichern**._

Sollte sich im **Immobilien-Import** eine **Datei mit dem angegebenen Wert** befinden, wird diese Datei im Ordner der Immobilie **gespeichert**.

