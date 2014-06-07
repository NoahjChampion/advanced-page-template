=== Advanced Page Template ===
Contributors: xingxing
Tags: page, template, advanced, custom, field, custom field
Requires at least: 3.0.0
Tested up to: 3.9
License: GPLv2 or later




== Description ==

Advanced Page Template is a nice new approach to custom fields of the page template.
It parses the php comment block starting with '@custom_field' in the php template file, and displays the available custom fields for that template in the backend.
It means that it doesn't save any configuration data to database, just config the custom fields in template file itself as how wordpress recognize the templates - just wordpress way! I am going to call it as 'templating comment lines'.

Note: I really recommend you to install and activate Advanced Custom Fields plugin so as to get its perfect benifit. Field Types only works with Advanced Custom Fields plugin.

= Usage =
Open a template file with any text editor and add some additional templating comment lines starting with @custom_field keyword:

Example 1:
/*
* Template Name: 2column-layout
*
* @custom_field main, type: textarea, label: 'Main content area'
* @custom_field sidebar, type: textarea, label: 'Sidebar area'
*/

Example 2:
/*
* Template Name: Contact Page
*
* @custom_field photo, type: image, label: 'Photo of manager'
* @custom_field phone, type: text
* @custom_field map, type: map
* 
* Note: The photo, phone, map are the custom field names in each '@custom_field' line,
* therefore use 'get_post_meta' method with those custom field names to get the values in this template. :)
*/

Please bring the page edit link up in the backend and select the template which you just edited and hit 'update' or 'save' button.
After page refreshing, You can't miss new custom fields block from this template file.





== Installation ==

1. Upload 'advanced-page-template' to the '/wp-content/plugins/' directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Add some templating comment lines to a template source code.
4. Specify that template which has templating comment lines to a page and save, then new custom fields block will appear on the bottom.




== Changelog ==

= 1.0.0 =
* Advanced Page Template.