# Konfiguration

### Schnittstellen konfigurieren

Schnittstellen können den eigenen Anforderungen entsprechend umfangreich konfiguriert werden. Dabei können beliebig viele Schnittstellen angelegt werden, um Datensätze unterschiedlicher Quellen und Strukturen zuverlässig importieren zu können. Eine Schnittstelle **muss einem eindeutigen Anbieter zugeordnet werden**, weshalb **vor der** Schnittstellen-**Konfiguration** der entsprechende **Anbieter angelegt werden muss**.

?> Anbieter können unter **EstateManager > Verwaltung > Anbieter/Standorte verwalten** eingerichtet werden. Für die Zuordnung von Immobiliendatensätzen ist die **Anbieternummer** von Nöten.

### Titel & Typ

<span class="field">Titel</span>

Dient der Identifizierung einer Schnittstelle im Backend.

<span class="field">Typ</span>

Mithilfe des Typs können verschiedene Arten von Schnittstellen konfiguriert werden. Standardmäßig steht der Typ "OpenImmo" zur Verfügung, welcher den Import nach den Regeln des OpenImmo Standards durchführt.

### OpenImmo Feld-Konfiguration

<span class="field">Anbieter</span>

Eine Schnittstelle **muss** einem bestimmten **Anbieter zugeordnet werden**, damit Immobilien und Kontaktpersonen stets diesem Anbieter zugeordnet werden können.

<span class="field">Anbieternummer</span>

Die eindeutige Anbieternummer der OpenImmo Übertragung.

!> Die **Anbieternummer ist essenziell** für die Übertragung von Immobilien und Kontaktpersonen.

<span class="field">Eindeutiges Anbieterfeld</span>

Gibt an, über welchen Wert eine OpenImmo Übertragung eindeutig einem bestimmten **Anbieter zugeordnet** werden kann.

<span class="field">Eindeutiges Feld</span>

Gibt an, über welchen Wert eine OpenImmo Übertragung eindeutig einer bestimmten **Immobilie zugeordnet** werden kann.

!> Immobilien müssen auf mehrsprachigen Websites mehrfach in den jeweils unterschiedlichen Sprachen importiert werden. Diese Immobilien teilen sich dabei oft eine gemeinsame Objektnummer, weswegen das eindeutige Feld auf den Wert festgelegt werden muss, über den sich ein Immobiliendatensatz eindeutig identifizieren lässt.

<span class="field">Importverzeichnis</span>

Verzeichnis, in welchem die OpenImmo **Übertragungen abgelegt werden**, damit diese durch die Schnittstelle **gefunden** und **importiert werden** können.

<span class="field">Zielverzeichnis</span>

Verzeichnis, in dem **Bilder und Dokumente von Immobiliendatensätzen** abgelegt werden. Für jeden Immobiliendatensatz wird dabei ein eigener Ordner (Objektnummer) innerhalb eines Ordners des Anbieters (Anbieternummer) angelegt.

<span class="field">Importverzeichnis Kontaktperson</span>

Verzeichnis, in dem **Bilder von Kontaktpersonen** abgelegt werden.

### Kontaktperson-Einstellungen

Über die Palette "Kontaktperson-Einstellungen" kann eingestellt werden, wie Kontaktpersonen während eines Imports behandelt werden sollen und ob Immobilien anderer Anbieter importiert und dabei einer eigenen Kontaktperson zugeordnet werden sollen.

<span class="field">Kontaktperson</span>

Hier kann angegeben werden, ob **neue Kontaktpersonen** durch die Schnittstelle **erstellt** und / oder **aktualisiert** werden sollen.

!> Kann eine Immobilie während eines Imports keiner Kontaktperson zugeordnet werden, wird die Immobilie übersprungen und nicht importiert. Darf über die Schnittstelle keine Kontaktperson erstellt werden, muss sichergestellt werden, dass die Kontaktperson in der Anbieterverwaltung existiert, um Immobilien importieren zu können.

<span class="field">Eindeutiges Feld der Kontaktperson</span>

Hier muss das Feld ausgewählt werden, über das eine Kontaktperson eindeutig identifiziert werden kann.

* E-Mail (Zentrale)
* E-Mail (Direkt)
* Persononennummer
* Nachname, Vorname

?> Die Personennummer stellt die zuverlässigste Möglichkeit der Identifizierung dar und wird daher von uns empfohlen.

<span class="field">Datensätze anderer Anbieter importieren</span>

Hier kann angegeben werden, wie mit Immobilien anderer Anbieter umgegangen werden soll. Für gewöhnlich werden innerhalb einer OpenImmo Übertragung lediglich Immobilien des eigenen Anbieters übertragen. Sollte dies nicht der Fall sein, können Immobilien anderer Anbieter schlicht mit den Einstellungen der eigenen Schnittstelle importiert werden oder alternativ anhand der Vermarktungsart einer bestimmten Kontaktperson zugeordnet werden.

#### Zuweisung von Datensätzen

Durch Auswahl der Option "Zuweisen" können **Datensätze**, welche **keinen Anbieter zugeordnet** werden können, **einer bestimmten Kontaktperson zugeordnet werden**.

<span class="field">Kontaktperson Kauf-Objekte</span>

Hier müssen Sie eine Kontaktperson auswählen, welcher **Kauf-Objekte** zugewiesen werden.

<span class="field">Kontaktperson Miet-Objekte</span>

Hier müssen Sie eine Kontaktperson auswählen, welcher **Miet-Objekte** zugewiesen werden.

<span class="field">Kontaktperson Erbpacht-Objekte</span>

Hier müssen Sie eine Kontaktperson auswählen, welcher **Erbpacht-Objekte** zugewiesen werden.

<span class="field">Kontaktperson Leasing-Objekte</span>

Hier müssen Sie eine Kontaktperson auswählen, welcher **Leasing-Objekte** zugewiesen werden.

### Experten-Einstellungen

<span class="field">Datensätze überspringen</span>

Hier können Sie **auswählen,** ob Immobiliendatensätze mit **fehlendem Objekttitel** oder fehlender **Objektbeschreibung nicht importiert** werden sollen.

<span class="field">Datensätze nicht veröffentlichen</span>

Einstellung, um **neu importierte Immobiliendatensätze nicht automatisch** auf der Website zu **veröffentlichen**.

### Synchronisierungs-Einstellungen

Für jede Schnittstelle kann festgelegt werden, wie oft die Synchronisierung der Immobiliendatensätze stattfinden soll, wie lange alte Synchronisierungsdateien existieren dürfen und wie viele Dateien pro Vorgang synchronisiert werden sollen.

!> Die Ausführung der Synchronisierung erfolgt über einen **poor man cron**. Hierbei handelt es sich um ein Modul, welches die **Cron-Operation** über **normale Browser-/Seitenanfragen** ausführt. [Weitere Hinweise zu Cronjobs (Contao)](https://docs.contao.org/manual/de/system/einstellungen/#cronjob-einstellungen)

<span class="field">Automatische Synchronisierung</span>

Hier kann die **Frequenz** der automatischen Synchronisierung eingestellt werden. Um **nur manuelle** Synchronisationen zu erlauben, kann hier "**Niemals**" ausgewählt werden.
Die manuelle Synchronisation wird über das ![](../../../_media/sync.svg)-Symbol in der Übersicht ausgeführt.

<span class="field">Dateien älter als * löschen</span>

Bereits **synchronisierte Immobiliendatensätze** werden **nicht** automatisch **gelöscht**. Mithilfe dieser Einstellung werden diese Datensätze **nach der eingestellten Frequenz gelöscht**.

<span class="field">Maximale Anzahl an Dateien pro Synchronisation</span>

Hier kann die maximale Anzahl an Dateien definiert werden, welche während des Imports synchronisiert werden sollen.
