
# IconSocial
Only social icon input field of the FontAwesome

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (iconsocial)
title | `optional` | String
desc | `optional` | String
std | `optional` | String

## Return
Always return `string`

## Example
```php
'addon_iconsocial' => array(
    'type' => 'iconsocial',
    'title' => __('Social Icon Field','your-textdomain'),
    'std' => 'fa fa-facebook',
)
```
Not support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div><i class="'.$data['settings']['addon_iconsocial'].'"></i></div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div><i class="{{data.addon_iconsocial}}"></i></div>
```
