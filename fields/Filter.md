# Filter
A CSS Filter Input Field
## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (filter)
title | `optional` | String
desc | `optional` | String
std | `optional` | Object ( Color Code )
selector | `optional` | String / Array
tab | `optional` | String(style)
section | `optional` | String
 ## Return
Always return `object` (Color HEX code)
 ## Example
```php
'addon_filter'=> array(
    'type' => 'filter',
    'title' => 'Filter Field',
    'std' => array(
					'brightness' => '100%',
					'contrast' => '100%',
					'grayscale' => '100%',
					'invert' => '100%',
					'huerotate' => '100deg',
					'saturate' => '100%',
					'sepia' => '100%',
		),
    'selector' => '{{SELECTOR}} .example-filter'
)
```
Support 'selector' parameters.
 ## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data['settings']['addon_filter']['brightness'].'</div>';
echo '<div class="example-filter">Example Filter</div>';
```
 ### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_filter.brightness}}</div>
<div class="example-filter">Example Filter</div>
```
