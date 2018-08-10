# Fontstyle2
A Font Styling Input Field (Simple Settings)

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (fontstyle2)
title | `optional` | String
desc | `optional` | String
std | `optional` | Array

## Return
Always return `object`

## Example
```php
'data_fontstyle2' => array(
	'type' => 'fontstyle2',
	'title' => __('Fontstyle2 Field','your-textdomain'),
	'std' => array(
		'fontFamily' 	=> '', // Google Font name
		'fontSize' 		=> [ 'md'=>'20px', 'sm'=>'18px', 'xs'=>'16px' ], // 0 to 400
		'lineHeight' 	=> [ 'md'=>'20px', 'sm'=>'18px', 'xs'=>'16px' ], // 0 to 400
		'fontWeight' 	=> '200', //100 to 900
		'textTransform' => '', // none inherit capitalize lowercase uppercase
		'fontStyle' 	=> '', //normal, italic, oblique
		'letterSpacing' => [ 'md'=>'0px', 'sm'=>'0px', 'xs'=>'0px' ],  // 0 to 20
		),
	'selector' => '{{SELECTOR}} .example-fontstyle2'
)
```
Support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data["settings"]["data_fontstyle2"]["fontFamily"].'</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.data_fontstyle2.fontFamily}}</div>
<div>{{data.data_fontstyle2.fontSize}}</div>
<div>{{data.data_fontstyle2.lineHeight}}</div>
<div>{{data.data_fontstyle2.fontWeight}}</div>
<div>{{data.data_fontstyle2.textTransform}}</div>
<div>{{data.data_fontstyle2.fontStyle}}</div>
<div>{{data.data_fontstyle2.letterSpacing}}</div>
```
