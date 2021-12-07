# Synchronisation

Bereits eingerichtete Schnittstellen synchronisieren Immobiliendatensätze anhand der Schnittstellen-Konfiguration.

### Manuelle Synchronisierung

Die manuelle Synchronisierung von Immobiliendatensätzen ist über das ![](../../../.gitbook/assets/sync.svg)-Symbol in der Schnittstellenübersicht möglich. Durch Klicken des Symbols öffnet sich eine neue Maske, in welcher weitere Details zu Datensätzen vorzufinden sind.

#### Symbole

Die nachfolgenden Symbole bilden den Synchronisierungsstatus ab:

* ![](../../../.gitbook/assets/status\_1.svg) = Bereits synchronisiert
* ![](../../../.gitbook/assets/status\_2.svg) = Fehler bei der Synchronisierung
* ![](../../../.gitbook/assets/status\_0.svg) = Noch nicht synchronisiert

#### Weitere Felder

:small\_blue\_diamond:`Dateipfad`

Der Dateipfad dient der Lokalisation des Datensatzes. Hier kann überprüft werden, um welchen Datensatz es sich handelt.

:small\_blue\_diamond:`Letzte Änderung`

Der Timestamp der letzten Änderung dient zur Kontrolle von aktualisierten Datensätzen.

:small\_blue\_diamond:`Dateigröße`

Gibt die Dateigröße des Datensatzes aus.

:small\_blue\_diamond:`Letzte Synchronisierung`

Gibt die Uhrzeit und das Datum der letzten Synchronisation dieses Datensatzes an.&#x20;

:small\_blue\_diamond:`Benutzer`

Zeigt den Benutzer an, durch den die Synchronisierung angestoßen wurde.

#### Datensatz synchronisieren

Durch das ![](../../../.gitbook/assets/sync.svg)-Symbol können Datensätze manuell synchronisiert werden.

### Verlauf der Synchronisationen

Der Verlauf der zuletzt synchronisierten Dateien lässt sich über das Symbol ![](../../../.gitbook/assets/history.svg)öffnen.\
In dieser Übersicht sieht man die zuletzt synchronisierten Dateien mit einer Meldung. Weitere Details lassen sich über die Details des Eintrags aufrufen.

### Bereinigung von Dateien

Beim Import von Immobiliendatensätzen werden Bilder und Anhänge in der Dateiverwaltung für eine Immobilie im ausgewählten Importverzeichnis abgelegt. Dateien von gelöschten Immobilien bleiben grundsätzlich in der Dateiverwaltung bestehen.

Mithilfe der Funktion **Datensätze aufräumen** ![](../../../.gitbook/assets/clear.svg) lassen sich Dateien, welche keiner Immobilie zugeordnet werden können, löschen.
