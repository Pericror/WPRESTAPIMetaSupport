=== REST API Meta Support ===
Contributors: Pericror
Tags: wp-api, rest, meta, plugin
Requires at least: 1.0
Tested up to: 1.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Automatically stores the meta data from the `meta` field of a REST posts or pages POST creation call in the meta data of the page/post.

== Description ==

Compatible with the [wordpress rest api version 2](http://v2.wp-api.org/)

Automatically stores the meta data from the `meta` field of a REST posts ([/wp-json/wp/v2/posts](https://developer.wordpress.org/rest-api/reference/posts/#create-a-post)) or pages POST call ([/wp-json/wp/v2/pages](https://developer.wordpress.org/rest-api/reference/pages/#create-a-page)) in the meta data associated with the created page or post using [update_post_meta](https://developer.wordpress.org/reference/functions/update_post_meta/). The key / value information sent in the REST POST 'meta' object field is stored as both 'key' and '_key' to support different plugin formats.
For example, if trying to set the YOAST SEO Plugin values dynamically when creating a page from the REST API, you would simply add the fields to the meta field
of the REST POST data when you POST the endpoint, and the plugin values will be added to the page:

```
{
...
  meta: {
    yoast_wpseo_title: "Title set from REST call"
    yoast_wpseo_metadesc: "Meta description set from REST call"
  }
...
}
```
Use this plugin when dynamically creating pages with the wordpress REST API to support modifying plugin settings for pages/posts created using the REST API!
Inspired as a broader alternative from https://github.com/ChazUK/wp-api-yoast-meta

== Installation ==

1. Upload the plugin files to the `/wp-content/plugins/rest-api-meta-support` directory, or install the plugin through the 'Plugins' menu in WordPress
2. Activate the plugin through the 'Plugins' menu in WordPress

== Changelog ==

= 1.0 =

- Initial Release
