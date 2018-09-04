# Background
A Background Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (background)
title | `optional` | String
desc | `optional` | String
video | `optional` | Boolean ( Video BG only return Data )
std | `optional` | String
selector | `optional` | String / Array
tab | `optional` | String(style)
section | `optional` | String

## Return
Always return `object`

## Example
```php
'addon_background' => array(
    'type' => 'background',
    'title' => __('Background Field','your-textdomain'),
    'selector' => '{{SELECTOR}} .example-background',
    'std' => array(
	'bgType' => 'color',
	'bgColor' => '',
	'bgImage' => array(),
	'bgimgPosition' => '',
	'bgimgAttachment' => '',
	'bgimgRepeat' => '',
	'bgimgSize' => '',
	'bgDefaultColor' => '',
	'bgGradient' => array(),
	'videoType' => 'local',
	'bgVideo' => array(),
	'bgExternalVideo' => '',
	'bgVideoFallback' =>array(),
	'bgHoverType' => 'color',
	'bgHoverColor' => '',
	'bgHoverImage' => array(),
	'bgHoverimgPosition' => '',
	'bgHoverimgAttachment' => '',
	'bgimgHoverRepeat' => '',
	'bgimgHoverSize' => '',
	'bgHoverDefaultColor' => '',
	'bgHoverGradient' => array(),
    )
)
```
Support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method
```php
echo '<div>'.$data["settings"]["addon_background"]["bgColor"].'</div>';
echo '<div class="example-background">Example Background</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_background.bgColor}}</div>
<div class="example-background">Example Background</div>
```
