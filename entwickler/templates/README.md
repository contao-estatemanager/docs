# Templates

Wie in Contao selber, können alle Templates des EstateManagers über den Reiter _Templates_ im Backend angepasst, überschrieben oder ergänzt werden. Dabei gibt es die Besonderheit, dass Templates welche für die Darstellung einer einzelnen Immobilien bereitgestellt werden, ein Objekt mit nützlichen Funktionen sowie den Immobilien-Eigenschaften übergeben wird. Dadurch können jegliche Informationen direkt über das Template abgerufen werden.

{% hint style="warning" %}
Das Immobilien-Objekt steht erst ab **Version 1.0** in Templates zur Verfügung.
{% endhint %}

### Template-Übersicht

| Template-Präfix \(html5\) | Beschreibung |   |
| :--- | :--- | ---: |
| **real\_estate\_item\_\*** | Definiert die Darstellung pro Immobilie in Listen. | ✅ |
| real\_estate\_item\_default |  | ✅ |
| real\_estate\_item\_simple |  | ✅ |
| **real\_estate\_itemext\_\*** | Templates für die Ergänzung weiterer Bestandteile für die Darstellung pro Immobilie in Listen. | ✅ |
| real\_estate\_itemext\_contact\_person\_default | Ausgabe der Kontaktperson pro Immobilie in Listen. | ✅ |
| real\_estate\_itemext\_provider\_default | Ausgabe des Anbieters pro Immobilie in Listen. | ✅ |
| **expose\_mod\_\*** | Definiert die Ausgabe des Exposé-Moduls. | ✅ |
| expose\_mod\_address |  | ✅ |
| expose\_mod\_attachments |  | ✅ |
| expose\_mod\_contactPerson |  | ✅ |
| expose\_mod\_details |  | ✅ |
| expose\_mod\_enquiryForm |  | ✅ |
| expose\_mod\_fieldList |  | ✅ |
| expose\_mod\_gallery |  | ✅ |
| expose\_mod\_gallery\_items |  | ✅ |
| expose\_mod\_html |  | ✅ |
| expose\_mod\_mainArea |  | ✅ |
| expose\_mod\_mainAttributes |  | ✅ |
| expose\_mod\_mainDetails |  | ✅ |
| expose\_mod\_mainPrice |  | ✅ |
| expose\_mod\_marketingToken |  | ✅ |
| expose\_mod\_print |  | ✅ |
| expose\_mod\_share |  | ✅ |
| expose\_mod\_share\_email |  | ✅ |
| expose\_mod\_statusToken |  | ✅ |
| expose\_mod\_texts |  | ✅ |
| expose\_mod\_title |  | ✅ |
| **mod\_realEstate\*** | Modul-Templates | ✖  |
| mod\_realEstateExpose |  | ✖ |
| mod\_realEstateList |  | ✖ |
| mod\_realEstateResultList |  | ✖ |

✅_Das Immobilien-Objekt steht im Template zur Verfügung_  
✖_Das Immobilien-Objekt steht **nicht** im Template zur Verfügung_

### Eigenschaften über das Immobilien-Objekt aus dem Template heraus abrufen

Über `$this->realEstate` kann auf Methoden und Eigenschaften zugegriffen werden. Sofern eine Funktion ohne eigene Parameterübergabe aufgerufen wird, werden die im Modul hinterlegten Einstellungen übernommen. Sollten wir uns bspw. im Listen-Modul befinden und wie im folgenden Beispiel die Funktion `generateExposeUrl` ohne eigene Parameter aufrufen, wird automatisch die im Modul hinterlegte "Weiterleitungsseite" verwendet, um die Exposé-URL zu generieren.

{% code title="Template - Beispiel 1" %}
```markup
<a href="<?= $this->realEstate->generateExposeUrl() ?>">Details</a>
```
{% endcode %}

{% hint style="info" %}
Bitte beachte, dass Eigenschaften, welche über bereitgestellte Funktionen abgeholt werden, meist als [FormattedCollection](formattedcollection.md) zurückgeliefert und somit bspw. durchlaufen werden müssen.
{% endhint %}

Der direkte Zugriff auf eine Eigenschaft liefert dabei immer den unformatierten Wert zurück. Um den formatierten Wert zu erhalten, muss die Eigenschaft über die `get` -Methode abgerufen werden.

{% code title="Template - Beispiel 2" %}
```php
// Formatierter Wert (array<FormattedCollection>|null)
<?= $this->realEstate->get('kaufpreis') ?> 

// Unformatierter Wert (string|float)
<?= $this->realEstate->kaufpreis ?>
```
{% endcode %}

