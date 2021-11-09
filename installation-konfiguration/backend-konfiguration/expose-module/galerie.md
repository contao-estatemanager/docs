---
description: Exposé-Modul
---

# Galerie

Das `Galerie` Exposé-Modul liefert die Bilder einer Immobilie unter Berücksichtigung der gewählten Galerie-Kategorien aus. Dabei stehen folgende Kategorien im Standard zur Verfügung:

* Titelbild
* Bilder
* Grundrisse
* Interior-Bilder
* Exterior-Bilder
* Kartenansicht
* Panorama
* Energieskala
* Logo
* QR-Code

### Einstellungen

:small\_blue\_diamond:`Galerie-Kategorien`

_Hier können die Kategorien, welche ausgegeben werden dürfen, sowie die Reihenfolge definiert werden._

:small\_blue\_diamond:`Gesamtzahl der Elemente`

_Definiert die maximale Anzahl an Elementen / Bildern._

:small\_blue\_diamond:`Großansicht/Neues Fenster`

_Großansicht des Bildes in einer "Lightbox" bzw. den Link in einem neuem Browserfenster öffnen. Die Initialisierung einer "Lightbox" muss dabei eigenständig eingerichtet werden._

:small\_blue\_diamond:`Ausblenden wenn keine Inhalte angezeigt werden können`

Verhindert die Ausgabe des Exposé-Moduls, sofern keine Elemente / Bilder in den gewählten Kategorien gefunden wurden. Andernfalls wird immer das in den [Einstellungen](../einstellungen.md) hinterlegte Standard-Bild ausgegeben.

### Templates

:small\_orange\_diamond:`expose_mod_gallery`

:small\_orange\_diamond:`expose_mod_gallery_items`

{% hint style="success" %}
Auf diesem Exposé-Modul können beliebige JavaScript-Slider initialisiert werden um die Bilder, wie man es von vielen anderen Webseiten kennt, als Bilder-Diashow o.ä. darstellen zu lassen.
{% endhint %}
