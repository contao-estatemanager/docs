# API

{% api-method method="get" host="https://domain.com" path="/api/estatemanager/v1/estates/:id" %}
{% api-method-summary %}
 Immobilien
{% endapi-method-summary %}

{% api-method-description %}
Abrufen einer oder mehrerer Immobilien.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" %}
ID der abzurufenden Immobilie
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="moduleID" type="integer" required=false %}
Modul-ID \(`required` für das verwenden eines Filters sowie eines Templates mit Immobilien-Objekt\)
{% endapi-method-parameter %}

{% api-method-parameter name="pageId" type="integer" required=false %}
Seiten-ID \(`required` für das verwenden eines Filters\)
{% endapi-method-parameter %}

{% api-method-parameter name="template" type="string" required=false %}
Name des Fronend-Templates \(Bspw. `real_estate_item_default`\).
{% endapi-method-parameter %}

{% api-method-parameter name="dataType" type="string" required=false %}
`json, geojson` Default: `json`
{% endapi-method-parameter %}

{% api-method-parameter name="fields" type="array" required=false %}
Die abzurufenden Immobilien-Felder. 
{% endapi-method-parameter %}

{% api-method-parameter name="groups" type="array" required=false %}
Die abzurufenden Immobilien-Gruppen. \(`required` für das verwenden eines Filters\)
{% endapi-method-parameter %}

{% api-method-parameter name="filter" type="boolean" %}
Die Abfrage findet unter Berücksichtigung eines Filters statt.
{% endapi-method-parameter %}

{% api-method-parameter name="filterMode" type="boolean" %}
Sofern ein Filter verwendet werden soll, kann hier der Filter-Modus definiert werden. \(`required` für das verwenden eines Filters\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
`/api/estatemanager/v1/estates/35`
{% endapi-method-response-example-description %}

```javascript
{
  "results": [
    {
      "id": "35",
      "dateAdded": "1543328488",
      "dateChanged": "1572949938"
    }
  ],
  "status": "OK"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://domain.com" path="/api/estatemanager/v1/contactpersons/:id" %}
{% api-method-summary %}
Kontaktpersonen
{% endapi-method-summary %}

{% api-method-description %}
Abrufen einer oder mehrerer Kontaktpersonen.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=false %}
ID der abzurufenden Kontaktperson
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="imgSize" type="array" required=false %}
Bildgröße des Kontaktpersonen-Fotos.
{% endapi-method-parameter %}

{% api-method-parameter name="fields" type="array" required=false %}
Die abzurufenden Kontaktperson-Felder.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
/api/estatemanager/v1/contactpersons?fields\[\]=vorname&fields\[\]=name
{% endapi-method-response-example-description %}

```javascript
{
  "results": {
    "4": {
      "vorname": "Maria",
      "name": "Musterfrau"
    }
  },
  "status": "OK"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

