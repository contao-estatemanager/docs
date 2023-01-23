# Immobilien-Exposé

Das `Immobilien-Exposé` Modul ermöglicht die Zusammenfassung und Ausgabe der Exposé-Module um eine Immobilien im Detail zu präsentieren.

### Einstellungen

:small\_blue\_diamond:`Exposé-Module`

_Hier können die zuvor unter _[_Exposé-Module_](../../backend-konfiguration/expose-module/)_ definierten Module in beliebiger Reihenfolge ausgewählt und in die für ein Exposé vordefinierten Layoutbereiche eingefügt werden._

:small\_blue\_diamond:`Referenzen erlauben`

_Erlaubt die Darstellung von Referenz-Immobilien in diesem Modul_

### Layoutbereiche

Das `Immobilien-Exposé` Modul liefert eigene Layoutbereiche, welche über das Exposé-Module Feld befüllt werden können. Folgende Layoutbereiche stehen dabei zur Verfügung.

:one: Kopfzeile \
:digit\_two: Über dem Inhaltsbereich\
:three: Linke Spalte\
:four: Hauptspalte\
:five: Rechte Spalte\
:digit\_six: Unter dem Inhaltsbereich\
:seven: Fußzeile

![Exposé-Modul - Layoutbereiche](../../../.gitbook/assets/expose-layoutbereiche.jpg)

{% hint style="info" %}
Layoutbereiche bilden ausschließlich die Struktur der Ausgabe ab. Die Anordnung und dessen Darstellung müssen selber über CSS definiert werden.
{% endhint %}

### Template

:small\_orange\_diamond:`mod_realEstateExpose`

