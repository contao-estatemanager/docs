# Immobilien-Objekt

Über das Immobilien-Objekt können alle Eigenschaften einer Immobilie ausgelesen, validiert und für die Ausgabe aufbereitet werden.

### Funktionsumfang

| Funktionen                                                                                                                                                  |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `get(<string> $name): null\|array<FormattedCollection>`                                                                                                     |
| `getType(): RealEstateTypeModel`                                                                                                                            |
| `generateExposeUrl(<int\|PageModel> $varPage): string`                                                                                                      |
| `getFields(<array> $fields): array`                                                                                                                         |
| `getMainImageUuid(): string`                                                                                                                                |
| `getImagesUuids(<array> $arrFields = null, $max = null): array`                                                                                             |
| `getStatusTokens(<array> $validStatusToken = null): array`                                                                                                  |
| `getMarketingToken(): array`                                                                                                                                |
| `getLocation(<bool> $forceCompleteAddress = false): array`                                                                                                  |
| `getLocationString(<bool> $forceCompleteAddress = false): string`                                                                                           |
| `getMainPrice(): null\|array<FormattedCollection>`                                                                                                          |
| `getMainArea(): null\|array<FormattedCollection>`                                                                                                           |
| `getAreas(): array\|null`                                                                                                                                   |
| `getPrices(): array\|null`                                                                                                                                  |
| `getAttributes(): array\|null`                                                                                                                              |
| `getDetails(<bool> $includeAddress = false): array\|null`                                                                                                   |
| `getEnergy(): array\|null`                                                                                                                                  |
| `getPropertiesByGroup(<array> $separateGroups=null, <bool> $includeAddress = false, <array> $validGroups = null, <string> $defaultGroup = 'detail'): array` |
| `getMainDetails(<int> $max = null): array`                                                                                                                  |
| `getMainAttributes(<int> $max = null): array`                                                                                                               |
| `getTexts(<array> $validTexts = null, <int> $maxTextLength = 0): array\|null`                                                                               |
| `getProvider(): ProviderModel`                                                                                                                              |
| `getContactPerson(<bool> $forceCompleteAddress = false, <bool> $useProviderForwarding = false): aray\|null`                                                 |
| `generateMainImage(<array\|string> $imgSize): string`                                                                                                       |
| `generateGallery(<array\|string> $imgSize, <array> $arrFields = null, <int> $max = null): array`                                                            |

**Siehe auch:** [Eigenschaften über das Immobilien-Objekt aus dem Template heraus abrufen](../templates.md#eigenschaften-ueber-das-immobilien-objekt-aus-dem-template-heraus-abrufen).
