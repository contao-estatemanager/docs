# Anbieter

Anbieterdatensätze repräsentieren entweder einen **Immobilienmakler** oder die verschiedenen **Standorte eines Immobilienmaklers**. Neben den reinen Eckdaten kann hier außerdem das Verhalten für die Zustellung von Anfragen eingestellt werden. Die vorhandenen Eckdaten entsprechen zum Großteil den Vorgaben zu Anbietern aus dem OpenImmo Standard.

### Neuen Anbieter erstellen

Neue Anbieter können über **Neuer Anbieter** ![](../../../.gitbook/assets/new.svg) erstellt werden.

### Allgemein

<span class="field">Anbieter Nr.</span>

Die Anbieternummer ist essenziell für die Übertragung von Immobilien und Kontaktpersonen.

<span class="field">Anbieter Nr. (OpenImmo)</span>

Die Anbieternummer (OpenImmo) kann als Alternative zur normalen Anbieternummer verwendet werden (Verhalten ist in Schnittstellen einstellbar).

<span class="field">Linzenzkennung</span>

Die Lizenzkennung wird vorallem für Portalübertragungen verwendet und ist rein informativer Natur.

### Weiterleitung

<span class="field">Weiterleitungsmodus</span>

Hier kann eingestellt werden, wer im Falle einer Kontakanfrage über das Anfrageformulars eines Exposés benachrichtig werden soll:

* Kontaktperson (wenn möglich)\
  _Zustellung erfolgt über das Feld "E-Mail-Adresse Direkt". Wenn dies nicht gesetzt ist, wird die "E-Mail-Adresse" des Anbieters verwendet._
* Anbieter\
  _Zustellung erfolgt über das Feld "E-Mail-Adresse" des Anbieters._
* Beide\
  _Versucht die E-Mail-Anfrage gleichwertig an den Anbieter und die Kontaktperson zu übermitteln._

<span class="field">Eigenen Absender verwenden</span>

Über diese Funktion kann ein alternativer Absender definiert werden, um nicht die E-Mail-Adresse des Systemadministrators verwenden zu müssen.

### Adressdaten & Impressum

Die Angaben zu den Adressdaten sowie dem Impressum entsprechen dem OpenImmo Standard und sollten insbesondere in Portalen sorgfältig gepflegt werden. Eckdaten eines Anbieters werden vor allem in Portalen und hier in Immobilienlisten und Exposés angezeigt und spielen für kleinere Websites keine weitere Rolle.

**Adressdaten:**

<span class="field">Firma</span>

<span class="field">Postleitzahl</span>

<span class="field">Ort</span>

<span class="field">Straße</span>

<span class="field">Hausnummer</span>

<span class="field">Bundesland</span>

<span class="field">Land</span>

<span class="field">Breitengrad</span>

<span class="field">Längengrad</span>

<span class="field">Telefonnummer</span>

<span class="field">Telefonnummer 2</span>

<span class="field">Faxnummer</span>

<span class="field">E-Mail-Adresse</span>

<span class="field">Homepage</span>

<span class="field">Adresse (Freitext)</span>

**Weitere Felder:**

<span class="field">Vertretungsberechtigte Person</span>

<span class="field">Beaufsichtigungsbehörde</span>

<span class="field">Handelsregister</span>

<span class="field">Handeslregisternummer</span>

<span class="field">Umsatzsteuer-Identifikationsnummer</span>

<span class="field">Steuernummer</span>

<span class="field">Weitere Angaben</span>

<span class="field">Impressum (Freitext)</span>

<span class="field">Beschreibung (Freitext)</span>

### Anbieter-Logo

Neben den reinen Eckdaten kann auch das Anbieterlogo im Frontend ausgegeben werden. Dieses muss über die Dateiverwaltung zugewiesen werden und kann nicht importiert werden.
