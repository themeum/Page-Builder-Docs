# Number
A Single Checkbox Input Field

Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (checkbox)
title | `optional` | String
desc | `optional` | String
std | `optional` | Number ( 0 or 1 )

## Return
return `0` or `1`

## Example
```php
'addon_checkbox' => array(
    'type' => 'checkbox',
    'title' => 'Checkbox Field',
    'std' => 0
)
```
Support 'selector' parameters but their is no need to use `selector`


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data['settings']['addon_checkbox'].'</div>';
```

### JS Template
Inside the `getTemplate()` method-

**Single**
```js
<div>{{data.addon_checkbox}}</div>
```
