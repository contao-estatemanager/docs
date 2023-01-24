# Immobilien-Objekt

Das Immobilien-Objekt beschreibt eine Funktionssammlung, welche für die meisten Templates des EstateManagers bereitgestellt wird und aus diesen heraus verwendet werden kann.\
Dabei können bspw. alle Eigenschaften einer Immobilie ausgelesen, validiert und für die Ausgabe aufbereitet werden.

!> Das Immobilien-Objekt steht erst ab **Version 1.0** in Templates zur Verfügung.

?> In der [Templateübersicht](/de-DE/developer/templates/?id=template-Übersicht) kannst du sehen, ob und in welchen Templates das Immobilien-Objekt zur Verfügung gestellt wird.

### Funktionsumfang

##### `get`
```php 
// Abrufen einer Immobilien-Eigenschaft
get(string $name): string
```

##### `getType`
```php 
// Liefert den Immobilien-Typen zurück
getType(): RealEstateTypeModel
```

##### `generateExposeUrl`
```php 
// Liefert die Immobilien-Detailseiten URL zurück
generateExposeUrl(int|PageModel $varPage): string
```

##### `getFields`
```php 
// Liefert die mitgegebenen Immobilien-Eigenschaften zurück
getFields(array $fields): array
```

##### `getMainImageUuid`
```php 
// Liefert die UUID des Titelbildes
getMainImageUuid(): string
```

##### `getImagesUuids`
```php 
// Liefert die UUIDs der zu berücksichtigen Immobilien-Eigenschaften zurück, $max definiert dabei die maximale Anzahl
getImagesUuids(array $fields, int $max): array
```

##### `getStatusTokens`
```php 
// Liefert alle Status-Token einer Immobilie zurück oder zutreffende Status-Token, welche als valide übergeben wurden
getStatusTokens(array $validStatusToken = null): array
```

##### `getMarketingToken`
```php 
// Liefert alle Vermarktungs-Token einer Immobilie zurück
getMarketingToken(): array
```

##### `getLocation`
```php 
// Liefert die Adresse der Immobilie als array zurück und erlaubt das forcieren der vollständigen Adresse
getLocation(bool $forceCompleteAddress = false): array
```

##### `getLocationString`
```php 
// Liefert die Adresse der Immobilie als string zurück und erlaubt das forcieren der vollständigen Adresse
getLocationString(bool $forceCompleteAddress = false): array
```

##### `getLocationString`
```php 
// Liefert die Adresse der Immobilie als string zurück und erlaubt das forcieren der vollständigen Adresse
getLocationString(bool $forceCompleteAddress = false): array
```

##### `getMainPrice`
```php 
// Liefert den ermittelten Preis einer Immobilie als FormattedCollection zurück
getMainPrice(): array
```

##### `getMainArea`
```php 
// Liefert die ermittelte Fläche einer Immobilie als FormattedCollection zurück
getMainArea(): array
```

##### `getAreas`
```php 
// Liefert alle Flächen einer Immobilie als array zurück
getAreas(): array
```

##### `getPrices`
```php 
// Liefert alle Preise einer Immobilie als array zurück
getPrices(): array
```

##### `getAttributes`
```php 
// Liefert alle Attribute einer Immobilie als array zurück
getAttributes(): array
```

##### `getDetails`
```php 
// Liefert alle Details einer Immobilie als array zurück
getDetails(bool $includeAddress = false): array
```

##### `getEnergy`
```php 
// Liefert alle Energiewerte einer Immobilie als array zurück
getEnergy(): array
```

##### `getPropertiesByGroup`
```php 
// Liefert alle Eigenschaften einer Immobilie anhand von einer Gruppe.
// Gruppen:
// - area
// - price
// - attribute
// - detail
// - energie
getPropertiesByGroup(array $separateGroups=null, bool $includeAddress = false, array $validGroups = null, string $defaultGroup = 'detail'): array
```

##### `getMainDetails`
```php 
// Liefert alle Hauptdetails einer Immobilie als array zurück
getMainDetails(int $max = null): array
```

##### `getMainAttributes`
```php 
// Liefert alle Hauptattribute einer Immobilie als array zurück
getMainAttributes(int $max = null): array
```

##### `getTexts`
```php 
// Liefert alle Texte unter Angabe der Immobilien-Eigenschaften als array zurück
getTexts(array $validTexts = null, int $maxTextLength = 0): array
```

##### `getProvider`
```php 
// Liefert den Anbieter der Immobilie zurück
getProvider(): ProviderModel
```

##### `getContactPerson`
```php 
// Liefert den Ansprechpartner der Immobilie zurück
getContactPerson(bool $forceCompleteAddress = false, bool $useProviderForwarding = false): ProviderModel
```

##### `generateMainImage`
```php 
// Liefert das Titelbild zurück
generateMainImage(string|array $imgSize): string
```

##### `generateGallery`
```php 
// Liefert die Bilder der angegebenen Gruppen einer Immobilie zurück
generateGallery(string|array $imgSize, array $arrFields = null, int $max = null): array
```

?> Siehe außerdem wie du aus das Immobilien-Objekt [aus einem Template heraus](/de-DE/developer/templates/?id=eigenschaften-über-das-immobilien-objekt-aus-dem-template-heraus-abrufen) zugreifen kannst.
