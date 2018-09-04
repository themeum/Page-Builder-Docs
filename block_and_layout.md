
# Block And Layout
*WP Page Builder* supports thirdparty block and layout inside the "Blocks" and "Layouts" menu. 
It is very easy to add custom block or layout from the plugin or theme.

## Block add
Firstly, you have to create a block using *WP Page Builder* and export it.
Secondly, add this via `wppb_add_block` filter.

### Example
```php
function prefix_add_block_callback( $blocks ){
	$blocks[] = array(
		'name' => 'Name of the Blocks', // Name of the Block
		'file' => plugin_dir_path( __FILE__ ).'test.json', // JSON export file directory path
		'banner' => 'https://builder.themeum.com/wp-content/uploads/2018/07/Content-1.png', // Banner Image URL
		'section' => 'Section Name', // Section Name
	);
	return $blocks;
}
add_filter('wppb_add_block', 'prefix_add_block_callback');
```
*Note:* All the field is required for the block.

## Layout add
Firstly, you have to create a Layout using *WP Page Builder* and export it.
Secondly, add this via `wppb_add_layout` filter.

### Example
```php
function prefix_add_layout_callback( $layouts ){
	$layouts[] = array(
		'name' => 'Example', // Name of the Layput
		'category' => array( 'Category Name', 'Creative' ), // Category Must be Array and 
		'preview2x' => 'https://builder.themeum.com/wp-content/uploads/2018/07/Content-1.png', // Preview in Listing 2x
		'preview' => 'https://builder.themeum.com/wp-content/uploads/2018/07/Pricing-table-1.png', // Preview in Listing
		'single' => array(
				array(
					'name' => 'EHome', // Name of the Inner Layout
					'preview' => 'https://builder.themeum.com/wp-content/uploads/2018/07/Content-1.png', // Preview in Inner
					'preview2x' => 'https://builder.themeum.com/wp-content/uploads/2018/07/Pricing-table-1.png', // Preview in Inner 2x
					'file' => plugin_dir_path( __FILE__ ).'template1.json', // File path of the Export JSON
				),
				array(
					'name' => 'EAbout',
					'preview' => 'https://builder.themeum.com/wp-content/uploads/2018/07/Content-1.png',
					'preview2x' => 'https://builder.themeum.com/wp-content/uploads/2018/07/Pricing-table-1.png',
					'file' => plugin_dir_path( __FILE__ ).'template2.json',
				)
		)
	);
	return $layouts;
}
add_filter('wppb_add_layout', 'prefix_add_layout_callback');
```
*Note:* All the field is required for the layout.
