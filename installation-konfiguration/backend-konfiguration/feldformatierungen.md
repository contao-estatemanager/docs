---
description: Formatierung und Ausgabe der Immobilienfelder
---

# Feldformatierungen

Um Immobilienfelder für die Ausgabe aufzubereiten bietet der EstateManager ein umfangreiches Werkzeug und beliebige Aktionen auf Felder und dessen Werte einer Immobilie anzuwenden.

### Formatierung zurücksetzen

Von Haus aus liefert der EstateManager bereits eine Vorkonfiguration von Feldern und dessen Aktionen aus, welche im ersten Schritt über den Button "Formatierung zurücksetzen" importiert werden können.

{% hint style="warning" %}
Bitte beachte, dass manuelle Änderungen nach dem zurücksetzen verworfen werden
{% endhint %}

### Feldformatierung erstellen

Über den Button "Neues Feld" können alle Immobilien-Felder, welche in der Datenbank bestehen, ausgewählt und eingerichtet werden.

**`Feld`**  
Definiert das Feld, welches durch eine Formatierung vor der Ausgabe manipuliert werden soll.

**`CSS-Klasse`**  
Jedes Feld kann ein oder mehrere CSS-Klassen beinhalten \(Leerzeichen getrennte Liste\). Dies ermöglicht die Erstellung eigener Selektoren um diese später mit CSS aufbereiten zu können.

**`Ausgabe erzwingen`**  
Erzwingt die Ausgabe des Feldes, auch wenn kein oder ein leerer Wert vorhanden ist.

> **Beispiel:**  
> In den Details sollen "Haustiere" immer ausgegeben werden. Wurde dieser Wert nicht übertragen, können wir davon ausgehen, dass das Objekt / die Immobilie keine Haustiere erlaubt. Wird die Ausgabe erzwungen, ist es egal, ob der Wert übertragen wurde. Somit würde nun "Haustiere: Nein" ebenfalls ausgegeben und nicht als leerer Wert erkannt und somit übersprungen werden.

**`Bedingung hinzufügen`**  
Ermöglicht die Definition einer oder mehrerer Bedingung.

> **Beispiel:**  
> Die Kaltmiete darf ausschließlich angezeigt werden, wenn die Vermarktungsart "miete" ist.

{% hint style="info" %}
Beim hinzufügen mehrerer Bedingungen werden diese "UND"-Verknüpft
{% endhint %}

### Formataktionen

Innerhalb eines Feldes können nun beliebig viele Aktionen für den Wert des Feldes angewendet werden. Diese werden dabei in der Reihenfolge abgearbeitet, wie sie in der Liste platziert werden.

#### Übersicht aller Aktionen

**`prepend`**  
Fügt einen beliebigen Text vor dem Wert ein.

**`append`**  
Fügt einen beliebigen Text nach dem Wert ein.

**`number_format`**  
Formatiert einen Zahlenwert anhand der angegebenen Nachkommastellen.

**`date_format`**  
Wandelt einen UNIX-Timestamp in ein leserliches Datums-Format um.

**`ucfirst`**  
Verwandelt das erste Zeichen eines Strings in einen Großbuchstaben.

**`wrap`**  
Umschließt den Wert mit dem angegebenen Text/HTML-Code. Die Verwendung eines Platzhalter ist dabei zwingend notwendig. \(s. "[sprintf](https://www.php.net/manual/de/function.sprintf.php#refsect1-function.sprintf-parameters)" PHP-Funktion\)

**`unserialize`**  
Validiert eine in der Datenbank serialisierte Liste und gibt diese anhand des angegebenen Trennzeichens aus.

**`combine`**  
Ermöglicht die Kombination beliebiger Felder und die Ausgabe anhand eines Trennzeichens. Um kombinierte Felder nicht doppelt in einer Detailliste auszugeben, können diese über die Checkbox "entfernen" für die spätere Ausgabe übersprungen werden.

**`boolToWord`**  
Wandelt Werte mit "0" oder "1" in "Nein" oder "Ja" um.

**`custom`**  
Verwendung einer eigenen Funktion. Eigene Funktionen müssen dabei als Template mit dem Prefix "re\_ac\_" angelegt werden.

```php
/**
 * $field:                {string}  Name des Feldes
 * $varValue:             {string}  Wert des Feldes
 * $objRealEstate:        {object}  Immobilien-Objekt 
 * $arrRemovedCollection: {array}   Array mit Feldnamen, welche durch diese Funktion im weiteren Verlauf nicht mehr mit ausgegeben werden dürfen
 */
return array('func' => function($field, $varValue, $objRealEstate, &$arrRemovedCollection)
{
    if($field !== 'meinFeld')
    {
        return $varValue;
    }

    // Your code

    return $varValue;
});
```



