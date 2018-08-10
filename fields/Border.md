# Border
A Border Input Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (textarea)
title | `optional` | String
desc | `optional` | String
std | `optional` | String
selector | `optional` | String

## Return
Always return `object`

## Example
```php
'widget_border' => array(
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
echo '<div>'.$data['settings']['widget_border'].'</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.widget_border.borderWidth}}</div>
<div>{{data.widget_border.borderStyle}}</div>
<div>{{data.widget_border.borderColor}}</div>
```
