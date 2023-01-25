# Fehlerbehandlung

### Fehlercodes

!> Dieses Feature steht erst ab Version 1.1.0 zur Verfügung.

| Fehlercode  | Beschreibung                                                                                                                                  |
|:------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| `1001`      | Beim Importieren von Immobilien und Kontaktpersonen ist ein Fehler aufgetreten. Weitere Informationen, entnehmen Sie bitte der Fehlermeldung. |

### API - Fehlercodes

| Fehlercode  | Beschreibung                                                                                                                                                        |
|:------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `3001`      | Es kann keine Verbindung hergestellt werden. Überprüfe ob der API-Schlüssel korrekt ist und eine Verbindung zum Server hergestellt werden kann.                     |
| `3002`      | Um die Abfrage durchzuführen werden ein oder mehrere Parameter benötigt. Welche Parameter fehlen, kann der Fehlermeldung entnommen werden.                          |
| `3003`      | Der Übergebene Parameter ist nicht korrekt. Dieser Fehler tritt auf, wenn ein Parameter bspw. als `string` übergeben, jedoch in Form eines `array`´s erwartet wird. |
| `3004`      | Fehler beim erstellen der Rückgabe. Dieser Fehler tritt auf, wenn bspw. ein falscher oder nicht existierender Wert im Parameter `format` übergeben wird.            |

?> Für kritische Fehler, die während der Laufzeit auftreten, können unter `Verwaltung` -> `Einstellungen` Benachrichtigungen aktiviert werden.
