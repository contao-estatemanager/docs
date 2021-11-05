# API

{% swagger baseUrl="https://domain.com" path="/api/estatemanager/v1/estates/:id" method="get" summary=" Immobilien" %}
{% swagger-description %}
Abrufen einer oder mehrerer Immobilien.
{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="integer" %}
ID der abzurufenden Immobilie
{% endswagger-parameter %}

{% swagger-parameter in="query" name="moduleID" type="integer" %}
Modul-ID (

`required`

 für das verwenden eines Filters sowie eines Templates mit Immobilien-Objekt)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="pageId" type="integer" %}
Seiten-ID (

`required`

 für das verwenden eines Filters)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="template" type="string" %}
Name des Fronend-Templates (Bspw. 

`real_estate_item_default`

).
{% endswagger-parameter %}

{% swagger-parameter in="query" name="dataType" type="string" %}
`json, geojson`

 Default: 

`json`
{% endswagger-parameter %}

{% swagger-parameter in="query" name="fields" type="array" %}
Die abzurufenden Immobilien-Felder. 
{% endswagger-parameter %}

{% swagger-parameter in="query" name="groups" type="array" %}
Die abzurufenden Immobilien-Gruppen. (

`required`

 für das verwenden eines Filters)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="filter" type="boolean" %}
Die Abfrage findet unter Berücksichtigung eines Filters statt.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="filterMode" type="boolean" %}
Sofern ein Filter verwendet werden soll, kann hier der Filter-Modus definiert werden. (

`required`

 für das verwenden eines Filters)
{% endswagger-parameter %}

{% swagger-response status="200" description="/api/estatemanager/v1/estates/35" %}
```javascript
{
  "status": "OK",
  "meta": [
    "total": 1,
    "query": []
  ],
  "results": [
    {
      "id": "35",
      "dateAdded": "1543328488",
      "dateChanged": "1572949938"
    }
  ]
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://domain.com" path="/api/estatemanager/v1/contactpersons/:id" method="get" summary="Kontaktpersonen" %}
{% swagger-description %}
Abrufen einer oder mehrerer Kontaktpersonen.
{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="string" %}
ID der abzurufenden Kontaktperson
{% endswagger-parameter %}

{% swagger-parameter in="query" name="imgSize" type="array" %}
Bildgröße des Kontaktpersonen-Fotos.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="fields" type="array" %}
Die abzurufenden Kontaktperson-Felder.
{% endswagger-parameter %}

{% swagger-response status="200" description="/api/estatemanager/v1/contactpersons?fields[]=vorname&fields[]=name" %}
```javascript
{
  "status": "OK",
  "meta": [
    "total": 1,
    "query": [
      "fields": [
        "vorname",
        "name"
      ]
    ]
  ],
  "results": [
    {
      "vorname": "Maria",
      "name": "Musterfrau"
    }
  ]
}
```
{% endswagger-response %}
{% endswagger %}
