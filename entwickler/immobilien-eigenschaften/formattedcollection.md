---
description: Aufbereitung eines Immobilien-Datensatzes
---

# FormattedCollection

Wie bereits unter [Feldformatierungen](../../installation-konfiguration/backend-konfiguration/feldformatierungen.md) beschrieben, können Werte der verfügbaren Immobilien-Eigenschaften über verschiedene Aktionen formatiert, umgewandelt oder gar ausgetauscht werden. Beim abholen der anzuzeigenden Felder wird der Wert also immer unter Berücksichtigung dieser Konfiguration validiert und ausgegeben.

Eine `FormattedCollection` bezeichnet also ein Paket von validierten / formatierten Feldwerten und setzt sich aus folgenden Bestandteilen zusammen:

```php
// FormattedCollection
array(
    'value' // formatierter Wert
    'raw'   // unformatierter Wert
    'label' // übersetzter Bezeichner
    'key'   // Feldname (nicht übersetzt)
    'class' // individuelle CSS-Klasse
);
```

