# Templates anpassen

Wie in Contao selber können auch alle Templates des EstateManagers über den Reiter "Templates" im Backend angepasst, überschrieben oder ergänzt werden. Dabei gibt es die Besonderheit, dass dem Template das Objekt der Immobilie \([RealEstateModulePreparation](php-klassen/realestatemodulepreparation.md)\) mit nützlichen Funktionen und aller Immobilien-Eigenschaften übergeben wird. Dadurch können jegliche Informationen direkt über das Template abgerufen werden. 

{% hint style="warning" %}
Das [RealEstateModulePreparation](php-klassen/realestatemodulepreparation.md) Objekt steht erst ab **Version 1.0** zur Verfügung.
{% endhint %}

{% hint style="info" %}
Bitte beachte, dass Werte, welche über das [RealEstateModulePreparation](php-klassen/realestatemodulepreparation.md)-Objekt abgeholt werden, meist als [FormattedCollection](php-klassen/realestate/formattedcollection.md) zurückgeliefert werden.
{% endhint %}

### Eigenschaften über das Template abrufen

Über `$this->realEstate` kann auf Funktionen und Eigenschaften zugegriffen werden.

```markup
<h1><?= $this->realEstate->title ?></h1>

<a href="<?= $this->realEstate->generateExposeUrl() ?>">Details</a>
```



