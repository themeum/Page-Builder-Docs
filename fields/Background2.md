# Background2
A Background2 Field With Opacity Fields

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (background2)
title | `optional` | String
desc | `optional` | String
opacity | `optional` | Boolean ( Default: false )
std | `optional` | String

## Return
Always return `object`

## Example
```php
'widget_background2' => array(
    'type' => 'background2',
    'title' => __('Background Field','your-textdomain'),
    'opacity' => true,
    'selector' => '{{SELECTOR}} .example-background2',
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
            'Opacity' => 1,
            'bgHoverType' => 'color',
            'bgHoverColor' => '',
            'bgHoverImage' => array(),
            'bgHoverimgPosition' => '',
            'bgHoverimgAttachment' => '',
            'bgimgHoverRepeat' => '',
            'bgimgHoverSize' => '',
            'bgHoverDefaultColor' => '',
            'bgHoverGradient' => array(),
            'hoverOpacity' => 1,
        )
    )
```
Support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method
```php
echo '<div>'.$data["settings"]["addon_background2"]["bgColor"].'</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_background2.bgColor}}</div>
```
