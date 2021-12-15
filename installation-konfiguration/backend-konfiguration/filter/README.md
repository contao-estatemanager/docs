---
description: Ein Immobilienfilter zur Suche und Filterung von Objekten
---

# Filter

Mithilfe von Immobilien-Filtern lassen sich Objekte in Kombination mit einer Immobilien-Ergebnisliste suche und filtern. Ein eingestellter Filter lässt sich als Inhaltselement oder als Frontend-Modul in einer Seite einbinden.

![](../../../.gitbook/assets/Filter.png)

### Funktionsweise

Filter können grundsätzlich wie Formulare im Contao Formulargenerator aufgebaut und verwaltet werden. Anstelle von Formularfeldern stehen dabei in der Filterverwaltung sogenannte Filter-Widgets zur verfügung, über die ein Filter ganz nach den eigenen Wünschen eingerichtet werden kann.

### Neuen Filter erstellen

Neue Filter können über **Neuer Filter** ![](../../../.gitbook/assets/new.svg) erstellt werden.

### Titel & Weiterleitung

:small\_blue\_diamond:`Titel`

Dient der Identifizierung im Backend.

``:small\_blue\_diamond:`Filteralias`

Der Filteralias ist eine eindeutige Referenz, die anstelle der numerischen Filter-ID verwendet werden kann.

:small\_blue\_diamond:`Weiterleitungsseite`

Hier kann die Seite eingetragen werden, zu der man beim Abschicken des Filters weitergeleitet wird.

{% hint style="info" %}
Verfügen Objekttypen eine eigene Referenzseite, muss die Weiterleitungsseite ggf. auf die Übersichtsseite aller Immobilien weitergeleitet werden, um stets zur korrekten Unterseite Weitergeleitet zu werden.
{% endhint %}

### Filter-Einstellungen

:small\_blue\_diamond:`Objektgruppen`

Hier können die Objektgruppen ausgewählt werden, die für die Filterung berücksichtigt werden sollen.

:small\_blue\_diamond:`Bei Änderung Seite wechseln`

Hier kann eingestellt werden, ob der Filter automatisch abgeschickt wird bei Änderung der Objektart.

:small\_blue\_diamond:`Standardfilter`

Standardfilter werden angezeigt, wenn kein spezieller Objekttyp ausgewählt wurde.&#x20;

{% hint style="info" %}
Standardfilter sollten den kleinsten gemeinsamen Nenner aller Filtermöglichkeiten der verfügbaren Objekttypen anbieten. In der Regel sind dies _Preise_ und _Flächen_, allerdings kann auch die _Anzahl der Zimmer_ relevant sein, wenn keine Grundstücke angeboten werden.
{% endhint %}

:small\_blue\_diamond:`Verfügbare Optionen: Zimmer`

Eine kommagetrennte Liste der verfügbaren Optionen im Filter für die _Anzahl der Zimmer_. Mit Hilfe eines Punktes können auch halbe Zimmer angegeben werden (1, 1.5, 2, 2.5, 3, etc.).
