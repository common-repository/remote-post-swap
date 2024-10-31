=== Remote Post Swap ===
Contributors: TyB
Tags: remote, database, posts, swap, post swap, remote database, wp-api, rest api, api
Requires at least: 4.7.0
Tested up to: 4.7.3
Stable tag: 0.8.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Swap local development post data out with live/remote post data on the fly

== Description ==
This plugin was built for developers to swap out local post data with post data from a live site. Useful if you need to make some styling changes to post content but don't want to pull in the live database. Simply enter the URL for the live site and turn on the API connection via the toggle provided.

All posts within the loop are replaced with posts from the URL you entered. This will change out the post title, post content, post excerpt and post date with the returned API data. This plugin will **NOT** replace your the post data in the database, but simply change out the data on the fly. To go back to your the posts saved locally simply uncheck the toggle switch on the settings page.

Post meta is used to store post IDs returned from the API call and matched up with the post IDs returned from your loop. This helps keep posts consistent across page loads. Single post pages will return the same post they were swapped out with in the main loop.

**NOTE:** This plugin requires the parent site (the live site) to be running at least WordPress Version 4.7.0 for the REST API to work properly.

== Installation ==

1. Upload the `remote-post-swap` directory to your `/wp-content/plugins/` directory.
2. Activate the plugin.

== Usage ==
1. After plugin activation go to the plugin settings page by hovering over the "Settings" menu item in wp-admin.
2. Click on the 'Remote Post Swap' link.
3. Check the toggle box shown.
4. Enter the URL to the live site you wish to pull posts from. This should be a valid URL.
5. Turn on which post data you wish to replace (Post Title, Post Excerpt, Post Content, Post Date, Featured Images)

== To Do ==
1. Pull in author data.
2. Pull in post comments.

== Changelog ==

= 0.8.0 =
* Major performance enhancements & code optimization

= 0.7.0 =
* Add in the ability to allow plugin users to choose which post data is swapped with remote post data (options page)
* Rewrite the admin classes to allow for separation of logic/display
* Add psr4 autoloader to autoload PHP classes without using require/include
* Separate the featured image functions from the replace-wp functions for better organization

= 0.6.0 =
* Re-wrote the replace-wp class to only make a maximum of 2 API calls per loop. (Performance enhancement)

= 0.5.0 =
* Initial Release
