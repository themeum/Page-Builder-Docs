# Media
A WordPress Media Manager Field

## Return
Always return `object`

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (media)
title | `optional` | String
desc | `optional` | String
multiple | `optional` | Boolean ( Default: false )
std | `optional` | String
tab | `optional` | String(style)
section | `optional` | String

## Example
**Single**
```php
'addon_media' => array(
    'type' => 'media',
    'title' => __('Media Title','your-textdomain'),
    'std' => 'http://example.com/example1.jpg', 
)
```
Not support 'selector' parameters.

**Multiple**
```php
'addon_media' => array(
    'type' => 'media',
    'title' => __('Media Title','your-textdomain'),
    'multiple' => true,
    'std' => array(
                'http://example.com/example1.jpg',
                'http://example.com/example2.jpg'
            ),
)
```
Not support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method-
**Single**
```php
echo '<div>'.$data['settings']['addon_media']['url'].'</div>';
echo '<div>'.$data['settings']['addon_media']['id'].'</div>';
```
**Multiple**
```php
echo '<div>';
foreach( $data['settings']['addon_media'] as $value) {
    echo $value['url'];
}
echo '</div>';
```

### JS Template
Inside the `getTemplate()` method-
**Single**
```js
<div>{{data.addon_media.url}}</div>
<div>{{data.addon_media.id}}</div>
```
**Multiple**
```js
<div>
<# _.forEach(data.addon_media, function(value, key) { #>
    {{value.url}}
<# } #>
</div>
```
