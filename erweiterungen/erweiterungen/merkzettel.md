---
description: Contao EstateManager Erweiterung
---

# Merkzettel

![](../../.gitbook/assets/produktbild\_merkzettel\_github.jpg)

Die `Merkzettel` Erweiterung integriert die Möglichkeit sich, als Besucher der Webseite einzelne Immobilien in einem ausschließlich für den Besucher sichtbaren Merkzettel zu speichern. Diese werden dabei vorerst für die laufende Session beibehalten. Sofern es einen internen Bereich für Besucher gibt, können die auf dem Merkzettel gespeicherten Immobilien nach dem Login dauerhaft im `Mitglied` - Datensatz gespeichert werden, bis diese wieder manuell vom Besucher aus dem Merkzettel entfernt werden.

### Installation

{% tabs %}
{% tab title="Composer" %}
```bash
$ composer require contao-estatemanager/watchlist
```
{% endtab %}

{% tab title="Contao-Manager" %}
Über die Suche des Contao-Manager kann der Begriff `EstateManager` oder `watchlist` gesucht werden. Anschließen wählt man das Paket `Contao EstateManager Watchlist` über die Schaltfläche "_hinzufügen_" aus und klickt zum installieren über den Reiter "_Pakete_" auf die Schaltfläche "_Änderungen anwenden_". Eine detaillierte Anleitung wie man mit dem Contao-Manager arbeitet findest du [hier](https://docs.contao.org/manual/de/installation/erweiterungen-installieren/).
{% endtab %}

{% tab title="GitHub" %}
Installation direkt über GitHub:

[https://github.com/contao-estatemanager/watchlist](https://github.com/contao-estatemanager/watchlist)
{% endtab %}
{% endtabs %}

Nach der Installation muss das [Contao-Installtool](https://docs.contao.org/manual/de/installation/contao-installtool/) aufgerufen und die Datenbank aktualisiert werden.&#x20;

### Module

Hier finden Sie eine Übersicht neuer (🟢), sowie erweiterte (🔵) Module.

{% tabs %}
{% tab title="🟢 Merkzettel Weiterleitung" %}
Das Modul `Merkzettel Weiterleitung` dient dazu, eine Weiterleitung auf eine beliebige Seite einzurichten, auf der der Besucher seine gemerkten Immobilien sichten oder entfernen kann.&#x20;

**Einstellungen**

:small\_blue\_diamond:`Weiterleitungsseite`

_Die zu Referenzierende Seite_

:small\_blue\_diamond:`Anzahl ausgeben`

_Gibt die Anzahl der sich auf dem Merkzettel befindenden Immobilien aus_

**Template**

:small\_orange\_diamond:`mod_watchlistRedirector`
{% endtab %}

{% tab title="🔵 Liste" %}
Erweitert die [Liste](../../installation-konfiguration/frontend-konfiguration/module/liste.md) um folgende Einstellungen.

**Einstellungen**

:small\_blue\_diamond:`Merkzettel hinzufügen`

_Fügt für jeder Immobilie in der Liste die Merkzettel-Schaltfläche hinzu. Die neue Einstellung befindet sich in der Palette `Immobilien Erweiterung` ._

**Template**

:small\_orange\_diamond:`real_estate_itemext_watchlist_default`

_Das Template muss über das Feld `Immobilien Template Erweiterung: Merkzettel`in der Palette `Templates-Einstellungen` ausgewählt werden._
{% endtab %}

{% tab title="🔵 Ergebnisliste" %}
Erweitert die [Ergebnisliste](../../installation-konfiguration/frontend-konfiguration/module/ergebnisliste.md) um folgende Einstellungen.

**Einstellungen**

:small\_blue\_diamond:`Merkzettel hinzufügen`

_Fügt für jeder Immobilie in der Liste die Merkzettel-Schaltfläche hinzu. Die neue Einstellung befindet sich in der Palette `Immobilien Erweiterung` ._

**Template**

:small\_orange\_diamond:`real_estate_itemext_watchlist_default`

_Das Template muss über das Feld `Immobilien Template Erweiterung: Merkzettel`in der Palette `Templates-Einstellungen` ausgewählt werden._
{% endtab %}
{% endtabs %}

### Exposé-Module

Hier finden Sie eine Übersicht neuer (🟢) und erweiterte (🔵) Exposé-Module.

{% tabs %}
{% tab title="🟢 Merkzettel" %}
Das Exposé-Modul `Merkzettel` ermöglicht die Ausgabe einer Schaltfläche, um die Immobilie direkt aus dem Exposé heraus auf dem Merkzettel zu speichern.

**Template**

:small\_orange\_diamond:`expose_mod_watchlist`
{% endtab %}
{% endtabs %}

### JavaScript-Templates

Hier finden Sie eine Übersicht neuer JavaScript-Templates.

{% tabs %}
{% tab title="🟢 Merkzettel" %}
Um die Seite bei Klick der oben gelieferten Merkzettel-Schaltfläche nicht neu laden zu müssen, liefert diese Erweiterung ebenfalls ein neues JS-Template aus, welches unter Layouts zur Verfügung gestellt wird.

**Template**

:small\_orange\_diamond:`js_realestatewatchlist`

**Events**

Um von außen auf einen Statuswechsel des Merkzettels Einfluss nehmen zu können, werden zwei `CustomEvents` registriert und können nach Bedarf entgegengenommen werden.

* `watchlist.onChange`
* `watchlist.onDelete`

```javascript
// Listen to the deletion of properties from the watchlist
document.addEventListener('watchlist.onDelete', function(e){
    // Do something
    console.log(e.detail);
});

// Listen to the adding of properties on the watchlist
document.addEventListener('watchlist.onChange', function(e){
    // Do something
    console.log(e.detail);
});
```

{% hint style="warning" %}
Um Immobilien asynchron aus einer Liste zu _entfernen_, ist es derzeit noch notwendig, dieser oder einem darüber liegenden Element die CSS-Klasse **`delete-list`** zu geben.
{% endhint %}
{% endtab %}
{% endtabs %}

### Lizenz

Für diese Erweiterung ist eine Lizenz erforderlich. Zum Erwerb einer Lizenz, folge bitte den Schritten unter [Lizenzen](../lizenzen.md).

