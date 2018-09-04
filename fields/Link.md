# Link
A Link Input Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (textarea)
title | `optional` | String
placeholder | `optional` | String
desc | `optional` | String / Array
std | `optional` | Array
selector | `optional` | String / Array
tab | `optional` | String(style)
section | `optional` | String

## Return
Always return `object`

## Example
```php
'addon_link' => array (
    'type' => 'link',
    'title' => __('Link Field','your-textdomain'),
    'std' => '#', // 'std' => array( 'link' => '', 'window' => 0, 'nofolow' => 0 ),
    'placeholder' => 'Link Placeholder'
)
```
Support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data["settings"]["addon_link"].'</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{ data.addon_link.link }}</div>
```
