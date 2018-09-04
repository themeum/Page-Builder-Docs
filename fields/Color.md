# Color
A Color Input Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (color)
title | `optional` | String
desc | `optional` | String
placeholder | `optional` | String
std | `optional` | String ( Color Code )
selector | `optional` | String / Array
tab | `optional` | String(style)
section | `optional` | String

## Return
Always return `string` (Color HEX code)

## Example
```php
'addon_color'=> array(
    'type' => 'color',
    'title' => 'Color Field',
    'std' => '#1a0dab',
    'selector' => '{{SELECTOR}} .example-color{ color: {{data.addon_color}}; }'
)
```
Support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data['settings']['addon_color'].'</div>';
echo '<div class="example-color">Example Color</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_color}}</div>
<div class="example-color">Example Color</div>
```
