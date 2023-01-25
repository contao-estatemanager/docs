# Lizenzsystem verwenden

Um das Lizenzsystem des EstateManagers verwenden zu können, wird die im [`skeleton-extension`](https://github.com/contao-estatemanager/skeleton-extension) mitgelieferte [`AddonManager`](https://github.com/contao-estatemanager/skeleton-extension/blob/master/src/Resources/contao/classes/AddonManager.php)-Klasse benötigt. Diese beinhaltet alle Lizenzen ([verschlüsselt](#verschlüsselung)) und kommuniziert mit der Core-Erweiterung um die Gültigkeit einer Lizenz zu prüfen.

!> Bitte beachte, dass wir eine Testmöglichkeit jeder Erweiterung voraussetzen. Somit können Erweiterungen, welche mit der `AddonManager`-Klasse aufgebaut werden, automatisch 2 Wochen kostenlos getestet werden.

### AddonManager-Klasse anpassen

<span class="field">$bundle</span>

Der Name des Bundles, auf dem die Erweiterung registriert wurde.

<span class="field">$package</span>

Der in der `composer.json` hinterlegte `name` (Bspw. `contao-estatemanager/neue-erweiterung`)

<span class="field">$key</span>

Der Feldname des Input-Feldes (Bspw. `addon_meine_erweiterung_license`).

<span class="field"><array> $liceses</span>

Sammlung verschlüsselter sowie gültiger Lizenzen.

### Verschlüsselung

Die Lizenzen werden `md5`-Verschlüsselt in der `AddonManager`-Klasse hinterlegt.

### Erweiterung registrieren

Damit die Erweiterung vom EstateManager entgegengenommen werden kann, muss diese unter `contao/config/config.php` wie folgt hinzugefügt werden:

```php
// Add extension to EstateManager
$GLOBALS['TL_ESTATEMANAGER_ADDONS'][] = array('MeinNamespace\MeineErweiterung', 'AddonManager');
```

### Lizenz im Code prüfen

Um DCA-Felder und Funktionen erst nach Verwendung einer gültigen Lizenz freizugeben, kann folgende Abfrage über die soeben angepasste `AddonManager`-Klasse durchgeführt werden:

```php
if(MeinNamespace\MeineErweiterung\AddonManager::valid()) {
    // Add front end modules...
}
```

Als Beispiel können bereits [verfügbare Erweiterungen](https://github.com/contao-estatemanager) herangezogen werden.

### Logo für die Lizenzverwaltung bereitstellen

Um in der Lizenzverwaltung ein eigenes Logo für die Erweiterung bereitzustellen, muss im `public`Ordner der Erweiterung das Logo als `logo.svg` abgelegt werden.
