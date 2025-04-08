# onOffice API Import

{% hint style="alert" %}
Für diese Erweiterung wird es aufgrund geringer Nachfrage keine Nachfolger geben. Sollten Sie dennoch eine Kompatibilität mit Contao 5 wünschen, können Sie uns gerne [mit der Umsetzung beauftragen](https://www.oveleon.de/kontakt.html#kontaktformular):
{% endhint %}

Die `onOffice API Import` Erweiterung ermöglicht den Import verschiedener Datensätze aus onOffice heraus.

{% hint style="warning" %}
Es wird ein kostenpflichtiger onOffice API Benutzer benötigt.
{% endhint %}

### Übersicht

| Import                  | benötigte Erweiterung                                                                                       |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| Regionen (onOffice)     | ``[`contao-estatemanager/region-entity`](https://github.com/contao-estatemanager/region-entity)``           |
| Objekttypen (onOffice)  | ``[`contao-estatemanager/object-type-entity`](https://github.com/contao-estatemanager/object-type-entity)`` |
| Suchaufträge (onOffice) | ``[`contao-estatemanager/lead-matching-tool`](https://github.com/contao-estatemanager/lead-matching-tool)`` |

| Synchronisation / Cronjob                       | benötigte Erweiterung                                                                                       |
| ----------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| Suchaufträge importieren (onOffice)             | ``[`contao-estatemanager/lead-matching-tool`](https://github.com/contao-estatemanager/lead-matching-tool)`` |
| Suchaufträge aktualisieren / löschen (onOffice) | [`contao-estatemanager/lead-matching-tool`](https://github.com/contao-estatemanager/lead-matching-tool)``   |
