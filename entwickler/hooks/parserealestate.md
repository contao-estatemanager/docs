# parseRealEstate

Der `parseRealEstate` Hook wird aufgerufen bevor das Template einer einzelnen Immobilie geparsed wird.

### Parameter

1. \Contao\FrontendTemplate `$objTemplate` Das Immobilien-Template 
2. \ContaoEstateManager\RealEstate`$objRealEstate` Das Immobilien-Objekt 
3. \ContaoEstateManager\ModuleRealEstate`$objModule` Das aktuelle Modul

### Beispiel

```php
public function onParseRealEstate(\Contao\FrontendTemplate &$objTemplate, \ContaoEstateManager\RealEstate $objRealEstate, \ContaoEstateManager\ModuleRealEstate $objModule): void
{
    // Do something …
}
```

