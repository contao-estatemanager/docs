# Schnittstellen

Mit Hilfe von Schnittstellen können Immobilen und Kontaktpersonen importiert, sowie mit einer Maklersoftware synchronisiert werden. Der Abgleich von Immobilien findet dabei auf Basis des OpenImmo Standards statt, sodass Immobilien-Datensätze und dessen Kontaktpersonen automatisch erstellt, aktualisiert und gelöscht werden können.

### Schnittstellen konfigurieren

Schnittstellen können den eigenen Anforderungen entsprechend umfangreich konfiguriert werden. Dabei können beliebig viele Schnittstellen angelegt werden, um Datensätze unterschiedlicher Quellen und Strukturen zuverlässig importieren zu können. Eine Schnittstelle muss einem eindeutigen Anbieter zugeordnet werden, weshalb vor der Schnittstellen-Konfiguration der entsprechende Anbieter angelegt werden muss.

:small\_blue\_diamond:`Titel`

_Dient der Identifizierung einer Schnittstelle im Backend_

:small\_blue\_diamond:`Typ`

_Mit Hilfe des Typs können verschiedene Arten von Schnittstellen konfiguriert werden. Im Standard steht ausschließlich der Typ "OpenImmo" zur Verfügung, welcher den Import nach den Regeln des OpenImmo Standards durchführt_

__:small\_blue\_diamond:`Anbieter`

_Eine Schnittstelle muss einem bestimmten Anbieter zugeordnet werden, damit Immobilien und Kontaktpersonen stets diesem Anbieter zugeordnet werden können_

:small\_blue\_diamond:`Anbieternummer`

_Die eindeutige Anbieternummer der OpenImmo Übertragung_

:small\_blue\_diamond:`Eindeutiges Anbieterfeld`

_Gibt an, über welchen Wert eine OpenImmo Übertragung eindeutig einem bestimmten Anbieter zugeordnet werden kann_

:small\_blue\_diamond:`Eindeutiges Feld`

_Gibt an, über welchen Wert eine OpenImmo Übertragung eindeutig einer bestimmten Immobilie zugeordnet werden kann_

{% hint style="warning" %}
Immobilien müssen auf mehrsprachigen Websites mehrfach in den jeweils unterschiedlichen Sprachen importiert werden. Diese Immobilien teilen sich dabei oft eine gemeinsame Objektnummer, weswegen das eindeutige Feld auf den Wert festgelegt werden muss, über den sich ein Immobiliendatensatz eindeutig identifizieren lässt.
{% endhint %}

:small\_blue\_diamond:`Importverzeichnis`

_Verzeichnis, in dem OpenImmo Übertragungen abgelegt werden, damit diese durch die Schnittstelle gefunden und importiert werden kann_

:small\_blue\_diamond:`Zielverzeichnis`

_Verzeichnis, in dem Bilder und Dokumente von Immobiliendatensätzen abgelegt werden. Für jeden Immobiliendatensatz wird dabei ein eigener Ordner (Objektnummer) innerhalb eines Ordners des Anbieters (Anbieternummer) angelegt_

:small\_blue\_diamond:`Importverzeichnis Kontaktperson`

_Verzeichnis, in dem Bilder von Kontaktpersonen abgelegt werden_

#### Datensätze Erstellen & Aktualisieren

Über die Palette "Erstellen & Aktualisieren" kann eingestellt werden, wie Kontaktpersonen während eines Imports behandelt werden sollen und ob Immobilien anderer Anbieter Importiert und dabei einer eigenen Kontaktperson zugeordnet werden sollen.

:small\_blue\_diamond:`Kontaktperson`

_Hier kann angegeben werden, ob neue Kontaktpersonen durch die Schnittstelle erstellt und / oder aktualisiert werden sollen_

{% hint style="warning" %}
Kann eine Immobilie während eines Imports keiner Kontaktperson zugeordnet werden, wird die Immobilie übersprungen und nicht importiert. Darf über die Schnittstelle keine Kontaktperson erstellt werden, muss sichergestellt werden, dass die Kontaktperson in der Anbieterverwaltung existiert, um Immobilien importieren zu können.
{% endhint %}

:small\_blue\_diamond:`Eindeutiges Feld der Kontaktperson`

_Hier muss das Feld angegeben werden, über das eine Kontaktperson eindeutig identifiziert werden kann._

&#x20;__ :small\_blue\_diamond:`Datensätze anderer Anbieter importieren`

_Hier kann angegeben werden, wie mit Immobilien anderer Anbieter umgegangen werden soll. Für gewöhnlich werden innerhalb einer OpenImmo Übertragung lediglich Immobilien des eigenen Anbieters übertragen. Sollte dies nicht der Fall sein, können Immobilien anderer Anbieter schlicht mit den Einstellungen der eigenen Schnittstelle importiert werden, oder alternativ anhand der Vermarktungsart einer bestimmten Kontaktperson zugeordnet werden._

#### Weitere Einstellungen

:small\_blue\_diamond:`Datensätze überspringen`

_Hier kann angegeben werden, ob Immobiliendatensätze nicht importiert werden sollen, wenn der Objekttitel oder die Objektbeschreibung nicht übergeben wurden._

:small\_blue\_diamond:`Datensätze nicht veröffentlichen`

_Einstellung, um neue Immobiliendatensätze nicht automatisch auf der Website zu veröffentlichen._
