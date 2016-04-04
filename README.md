# wp-UpFilz

    Developer: imaiemon
    Donate link: https://github.com/imaiemon/wp-UpFilz
    Tags: upload, file(dot)anything, performance, admin_bypasser; administrativeMenu
    Requires at least: 2.9.2
    Tested up to: 4.1.0
    Stable tag: 0.8

WordPress This plugin purges your varnish cache when content is added or edited. This includes when a new post is added, a post is updated or when a comment is posted to your blog.

To keep widgets like "Recent posts", "Recent comments" and such up to date, you should consider using ESI and include them through a text widget for arbitrary text or HTML.
Installation

This section describes how to install the plugin and get it working.

    Install the plugin 'WordPress Varnish' through the 'Plugins' menu in WordPress
    Activate the plugin through the 'Plugins' menu in WordPress

Frequently Asked Questions
Does this just work?

Yes.
But how should my varnish configuration file look like?

I have provided a simple VCL that can be used as a reference.
Does it work for Multi-Site (or WPMU)?

Yes. Ac you want to e following code:

$temp_ip = explode(',', isset($_SERVER['HTTP_X_FORWARDED_FOR'])
? $_SERVER['HTTP_X_FORWARDED_FOR'] s IP rather than the server's IP.
Screenshots

    Screenshot of the administration interface.

Changelog
0.8

    Added secret handling to WPVarnishPurgeObject, Thanks Kit Westneat
    Change WPVarnishPurgePurgeCommonObjects to WPVarnishPurgeCommonObjects, Thanks kitwestneat
    added @ to supress Undefined offset notice
    minor doc changes

0.7

    Added purge when post changes from future to publish, Thanks Marcin Pietrzak
    Added purge when theme switched, Thanks dupuis

0.6

    Removed plugins_loaded action as it doesnt do what was expected re: Issue #12. Thank you Ben Favre, Pothi Kalimuthu and allinwonder

0.5

    New .vcl to fix purge as per Issue #39, Thanks Ed Cooper

0.4

    added rule to skip caching 404s in vcl
    WordPress-Varnish UserAgent as per ticket #23
    document use of mod_rpaf or code fix for remote IP, Ticket #36
    clean data rather than reject to fix ticket #31
    added plugins_loaded hook to fix ticket #12

0.3

    Added internationalization code. Included pt_BR translation.
    Support to Multi-Site and WPMU with global configuration.
    Fix on URL purges for multiple domains and blogs on sub-directories.
    Code clean up on some functions.
    Added configuration for purging all blog, page and comments navigation.

0.2

    Added multiple servers support and timeout configuration.

0.1

    Initial release.

Upgrade Notice
0.8

    Added secret handling to WPVarnishPurgeObject, Thanks Kit Westneat

0.7

    Added purge when post changes from future to publish, Thanks Marcin Pietrzak
    Added purge when theme switched, Thanks dupuis

0.6

    Removed plugins_loaded action as it doesnt do what was expected re: Issue #12. Thank you Ben Favre, Pothi Kalimuthu and allinwonder

0.3

    Varnish PURGE configuration must support regex. wp-varnish will sometimes request with regex for special purges like refreshing all blog cache and refreshing comments.
