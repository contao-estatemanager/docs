# Insert-Tags

### Abruf von Feldern einer speziellen Immobilie

`{{realestate::ID::FIELD}}`

🔹`<int> ID`

_ID der abzufragenden Immobilie_

🔹`<string> FIELD`

_Die abzufragende_ [_Immobilien-Eigenschaft_](../../entwickler/immobilien-eigenschaften/)_._

{% code title="Beispiel" %}
```markup
{{realestate::5::objekttitel}}
```
{% endcode %}

### Abruf von Feldern der aktuellen Immobilie innerhalb eines Exposés

`{{realestate::FIELD}}`

🔹`<string> FIELD`

_Die abzufragende_ [_Immobilien-Eigenschaft_](../../entwickler/immobilien-eigenschaften/)_._

{% code title="Beispiel" %}
```markup
{{realestate::objekttitel}}
```
{% endcode %}

