# Ähnliche Objekte

Die `Ähnliche Objekte` Erweiterung integriert die Möglichkeit, ähnliche Immobilien innerhalb eines Exposés zu filtern und auszugeben. Dabei können die Immobilien-Eigenschaften der derzeit betrachteten Immobilie für die Abfrage weiterer Objekte durch einen prozentualen Faktor vergröbert werden.

### Installation

{% tabs %}
{% tab title="Composer" %}
```bash
$ composer require contao-estatemanager/similar
```
{% endtab %}

{% tab title="Contao-Manager" %}
Über die Suche des Contao-Manager kann der Begriff `EstateManager` oder `similar` gesucht werden. Anschließen wählt man das Paket `Contao EstateManager Similar` über die Schaltfläche "_hinzufügen_" aus und klickt zum installieren über den Reiter "_Pakete_" auf die Schaltfläche "_Änderungen anwenden_". Eine detaillierte Anleitung wie man mit dem Contao-Manager arbeitet findest du [hier](https://docs.contao.org/manual/de/installation/erweiterungen-installieren/).
{% endtab %}

{% tab title="GitHub" %}
Installation direkt über GitHub:

[https://github.com/contao-estatemanager/similar](https://github.com/contao-estatemanager/similar)
{% endtab %}
{% endtabs %}

Nach der Installation muss das [Contao-Installtool](https://docs.contao.org/manual/de/installation/contao-installtool/) aufgerufen und die Datenbank aktualisiert werden.&#x20;

### Exposé-Module

Hier finden Sie eine Übersicht neuer (🟢) und erweiterte (🔵) Exposé-Module.

{% tabs %}
{% tab title="🟢 Ähnliche Objekte" %}
**Einstellungen**

:small\_blue\_diamond:`Weiterleitungsseite`

_Definiert die Seite, auf die bei Klick einer Immobilie geleitet werden soll._

:small\_blue\_diamond:`Gesamtanzahl der Elemente`

_Hier können die auszugebenden Immobilien begrenzt werden._

__:small\_blue\_diamond:`Elemente pro Seite`

_Die Anzahl an Elementen pro Seite._

:small\_blue\_diamond:`Filter vergröbern`

_Hier können Sie einen Wert in Prozent eintragen, um den die Suche vergröbert werden soll._

:small\_blue\_diamond:`Maximale Entfernung`

_Hier können Sie den Radius in km eingeben, in welchem ähnliche Immobilien berücksichtigt werden._

:small\_blue\_diamond:`Ausblenden bei keinen Ergebnissen`

_Dieses Modul wird nur ausgegeben wenn Ergebnisse für die Darstellung gefunden wurden._

:small\_blue\_diamond:`Bildgröße`

_Hier können Sie die Abmessungen der Bilder und den Skalierungsmodus festlegen._

**Template**

:small\_orange\_diamond:`expose_mod_similar`
{% endtab %}
{% endtabs %}

### Lizenz

Für diese Erweiterung ist eine Lizenz erforderlich. Zum Erwerb einer Lizenz, folge bitte den Schritten unter [Lizenzen](../lizenzen.md).
