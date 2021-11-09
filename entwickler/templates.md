# Templates

Wie in Contao selber, können alle Templates des EstateManagers über den Reiter _Templates_ im Backend angepasst, überschrieben oder ergänzt werden. Dabei gibt es die Besonderheit, dass Templates welche für die Darstellung einzelner Immobilien bereitgestellt werden, ein Objekt mit [nützlichen Funktionen](immobilien-eigenschaften/immobilien-objekt.md) sowie den [Immobilien-Eigenschaften](immobilien-eigenschaften/) übergeben wird. Dadurch können jegliche Informationen direkt über das Template abgerufen werden.

{% hint style="warning" %}
Das [Immobilien-Objekt](immobilien-eigenschaften/immobilien-objekt.md) steht erst ab **Version 1.0** in Templates zur Verfügung.
{% endhint %}

### Template-Übersicht

| Template-Präfix (html5)                         | Beschreibung                                                                                   |                             |
| ----------------------------------------------- | ---------------------------------------------------------------------------------------------- | --------------------------: |
| **real\_estate\_item\_\***                      | Definiert die Darstellung pro Immobilie in Listen.                                             |        :white\_check\_mark: |
| real\_estate\_item\_default                     |                                                                                                |        :white\_check\_mark: |
| real\_estate\_item\_simple                      |                                                                                                |        :white\_check\_mark: |
| **real\_estate\_itemext\_\***                   | Templates für die Ergänzung weiterer Bestandteile für die Darstellung pro Immobilie in Listen. |        :white\_check\_mark: |
| real\_estate\_itemext\_contact\_person\_default | Ausgabe der Kontaktperson pro Immobilie in Listen.                                             |        :white\_check\_mark: |
| real\_estate\_itemext\_provider\_default        | Ausgabe des Anbieters pro Immobilie in Listen.                                                 |        :white\_check\_mark: |
| **expose\_mod\_\***                             | Definiert die Ausgabe des Exposé-Moduls.                                                       |        :white\_check\_mark: |
| expose\_mod\_address                            |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_attachments                        |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_contactPerson                      |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_details                            |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_enquiryForm                        |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_fieldList                          |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_gallery                            |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_gallery\_items                     |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_html                               |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_mainArea                           |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_mainAttributes                     |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_mainDetails                        |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_mainPrice                          |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_marketingToken                     |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_print                              |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_share                              |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_share\_email                       |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_statusToken                        |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_texts                              |                                                                                                |        :white\_check\_mark: |
| expose\_mod\_title                              |                                                                                                |        :white\_check\_mark: |
| **mod\_realEstate\***                           | Modul-Templates                                                                                | :heavy\_multiplication\_x:  |
| mod\_realEstateExpose                           |                                                                                                |  :heavy\_multiplication\_x: |
| mod\_realEstateList                             |                                                                                                |  :heavy\_multiplication\_x: |
| mod\_realEstateResultList                       |                                                                                                |  :heavy\_multiplication\_x: |

:white\_check\_mark:_Das _[_Immobilien-Objekt_](immobilien-eigenschaften/immobilien-objekt.md)_ steht im Template zur Verfügung_\
__:heavy\_multiplication\_x:_Das _[_Immobilien-Objekt_](immobilien-eigenschaften/immobilien-objekt.md)_ steht **nicht **im Template zur Verfügung_

### Eigenschaften über das Immobilien-Objekt aus dem Template heraus abrufen

Über `$this->realEstate` kann auf Methoden und Eigenschaften zugegriffen werden. Sofern eine Funktion ohne eigene Parameterübergabe aufgerufen wird, werden die im Modul hinterlegten Einstellungen übernommen. Sollten wir uns bspw. im Listen-Modul befinden und wie im folgenden Beispiel die Funktion `generateExposeUrl` ohne eigene Parameter aufrufen, wird automatisch die im Modul hinterlegte "Weiterleitungsseite" verwendet, um die Exposé-URL zu generieren.

{% code title="Template - Beispiel 1" %}
```markup
<a href="<?= $this->realEstate->generateExposeUrl() ?>">Details</a>
```
{% endcode %}

{% hint style="info" %}
Bitte beachte, dass Eigenschaften, welche über bereitgestellte Funktionen abgeholt werden, meist als [FormattedCollection](immobilien-eigenschaften/formattedcollection.md) zurückgeliefert werden.
{% endhint %}

Der direkte Zugriff auf eine Eigenschaft liefert dabei immer den unformatierten Wert zurück. Um den formatierten Wert, sowie weitere Informationen zu erhalten, muss die Eigenschaft über die `get` -Methode abgerufen werden.

{% code title="Template - Beispiel 2" %}
```php
// Formatierter Wert (array<FormattedCollection>|null)
<?php $price = $this->realEstate->get('kaufpreis') ?> 

// Unformatierter Wert (string|float)
<?= $this->realEstate->kaufpreis ?>
```
{% endcode %}
