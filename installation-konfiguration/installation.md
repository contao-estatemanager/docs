---
description: Open Source EstateManager for Contao CMS
---

# Installation

### Installation

{% tabs %}
{% tab title="Composer" %}
```bash
$ composer require contao-estatemanager/core
```
{% endtab %}

{% tab title="Contao-Manager" %}
Über die Suche des Contao-Manager kann der Begriff `EstateManager` gesucht werden. Anschließend wählt man das Paket `Contao EstateManager Core` aus und installiert es. Eine detaillierte Anleitung wie man mit dem Contao-Manager arbeitet findest du [hier](https://docs.contao.org/manual/de/installation/erweiterungen-installieren/).
{% endtab %}

{% tab title="GitHub" %}
Installation direkt über GitHub:

[https://github.com/contao-estatemanager/core](https://github.com/contao-estatemanager/core)
{% endtab %}
{% endtabs %}

Nach der Installation muss das [Contao-Installtool](https://docs.contao.org/manual/de/installation/contao-installtool/) aufgerufen und die Datenbank aktualisiert werden.

### Systemvoraussetzungen

* [PHP](https://www.php.net/ChangeLog-7.php#PHP_7_1) `>=7.2`
* [MySQL](https://www.mysql.com/de/) `>5.7` oder gleichwertiger [MariaDB](https://mariadb.org/) Server
* [Contao](https://github.com/contao/contao) `^4.4`
* [MultiColumnWizard](https://github.com/menatwork/contao-multicolumnwizard-bundle) `^3.3`

Sofern der EstateManager über Composer oder dem Contao Manager installiert wird, werden alle benötigten Abhängigkeiten mit installiert.

{% hint style="info" %}
Bitte überprüfe ebenfalls die [Systemvoraussetzungen](https://docs.contao.org/manual/de/installation/systemvoraussetzungen/) von Contao
{% endhint %}

