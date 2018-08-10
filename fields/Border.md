# Border
A Border Input Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (border)
title | `optional` | String
desc | `optional` | String
std | `optional` | Array
selector | `optional` | String

## Return
Always return `object`

## Example
```php
'addon_border' => array(
    'type' => 'border',
    'title' => __('Border Field','your-textdomain'),
    'std' => array(
        'borderWidth' => array( 'top' => '0px', 'right' => '0px', 'bottom' => '0px', 'left' => '0px' ), 
        'borderStyle' =>'solid', 
        'borderColor' => '#cccccc' 
    ),
    'selector' => '{{SELECTOR}} .example-border'
)
```
Support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data['settings']['addon_border'].'</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_border.borderWidth}}</div>
<div>{{data.addon_border.borderStyle}}</div>
<div>{{data.addon_border.borderColor}}</div>
```
