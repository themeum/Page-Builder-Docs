
#Checkbox
A Multiple Checkbox Input Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (checkbox2)
title | `optional` | String
desc | `optional` | String
values | `optional` | Array
std | `optional` | String

## Return
return single `string` for not multiple  
return `array` for the multiple

## Example
**Single**
```php
'addon_checkbox2' => array (
    'type' => 'checkbox2',
    'title' => 'Checkbox2 Field',
    'values' => array(
		'10px' => 'Small Height',
		'20px' => 'Medium Height',
		'40px' => 'Large height'
	    ),
    'std' => '20px',
    'selector'	=> '{{SELECTOR}} .example-checkbox2{{data.addon_checkbox2}}'
)
```
Support 'selector' parameters.


**Multiple**
```php
'addon_checkbox2' => array (
    'type' => 'checkbox2',
    'title' => 'Checkbox2 Title',
    'values' => array(
                    'type1' => 'Type 1',
                    'type2' => 'Type 2',
                    'type3' => 'Type 3'
                ),
    'std' => ['type1','type2'],
    'multiple' => true
)
```

## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data['settings']['addon_checkbox2'].'</div>';

```

**Multiple**
```php
echo '<div>';
    foreach($data['settings']['addon_checkbox2'] as $value) {
        echo $value;
    }
echo '</div>';
```

### JS Template
Inside the `getTemplate()` method-

**Single**
```js
<div>{{data.addon_checkbox2}}</div>

```

**Multiple**
```js
<div>
<# _.forEach(data.addon_checkbox2, function(value, key) { #>
    {{value}}
<# } #>
</div>

```
