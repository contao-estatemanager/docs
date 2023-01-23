# API

## Immobilien

<!-- panels:start -->
<!-- div:left-panel -->

Ermöglicht das Abrufen einer oder mehrerer Immobilien-Datensätze aus dem System. Hierbei werden nur die Immoblien berücksichtigt, welche dem EstateManager zur Verfügung stehen.

|                                   | Typ       | Standard                         | Beschreibung                                                                                                                       |
|----------------------------------:|:----------|:---------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
|            **id** <br> *optional* | *integer* |                                  | ID der abzurufenden Immobilie                                                                                                      |
|   **moduleId** <br/> *required\** | *integer* |                                  | Modul-ID (`required` für das verwenden eines Filters sowie eines Templates mit Immobilien-Objekt)                                  |
|     **pageId** <br/> *required\** | *integer* |                                  | Seiten-ID (`required` für das verwenden eines Filters)                                                                             |
|     **template** <br/> *optional* | *string*  | `real_estate_item_default`       | Name des Fronend-Templates.                                                                                                        |
|     **dataType** <br/> *optional* | *string*  | `json`                           | `json`, `geojson`                                                                                                                  |
|       **fields** <br/> *optional* | *array*   | `id`, `dateAdded`, `dateChanged` | Die abzurufenden Immobilien-Felder.                                                                                                |
|     **groups** <br/> *required\** | *array*   |                                  | Die abzurufenden Immobilien-Gruppen. (required für das verwenden eines Filters)                                                    |
|       **filter** <br/> *optional* | *boolean* | `false`                          | Die Abfrage findet unter Berücksichtigung eines Filters statt.                                                                     |
| **filterMode** <br/> *required\** | *integer* |                                  | Sofern ein Filter verwendet werden soll, muss hier der Filter-Modus angegeben werden. (`required` für das verwenden eines Filters) |


<!-- div:right-panel -->

<div class="api-route"><span class="method get">GET</span> <span class="read-only">domain.com</span>/api/estatemanager/v1/estates<span class="read-only">/:id</span></div>
<!-- tabs:start -->

#### **200**
```json
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

#### **401**
Autorisierung erforderlich

<!-- tabs:end -->
<!-- panels:end -->

## Kontaktpersonen

<!-- panels:start -->
<!-- div:left-panel -->

Ermöglicht das Abrufen einer oder mehrerer Kontakt-Datensätze aus dem System. Hierbei werden nur die Kontakte berücksichtigt, welche dem EstateManager zur Verfügung stehen.

|                                   | Typ       | Standard                   | Beschreibung                                                                                                                       |
|----------------------------------:|:----------|:---------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
|            **id** <br> *optional* | *integer* |                            | ID der abzurufenden Kontaktperson                                                                                                  |
|     **imgSize** <br/> *optional*  | *array*   |                            | Bildgröße des Kontaktpersonen-Fotos                                                                                                |
|       **fields** <br/> *optional* | *array*   | `vorname`, `name`          | Die abzurufenden Immobilien-Felder.                                                                                                |


<!-- div:right-panel -->

<div class="api-route"><span class="method get">GET</span> <span class="read-only">domain.com</span>/api/estatemanager/v1/contactpersons<span class="read-only">/:id</span></div>
<!-- tabs:start -->

#### **200**
```json
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

#### **401**
Autorisierung erforderlich

<!-- tabs:end -->
<!-- panels:end -->
