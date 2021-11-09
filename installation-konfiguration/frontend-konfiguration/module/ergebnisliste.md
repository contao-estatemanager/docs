# Immobilien-Ergebnisliste

Das `Immobilien-Ergebnislisten`-Modul liefert den Einstellungen entsprechend eine Liste von Immobilien unter Berücksichtigung eines [Filters](../../backend-konfiguration/filter/) aus.

### Einstellungen

:small\_blue\_diamond:`Gesamtanzahl der Beiträge`

_Hier können die auszugebenden Immobilien begrenzt werden._

__:small\_blue\_diamond:`Elemente pro Seite`

_Die Anzahl an Elementen pro Seite._

:small\_blue\_diamond:`Immobilien-Gruppen`

_Auswahl der anzuzeigenden Immobilien-Gruppen._

:small\_blue\_diamond:`Filter-Modus`

_Über den Filter-Modus kann die Liste auf einen bestimmten Typ an Immobilien begrenzt werden._

:small\_blue\_diamond:`Anzahl der Immobilien ausgeben`

_Gibt die Anzahl gefundener Immobilien unter Berücksichtigung der Filtereinstellungen aus._

:small\_blue\_diamond:`Sortierung hinzufügen`

_Definiert die Reihenfolge wie die Immobilien ausgegeben werden. Bspw. nach `Datum`._

:small\_blue\_diamond:_`Benutzerdefinierte Sortierung hinzufügen`_

_Ermöglicht die Ergänzung einer benutzerdefinierten Sortierung._

:small\_blue\_diamond:`Benutzerdefinierte Sortierung`

_Hier muss das Benutzerdefinierte SQL-Order-Statement eingetragen werden (z.B. FIELD(anbieternr, 'xyz')). Bitte beachte, dass die zuvor über das Feld _`Sortierreihenfolge` ausgewählte Eigenschaft immer mit Priorität behandelt wird.

:small\_blue\_diamond:`Weiterleitungsseite`

_Die Seite auf welche bei Klick auf einer Immobilie weitergeleitet werden soll._

:small\_blue\_diamond:`Erlaubte Status-Token`

_Definiert die anzuzeigenden Status-Token in diesem Modul._

### Immobilien-Erweiterungen

Immobilien-Erweiterungen ermöglichen bspw. die Ausgabe des `Anbieters` oder der zugewiesenen `Kontaktperson` pro Immobilie. Durch Erweiterungen kann dieser Bereich um weitere Funktionalitäten ergänzt werden (s. bspw. [Merkzettel](../../../erweiterungen/erweiterungen/merkzettel.md)).

### Templates

:small\_orange\_diamond:`mod_realEstateResultList`

**Immobilien-Templates**

:small\_orange\_diamond:`real_estate_item_default`

:small\_orange\_diamond:`real_estate_item_simple`

#### Immobilien Template Erweiterung: Anbieter

:small\_orange\_diamond:`real_estate_itemext_provider_default`

#### Immobilien Template Erweiterung: Kontaktperson

:small\_orange\_diamond:`real_estate_itemext_contact_person_default`

__
