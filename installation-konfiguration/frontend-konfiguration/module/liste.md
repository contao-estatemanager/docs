# Liste

Das `Listen`-Modul liefert den Einstellungen entsprechend ein Liste von Immobilien aus.

### Einstellungen

🔹`Gesamtanzahl der Beiträge`

_Hier können die auszugebenden Immobilien begrenzt werden._

\_\_🔹`Elemente pro Seite`

_Die Anzahl an Elementen pro Seite._

🔹`Leere Listen ausgeben`

_Sollte für die aktuelle Konfiguration der Liste keine Immobilie gefunden werden, kann die Liste mit dieser Einstellung dennoch ausgegeben werden._

🔹`Ausgabe-Modus`

_Der Ausgabe-Modus bietet die Möglichkeit die Immobilien-Typen der Ausgabe wie bspw. `Bisher besuchte Immobilien`, eine `Immobilien-Gruppe` oder `Ferienimmobilien` zu definieren._

🔹`Immobilien-Gruppen`

_Auswahl der anzuzeigenden Immobilien-Gruppen._

🔹`Filter-Modus`

_Über den Filter-Modus kann die Liste auf einen bestimmten Typ an Immobilien begrenzt werden._

🔹`Sortierreihenfolge`

_Definiert die Reihenfolge wie die Immobilien ausgegeben werden. Bspw. nach `Einstellungsdatum` oder `Aktualität`._

🔹_`Benutzerdefinierte Sortierung hinzufügen`_

_Ermöglicht die Ergänzung einer benutzerdefinierten Sortierung._

🔹`Benutzerdefinierte Sortierung`

_Hier muss das Benutzerdefinierte SQL-Order-Statement eingetragen werden \(z.B. FIELD\(anbieternr, 'xyz'\)\). Bitte beachte, dass die zuvor über das Feld_ `Sortierreihenfolge` ausgewählte Eigenschaft immer mit Priorität behandelt wird.

🔹`Weiterleitungsseite`

_Die Seite auf welche bei Klick auf einer Immobilie weitergeleitet werden soll._

🔹`Erlaubte Status-Token`

_Definiert die anzuzeigenden Status-Token in diesem Modul._

### Immobilien-Erweiterungen

Immobilien-Erweiterungen ermöglichen bspw. die Ausgabe des `Anbieters` oder der zugewiesenen `Kontaktperson` pro Immobilie. Durch Erweiterungen kann dieser Bereich um weitere Funktionalitäten ergänzt werden \(s. bspw. [Merkzettel](../../../erweiterungen/erweiterungen/merkzettel.md)\).

### Templates

**Immobilien-Templates**

🔸`real_estate_item_default`

🔸`real_estate_item_simple`

#### Immobilien Template Erweiterung: Anbieter

🔸`real_estate_itemext_provider_default`

#### Immobilien Template Erweiterung: Kontaktperson

🔸`real_estate_itemext_contact_person_default`

\_\_

