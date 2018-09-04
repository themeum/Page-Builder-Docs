# Slider
A Draggable Control Number Input Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String ( slider )
title | `optional` | String
desc | `optional` | String
unit | `optional` | Array
range | `optional` | Array
responsive | `optional` | Boolean ( Default: false )
range | `optional` | Array ( See Example  )
std | `optional` | String
selector | `optional` | String / Array

## Return
return `Number` for responsive false.  
return `Array` for responsive true.

## Example
**For Responsive**
```php
'addon_slider' => array(
    'type' => 'slider',
    'title' => __('Slider Title','your-textdomain'),
    'responsive' => true,
    'range' => array(
                'em' => array(
                  'min' => 0,
                  'max' => 8,
                  'step' => 1,
                ),
                'px' => array(
                  'min' => 1,
                  'max' => 100,
                  'step' => 1,
                ),
                '%' => array(
                  'min' => 0,
                  'max' => 100,
                  'step' => 1,
                ),
              ),
    'std' => array(
                'md' => '10px',
                'sm' => '11px',
                'xs' => '0px',
            ),
    'unit' => array( '%','px','em' ),
    'selector' => '{{SELECTOR}} .example-slider{ font-size: {{data.addon_slider}}; }'
),
```


**Not Responsive**
```php
'addon_slider' => array(
    'type' => 'slider',
    'title' => __('Slider Title','your-textdomain'),
    'range' => array(
                'min' => 0,
                'max' => 8,
                'step' => 1,
            ),
    'std' => '12px',
    'unit' => array( '%','px','em' ),
    'selector' => '{{SELECTOR}} .example-slider{ font-size: {{data.addon_slider}}; }'
),
```

**Not Responsive & Without Units**
```php
'addon_slider' => array(
    'type' => 'slider',
    'title' => 'Slider Title',
    'range' => array(
                'min' => 0,
                'max' => 100,
                'step' => 1,
            ),
    'std' => '12',
    'selector' 	=> '{{SELECTOR}} .example-slider{ font-size: {{data.addon_slider}}px; }'
),
```

## Controls
### PHP
Inside the `rander()` method-  
**For Responsive**
```php
echo '<div>'.$data['settings']['addon_slider']['md'].'</div>';
echo '<div>'.$data['settings']['addon_slider']['sm'].'</div>';
echo '<div>'.$data['settings']['addon_slider']['xs'].'</div>';
```

**Not Responsive** 
```php
echo '<div>'.$data['settings']['addon_slider'].'</div>';
```

### JS Template
Inside the `getTemplate()` method-

**For Responsive**
```js
<div>{{data.addon_slider.md}}</div>
<div>{{data.addon_slider.sm}}</div>
<div>{{data.addon_slider.xs}}</div>
```
Or
```js
<div>
<# _.forEach(data.addon_slider, function(value, key) { #>
    {{value}}
<# } #>
</div>
```

**Not Responsive** 
```js
<div>{{data.addon_slider}}</div>
```
