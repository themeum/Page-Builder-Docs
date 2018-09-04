# Icon
A Icon select field (FontAwesome 4 & WPPB Font)

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (icon)
title | `optional` | String
desc | `optional` | String
std | `optional` | String
selector | `optional` | String / Array

## Return
Always return `string`

## Example
```php
'addon_icon' => array(
    'type' => 'icon',
    'title' => __('Icon Field','your-textdomain'),
    'std' => 'fa fa-adn',
)
```
Not support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div><i class="'.$data['settings']['addon_icon'].'"></i></div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div><i class="{{data.addon_icon}}"></i></div>

```
