# Select
A Input Select Field


## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (select)
title | `optional` | String
desc | `optional` | String
placeholder | `optional` | String
multiple | `optional` | Boolean ( Default: false )
responsive | `optional` | Boolean ( Default: false )
std | `optional` | String (for multiple:false ) / Array (for multiple:true )
tab | `optional` | String(style)
section | `optional` | String


## Return
return `string` for not multiple  
return `object` for multiple

## Example

**For Responsive**
```php
'addon_select' => array(
    'type' => 'select',
    'title' => __('Select Title','your-textdomain'),
    'placeholder' => __('Select Placeholder','your-textdomain'),
    'responsive' => true,
    'values' => array(
        'block' => 'Block',
        'inline-block' => 'Inline Block',
        'flex' => 'flex',
    ),
    'std' => array(
        'md' => 'block',
        'sm' => 'flex',
        'xs' => 'flex',
    ),
),
```
Not Support 'selector' parameters.


**For Multiple**
```php
'addon_select' => array(
    'type' => 'select',
    'title' => __('Select Title','your-textdomain'),
    'placeholder' => __('Select Placeholder','your-textdomain'),
    'multiple' => true,
    'values' => array(
        'block' => 'Block',
        'inline-block' => 'Inline Block',
        'flex' => 'flex',
    ),
    'std' => 'block,flex',
),
```
Not Support 'selector' parameters.



**Not Responsive + Not Multiple**
```php
'addon_select' => array(
    'type' => 'select',
    'title' => __('Select Title','your-textdomain'),
    'placeholder' => __('Select Placeholder','your-textdomain'),
    'values' => array(
        'block' => 'Block',
        'inline-block' => 'Inline Block',
        'flex' => 'flex',
    ),
    'std' => 'block',
    'selector' => '{{SELECTOR}} .example-select{ display:{{data.addon_select}}; }'
),
```
Support 'selector' parameters.


**Responsive + Multiple**
```php
'addon_select' => array(
    'type' => 'select',
    'title' => __('Select Title','your-textdomain'),
    'placeholder' => __('Select Placeholder','your-textdomain'),
    'responsive' => true,
    'multiple' => true,
    'values' => array(
        'block' => 'Block',
        'flex' => 'Inline Block',
        'flex' => 'flex',
    ),
    'std' => array(
        'md' => 'block,flex',
        'sm' => 'flex,flex',
        'xs' => 'flex',
    ),
),
```
Not Support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method-

**For Responsive**
```php
echo '<div>'.$data['settings']['addon_select']['md'].'</div>';
echo '<div>'.$data['settings']['addon_select']['sm'].'</div>';
echo '<div>'.$data['settings']['addon_select']['xs'].'</div>';
```

**For Multiple**
```php
echo $data['settings']['addon_select']
```

**Not Responsive + Not Multiple**
```php
echo '<div>'.$data['settings']['addon_select'].'</div>';
```

**Responsive + Multiple**
```php
foreach( $data['settings']['addon_select'] as $key => $value ){
    echo '<div>'.$value.'</div>';
}
```

### JS Template
Inside the `getTemplate()` method-

**For Responsive**
```js
<div>
<# _.forEach(data.addon_select, function(value, key) { #>
    {{value}}
<# } #>
</div>
```

**For Multiple**
```js
<div>{{data.addon_select}}</div>
```

**Not Responsive + Not Multiple**
```js
<div>{{data.addon_select}}</div>
```

**Responsive + Multiple**
```js
<div>
<# _.forEach(data.addon_select, function(value, key) { #>
    {{value}}
<# } #>
</div>
```
