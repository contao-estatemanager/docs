---
description: Zuordnung von Feldern für Immobiliendatensätze
---

# Feldzuordnungen

{% hint style="warning" %}
Dieser Bereich befindet sich zurzeit in Bearbeitung.
{% endhint %}

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

#### **Beispiele für OpenImmo-Feldgruppen**

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

{% tabs %}
{% tab title="Wert auslesen" %}
Im nachfolgenden Beispiel soll der Wert **Mustermann** innerhalb von `<name>` ausgelesen werden.

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
{% endtabs %}

:small\_blue\_diamond:`OpenImmo-Bedingungsfeld`



:small\_blue\_diamond:`OpenImmo-Bedingungswert`



:small\_blue\_diamond:`Werte serialisieren`



:small\_blue\_diamond:`Leeren Wert mappen`



### Formatierung



:small\_blue\_diamond:`Formatierung`



### Experten-Einstellungen



:small\_blue\_diamond:`Datei speichern`



