---
description: Contao EstateManager Erweiterung
---

# Käufer- / Mieterfinder

{% hint style="alert" %}
Für diese Erweiterung wird es aufgrund geringer Nachfrage keine Nachfolger geben. Sollten Sie dennoch eine Kompatibilität mit Contao 5 wünschen, können Sie uns gerne [mit der Umsetzung beauftragen](https://www.oveleon.de/kontakt.html#kontaktformular):
{% endhint %}

![](../../.gitbook/assets/produktbild\_kaeufer-mieterfinder\_github.jpg)

Die `Käufer- / Mieterfinder` Erweiterung liefert ein Tool, welches Verkäufern / Immobilienbesitzern anhand der eigenen Immobilien-Eckdaten ermöglicht, passende Interessenten zu finden. Dabei können bis zu drei Bereiche ausgegeben und kombiniert werden.&#x20;

1. **Ermittlung der Immobilien-Eckdaten (Filter)**\
   _Ermöglicht die Filterung der Interessenten anhand eigener Immobilien-Eckdaten_\
   __
2. **Anzeige der gefundenen Interessenten (Liste)**\
   _Zeigt anonyme Daten der Interessenten wie Anzahl der Zimmer oder Preisvorstellungen._\
   __
3. **Kontaktaufnahme (Formular)**\
   ****Beliebiges Formular, welches über den von Contao mitgelieferten Formulargenerator angelegt werden kann.

{% hint style="warning" %}
Der Käufer- / Mieterfinder zeigt ausschließlich Daten (Suchanfragen) an, welche manuell im System angelegt, durch andere Systeme importiert wurden oder über ein Formular (Frontend) in die dafür vorgesehene Tabelle (`tl_search_criteria`) gespeichert werden.
{% endhint %}

### Installation

{% tabs %}
{% tab title="Composer" %}
```bash
$ composer require contao-estatemanager/lead-matching-tool
```
{% endtab %}

{% tab title="GitHub" %}
Installation direkt über GitHub:

[https://github.com/contao-estatemanager/lead-matching-tool](https://github.com/contao-estatemanager/lead-matching-tool)
{% endtab %}
{% endtabs %}

Nach der Installation muss das [Contao-Installtool](https://docs.contao.org/manual/de/installation/contao-installtool/) aufgerufen und die Datenbank aktualisiert werden.&#x20;

### Suchanfragen

Suchanfragen dienen als Grundlage des Käufer- / Mieterfinders und können über verschiedene Wege in das System überführt werden.

![](../../.gitbook/assets/grafik-onoffice-import.svg)

{% hint style="info" %}
Mit der Erweiterung [onOffice API Import](onoffice-api-import.md) können alle benötigten Daten für den Käufer- / Mieterfinders direkt aus onOffice importiert und aktuell gehalten werden.
{% endhint %}

### Konfiguration

Um das Tool im Frontend über das mitgelieferte Modul ausgeben lassen zu können, muss vorerst eine Konfiguration im Backend angelegt werden.

#### Titel / Grundkonfiguration

:small\_blue\_diamond:`Titel`

_Dieser Titel wird ausschließlich zu Beschreibungszwecken im  Backend verwendet._

:small\_blue\_diamond:_`Vermarktungsart`_

_Hier stehen drei Auswahlmöglichkeiten zur Verfügung. Bei Auswahl einer fest definierten Option wie **Kauf** oder **Miete**, wird die Auswahl der Vermarktungsart im Frontend unterbunden._

:small\_blue\_diamond:_`Regionen Eingabemodus`_

_Definiert die Möglichkeit, wie Regionen im Frontend ausgegeben und gewählt werden können. Regionen können im Reiter "Regionen" verwaltet werden. Bei Auswahl einer Umkreissuche (empfohlen) werden Längen- und Breitengrade in den Regionen vorausgesetzt._

#### _Daten-Konfiguration_

:small\_blue\_diamond:_`Vermarktungsarten`_

_Sofern die Vermarktungsart nicht fest definiert wurde, kann der Besucher aus den hier ausgewählten Vermarktungsarten wählen._

:small\_blue\_diamond:`Objektarten`

_Definiert die wählbaren Objektarten im Frontend. Objektarten können im Reiter "Objektarten" verwaltet werden._

#### _Suchanfragen / Liste_

:small\_blue\_diamond:`Feld Meta-Daten`

_Definiert die auszugebenden Felder der Suchaufträge innerhalb der Liste._

:small\_blue\_diamond:_`Überschrift`_

_Eine Überschrift, welche oberhalb der Liste ausgegeben wird._

:small\_blue\_diamond:_`Beschreibung`_

_Ein Beschreibungstext, welcher oberhalb der Liste ausgegeben wird._

:small\_blue\_diamond:_`Gesamtanzahl der Beiträge`_

_Definiert die Gesamtanzahl der Beiträge. Bei 0 werden alle Beiträge ausgegeben._

:small\_blue\_diamond:`Elemente pro Seite`

_Definiert die Anzahl pro Seite (Paginierung)._

:small\_blue\_diamond:_`Listen Element-Template`_

_Definiert das zu verwendende Template für Listenelemente._

:small\_blue\_diamond:_`Anzahl anzeigen`_

_Gibt die Anzahl der gefundenen Interessent aus und aktualisiert die Zahl sofort, sofern ein Filter verwendet und durch den Besucher angepasst wird._

#### _Filter / Immobilienformular_

:small\_blue\_diamond:`Filter hinzufügen`

_Definiert, ob ein Filter für Immobilien-Eckdaten aktiviert und angezeigt wird._

:small\_blue\_diamond:_`Überschrift`_

_Eine Überschrift, welche oberhalb des Filters ausgegeben wird._

:small\_blue\_diamond:_`Beschreibung`_

_Ein Beschreibungstext, welcher oberhalb der Liste ausgegeben wird._

:small\_blue\_diamond:_`Liste immer anzeigen`_

_Definiert, ob die Liste bereits ohne Filterung ausgegeben werden darf._

:small\_blue\_diamond:_`Immobilien-Formularfelder`_

_Definiert die Felder, welche im Filter ausgegeben werden. Das Feld Vermarktungsart wird nur ausgegeben, sofern keine feste Vermarktungsart unter "Daten-Konfiguration" gewählt wurde. Das Feld **Umkreis** wird nur berücksichtig, sofern eine Umkreissuche unter **Regionen Eingabemodus** ausgewählt wurde._

#### _Kontaktformular_

:small\_blue\_diamond:`Kontaktformular hinzufügen`

_Definiert, ob ein Kontaktformular ausgegeben werden soll._

:small\_blue\_diamond:_`Überschrift`_

_Eine Überschrift, welche oberhalb des Formulars ausgegeben wird._

:small\_blue\_diamond:_`Beschreibung`_

_Ein Beschreibungstext, welcher oberhalb des Formulars ausgegeben wird._

:small\_blue\_diamond:_`Kontaktformular immer anzeigen`_

_Definiert, ob das Kontaktformular bereits ohne Filterung ausgegeben werden darf._

:small\_blue\_diamond:_`Kontakt-Formular`_

_Definiert das auszugebende Formular, welches zuvor im Formulargenerator gebaut wurde._

### Module

Hier finden Sie eine Übersicht neuer (🟢) Module.

{% tabs %}
{% tab title="🟢 Käufer- / Mieterfinder" %}
Gibt das Tool "Käufer- / Mieterfinder" anhand einer Konfiguration aus.

**Einstellungen**

:small\_blue\_diamond:`Konfiguration`

_Die zu verwendende Konfiguration._

**Template**

:small\_orange\_diamond:`mod_lead_matching`

:small\_orange\_diamond:`search_criteria_item_default`
{% endtab %}
{% endtabs %}

### Lizenz

Für diese Erweiterung ist eine Lizenz erforderlich. Zum Erwerb einer Lizenz folge bitte den Schritten unter [Lizenzen](../lizenzen.md).
