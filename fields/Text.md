# Text
A text input field.

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (text)
title | `optional` | String
desc | `optional` | String
placeholder | `optional` | String
std | `optional` | String
selector | `optional` | String (better not to use)

## Return
Always return `string`

## Example
```php
'addon_text' => array(
    'type' => 'text',
    'title' => __('Text Field','your-textdomain'),
    'placeholder' => __('Text Placeholder','your-textdomain'),
    'std' => 'Default Value of Text',
)
```
Support 'selector' parameters but it's better not to use the selector.


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data['settings']['addon_text'].'</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_text}}</div>
```
