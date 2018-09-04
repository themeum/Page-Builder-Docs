# Alignment
An Alignment Selector Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (alignment)
title | `optional` | String
desc | `optional` | String
selector | `optional` | Boolean ( Default: false )
std | `optional` | String

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
'<div>'.$data["settings"]["addon_alignment"].'</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_alignment}}</div>
```
