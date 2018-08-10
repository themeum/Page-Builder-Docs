
# RadioImage
A Radio Image Input Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (radioimage)
title | `optional` | String
desc | `optional` | String
std | `optional` | String
selector | `optional` | String

## Return
Always return `string`

## Example
```php
'widget_radioimage' => array(
    'type' => 'radioimage',
    'title' => __('Radioimage Title','your-textdomain'),
    'values' => array(
            'one' => plugin_dir_url( __FILE__ ).'icon1.png',
            'two' => plugin_dir_url( __FILE__ ).'icon2.png',
            'three' => plugin_dir_url( __FILE__ ).'icon3.png',
	),
    'std' => 'two'
)
```
Support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$settings['widget_radioimage'].'</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.widget_radioimage}}</div>
```
