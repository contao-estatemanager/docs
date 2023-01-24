# Filter

Mithilfe von Immobilien-Filtern lassen sich Objekte in Kombination mit einer Immobilien-Ergebnisliste suchen und filtern. Ein eingestellter Filter lässt sich als Inhaltselement oder als Frontend-Modul in einer Seite einbinden.

![](../../../_media/Filter.png)

### Funktionsweise

Filter können ähnlich wie Formulare im Contao Formulargenerator aufgebaut und verwaltet werden. Anstelle von Formularfeldern stehen dabei in der Filterverwaltung sogenannte Filter-Widgets zur Verfügung, über die ein Filter ganz nach den eigenen Wünschen eingerichtet werden kann.

### Neuen Filter erstellen

Neue Filter können über **Neuer Filter** ![](../../../../_media/new.svg) erstellt werden.

### Titel & Weiterleitung

<span class="field">Titel</span>

Dient der Identifizierung im Backend.

<span class="field">Filteralias</span>

Der Filteralias ist eine eindeutige Referenz, die anstelle der numerischen Filter-ID verwendet werden kann.

<span class="field">Weiterleitungsseite</span>

Hier kann die Seite eingetragen werden, zu der man beim Abschicken des Filters weitergeleitet wird.

?> Verfügen Objekttypen über eine eigene Referenzseite, muss die Weiterleitungsseite ggf. auf die Übersichtsseite aller Immobilien weitergeleitet werden, um stets zur korrekten Unterseite weitergeleitet zu werden.

### Filter-Einstellungen

<span class="field">Objektgruppen</span>

Hier können die Objektgruppen ausgewählt werden, die für die Filterung berücksichtigt werden sollen.

<span class="field">Bei Änderung Seite wechseln</span>

Hier kann eingestellt werden, ob der Filter automatisch abgeschickt wird bei Änderung der Objektart.

<span class="field">Standardfilter</span>

Standardfilter werden angezeigt, wenn kein spezieller Objekttyp ausgewählt wurde.&#x20;

?> Standardfilter sollten den kleinsten gemeinsamen Nenner aller Filtermöglichkeiten der verfügbaren Objekttypen anbieten. In der Regel sind dies _Preise_ und _Flächen_, allerdings kann auch die _Anzahl der Zimmer_ relevant sein, wenn keine Grundstücke angeboten werden.

<span class="field">Verfügbare Optionen: Zimmer</span>

Eine kommagetrennte Liste der verfügbaren Optionen im Filter für die _Anzahl der Zimmer_. Mit Hilfe eines Punktes können auch halbe Zimmer angegeben werden (1, 1.5, 2, 2.5, 3, etc.).
