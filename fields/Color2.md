# Color2
A Color Input Field with Gradient Input
 ## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (color2)
title | `optional` | String
desc | `optional` | String
placeholder | `optional` | String
std | `optional` | String ( Color Code )
selector | `optional` | String / Array
tab | `optional` | String(style)
clip | `optional` | boolean( default: false )
section | `optional` | String
 ## Return
Always return `string` (Color HEX code)
 ## Example
```php
'addon_color'=> array(
    'type' => 'color2',
    'title' => 'Color2 Field',
    'std' => array(
					'colorType' => 'color',
					'colorColor' => '#f8f8f8',
					'clip' => false
		),
    'selector' => '{{SELECTOR}} .example-color'
)
```
Support 'selector' parameters.
 ## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data['settings']['addon_color']['colorType'].'</div>';
echo '<div class="example-color">Example Color</div>';
```
 ### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_color.colorType}}</div>
<div class="example-color">Example Color</div>
```
