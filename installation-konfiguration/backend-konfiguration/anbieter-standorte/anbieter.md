# Anbieter

Anbieterdatensätze repräsentieren entweder einen **Immobilienmakler** oder die verschiedenen **Standorte eines Immobilienmaklers**. Neben den reinen Eckdaten kann hier außerdem das Verhalten für die Zustellung von Anfragen eingestellt werden. Die vorhandenen Eckdaten entsprechen zum Großteil den Vorgaben zu Anbietern aus dem OpenImmo Standard.

### &#x20;Neuen Anbieter erstellen

Neue Anbieter können über **Neuer Anbieter** ![](../../../.gitbook/assets/new.svg) erstellt werden.

### Allgemein

:small\_blue\_diamond:`Anbieter Nr.`

Die Anbieternummer ist essenziell für die Übertragung von Immobilien und Kontaktpersonen.

:small\_blue\_diamond:`Anbieter Nr. (OpenImmo)`

Die Anbieternummer (OpenImmo) kann als Alternative zur normalen Anbieternummer verwendet werden (Verhalten ist in Schnittstellen einstellbar).

:small\_blue\_diamond:`Linzenzkennung`

Die Lizenzkennung wird vorallem für Portalübertragungen verwendet und ist rein informativer Natur.

### Weiterleitung

:small\_blue\_diamond:`Weiterleitungsmodus`

Hier kann eingestellt werden, wer im Falle einer Kontakanfrage über das Anfrageformulars eines Exposés benachrichtig werden soll:

* Kontaktperson (wenn möglich)\
  _Zustellung erfolgt über das Feld "E-Mail-Adresse Direkt". Wenn dies nicht gesetzt ist, wird die "E-Mail-Adresse" des Anbieters verwendet._
* Anbieter\
  _Zustellung erfolgt über das Feld "E-Mail-Adresse" des Anbieters._
* Beide\
  _Versucht die E-Mail-Anfrage gleichwertig an den Anbieter und die Kontaktperson zu übermitteln._

:small\_blue\_diamond:`Eigenen Absender verwenden`

Über diese Funktion kann ein alternativer Absender definiert werden, um nicht die E-Mail-Adresse des Systemadministrators verwenden zu müssen.

### Adressdaten & Impressum

Die Angaben zu den Adressdaten sowie dem Impressum entsprechen dem OpenImmo Standard und sollten insbesondere in Portalen sorgfältig gepflegt werden. Eckdaten eines Anbieters werden vor allem in Portalen und hier in Immobilienlisten und Exposés angezeigt und spielen für kleinere Websites keine weitere Rolle.

**Adressdaten:**

:small\_blue\_diamond:`Firma`

:small\_blue\_diamond:`Postleitzahl`

:small\_blue\_diamond:`Ort`

:small\_blue\_diamond:`Straße`

:small\_blue\_diamond:`Hausnummer`

:small\_blue\_diamond:`Bundesland`

:small\_blue\_diamond:`Land`

:small\_blue\_diamond:`Breitengrad`

:small\_blue\_diamond:`Längengrad`

:small\_blue\_diamond:`Telefonnummer`

:small\_blue\_diamond:`Telefonnummer 2`

:small\_blue\_diamond:`Faxnummer`

:small\_blue\_diamond:`E-Mail-Adresse`

:small\_blue\_diamond:`Homepage`

:small\_blue\_diamond:`Adresse (Freitext)`

**Weitere Felder:**

:small\_blue\_diamond:`Vertretungsberechtigte Person`

:small\_blue\_diamond:`Beaufsichtigungsbehörde`

:small\_blue\_diamond:`Handelsregister`

:small\_blue\_diamond:`Handeslregisternummer`

:small\_blue\_diamond:`Umsatzsteuer-Identifikationsnummer`

:small\_blue\_diamond:`Steuernummer`

:small\_blue\_diamond:`Weitere Angaben`

:small\_blue\_diamond:`Impressum (Freitext)`

:small\_blue\_diamond:`Beschreibung (Freitext)`

### Anbieter-Logo

Neben den reinen Eckdaten kann auch das Anbieterlogo im Frontend ausgegeben werden. Dieses muss über die Dateiverwaltung zugewiesen werden und kann nicht importiert werden.
