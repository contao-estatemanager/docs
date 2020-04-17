---
description: Contao EstateManager Erweiterung
---

# Merkzettel

Die `Merkzettel` Erweiterung integriert die Möglichkeit sich als Besucher der Webseite einzelne Immobilien in einem ausschließlich für den Besucher sichtbaren Merkzettel zu speichern. Diese werden dabei vorerst für die laufende Session beibehalten. Sofern es einen internen Bereich für Besucher gibt, können die auf dem Merkzettel gespeicherten Immobilien nach dem Login dauerhaft im `Mitglied` -Datensatz gespeichert werden, bis diese wieder manuell vom Besucher aus dem Merkzettel entfernt werden.

### Installation

{% tabs %}
{% tab title="Composer" %}
```bash
$ composer require contao-estatemanager/watchlist
```
{% endtab %}

{% tab title="Contao-Manager" %}
Über die Suche des Contao-Manager kann der Begriff `EstateManager` gesucht werden. Anschließen wählt man das Paket `Contao EstateManager Watchlist` aus und installiert es anschließend. Eine detaillierte Anleitung wie man mit dem Contao-Manager arbeitet findest du [hier](https://docs.contao.org/manual/de/installation/erweiterungen-installieren/).
{% endtab %}

{% tab title="GitHub" %}
Installation direkt über GitHub:

[https://github.com/contao-estatemanager/watchlist](https://github.com/contao-estatemanager/watchlist)
{% endtab %}
{% endtabs %}

Nach der Installation muss das [Contao-Installtool](https://docs.contao.org/manual/de/installation/contao-installtool/) aufgerufen und die Datenbank aktualisiert werden. 

### Module

Hier finden Sie eine Übersicht neuer, sowie erweiterte Module.

{% tabs %}
{% tab title="🟢 Merkzettel Weiterleitung" %}
Das Modul `Merkzettel Weiterleitung` dient dazu, eine Weiterleitung auf eine beliebige Seite einzurichten, auf der der Besucher seine gemerkten Immobilien sichten oder entfernen kann. 

**Einstellungen**

🔹`Weiterleitungsseite`

_Die zu Referenzierende Seite_

🔹`Anzahl ausgeben`

_Gibt die Anzahl der sich auf dem Merkzettel befindenden Immobilien aus_

**Template**

🔸`mod_watchlistRedirector`
{% endtab %}

{% tab title="🔵 Liste" %}

{% endtab %}
{% endtabs %}

### Exposé-Module

Hier finden Sie eine Übersicht neuer, sowie erweiterte Exposé-Module.

{% tabs %}
{% tab title="🟢 Merkzettel" %}
Das Exposé-Modul `Merkzettel` ermöglicht die Ausgabe einer Schaltfläche, um die Immobilie direkt aus dem Exposé heraus auf dem Merkzettel zu speichern.

**Template**

🔸`expose_mod_watchlist`
{% endtab %}
{% endtabs %}

### JavaScript-Templates

Hier finden Sie eine Übersicht neuer, sowie erweiterte JavaScript-Templates.

{% tabs %}
{% tab title="🟢 Merkzettel" %}
Um die Seite bei Klick der oben gelieferten Merkzettel-Schaltfläche nicht neu laden zu müssen, liefert diese Erweiterung ebenfalls ein neues JS-Template aus, welches unter Layouts zur Verfügung gestellt wird.

**Template**

🔸`js_realestatewatchlist`

**Events**

Um von außen auf einen Statuswechsel des Merkzettels Einfluss nehmen zu können, werden zwei `CustomEvents` registriert und können nach Bedarf entgegengenommen werden.

* `watchlist.onChange`
* `watchlist.onDelete`

```javascript
// Listen to the deletion of properties from the watchlist
document.addEventListener('watchlist.onDelete', function(e){
    console.log(e.detail);
    // Do something
});

// Listen to the adding of properties on the watchlist
document.addEventListener('watchlist.onChange', function(e){
    console.log(e.detail);
    // Do something
});
```

{% hint style="warning" %}
Um Immobilien asynchron aus einer Liste zu entfernen, ist es derzeit noch zwingend notwendig, dieser oder einem darüber liegenden Element die CSS-Klasse **`delete-list`** zu geben.
{% endhint %}
{% endtab %}
{% endtabs %}

### Lizenz

Für diese Erweiterung ist eine Lizenz erforderlich. Zum Erwerb einer Lizenz folge bitte den Schritten unter [Lizenzen](../lizenzen.md).



