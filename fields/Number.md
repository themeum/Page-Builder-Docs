
# Number
A Number Input Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (number)
title | `optional` | String
desc | `optional` | String
unit | `optional` | Array
responsive | `optional` | Boolean ( Default: false )
range | `optional` | Array ( See Example  )
placeholder | `optional` | String
std | `optional` | String for not responsive / Array for responsive 
selector | `optional` | String / Array
tab | `optional` | String(style)
section | `optional` | String


## Return
return `number` for not multiple.  
return `object` for multiple.

## Example
**For Responsive**
```php
'addon_number' => array(
    'type' => 'number',
    'title' => __('Number Field','your-textdomain'),
    'placeholder' => __('Number Placeholder','your-textdomain'),
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
    'responsive' => true,
    'selector' => '{{SELECTOR}} .example-number{ font-size: {{data.addon_number}}; }'
)
```


**Not Responsive - with unit**
```php
'addon_number' => array(
    'type' => 'number',
    'title' => __('Number Field','your-textdomain'),
    'range' => array(
                'min' => 0,
                'max' => 8,
                'step' => 1,
            ),
    'std' => '12px',
    'unit' => array( '%','px','em' ),
    'selector' => '{{SELECTOR}} .example-slider{ font-size: {{data.addon_number}}; }'
),
```

**Not Responsive & Without Units**
```php
'addon_number' => array(
    'type' => 'number',
    'title' => __('Number Field','your-textdomain'),
    'range' => array(
                'min' => 0,
                'max' => 100,
                'step' => 1,
            ),
    'std' => '12',
    'selector' 	=> '{{SELECTOR}} .example-slider{ font-size: {{data.addon_number}}px; }'
),
```

## Controls
### PHP
Inside the `rander()` method-
**For Responsive**
```php
echo '<div>'.$settings['addon_number']['md'].'</div>';
echo '<div>'.$settings['addon_number']['sm'].'</div>';
echo '<div>'.$settings['addon_number']['xs'].'</div>';
echo '<div class="example-slider">Example Slider</div>';

```

**Not Responsive** 
```php
echo '<div>'.$settings['addon_number'].'</div>';
echo '<div class="example-slider">Example Slider</div>';
```

### JS Template
Inside the `getTemplate()` method-

**For Responsive**
```js
<div>{{data.addon_number.md}}</div>
<div>{{data.addon_number.sm}}</div>
<div>{{data.addon_number.xs}}</div>
<div class="example-slider">Example Slider</div>
```
Or
```js
<div>
<# _.forEach(data.addon_number, function(value, key) { #>
    {{value}}
<# } #>
</div>
<div class="example-slider">Example Slider</div>
```

**Not Responsive** 
```js
<div>{{data.addon_number}}</div>
<div class="example-slider">Example Slider</div>
```
