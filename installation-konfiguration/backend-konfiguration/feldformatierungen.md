---
description: Formatierung und Ausgabe der Immobilienfelder
---

# Feldformatierungen

Um Immobilienfelder für die Ausgabe aufzubereiten bietet der EstateManager ein umfangreiches Werkzeug um beliebige Aktionen auf Felder und Werte einer Immobilie anzuwenden.

### Formatierung zurücksetzen

Von Haus aus liefert der EstateManager bereits eine Vorkonfiguration von Feldformatierungen und dessen Aktionen, welche im ersten Schritt oder nach Fehlkonfiguration über den Button "Formatierung zurücksetzen" importiert / zurückgesetzt werden können.

{% hint style="warning" %}
Bitte beachte, dass manuelle Änderungen nach dem zurücksetzen verworfen werden
{% endhint %}

### Feldformatierung erstellen

Über den Button "Neues Feld" können alle Immobilien-Felder, welche in der Datenbank bestehen, ausgewählt und für die Darstellung konfiguriert werden.

:small\_blue\_diamond:`Feld`

_Definiert das Feld, welches durch eine Formatierung vor der Ausgabe formatiert werden soll._

:small\_blue\_diamond:`CSS-Klasse`

_Jedes Feld kann ein oder mehrere CSS-Klassen beinhalten (Leerzeichen getrennte Liste). Dies ermöglicht die Erstellung eigener Selektoren um diese später mittels CSS aufbereiten zu können._

:small\_blue\_diamond:`Ausgabe erzwingen`

_Erzwingt die Ausgabe des Feldes, auch wenn kein Wert vorhanden ist._

Beispiel:

> In den Details sollen "Haustiere" immer ausgegeben werden. Wurde dieser Wert nicht übertragen, sollen wir davon ausgehen, dass das Objekt / die Immobilie keine Haustiere erlaubt. Mit der Einstellung, dass die Ausgabe erzwungen werden soll, würde nun "Haustiere: Nein" ebenfalls ausgegeben und nicht als leerer Wert erkannt und somit in den Details übersprungen werden.

:small\_blue\_diamond:`Bedingung hinzufügen`

_Ermöglicht die Definition einer oder mehrerer Bedingungen. Beim hinzufügen mehrerer Bedingungen werden diese "UND"-Verknüpft abgearbeitet._

Beispiel:

> Die Breitband-Geschwindigkeit für die Immobilie soll ausschließlich angezeigt werden, wenn die Immobilie auch einen Breitbandanschluss besitzt.

### Formataktionen

Innerhalb eines Feldes können beliebig viele Aktionen für den Wert des Feldes konfiguriert werden. Diese werden dabei in der Reihenfolge abgearbeitet, wie sie in der Liste definiert werden.

{% hint style="warning" %}
**Logische Reihenfolge der Aktionen verwenden:**\
Preis- oder Flächenangaben müssen bspw. vor dem Anhängen von Einheiten wie `€` oder `m²` (Aktion: `append`) den eigentlichen / noch unformatierten Wert formatiert bekommen (Aktion: `number_format`).

_Falsch:_\
:digit\_one: append\
:digit\_two: number\_format

_Richtig:_\
:digit\_one: number\_format\
:digit\_two: append
{% endhint %}

#### Übersicht aller Aktionen

:small\_orange\_diamond:`prepend`

_Fügt einen beliebigen Text vor dem Wert ein._

:small\_orange\_diamond:`append`

_Fügt einen beliebigen Text nach dem Wert ein._

:small\_orange\_diamond:`number_format`

_Formatiert einen Zahlenwert anhand der angegebenen Nachkommastellen._

:small\_orange\_diamond:`date_format`

_Wandelt einen UNIX-Timestamp in ein leserliches Datums-Format um._

:small\_orange\_diamond:`ucfirst`

_Verwandelt das erste Zeichen eines Strings in einen Großbuchstaben._

:small\_orange\_diamond:`wrap`

_Umschließt den Wert mit dem angegebenen Text/HTML-Code. Die Verwendung eines_ Spezifizierer-_Platzhalters ist dabei zwingend notwendig. (s. "_[_sprintf_](https://www.php.net/manual/de/function.sprintf.php#refsect1-function.sprintf-parameters)_" PHP-Funktion)_

:small\_orange\_diamond:`unserialize`

_Validiert eine in der Datenbank serialisierte Liste und gibt diese anhand des angegebenen Trennzeichens aus._

:small\_orange\_diamond:`combine`

_Ermöglicht die Kombination beliebiger Felder und die Ausgabe anhand eines Trennzeichens. Um kombinierte Felder nicht doppelt in einer Detailliste auszugeben, können diese über die Checkbox "entfernen" für die spätere Ausgabe übersprungen werden._

:small\_orange\_diamond:`boolToWord`

_Wandelt Werte mit "0" oder "1" in "Nein" oder "Ja" um._

:small\_orange\_diamond:`custom`

_Verwendung einer eigenen Funktion. Eigene Funktionen müssen dabei als Template mit dem Präfix "re\_ac\_" angelegt werden._

Beispiel:

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

    // Do something

    return $varValue;
});
```

