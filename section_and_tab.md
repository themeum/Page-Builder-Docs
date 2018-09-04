# Section & Tab
If you want to display the field type in the `style` Tab, then add `'tab' => 'style'` in parameters.
 
If you do not use `section` then the field automatically goes to the `General` section. If you use `section` then it goes to that specific section. 

### Tab without section
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
    'tab' => 'style',
),
```

### Section in General tab
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
    'section' => 'Style',
),
'button_type' => array(
    'type' => 'select',
    'title' => __('Button Type','your-textdomain'),
    'values' => array(
        'solid' => __('Solid Border','your-textdomain'),
        'dotted' => __('Dotted Border','your-textdomain'),
    ),
    'std' => 'primary',
    'section' => 'Style',
),
'button_color' => array(
    'type' => 'color',
    'title' => __('Button Color','your-textdomain'),
    'section' => 'Color',
),
```

### Section in Style tab
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
    'tab' => 'style',
    'section' => 'Style',
),
'button_type' => array(
    'type' => 'select',
    'title' => __('Button Type','your-textdomain'),
    'values' => array(
        'solid' => __('Solid Border','your-textdomain'),
        'dotted' => __('Dotted Border','your-textdomain'),
    ),
    'std' => 'primary',
    'tab' => 'style',
    'section' => 'Style',
),
'button_color' => array(
    'type' => 'color',
    'title' => __('Button Color','your-textdomain'),
    'tab' => 'style',
    'section' => 'Color',
),
```
