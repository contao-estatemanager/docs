# Synchronisation

Bereits eingerichtete Schnittstellen synchronisieren Immobiliendatensätze anhand der Schnittstellen-Konfiguration.

?> Die **Synchronisation** von Immobiliendatensätzen erfolgt **über einen Teilabgleich**. Durch einen Teilabgleich können einzelne **Löschaufträge** für Immobiliendatensätze erfolgen. Löschaufträge werden ausschließlich von Teilabgleichen eines ERP-Systems (z. B. onOffice) übermittelt. Ein **Vollausgleich ist bei der initialen Befüllung** des Systems erlaubt. Hierbei werden Immobilien **nur hinzugefügt**, durch den Vollausgleich können jedoch die Datensätze jedoch **nicht gelöscht** werden.

### Manuelle Synchronisierung

Die manuelle Synchronisierung von Immobiliendatensätzen ist über das ![](../../../_media/sync.svg)-Symbol in der Schnittstellenübersicht möglich. Durch Klicken des Symbols öffnet sich eine neue Maske, in welcher weitere Details zu Datensätzen vorzufinden sind.

#### Symbole

Die nachfolgenden Symbole bilden den Synchronisierungsstatus ab:

|     |                                 |
|-----|---------------------------------|
| ![](../../../_media/status_1.svg)    | Bereits synchronisiert          |
| ![](../../../_media/status_2.svg)    | Fehler bei der Synchronisierung |
|  ![](../../../_media/status_0.svg)   | Noch nicht synchronisiert       |

#### Weitere Felder

<span class="field">Dateipfad</span>

Der Dateipfad dient der Lokalisation des Datensatzes. Hier kann überprüft werden, um welchen Datensatz es sich handelt.

<span class="field">Letzte Änderung</span>

Der Timestamp der letzten Änderung dient zur Kontrolle von aktualisierten Datensätzen.

<span class="field">Dateigröße</span>

Gibt die Dateigröße des Datensatzes aus.

<span class="field">Letzte Synchronisierung</span>

Gibt die Uhrzeit und das Datum der letzten Synchronisation dieses Datensatzes an.&#x20;

<span class="field">Benutzer</span>

Zeigt den Benutzer an, durch den die Synchronisierung angestoßen wurde.

#### Datensatz synchronisieren

Durch das ![](../../../_media/sync.svg)-Symbol können Datensätze manuell synchronisiert werden.

### Verlauf der Synchronisationen

Der Verlauf der zuletzt synchronisierten Dateien lässt sich über das Symbol ![](../../../_media/history.svg)öffnen.\
In dieser Übersicht sieht man die zuletzt synchronisierten Dateien mit einer Meldung. Weitere Details lassen sich über die Details des Eintrags aufrufen.

### Bereinigung von Dateien

Beim Import von Immobiliendatensätzen werden Bilder und Anhänge in der Dateiverwaltung für eine Immobilie im ausgewählten Importverzeichnis abgelegt. Durch Löschaufträge werden die zugehörigen Dateien gelöscht.

!> Bei einem **Vollausgleich** werden Immobiliendatensätze **nur angelegt**, eine **Löschung** der Datensätze ist hier **nicht möglich**.

Mithilfe der Funktion **Datensätze aufräumen** ![](../../../_media/clear.svg) lassen sich Dateien, welche keiner Immobilie zugeordnet werden können, löschen.
