# Selector

Most of the field types support the selector parameters.

`{{SELECTOR}}` is replaced by the unique addon class.

`data.field_key` is replaced by the value of the field.

### Single selector
```php
'selector' => '{{SELECTOR}} .example-class { font-size: {{data.number_height}}; }',
```

### Multiple selectors using array
```php
'selector' => array(
    '{{SELECTOR}} .example-class-1 { font-size: {{data.number_height}}; }',
    '{{SELECTOR}} .example-class-2 { line-height: {{data.number_height}}; }',
)
```

### Multiple selectors using string
```php
'selector' => '{{SELECTOR}} .example-class-1 { font-size: {{data.number_height}}; }, {{SELECTOR}} .example-class-2 { line-height: {{data.number_height}}; }'
```

### You can use one selector data in another type
```php
'addon_alignment' => array(
    'type' => 'alignment',
    'title' => __('Alignment Field','your-textdomain'),
    'selector' => '{{SELECTOR}} .example-alignment{ color: {{data.addon_color}}; }',
),
'addon_color' => array(
    'type' => 'color',
    'title' => __('Color Field','your-textdomain'),
),
```


### These field types do not need enclosed brackets
1. typography
2. typography2
3. gradient
4. border
5. color2
6. boxshadow

```php
'selector' => '{{SELECTOR}} .example-class'
```

