# BoxShadow 
A Box-shadow input field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (boxshadow)
title | `optional` | String
desc | `optional` | String
std | `optional` | Array
selector | `optional` | String / Array
tab | `optional` | String(style)
section | `optional` | String

## Return
Always return `object`

## Example
```php
'widget_boxshadow' => array(
	'type' => 'boxshadow',
	'title' => __('Boxshadow Field','your-textdomain'),
	'std' => array(
		    'shadowValue'=> array( 'top' => '120px', 'right' => '0px', 'bottom' => '0px', 'left' => '0px' ), 
		    'shadowColor' 	=> '#ffffff' 
		),
	'selector' => '{{SELECTOR}} .example-boxshadow'
)
```
Support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data["settings"]["widget_boxshadow"]["shadowValue"]["top"].'</div>';
echo '<div>'.$data["settings"]["widget_boxshadow"]["shadowColor"].'</div>';
echo '<div class="example-boxshadow">Example Boxshadow</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.widget_border.shadowValue.top}}</div>
<div>{{data.widget_border.shadowColor}}</div>
<div class="example-boxshadow">Example Boxshadow</div>
```
