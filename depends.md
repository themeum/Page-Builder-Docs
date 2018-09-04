# Depends

Sometimes you may need a conditional field in your addon.

WP Page Builder supports `!=` and `=` conditional keys.

### Single condition
`Button Color` field shows when `Button Style` value is `primary`
```php
'button_style' => array(
    'type' => 'select',
    'title' => __('Button Style','your-textdomain'),
    'values' => array(
        'primary' => __('Primary','your-textdomain'),
        'success' => __('Success','your-textdomain'),
        'info' => __('Info','your-textdomain'),
    ),
    'std' => 'primary',
),
'button_color' => array(
    'type' => 'color',
    'title' => __('Button Color','your-textdomain'),
    'depends' => array( array('button_style', '=', 'primary' ) ),
),
```

### Multiple conditions
`Button Color` field shows when `Button Style` value is `primary` or `info`
```php
'button_style' => array(
    'type' => 'select',
    'title' => __('Style','your-textdomain'),
    'values' => array(
        'primary' => __('Primary','your-textdomain'),
        'success' => __('Success','your-textdomain'),
        'info' => __('Info','your-textdomain'),
    ),
    'std' => 'primary',
),
'button_color' => array(
    'type' => 'color',
    'title' => __('Button color','your-textdomain'),
    'depends' => array( array('button_style', '=', array('primary','info') ) ),
),
```

### Multiple conditions in multiple fields
`Button Color` field shows when `Button Style` value is `primary` and `Button Type` value is `solid`
```php
'button_style' => array(
    'type' => 'select',
    'title' => __('Style','your-textdomain'),
    'values' => array(
        'primary' => __('Primary','your-textdomain'),
        'success' => __('Success','your-textdomain'),
        'info' => __('Info','your-textdomain'),
    ),
    'std' => 'primary',
),
'button_type' => array(
    'type' => 'select',
    'title' => __('Button Type','your-textdomain'),
    'values' => array(
        'solid' => __('Solid Border','your-textdomain'),
        'dotted' => __('Dotted Border','your-textdomain'),
    ),
    'std' => 'primary',
),
'button_color' => array(
    'type' => 'color',
    'title' => __('Button color','your-textdomain'),
    'depends' => array( 
                    array('button_style', '=', 'primary' ), 
                    array('button_type', '=', 'solid' ),
                ),
),
```

### Single condition not equal
`Button Color` field shows when `Button Style` value is not equal `primary`
```php
'button_style' => array(
    'type' => 'select',
    'title' => __('Button Style','your-textdomain'),
    'values' => array(
        'primary' => __('Primary','your-textdomain'),
        'success' => __('Success','your-textdomain'),
        'info' => __('Info','your-textdomain'),
    ),
    'std' => 'primary',
),
'button_color' => array(
    'type' => 'color',
    'title' => __('Button Color','your-textdomain'),
    'depends' => array( array('button_style', '!=', 'primary' ) ),
),
```
