# Objekttypen

Objekttypen stellen den Dreh- und Angelpunkt dar, wenn es sich um das exakte **Verhalten und die Darstellung von Immobilien im Frontend** geht. Sie sorgen dafür, dass sich sämtliche Immobiliendatensätze im Frontend fachlich korrekt **filtern**, **sortieren** und **durchsuchen** lassen und sorgen für die korrekte Darstellung von Informationen jeder einzelnen Immobilie. Ein Immobiliendatensatz wird dabei durch die Kombination aus **Nutzungsart**, **Vermarktungsart** und **Objektart** eindeutig identifiziert.

{% hint style="info" %}
Das Verhalten kann durch Objekttypen detailliert eingestellt werden, sodass man beispielsweise bei Grundstücken nicht nach der Anzahl von Zimmern filtern kann oder bei Wohnungen nicht nach der Grundstücksfläche sortieren kann.
{% endhint %}

### Konfiguration

Objekttypen werden anhand der **Nutzungsart**, **Vermarktungsart** und **Objektart** einer Immobilie eindeutig identifiziert, wodurch wichtige Felder wie das primäre Flächen- und Preisfeld und andere Merkmale ermittelt werden können. Des Weiteren lassen sich **primäre Details**, **Sortierfelder**, **Filtermöglichkeiten** und weiteres einstellen und konfigurieren, wodurch Objekttypen exakt an individuelle Gegebenheiten angepasst werden können.

:small\_blue\_diamond:`Bezeichnung`

Dient als Bezeichner für den Objekttyp-Filter im Frontend.&#x20;

:small\_blue\_diamond:`Detaillierte Bezeichnung`

Die detaillierte Bezeichnung kann im Frontend anstelle der einfachen Bezeichnung ausgegeben werden.

{% hint style="info" %}
Muss verwendet werden, wenn im Objekttyp-Filter sowohl Kauf- als auch Miet-Objekte zur Verfügung stehen.&#x20;
{% endhint %}

:small\_blue\_diamond:`Äquivalenter Objekttyp`

Der Äquivalente Objekttyp wird angesteuert, wenn die Vermarktungsart des Vermarktungsart-Filter geändert wird.

{% hint style="info" %}
Wird verwendet, um beim Wechsel der Vermarktungs im Filter automatisch von z.B. _Eigentumswohnungen_ zu _Wohnungen zur Miete_ zu wechseln.&#x20;
{% endhint %}

### Weiterleitung

:small\_blue\_diamond:`Referenzseite`

Unterseite für einen oder mehrere spezielle Objekttypen. Wird hauptsächlich verwendet, wenn Objekttypen direkt über die Navigation erreichbar gemacht werden sollen. Des Weiteren wird man bei Auswahl des Objekttypen im Objekttyp-Filter automatisch zur zugewiesenen Referenzseite weitergeleitet.

:small\_blue\_diamond:`Spezielle Exposé-Seite`

Führt zu einer speziellen Exposé-Seite des Objekttypen, um im Frontend eine individuelle Darstellung zu ermöglichen.

### Feld-Konfiguration

Damit eine Immobilie im Frontend ausgegeben werden kann, muss diese eindeutig anhand der folgenden Felder identifiziert werden können.

:small\_blue\_diamond:`Nutzungsart`

Anhand der Nutzungsart kann eine Immobilie eindeutig einem Objekttypen zugeordnet werden.

:small\_blue\_diamond:`Vermarktungsart`

Anhand der Vermarktungsart kann eine Immobilie eindeutig einem Objekttypen zugeordnet werden.

:small\_blue\_diamond:`Objektart`

Anhand der Objektart kann eine Immobilie eindeutig einem Objekttypen zugeordnet werden.

{% hint style="danger" %}
Kann ein Immobiliendatensatz gleichzeitig mehreren Objekttypen zugeordnet werden, wird der zuerst gefundene Objekttyp verwendet, wodurch es zu Fehlern in der Darstellung und dem Verhalten kommen kann.
{% endhint %}

### Filter-Einstellungen

Hier werden die wichtigsten Eckdaten zur Filterung einer Immobilie definiert. Dient auch der korrekten Darstellung von Information in Immobilienlisten und dem Exopsé.

:small\_blue\_diamond:`Primäres Preisfeld`

Dient der zuverlässigen Anzeige des Preises eines speziellen Objekttypen.

{% hint style="warning" %}
Es wird automatisch **"auf Anfrage"** anstelle des Preises ausgegeben, sollte das primäre Preisfeld nicht befüllt sein.
{% endhint %}

:small\_blue\_diamond:`Primäres Flächenfeld`

Dient der zuverlässigen Anzeige der primären Fläche eines speziellen Objekttypen. Bei Grundstücken ist z.B. vor allem die Grundstücksfläche interessant, wohingegen bei Wohnobjekten die Wohnfläche angezeigt werden sollte.

:small\_blue\_diamond:`Primäre Filter`

Hier kann angegeben werden, über welche Filter ein Objekttyp im Frontend gefiltert werden kann. Bei Grundstücken sollte z.B. keine Möglichkeit bestehen nach Zimmern zu filtern.

:small\_blue\_diamond:`Sortieroptionen`

Hier kann angegeben werden, anhand welcher Felder ein Objekttyp über die Immobilien-Ergebnisliste sortiert werden kann. Bei Wohnungen ist es sinnvoll eine Sortiermöglichkeit anhand der Wohnfläche anzubieten, wohingegen Grundstücken nach der Grundstücksfläche sortierbar sein sollten. Weiterführend sollten Häuser beide Möglichkeiten anbieten.

### Darstellungseinstellungen

:small\_blue\_diamond:`Primäre Details`

Primäre Details werden in Immobilienlisten, sowie über das Exposé-Modul _Primäre Details_ angezeigt, um im Frontend stets für den Objekttyp relevante Informationen anzuzeigen.

:small\_blue\_diamond:`Primäre Attribute`

Primäre Attribute werden vor allem über das Exposé-Modul _Primäre Attribute_ ausgegeben, können optional aber bereits in Immobilienlisten angezeigt werden.

:small\_blue\_diamond:`Details sortieren`

Details einer Immobilie können über das Exposé-Modul _Details_ in einer für den Objekttyp speziellen Reihenfolge ausgegeben werden.

:small\_blue\_diamond:`Feldsortierung`

Hier kann die Reihenfolge der Felder definiert werden, wenn Details sortieren aktiviert ist.

### Veröffentlichen

Unveröffentlichte Objekttypen werden nicht berücksichtigt und damit im Frontend nicht ausgegeben.&#x20;

{% hint style="danger" %}
Immobilien können nur angezeigt werden, wenn diese einem veröffentlichten Objekttypen zugeordnet werden können.
{% endhint %}
