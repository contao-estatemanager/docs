# Immobilien-Liste

Das "Immobilien-Liste"-Modul liefert den Einstellungen entsprechend eine Liste von Immobilien aus.

### Einstellungen

<span class="field">Gesamtanzahl der Beiträge</span>

Hier können die auszugebenden Immobilien begrenzt werden.

<span class="field">Elemente pro Seite</span>

Die Anzahl an Elementen pro Seite.

<span class="field">Leere Listen ausgeben</span>

Sollte für die aktuelle Konfiguration der Liste keine Immobilie gefunden werden, kann die Liste mit dieser Einstellung dennoch ausgegeben werden.

<span class="field">Ausgabe-Modus</span>

Der Ausgabe-Modus bietet die Möglichkeit die Immobilien-Typen der Ausgabe wie bspw. `Bisher besuchte Immobilien`, eine `Immobilien-Gruppe` oder `Ferienimmobilien` zu definieren.

<span class="field">Immobilien-Gruppen</span>

Auswahl der anzuzeigenden Immobilien-Gruppen.

<span class="field">Filter-Modus</span>

Über den Filter-Modus kann die Liste auf einen bestimmten Typ an Immobilien begrenzt werden.

<span class="field">Sortierreihenfolge</span>

Definiert die Reihenfolge wie die Immobilien ausgegeben werden. Bspw. nach `Einstellungsdatum` oder `Aktualität`.

<span class="field">Benutzerdefinierte Sortierung hinzufügen</span>

Ermöglicht die Ergänzung einer benutzerdefinierten Sortierung.

<span class="field">Benutzerdefinierte Sortierung</span>

Hier muss das benutzerdefinierte SQL-Order-Statement eingetragen werden (z.B. FIELD(anbieternr, 'xyz')). Bitte beachte, dass die zuvor über das Feld_ `Sortierreihenfolge` ausgewählte Eigenschaft immer mit Priorität behandelt wird.

<span class="field">Weiterleitungsseite</span>

Die Seite auf welche bei Klick auf einer Immobilie weitergeleitet werden soll.

<span class="field">Erlaubte Status-Token</span>

Definiert die anzuzeigenden Status-Token in diesem Modul.

### Immobilien-Erweiterungen

Immobilien-Erweiterungen ermöglichen bspw. die Ausgabe des `Anbieters` oder der zugewiesenen `Kontaktperson` pro Immobilie. Durch Erweiterungen kann dieser Bereich um weitere Funktionalitäten erweitert werden.

### Templates

<span class="template-field">mod_realEstateList</span>

**Immobilien-Templates**

<span class="template-field">real_estate_item_default</span>

<span class="template-field">real_estate_item_simple</span>

#### Immobilien Template Erweiterung: Anbieter

<span class="template-field">real_estate_itemext_provider_default</span>

#### Immobilien Template Erweiterung: Kontaktperson

<span class="template-field">real_estate_itemext_contact_person_default</span>
