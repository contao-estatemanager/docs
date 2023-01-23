# Insert-Tags

### Abruf von Feldern einer speziellen Immobilie

`{{realestate::ID::FIELD}}`

:small\_blue\_diamond:`<int> ID`

_ID der abzufragenden Immobilie_

:small\_blue\_diamond:`<string> FIELD`

_Die abzufragende _[_Immobilien-Eigenschaft_](../../entwickler/immobilien-eigenschaften/)_._

{% code title="Beispiel" %}
```markup
{{realestate::5::objekttitel}}
```
{% endcode %}

### Abruf von Feldern der aktuellen Immobilie innerhalb eines Exposés

`{{realestate::FIELD}}`

:small\_blue\_diamond:`<string> FIELD`

_Die abzufragende _[_Immobilien-Eigenschaft_](../../entwickler/immobilien-eigenschaften/)_._

{% code title="Beispiel" %}
```markup
{{realestate::objekttitel}}
```
{% endcode %}
