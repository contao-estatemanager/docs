# Immobilien-Exposé

Das `Immobilien-Exposé` Modul ermöglicht die Zusammenfassung und Ausgabe der Exposé-Module um eine Immobilien im Detail zu präsentieren.

### Einstellungen

🔹`Exposé-Module`

_Hier können die zuvor unter_ [_Exposé-Module_](../../backend-konfiguration/expose-module/) _definierten Module in beliebiger Reihenfolge ausgewählt und in die für ein Exposé vordefinierten Layoutbereiche eingefügt werden._

🔹`Referenzen erlauben`

_Erlaubt die Darstellung von Referenz-Immobilien in diesem Modul_

### Layoutbereiche

Das `Immobilien-Exposé` Modul liefert eigene Layoutbereiche, welche über das Exposé-Module Feld befüllt werden können. Folgende Layoutbereiche stehen dabei zur Verfügung.

1⃣ Kopfzeile   
2 Über dem Inhaltsbereich  
3⃣ Linke Spalte  
4⃣ Hauptspalte  
5⃣ Rechte Spalte  
6 Unter dem Inhaltsbereich  
7⃣ Fußzeile

![Expos&#xE9;-Modul - Layoutbereiche](../../../.gitbook/assets/expose-layoutbereiche.jpg)

{% hint style="info" %}
Layoutbereiche bilden ausschließlich die Struktur der Ausgabe ab. Die Anordnung und dessen Darstellung müssen selber über CSS definiert werden.
{% endhint %}

### Template

🔸`mod_realEstateExpose`



