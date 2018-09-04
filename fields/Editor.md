# Editor
A WordPress Default wysiwyg Editor Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (editor)
title | `optional` | String
desc | `optional` | String
std | `optional` | String
tab | `optional` | String(style)
section | `optional` | String

## Return
Return `string` (wysiwyg editor output)

## Example
```php
'addon_editor' => array(
    'type' => 'editor',
    'title' => __('Editor Field','your-textdomain'),
    'std' => 'Editor Default Value',
)
```
Not Support 'selector' parameter.


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data['settings']['addon_editor'].'</div>';
```

### JS Template
Inside the `getTemplate()` method-

```js
<div>{{data.addon_editor}}</div>
```
