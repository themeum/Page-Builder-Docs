#  Repeatable
Repeatable Group Element Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (repeatable)
title | `optional` | String
desc | `optional` | String
attr | `optional` | Array
std | `optional` | Array

## Return
Always return `object`


```php
'repeatable_item' => array(
    'title' => 'Repeatable Item',
    'type' => 'repeatable',
    'attr' => array(
	    'icon_list' => array(
		    'type' => 'iconsocial',
		    'title' => 'Iconsocial Field',
		    'std' => 'fa fa-facebook'
	        ),
		'social_url' => array(
		    'type' => 'text',
		    'title' => 'Add social URL',
		    'std' => '#'
		),
    ),
    'std' => array(
        array( 
            'icon_list' => 'fa fa-twitch',
            'social_url' => '#',
        ),
        array( 
            'icon_list' => 'fa fa-twitter',
            'social_url' => '#',
        ),
    ),
)
```


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>';
foreach ( $settings['repetable_check'] as $key => $value ){
    echo $value['icon_list'];
    echo $value['social_url'];
}
echo '</div>';

### JS Template
Inside the `getTemplate()` method-
```js
<div>
<# _.forEach(data.repetable_check, function(value, key) { #>
    {{value.icon_list}}
    {{value.social_url}}
<# } #>
</div>
```
