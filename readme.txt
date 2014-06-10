=== Advanced Page Template ===
Contributors: xingxing
Tags: page, template, advanced, custom, field, custom field
Requires at least: 3.0.0
Tested up to: 3.9
License: GPLv2 or later




== Description ==

Advanced Page Template is a nice new approach to custom fields by page template.
As a wordpress developer, I've been using custom fields by post or page (custom post type).
And there are several awesome plugins for that like "Advanced Custom Fields" plugin.

But I noticed that some times custom fields should be managed by page template.
Actually, It was very often in my case for several projects. 
It was more realistic when I maintain the project which other developer developed.

Lets say that client want to customize some pages easily in the backend and he doesn't know HTML well. In this case, we should have client to input the each part of the template simply in some where.

It can be done by widget or post's custom fields.
As a client, Custom fields is better because it is editable in edit page window itself.

With original approach, I had to configure custom fields group for a page and assign it to that page and assign specific page template for that page.

Not good, but we have a simple solution.

Please try to simply configure the custom fields in the template file itself using this plugin and upload that template to the server. Its easy.

This plugin parses the php comment lines starting with '@custom_field' in the wordpress template file, and allow user to input the those configured custom fields for that template in the backend.

It means that it doesn't save any configuration data to database, just config the custom fields in template file itself as how wordpress recognize the templates - Its just wordpress way!

I think that it makes developing and deploying more easy and more sense for the developers. :)

Note: I highly recommend you to install and activate Advanced Custom Fields plugin so as to get its perfect benefit. Field Types only works with Advanced Custom Fields plugin.

= Usage =
Open a template file with any text editor and add some additional templating comment lines starting with @custom_field keyword:

Example 1:
/*
* Template Name: 2column-layout
*
* @custom_field main, type: wysiwyg, label: 'Main content area'
* @custom_field sidebar, type: wysiwyg, label: 'Sidebar area'
*/

Example 2:
/*
* Template Name: Contact Page
*
* @custom_field photo, type: image, label: 'Photo of manager'
* @custom_field phone, type: text
* @custom_field map, type: google_map
* 
* Note: The photo, phone, map are the custom field names in each '@custom_field' line,
* therefore use 'get_post_meta' method with those custom field names to get the values in this template. :)
*/

Please bring the page edit link up in the backend and select the template which you just edited and hit 'Update' or 'Save' button.
After page refreshing, You can't miss new custom fields block from this template file.

Please read my documentation http://forum.webuddysoft.com/blogs/advanced-page-template/53-wordpress-advanced-page-template-guide




== Installation ==

1. Upload 'advanced-page-template' to the '/wp-content/plugins/' directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Add some templating comment lines to a template source code.
4. Specify that template which has templating comment lines to a page and save, then new custom fields block will appear on the bottom.




== Screenshots ==

1. Configuring the Custom Fields in the template file

2. Check custom fields out on the backend




== Changelog ==

= 1.1.0 =
* enabled array options.

= 1.0.0 =
* Advanced Page Template.