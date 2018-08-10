
# Custom Addon
You can add any number of custom addons in *WP Page Builder* from your WordPress theme or plugin. You just have to add a filter and include your addon Class name using this filter-

```php
add_filter( 'wppb_available_addons', 'prefix_custom_addon_include' );
if ( ! function_exists('prefix_custom_addon_include')){
    function prefix_custom_addon_include($addons){
        $addons[] = 'Custom_Addon';
        // Add Other Custom Addon class name in here, at a time.
        return $addons;
    }
}
```

You can check our [plugins](https://wordpress.org/plugins/wp-pagebuilder/) shortcode inside in here `plugins_directory/addons`  
Here is a sample addon code-

## Some Tips
01. `get_name()` must be unique and without space
02. `get_title()` You can use space and it will be display as Addon name
03. `get_icon()` support [FontAwesome 4](https://fontawesome.com/v4.7.0/) and WPPB [default icon.](https://builder.themeum.com/wppbicon/)
04. `get_category_name()` If want to show the addon in a specific category then use this function
05. `get_settings()` You can use any [field type](https://github.com/themeum/WP-Page-Builder#field-type) in here.
06. `render()` here is a frontend output. If you don't use `getTemplate()` then live editing comes from AJAX request via `render()` function.
07. `getTemplate()` Speedup your frontend editing. It's using [Lodash](https://lodash.com/docs/4.17.10#template) templating. So follow lodash templating documentation. 
08. `get_enqueue_script()` and `get_enqueue_style()` stands for specific script and style for specific addons. If the addon remains on the page then the style or script add on the page. You just have to `wp_register_script` and `wp_register_style` anywhere in your theme or plugins (Don not `wp_enqueue_script` or `wp_enqueue_style`).




```php
class Custom_Addon{
    public function get_name(){
        return 'checkit';
    }
    public function get_title(){
        return 'Checkit';
    }
    public function get_icon() {
        return 'wppb-font-trash';
    }
    public function get_category_name(){
        return 'Addon Category';
    }
    /* 
    public function get_enqueue_script(){
        return array( 'script-name' ); 
    }
    public function get_enqueue_style(){
			  return array( 'style-name' );
		}
    */

    // Textarea Settings Fields
    public function get_settings() {
        $settings = array(
            'custom_addon_textarea' => array(
                'type' => 'textarea',
                'title' => 'Textarea Title',
                'placeholder' => 'Textarea Placeholder',
                'std' => 'Textarea Default'
            ),
        );
        return $settings;
    }

    public function render($data = null){
        $settings = $data['settings'];
        return '<div class="wrapper">TextArea Output:'.$settings['custom_addon_textarea'].'</div>';;
    }

    // headline Template
    public function getTemplate(){
        return '<# if(data.custom_addon_textarea){ #>
                    <div class="sample-number1">DATA:{{data.custom_addon_textarea}}</div>
                <# } #>';
    }
}

```
