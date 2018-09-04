
# Gradient
A Gradient Color Input Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (gradient)
title | `optional` | String
desc | `optional` | String
clip | `optional` | Boolean ( Default: false )
std | `optional` | Array
selector | `optional` | String / Array

## Return
Always return `object`

## Example
```php
'addon_gradient' => array(
    'type' => 'gradient',
    'title' => __('Gradient Field','your-textdomain'),
    'std' => array(
		'bgFirst' => '#ff0000',
		'bgSecond' => '#ffff00',
		'degValue' => 90,
		'direction' => 90,
		'startPosition' => 50,
		'endPosition' => 90,
		'type' => 'linear', 
		'radialValue' => 'center'
	    ),
    'selector' => '{{SELECTOR}} .example-gradient'
)
```

`clip` parameter is used for foreground color.

## Controls
### PHP
Inside the `rander()` method
```php
echo '<div>'.$data["settings"]["addon_gradient"]["bgFirst"].'</div>';
echo '<div class="example-gradient">Example Gradient</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_gradient.bgFirst}}</div>
<div>{{data.addon_gradient.bgSecond}}</div>
<div class="example-gradient">Example Gradient</div>
```
