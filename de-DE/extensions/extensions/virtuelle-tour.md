# Virtuelle Tour

Die `Virtual Tour` Erweiterung ermöglicht das entgegennehmen und darstellen von 3D-Rundgängen bekannter Drittanbieter. Folgende Drittanbieter werden dabei bereits unterstützt:

* Ogulo
* Immoviewer

Um beliebige Drittanbieter unterstützen zu können, werden Links, welcher der Immobilie zugewiesen sind und mit folgenden Subdomains übertragen / eingerichtet wurden, ebenfalls als 3D-Rundgang erkannt.

* 3d.\*
* 360.\*
* 360grad.\*

Darüber hinaus, steht nach der Installation dieser Erweiterung ein weiteres Immobilien-Feld zur Verfügung, welches unabhängig vom Drittanbieter oder der URL, den dort eingetragenen Link als virtuellen Rundgang erkennt:

* Virtueller 3D-Rundgang

### Installation

{% tabs %}
{% tab title="Composer" %}
```bash
$ composer require contao-estatemanager/virtual-tour
```
{% endtab %}

{% tab title="Contao-Manager" %}
Über die Suche des Contao-Manager kann der Begriff `EstateManager` oder `virtual-tour` gesucht werden. Anschließen wählt man das Paket `Contao EstateManager Virtueller 3D-Rundgang` über die Schaltfläche "_hinzufügen_" aus und klickt zum installieren über den Reiter "_Pakete_" auf die Schaltfläche "_Änderungen anwenden_". Eine detaillierte Anleitung wie man mit dem Contao-Manager arbeitet findest du [hier](https://docs.contao.org/manual/de/installation/erweiterungen-installieren/).
{% endtab %}

{% tab title="GitHub" %}
Installation direkt über GitHub:

[https://github.com/contao-estatemanager/virtual-tour](https://github.com/contao-estatemanager/virtual-tour)
{% endtab %}
{% endtabs %}

Nach der Installation muss das [Contao-Installtool](https://docs.contao.org/manual/de/installation/contao-installtool/) aufgerufen und die Datenbank aktualisiert werden.&#x20;

### Module

Hier finden Sie eine Übersicht neuer (🟢), sowie erweiterte (🔵) Module.

{% tabs %}
{% tab title="🔵 Liste" %}
Erweitert die [Liste](../../installation-konfiguration/frontend-konfiguration/module/liste.md) um folgende Einstellungen.

**Einstellungen**

:small\_blue\_diamond:`Virtuellen Rundgang hinzufügen`

_Fügt für jeder Immobilie in der Liste die Möglichkeit hinzu, den virtuellen Rundgang zu öffnen. Die neue Einstellung befindet sich in der Palette `Immobilien Erweiterung` ._

**Template**

:small\_orange\_diamond:`real_estate_itemext_virtual_tour_default`

_Das Template muss über das Feld `Immobilien Template Erweiterung: Virtueller Rundgang`in der Palette `Templates-Einstellungen` ausgewählt werden._
{% endtab %}

{% tab title="🔵 Ergebnisliste" %}
Erweitert die [Ergebnisliste](../../installation-konfiguration/frontend-konfiguration/module/ergebnisliste.md) um folgende Einstellungen.

**Einstellungen**

:small\_blue\_diamond:`Virtuellen Rundgang hinzufügen`

_Fügt für jeder Immobilie in der Liste die Möglichkeit hinzu, den virtuellen Rundgang zu öffnen. Die neue Einstellung befindet sich in der Palette `Immobilien Erweiterung` ._

**Template**

:small\_orange\_diamond:`real_estate_itemext_virtual_tour_default`

_Das Template muss über das Feld `Immobilien Template Erweiterung: Virtueller Rundgang`in der Palette `Templates-Einstellungen` ausgewählt werden._
{% endtab %}
{% endtabs %}

### Exposé-Module

Hier finden Sie eine Übersicht neuer (🟢) und erweiterte (🔵) Exposé-Module.

{% tabs %}
{% tab title="🟢 Virtueller-Rundgang" %}
Das Exposé-Modul `Virtueller-Rundgang` ermöglicht die Ausgabe einer Schaltfläche zum öffnen des virtuellen Rundgangs.

**Einstellungen**

:small\_blue\_diamond:`Text`

_Ermöglicht die Ergänzung eines beliebigen Textes._

:small\_blue\_diamond:`Ausblenden bei keinen Ergebnissen`

_Dieses Modul wird nur ausgegeben wenn ein virtueller Rundgang zum darstellen gefunden wurde._

**Template**

:small\_orange\_diamond:`expose_mod_virtualTour`
{% endtab %}

{% tab title="🔵 Galerie" %}
Erweitert das Exposé-Modul [Galerie](../../installation-konfiguration/backend-konfiguration/expose-module/galerie.md) um eine weitere Galerie-Kategorie (Virtueller-Rundgang). Des Weiteren wird eine neue Palette (Virtueller-Rundgang Einstellungen) erzeugt um folgende Einstellungen vornehmen zu können.

**Einstellungen**

:small\_blue\_diamond:`Vorschaubild verwenden`

Gibt ein Vorschaubild aus. Sofern kein eigenes Bild ausgewählt wurde, wird das Titelbild der Immobilie verwendet.

:small\_blue\_diamond:`Eigenes Vorschaubild`

Hier können Sie ein eigenes Vorschaubild definieren.

{% hint style="warning" %}
Bitte beachte das mitgelieferte JavaScript-Template für die Verwendung von Vorschaubildern.
{% endhint %}

**Template**

:small\_orange\_diamond:`expose_mod_virtual_tour_gallery_default`
{% endtab %}
{% endtabs %}

### Status-Token

Die Liste von vorhandenen Status-Token wird um den `Virtuellen-Rundgang` Status-Token ergänzt und steht anschließend überall dort zur Verfügung, wo Status-Token ausgegeben werden können.

### JavaScript-Templates

Hier finden Sie eine Übersicht neuer JavaScript-Templates.

{% tabs %}
{% tab title="🟢 Virtueller Rundgang" %}
Um den virtuellen Rundgang bei Verwendung eines Vorschaubild nicht direkt einzubinden (da diese zum Beispiel bei verschiedenen Anbietern mit Musik unterspielt werden), bindet das mitgelieferte JavaScript-Template die Zielseite erst nach Klick auf das Vorschaubild ein.

**Template**

:small\_orange\_diamond:`js_realestatevirtualtour`

**Events**

Um von außen bei Klick auf das Vorschaubild Einfluss nehmen zu können, wird ein`CustomEvent` registriert und kann nach Bedarf entgegengenommen werden.

* `virtualtour.onClickPreview`

```javascript
document.addEventListener('virtualtour.onClickPreview', function(e){
    // Do something
    console.log(e.detail);
});
```
{% endtab %}
{% endtabs %}

### Lizenz

Für diese Erweiterung ist eine Lizenz erforderlich. Zum Erwerb einer Lizenz folge bitte den Schritten unter [Lizenzen](../lizenzen.md).
