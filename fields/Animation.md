# Animation
An Animation Input Field (wowjs)

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (textarea)
title | `optional` | String
desc | `optional` | String
std | `optional` | Array
tab | `optional` | String(style)
section | `optional` | String

## Return
Always return `object`

## Example
```php
'addon_animation'=> array(
	'type' => 'animation',
	'title' => __('Animation Field','your-textdomain'),
	'std' => array(
	    	'name' => 'wow animated fadeIn',
		'delay' => '300',
		'duration' => '400'
	    ),
)
```
Not support 'selector' parameters.

## Controls
### PHP
Inside the `rander()` method
```php
echo '<div class="sample-animation wppb-wow wppb-animated '.$data['settings']['addon_animation']['name'].' '.$data['settings']['addon_animation']['duration'].'" data-wppb-wow-delay="'.$data['settings']['addon_animation']['delay'].'"> Animated Text </div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_animation.duration}}</div>
```
