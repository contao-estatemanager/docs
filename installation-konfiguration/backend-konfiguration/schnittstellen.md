# Schnittstellen

Mithilfe von Schnittstellen können **Immobilen und Kontaktpersonen importiert** sowie mit einer **Maklersoftware synchronisiert** werden. Der Abgleich von Immobilien findet dabei auf Basis des **OpenImmo** Standards statt, sodass Immobilien-Datensätze und dessen Kontaktpersonen automatisch erstellt, aktualisiert und gelöscht werden können.

### Schnittstellen konfigurieren

Schnittstellen können den eigenen Anforderungen entsprechend umfangreich konfiguriert werden. Dabei können beliebig viele Schnittstellen angelegt werden, um Datensätze unterschiedlicher Quellen und Strukturen zuverlässig importieren zu können. Eine Schnittstelle **muss einem eindeutigen Anbieter zugeordnet werden**, weshalb **vor der** Schnittstellen-**Konfiguration** der entsprechende **Anbieter angelegt werden muss**.

### Titel & Typ

:small\_blue\_diamond:`Titel`

_Dient der Identifizierung einer Schnittstelle im Backend._

:small\_blue\_diamond:`Typ`

_Mithilfe des Typs können verschiedene Arten von Schnittstellen konfiguriert werden. Standardmäßig steht der Typ "OpenImmo" zur Verfügung, welcher den Import nach den Regeln des OpenImmo Standards durchführt._

### OpenImmo Feld-Konfiguration

__:small\_blue\_diamond:`Anbieter`

_Eine Schnittstelle **muss** einem bestimmten **Anbieter zugeordnet werden**, damit Immobilien und Kontaktpersonen stets diesem Anbieter zugeordnet werden können._

:small\_blue\_diamond:`Anbieternummer`

_Die eindeutige Anbieternummer der OpenImmo Übertragung._

:small\_blue\_diamond:`Eindeutiges Anbieterfeld`

_Gibt an, über welchen Wert eine OpenImmo Übertragung eindeutig einem bestimmten **Anbieter zugeordnet** werden kann._

:small\_blue\_diamond:`Eindeutiges Feld`

_Gibt an, über welchen Wert eine OpenImmo Übertragung eindeutig einer bestimmten **Immobilie zugeordnet** werden kann._

{% hint style="warning" %}
Immobilien müssen auf mehrsprachigen Websites mehrfach in den jeweils unterschiedlichen Sprachen importiert werden. Diese Immobilien teilen sich dabei oft eine gemeinsame Objektnummer, weswegen das eindeutige Feld auf den Wert festgelegt werden muss, über den sich ein Immobiliendatensatz eindeutig identifizieren lässt.
{% endhint %}

:small\_blue\_diamond:`Importverzeichnis`

_Verzeichnis, in welchem die OpenImmo **Übertragungen abgelegt werden**, damit diese durch die Schnittstelle **gefunden** und **importiert werden** können._

:small\_blue\_diamond:`Zielverzeichnis`

_Verzeichnis, in dem **Bilder und Dokumente von Immobiliendatensätzen** abgelegt werden. Für jeden Immobiliendatensatz wird dabei ein eigener Ordner (Objektnummer) innerhalb eines Ordners des Anbieters (Anbieternummer) angelegt._

:small\_blue\_diamond:`Importverzeichnis Kontaktperson`

_Verzeichnis, in dem **Bilder von Kontaktpersonen** abgelegt werden._

### Kontaktperson-Einstellungen

Über die Palette "Kontaktperson-Einstellungen" kann eingestellt werden, wie Kontaktpersonen während eines Imports behandelt werden sollen und ob Immobilien anderer Anbieter importiert und dabei einer eigenen Kontaktperson zugeordnet werden sollen.

:small\_blue\_diamond:`Kontaktperson`

_Hier kann angegeben werden, ob **neue Kontaktpersonen** durch die Schnittstelle **erstellt** und / oder **aktualisiert** werden sollen._

{% hint style="warning" %}
Kann eine Immobilie während eines Imports keiner Kontaktperson zugeordnet werden, wird die Immobilie übersprungen und nicht importiert. Darf über die Schnittstelle keine Kontaktperson erstellt werden, muss sichergestellt werden, dass die Kontaktperson in der Anbieterverwaltung existiert, um Immobilien importieren zu können.
{% endhint %}

:small\_blue\_diamond:`Eindeutiges Feld der Kontaktperson`

_Hier muss das Feld ausgewählt werden, über das eine Kontaktperson eindeutig identifiziert werden kann._

&#x20;__ :small\_blue\_diamond:`Datensätze anderer Anbieter importieren`

_Hier kann angegeben werden, wie mit Immobilien anderer Anbieter umgegangen werden soll. Für gewöhnlich werden innerhalb einer OpenImmo Übertragung lediglich Immobilien des eigenen Anbieters übertragen. Sollte dies nicht der Fall sein, können Immobilien anderer Anbieter schlicht mit den Einstellungen der eigenen Schnittstelle importiert werden oder alternativ anhand der Vermarktungsart einer bestimmten Kontaktperson zugeordnet werden._

#### Zuweisung von Datensätzen

Durch Auswahl der Option "Zuweisen" können **Datensätze**, welche **keinen Anbieter zugeordnet** werden können, **einer bestimmten Kontaktperson zugeordnet werden**.

:small\_blue\_diamond:`Kontaktperson Kauf-Objekte`

_Hier müssen Sie eine Kontaktperson auswählen, welcher **Kauf-Objekte** zugewiesen werden._

:small\_blue\_diamond:`Kontaktperson Miet-Objekte`

_Hier müssen Sie eine Kontaktperson auswählen, welcher **Miet-Objekte** zugewiesen werden._

:small\_blue\_diamond:`Kontaktperson Erbpacht-Objekte`

_Hier müssen Sie eine Kontaktperson auswählen, welcher **Erbpacht-Objekte** zugewiesen werden._

:small\_blue\_diamond:`Kontaktperson Leasing-Objekte`

_Hier müssen Sie eine Kontaktperson auswählen, welcher **Leasing-Objekte** zugewiesen werden._

### Experten-Einstellungen

:small\_blue\_diamond:`Datensätze überspringen`

_Hier können Sie **auswählen,** ob Immobiliendatensätze mit **fehlendem Objekttitel** oder fehlender **Objektbeschreibung**  <mark style="color:orange;">**nicht importiert**</mark> werden sollen._

:small\_blue\_diamond:`Datensätze nicht veröffentlichen`

_Einstellung, um **neu importierte Immobiliendatensätze nicht automatisch** auf der Website zu **veröffentlichen**._

### Synchronisierungs-Einstellungen

Für jede Schnittstelle kann festgelegt werden, wie oft die Synchronisierung der Immobiliendatensätze stattfinden soll, wie lange alte Synchronisierungsdateien existieren dürfen und wie viele Dateien pro Vorgang synchronisiert werden sollen.

{% hint style="warning" %}
Die Ausführung der Synchronisierung erfolgt über einen **poor man cron**. Hierbei handelt es sich um ein Modul, welches die **Cron-Operation** über **normale Browser-/Seitenanfragen** ausführt.\
\
[Weitere Hinweise zu Cronjobs (Contao)](https://docs.contao.org/manual/de/system/einstellungen/#cronjob-einstellungen)
{% endhint %}

:small\_blue\_diamond:`Automatische Synchronisierung`

_Hier kann die **Frequenz** der automatischen Synchronisierung eingestellt werden. Um **nur manuelle** Synchronisationen zu erlauben, kann hier "**Niemals**" ausgewählt werden._\
_Die manuelle Synchronisation wird über das_ ![](../../.gitbook/assets/sync.svg)-Symbol in der Übersicht ausgeführt.

:small\_blue\_diamond:`Dateien älter als * löschen`

Bereits **synchronisierte Immobiliendatensätze** werden **nicht** automatisch **gelöscht**. Mithilfe dieser Einstellung werden diese Datensätze **nach der eingestellten Frequenz gelöscht**.

:small\_blue\_diamond:`Maximale Anzahl an Dateien pro Synchronisation`

Hier kann die maximale Anzahl an Dateien definiert werden, welche während des Imports synchronisiert werden sollen.
