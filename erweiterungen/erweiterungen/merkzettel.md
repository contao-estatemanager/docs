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

### Lizenz

Für diese Erweiterung ist eine Lizenz erforderlich. Bitte folge dafür den Schritten unter [Lizenzen](../lizenzen.md).



