---
description: Erweiterung erstellen
---

# Lizenzsystem verwenden

Um das Lizenzsystem des EstateManagers verwenden zu können, benötigen Sie die im [`skeleton-extension`](https://github.com/contao-estatemanager/skeleton-extension) mitgelieferte [`AddonManager`](https://github.com/contao-estatemanager/skeleton-extension/blob/master/src/Resources/contao/classes/AddonManager.php)-Klasse. Diese beinhaltet alle Lizenzen \(verschlüsselt\) und kommuniziert mit der Core-Erweiterung um die Gültigkeit einer Lizenz zu prüfen.

{% hint style="info" %}
Bitte beachte, dass wir eine Testmöglichkeit jeder Erweiterung voraussetzen. Somit können Erweiterungen, welche mit der `AddonManager`-Klasse aufgebaut werden, automatisch 2 Wochen kostenlos getestet werden.
{% endhint %}

### `AddonManager`-Klasse anpassen

🔹`$name`

_Der Name der Erweiterung, welcher auch als Bezeichner in der Lizenz-Übersicht dient._

🔹`$key`

_Der Feldname des Input-Feldes \(Bspw._ `addon_meine_erweiterung_license`\)_._

🔹`<array> $liceses`

_Die Sammlung verschlüsselter und gültiger Lizenzen._

### Verschlüsselung

Die Lizenzen werden `md5`-Verschlüsselt in der `AddonManager`-Klasse hinterlegt.

