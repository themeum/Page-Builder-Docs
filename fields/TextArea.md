

# TextArea
A Textarea input field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (textarea)
title | `optional` | String
desc | `optional` | String
placeholder | `optional` | String
std | `optional` | String
tab | `optional` | String(style)
section | `optional` | String

## Return
Always return `string`

## Example
```php
'addon_textarea' => array(
    'type' => 'textarea',
    'title' => __('Textarea Field','your-textdomain'),
    'placeholder' => __('Textarea Placeholder','your-textdomain'),
    'std' => 'Textarea Default Value'
)
```
Not Support `selector` parameters for Textarea case.

## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data['settings']['addon_textarea'].'</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_textarea}}</div>
```
