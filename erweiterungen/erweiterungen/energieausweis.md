---
description: Contao EstateManager Erweiterung
---

# Energieskala

![](<../../.gitbook/assets/produktbild\_energiepass\_github (1).jpg>)

Die `Energieskala` Erweiterung integriert eine visuelle Ansicht (Skala) des Energieverbrauchs der Immobilie.

### Installation

{% tabs %}
{% tab title="Composer" %}
```bash
$ composer require contao-estatemanager/energiy-pass
```
{% endtab %}

{% tab title="Contao-Manager" %}
Über die Suche des Contao-Manager kann der Begriff `EstateManager` oder `energy-pass` gesucht werden. Anschließen wählt man das Paket `Contao EstateManager Energieausweis` über die Schaltfläche "_hinzufügen_" aus und klickt zum installieren über den Reiter "_Pakete_" auf die Schaltfläche "_Änderungen anwenden_". Eine detaillierte Anleitung wie man mit dem Contao-Manager arbeitet findest du [hier](https://docs.contao.org/manual/de/installation/erweiterungen-installieren/).
{% endtab %}

{% tab title="GitHub" %}
Installation direkt über GitHub:

[https://github.com/contao-estatemanager/energy-pass](https://github.com/contao-estatemanager/energy-pass)
{% endtab %}
{% endtabs %}

Nach der Installation muss das [Contao-Installtool](https://docs.contao.org/manual/de/installation/contao-installtool/) aufgerufen und die Datenbank aktualisiert werden.&#x20;

### Exposé-Module

Hier finden Sie eine Übersicht neuer (🟢) und erweiterte (🔵) Exposé-Module.

{% tabs %}
{% tab title="🔵 Details" %}
Erweitert die [Details](../../installation-konfiguration/backend-konfiguration/expose-module/details.md) um folgende Einstellungen.

**Einstellungen**

:small\_blue\_diamond:`Energieskala hinzufügen`

_Fügt nach dem Energieausweis eine Energieskala ein. Dafür muss die Detail-Kategorie Energieausweis angewählt sein._

**Template**

:small\_orange\_diamond:`energiebar_default`
{% endtab %}
{% endtabs %}

### JavaScript-Templates

Hier finden Sie eine Übersicht neuer JavaScript-Templates.

{% tabs %}
{% tab title="🟢 Energieausweis" %}
Für die Animationen innerhalb der Energieskala wird folgendes JavaScript-Template unter Layouts zur Verfügung gestellt.

**Template**

:small\_orange\_diamond:`js_realestateenergiebar`

{% hint style="info" %}
Die zugehörigen CSS-Stile der Energieskala werden automatisch über dieses Template mit eingebunden.
{% endhint %}
{% endtab %}
{% endtabs %}

### Lizenz

Für diese Erweiterung ist eine Lizenz erforderlich. Zum Erwerb einer Lizenz, folge bitte den Schritten unter [Lizenzen](../lizenzen.md).
