#Software 1 : Apache HTTP Server Changelog

Changes with Apache 2.4.27

  *) SECURITY: CVE-2017-9789 (cve.mitre.org)
     mod_http2: Read after free. When under stress, closing many connections,
     the HTTP/2 handling code would sometimes access memory after it has been
     freed, resulting in potentially erratic behaviour.
     [Stefan Eissing]

  *) SECURITY: CVE-2017-9788 (cve.mitre.org)
     mod_auth_digest: Uninitialized memory reflection.  The value placeholder
     in [Proxy-]Authorization headers type 'Digest' was not initialized or
     reset before or between successive key=value assignments.
     [William Rowe]

  *) COMPATIBILITY: mod_lua: Remove the undocumented exported 'apr_table'
     global variable when using Lua 5.2 or later. This was exported as a
     side effect from luaL_register, which is no longer supported as of
     Lua 5.2 which deprecates pollution of the global namespace.
     [Rainer Jung]

  *) COMPATIBILITY: mod_http2: Disable and give warning when using Prefork.
     The server will continue to run, but HTTP/2 will no longer be negotiated.
     [Stefan Eissing]

  *) COMPATIBILITY: mod_proxy_fcgi: Revert to 2.4.20 FCGI behavior for the
     default ProxyFCGIBackendType, fixing a regression with PHP-FPM. PR 61202.
     [Jacob Champion, Jim Jagielski]

  *) mod_lua: Improve compatibility with Lua 5.1, 5.2 and 5.3.
     PR58188, PR60831, PR61245. [Rainer Jung]
  
  *) mod_http2: Simplify ready queue, less memory and better performance. Update
     mod_http2 version to 1.10.7. [Stefan Eissing]
  
  *) Allow single-char field names inadvertently disallowed in 2.4.25.
     PR 61220. [Yann Ylavic]

  *) htpasswd / htdigest: Do not apply the strict permissions of the temporary
     passwd file to a possibly existing passwd file. PR 61240. [Ruediger Pluem]

  *) core: Avoid duplicate HEAD in Allow header.
     This is a regression in 2.4.24 (unreleased), 2.4.25 and 2.4.26.
     PR 61207. [Christophe Jaillet]



  [Apache 2.3.0-dev includes those bug fixes and changes with the
   Apache 2.2.xx tree as documented, and except as noted, below.]

Changes with Apache 2.2.x and later:

  *) http://svn.apache.org/viewvc/httpd/httpd/branches/2.2.x/CHANGES?view=markup

Changes with Apache 2.0.x and later:

  *) http://svn.apache.org/viewvc/httpd/httpd/branches/2.0.x/CHANGES?view=markup

#==================================================================================

#Software 2 : NGINX Changelog stable version (1.12.1)

Changes with nginx 1.12.1                                        11 Jul 2017

    *) Security: a specially crafted request might result in an integer
       overflow and incorrect processing of ranges in the range filter,
       potentially resulting in sensitive information leak (CVE-2017-7529).

#===================================================================================

#Software 3 : WordPress changelog

From the WordPress 4.8.1 release post: WordPress 4.8.1 contains 29 maintenance fixes and enhancements to the 4.8 release series, chief among them are fixes to the rich Text widget and the introduction of the Custom HTML widget.

Administration

#40982 - Permalink Settings: custom structure field keyboard trap
Build/Test Tools

#41327 - Bump Akismet External - 4.9 Edition
Comments

#40975 - 'Empty Spam' and 'Empty Trash' comment buttons not displayed on mobile
Customize

#40978 - Customizer Panel Footer border missing
#40981 - Customizer: Menus: it is far too easy to mistakenly delete a menu because the "Delete Menu" link and the "Add Items" button are too close together
#41158 - Increase tinymce panel z-index
#41410 - Set `'filter' => 'content'` on starter content "business info" widget
Embeds

#41019 - oEmbed: Update VideoPress oEmbed URL
#41048 - `WP_oEmbed_Controller::get_proxy_item()` should remove `_wpnonce` from cached `$args`
#41299 - oEmbed proxy fails to forward maxwidth and maxheight params
General

#41056 - WP-API JS Client: Settings is incorrectly registered as a collection
Media

#41231 - media-views.js: Cannot read .length of undefined (this.controller.$uploaderToggler.length)
REST API

#38964 - Add filter to allow modifying response *after* embedded data is added
#40886 - REST API: PUT requests fail on Nginx servers when fancy permalinks aren't enabled
Taxonomy

#41010 - wp_get_object_terms() returns duplicate terms if more than one taxonomy is given in args
TinyMCE

#41408 - TinyMCE: Images with link and caption look "broken" when selected
Widgets

#40907 - Introduce widget dedicated for HTML code
#40935 - Facebook Video Works On Preview But Not On Theme
#40951 - New Text Widget - Switching Between Visual/Text Editor Strips Out Code
#40960 - Widgets: The Text widget should respect the “Disable the visual editor when writing” setting
#40972 - TinyMCE editor in Text widget does not have RTL contents
#40974 - Updated text widget do not save text (when using paste)
#40977 - Widgets: Query param for `loop` added for non-hosted external videos
#40986 - Widgets: text widget and media widgets cannot be edited in accessibility mode
#41021 - Text widget does not show Title field or TinyMCE editor
#41361 - Text widget can raise JS error if customize-base is enqueued on widgets admin screen
#41386 - Text Widget - Wording - Legacy Mode 4.8.1 beta
#41392 - Theme styles for Text widget do not apply to Custom HTML widget
#41394 - Text widget: Rename legacy mode to visual mode and improve back-compat for widget_text filters
List of Files Revised
wp-admin/css/themes.css
wp-admin/css/widgets.css
wp-admin/includes/class-wp-comments-list-table.php
wp-admin/includes/options.php
wp-admin/js/customize-controls.js
wp-admin/js/customize-nav-menus.js
wp-admin/js/widgets/media-widgets.js
wp-admin/js/widgets/text-widgets.js
wp-includes/class-oembed.php
wp-includes/class-wp-customize-widgets.php
wp-includes/class-wp-editor.php
wp-includes/class-wp-oembed-controller.php
wp-includes/default-widgets.php
wp-includes/js/media-views.js
wp-includes/js/media/views/uploader/inline.js
wp-includes/js/tinymce/plugins/wordpress/plugin.js
wp-includes/js/tinymce/skins/wordpress/wp-content.css
wp-includes/js/wp-api.js
wp-includes/media.php
wp-includes/rest-api.php
wp-includes/rest-api/class-wp-rest-server.php
wp-includes/script-loader.php
wp-includes/taxonomy.php
wp-includes/theme.php
wp-includes/version.php
wp-includes/widgets.php
wp-includes/widgets/class-wp-widget-media-video.php
wp-includes/widgets/class-wp-widget-media.php
wp-includes/widgets/class-wp-widget-text.php
