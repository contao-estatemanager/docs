# Objekttypen

Objekttypen stellen den Dreh- und Angelpunkt dar, wenn es sich um das exakte **Verhalten und die Darstellung von Immobilien im Frontend** geht. Sie sorgen dafür, dass sich sämtliche Immobiliendatensätze im Frontend fachlich korrekt **filtern**, **sortieren** und **durchsuchen** lassen und sorgen für die korrekte Darstellung von Informationen jeder einzelnen Immobilie. Ein Immobiliendatensatz wird dabei durch die Kombination aus **Nutzungsart**, **Vermarktungsart** und **Objektart** eindeutig identifiziert.

?> Das Verhalten kann durch Objekttypen detailliert eingestellt werden, sodass man beispielsweise bei Grundstücken nicht nach der Anzahl von Zimmern filtern kann oder bei Wohnungen nicht nach der Grundstücksfläche sortieren kann.

### Konfiguration

Objekttypen werden anhand der **Nutzungsart**, **Vermarktungsart** und **Objektart** einer Immobilie eindeutig identifiziert, wodurch wichtige Felder wie das primäre Flächen- und Preisfeld und andere Merkmale ermittelt werden können. Des Weiteren lassen sich **primäre Details**, **Sortierfelder**, **Filtermöglichkeiten** und weiteres einstellen und konfigurieren, wodurch Objekttypen exakt an individuelle Gegebenheiten angepasst werden können.

<span class="field">Bezeichnung</span>

Dient als Bezeichner für den Objekttyp-Filter im Frontend.&#x20;

<span class="field">Detaillierte Bezeichnung</span>

Die detaillierte Bezeichnung kann im Frontend anstelle der einfachen Bezeichnung ausgegeben werden.

?> Muss verwendet werden, wenn im Objekttyp-Filter sowohl Kauf- als auch Miet-Objekte zur Verfügung stehen.&#x20;

<span class="field">Äquivalenter Objekttyp</span>

Der Äquivalente Objekttyp wird angesteuert, wenn die Vermarktungsart des Vermarktungsart-Filter geändert wird.

?> Wird verwendet, um beim Wechsel der Vermarktungs im Filter automatisch von z.B. _Eigentumswohnungen_ zu _Wohnungen zur Miete_ zu wechseln.&#x20;

### Weiterleitung

<span class="field">Referenzseite</span>

Unterseite für einen oder mehrere spezielle Objekttypen. Wird hauptsächlich verwendet, wenn Objekttypen direkt über die Navigation erreichbar gemacht werden sollen. Des Weiteren wird man bei Auswahl des Objekttypen im Objekttyp-Filter automatisch zur zugewiesenen Referenzseite weitergeleitet.

<span class="field">Spezielle Exposé-Seite</span>

Führt zu einer speziellen Exposé-Seite des Objekttypen, um im Frontend eine individuelle Darstellung zu ermöglichen.

### Feld-Konfiguration

Damit eine Immobilie im Frontend ausgegeben werden kann, muss diese eindeutig anhand der folgenden Felder identifiziert werden können.

<span class="field">Nutzungsart</span>

Anhand der Nutzungsart kann eine Immobilie eindeutig einem Objekttypen zugeordnet werden.

<span class="field">Vermarktungsart</span>

Anhand der Vermarktungsart kann eine Immobilie eindeutig einem Objekttypen zugeordnet werden.

<span class="field">Objektart</span>

Anhand der Objektart kann eine Immobilie eindeutig einem Objekttypen zugeordnet werden.

!> Kann ein Immobiliendatensatz gleichzeitig mehreren Objekttypen zugeordnet werden, wird der zuerst gefundene Objekttyp verwendet, wodurch es zu Fehlern in der Darstellung und dem Verhalten kommen kann.

### Filter-Einstellungen

Hier werden die wichtigsten Eckdaten zur Filterung einer Immobilie definiert. Dient auch der korrekten Darstellung von Information in Immobilienlisten und dem Exopsé.

<span class="field">Primäres Preisfeld</span>

Dient der zuverlässigen Anzeige des Preises eines speziellen Objekttypen.

!> Es wird automatisch **"auf Anfrage"** anstelle des Preises ausgegeben, sollte das primäre Preisfeld nicht befüllt sein.

<span class="field">Primäres Flächenfeld</span>

Dient der zuverlässigen Anzeige der primären Fläche eines speziellen Objekttypen. Bei Grundstücken ist z.B. vor allem die Grundstücksfläche interessant, wohingegen bei Wohnobjekten die Wohnfläche angezeigt werden sollte.

<span class="field">Primäre Filter</span>

Hier kann angegeben werden, über welche Filter ein Objekttyp im Frontend gefiltert werden kann. Bei Grundstücken sollte z.B. keine Möglichkeit bestehen nach Zimmern zu filtern.

<span class="field">Sortieroptionen</span>

Hier kann angegeben werden, anhand welcher Felder ein Objekttyp über die Immobilien-Ergebnisliste sortiert werden kann. Bei Wohnungen ist es sinnvoll eine Sortiermöglichkeit anhand der Wohnfläche anzubieten, wohingegen Grundstücken nach der Grundstücksfläche sortierbar sein sollten. Weiterführend sollten Häuser beide Möglichkeiten anbieten.

### Darstellungseinstellungen

<span class="field">Primäre Details</span>

Primäre Details werden in Immobilienlisten, sowie über das Exposé-Modul _Primäre Details_ angezeigt, um im Frontend stets für den Objekttyp relevante Informationen anzuzeigen.

<span class="field">Primäre Attribute</span>

Primäre Attribute werden vor allem über das Exposé-Modul _Primäre Attribute_ ausgegeben, können optional aber bereits in Immobilienlisten angezeigt werden.

<span class="field">Details sortieren</span>

Details einer Immobilie können über das Exposé-Modul _Details_ in einer für den Objekttyp speziellen Reihenfolge ausgegeben werden.

<span class="field">Feldsortierung</span>

Hier kann die Reihenfolge der Felder definiert werden, wenn Details sortieren aktiviert ist.

### Veröffentlichen

Unveröffentlichte Objekttypen werden nicht berücksichtigt und damit im Frontend nicht ausgegeben.&#x20;

!> Immobilien können nur angezeigt werden, wenn diese einem veröffentlichten Objekttypen zugeordnet werden können.
