=== Payment Gateways Caller for WP e-Commerce ===
Contributors: andrezrv
Tags: wp-e-commerce, merchants, gateway, load
Requires at least: 3.0
Tested up to: 3.8.1
Stable tag: 1.0.1
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Allows to include a merchant file through a GET request without specifying its whole URL.

== Description ==

This WordPress plugin for WP-E-Commerce allows to include a merchant file through a GET request without specifying its whole URL. Just call `http://yoursite.com/?load_merchant=filename`, without the `.php` extension, and you're done.

Please note that these requests cannot be used to display pages.

**Very important:** Though this plugin avoids Local File Inclusion vulnerability, it is not responsible for the processes that are executed inside your gateway files. Before using it, you should be very sure that all your custom gateways are secure and will not perform any unwanted modifications or deletions of sensitive data.

== Installation ==

1. Unzip `wp-e-commerce-merchants-caller.zip` and upload the `wp-e-commerce-merchants-caller` folder to your `/wp-content/plugins/` directory.
2. Activate the plugin through the **"Plugins"** menu in WordPress.

== Changelog ==

= 1.0.1 =
* Fixed bug related to object instance.

= 1.0 =
* Object oriented code.
* Modified action hook for gateway loading from `plugins_loaded` to `init`, so WordPress gets fully loaded before loading the gateway file.
* New `$wpscgc` global object, which allows to get information about the current loaded gateway. 
* New `wpscmc_before_gateway_load` action, for custom functionality before gateway loading.
* New `wpscmc_after_gateway_load` action, for custom functionality after gateway loading.

= 0.1.1 =
**Security fix:** avoids LFI vulnerability.

= 0.1 =
First public release.