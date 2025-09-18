# Import

## Einleitung

Der bisher im Core enthaltene **Immobilien-Importer** wurde entfernt und ist nun als **Add-on im Abonnement** verfügbar.
Der Import basiert auf der Anzahl der bereits im System befindlichen Immobilien.

Das Abo-Modell ist entscheidend, um die Weiterentwicklung des EstateManagers zu fördern und die Nachhaltigkeit des Projekts zu gewährleisten.

---

## Einrichtung

1. Schließen Sie ein Abo auf [contao-estatemanager.com](https://www.contao-estatemanager.com/de/store/openimmo-import.html) ab.
2. Der Download der Add-on-Erweiterung wird innerhalb von **2 Werktagen** im internen Bereich als Download freigeschaltet.
3. Installation der Add-on-Erweiterung über den Contao-Manager via Drag-and-Drop
4. Nach der Installation kann im Contao-Backend unter **Estatemanager → Verwaltung → Add-Ons → Lizenzen verwalten**, die erworbene Lizenz unter *Addon Import Lizenz* eingetragen werden.
5. Anschließend muss der **Anwendungs-Cache** (z. B. über den Contao-Manager) geleert werden.

---

## Upgrade

- Für ein Upgrade eines Abonnements muss das vorherige Abo über **Paddle** gekündigt werden.
- Nach Abschluss des neuen Abonnements für ein größeres Paket wird ein neuer Lizenzschlüssel generiert.
- Folgen Sie hierbei erneut den Schritten unter *Einrichtung*.

---

## Fehlermeldungen

### „Verbindung fehlgeschlagen! Bitte in der Dokumentation nachschlagen.“

Mögliche Ursachen:
- Die beim Abschluss des Abonnements eingetragene Domain stimmt nicht überein.
- Der Lizenzschlüssel ist nicht valide oder wurde falsch eingetragen.
- Eine Verbindung zwischen dem Shop und der Webseite konnte nicht hergestellt werden
  - Seite gesperrt
  - Wartungsmodus eingeschaltet
  - falsch konfigurierte Weiterleitungen, beispielsweise fehlerhaft auf `www.`. [htaccess Validator](https://htaccess.madewithlove.com/)
  - etc.

Um eine erneute Verbindung nach Behebung des Fehelrs zu testen, muss der **Anwendungscache** erneut geleert werden.

---

### „Limit erreicht“

Mögliche Ursachen:
- Das bestellte Abonnement ist zu klein für die Anzahl der Immobilien.

Beispiele:
- 17 veröffentlichte Immobilien – Abonnement von 10 Immobilien
  - **Importer wird deaktiviert**, es müssen Immobilien gelöscht werden.
- 9 veröffentlichte Immobilien – Abonnement von 10 Immobilien, 2 Immobilien in einer Übertragung
  - **Teilimport**, nur eine Immobilie wird importiert.

---

## Weitere Hinweise

- Falscheingaben von Lizenzschlüsseln und manuelles Synchronisieren führen zur Deaktivierung des Imports.
  → Der Import muss über **Estatemanager → Verwaltung → Einstellungen → Import deaktivieren** wieder freigeschaltet werden.
- Missbrauchsversuche von Importen mit falschen oder keinem Lizenzschlüssel werden protokolliert.
- Sofern ein Abonnement gekündigt wird und abläuft, wird der Importer nach einiger Zeit **automatisch deaktiviert**.
