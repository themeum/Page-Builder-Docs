
# Block And Layout
*WP Page Builder* supports third-party blocks and layouts. 
It is very easy to add a custom block or layout via a plugin or theme.

## Adding a Custom Block
Firstly, you need to create a block using *WP Page Builder* and export it.
Secondly, add this via `wppb_add_block` filter.

### Example
```php
function prefix_add_block_callback( $blocks ){
	$blocks[] = array(
		'name' => 'Name of the Blocks', // Name of the Block
		'file' => plugin_dir_path( __FILE__ ).'test.json', // JSON export file directory path
		'banner' => 'https://builder.themeum.com/wp-content/uploads/2018/07/Content-1.png', // Banner Image URL
		'section' => 'Section Name', // Section Name
		'liveurl' => 'https://builder.themeum.com/call-to-action-item-1/' //
	);
	return $blocks;
}
add_filter('wppb_add_block', 'prefix_add_block_callback');
```
*Note:* All the fields are required except `liveurl`.

## Adding a Custom Layout
Firstly, you need to create a layout using *WP Page Builder* and export it.
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
					'liveurl' => 'https://builder.themeum.com/agency-home/'
				),
				array(
					'name' => 'EAbout',
					'preview' => 'https://builder.themeum.com/wp-content/uploads/2018/07/Content-1.png',
					'preview2x' => 'https://builder.themeum.com/wp-content/uploads/2018/07/Pricing-table-1.png',
					'file' => plugin_dir_path( __FILE__ ).'template2.json',
					'liveurl' => 'https://builder.themeum.com/agency-home/'
				)
		)
	);
	return $layouts;
}
add_filter('wppb_add_layout', 'prefix_add_layout_callback');
```
*Note:* All the fields are required except `liveurl`.
