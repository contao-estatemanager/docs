# Primäre Felder

Das `primäre Felder` Widget zeigt dynamisch die Filtermöglichkeiten an, **welche in einem Objekttyp als Suchfelder aktiviert wurden**. Dadurch ist es möglich, genau einzustellen, welche Filtermöglichkeiten bei der Auswahl jedes einzelnen Objekttypen zur Verfügung stehen.

{% hint style="warning" %}
**JavaScript-Template notwendig**

Damit die korrekten Filter automatisch anhand des Objekttypen ausgegeben werden können, muss **im Layout** das "**js\_**_**em**_**\_filter"** JavaScript-Template **aktiviert werden**.
{% endhint %}

### Anwendungsbeispiel

Die verschiedenen [Objekttypen](../../objekttypen/objekttypen.md) zeichnen sich fachlich durch unterschiedliche Eckdaten und Informationen aus. Alle Objekttypen lassen sich in der Regel anhand des Preises oder der Fläche filtern. Bei Anzahl der Zimmer wird dieser Umstand im Falle von Grundstücken allerdings schwieriger. Bei Gewerbeobjekten ist oftmals der Quadratmeterpreis entscheidend, sodass bei jedem Objekttyp die Filtermöglichkeiten nach Bedarf definiert werden können.

### Konfiguration

:small\_blue\_diamond:`Label anzeigen`

Hier kann eingestellt werden, ob HTML-Label vor den eigentlichen Auswahlfeldern ausgeliefert werden sollen.

:small\_blue\_diamond:`Placeholder anzeigen`

Hier kann angegeben werden, ob Placeholder in den jeweiligen Auswahlfeldern ausgegeben werden sollen.

:small\_blue\_diamond:`Bereichs-Modus`

Hier kann eingestellt werden, dass in einen Bereich von zwei Werten gefiltert werden soll (Von-Bis Suche).
