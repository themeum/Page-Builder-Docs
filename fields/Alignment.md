# Alignment
An Alignment Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (alignment)
title | `optional` | String
desc | `optional` | String
std | `optional` | String
selector | `optional` | String / Array
tab | `optional` | String(style)
section | `optional` | String

## Example
```php
'addon_alignment' => array(
    'type' => 'alignment',
    'title' => __('Alignment Field','your-textdomain'),
    'std' => 'center',
    'selector' => '{{SELECTOR}} .example-alignment{ text-align: {{data.addon_alignment}}; }',
)
```
Support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data["settings"]["addon_alignment"].'</div>';
echo '<div class="example-alignment">Alignment Check</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_alignment}}</div>
<div class="example-alignment">Alignment Check</div>
```
