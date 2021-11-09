# Fehlerbehandlung

### Fehlercodes

Für kritische Fehler, die während der Laufzeit auftreten, können unter `Verwaltung` -> `Einstellungen` Benachrichtigungen aktiviert werden.



{% hint style="warning" %}
Dieses Feature steht erst ab Version 1.1.0 zur Verfügung.
{% endhint %}

| Fehlercode                             | Beschreibung                                                                                                                                  |
| -------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| <mark style="color:red;">`1001`</mark> | Beim Importieren von Immobilien und Kontaktpersonen ist ein Fehler aufgetreten. Weitere Informationen, entnehmen Sie bitte der Fehlermeldung. |

### API - Fehlercodes

| Fehlercode                             | Beschreibung                                                                                                                                                        |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <mark style="color:red;">`3001`</mark> | Es kann keine Verbindung hergestellt werden. Überprüfe ob der API-Schlüssel korrekt ist und eine Verbindung zum Server hergestellt werden kann.                     |
| <mark style="color:red;">`3002`</mark> | Um die Abfrage durchzuführen werden ein oder mehrere Parameter benötigt. Welche Parameter fehlen, kann der Fehlermeldung entnommen werden.                          |
| <mark style="color:red;">`3003`</mark> | Der Übergebene Parameter ist nicht korrekt. Dieser Fehler tritt auf, wenn ein Parameter bspw. als `string` übergeben, jedoch in Form eines `array`´s erwartet wird. |
| <mark style="color:red;">`3004`</mark> | Fehler beim erstellen der Rückgabe. Dieser Fehler tritt auf, wenn bspw. ein falscher oder nicht existierender Wert im Parameter `format` übergeben wird.            |
