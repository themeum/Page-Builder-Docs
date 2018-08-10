# Fontstyle 
A Font Styling Input Field (Full Settings)

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (fontstyle)
title | `optional` | String
desc | `optional` | String
std | `optional` | Array

## Return
Always return `object`

## Example
```php
'addon_fontstyle' => array(
	'type' => 'fontstyle',
	'title' => __('Fontstyle Field','your-textdomain'),
	'std' => array(
		    'textDecoration' => 'underline',
		    'fontStyle' => 'italic',
		    'textTransform' => 'uppercase',
		    'fontWeight' => 700
		),
	'selector' => '{{SELECTOR}} .example-fontstyle'
)
```
Support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data['settings']['addon_fontstyle']['fontStyle'].'</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_fontstyle.fontStyle}}</div>
```
