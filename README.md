correcthorse.php
=========

A role for installing php.

Role Variables
--------------

| Variable                              | Default				| Notes					|
| :---                                  | :---                          	| :---					|
| php_base_name				| php					| php, php73, etc		|
| php_version				| 7.2					|					|
| php_mod_php   | false         | This will only get used with a prefork apache |
| php_fpm				| true					|					|
| php_fpm_user				| apache				|					|
| php_fpm_group				| apache				|					|
| php_fpm_proxy_timeout			| 30					| timeout for mod_proxy_fcgi handler	|
| php_fpm_logrotate_period		| weekly				| daily, weekly, monthly     		|
| php_fpm_logrotate_keep		| 5					| number of rotations to keep		|
| php_fpm_logrotate_compress		| false					| compress logs if true	 		|
| php_fpm_pm				| dynamic				| dynamic|static   			|
| php_fpm_max_children			| 50					| max children for dynamic or total children for static |
| php_fpm_start_servers			| 5					|     	       	   	      	    	|
| php_fpm_min_spare_servers		| 5					|					|
| php_fpm_max_spare_servers		| 35					|					|
| php_fpm_max_requests			| 0					| 0 is unlimited			|
| php_timezone				| America/New_York			|					|
| php_upload_max			| 30M					|					|
| php_post_max				| 30M					|					|
| php_html_errors			| "Off"					|					|
| php_memory_limit			| 256M					|					|
| php_expose_php			| "Off"					|					|
| php_max_execution_time		| 120					|					|
| php_error_reporting			| "E_ALL & ~E_DEPRECATED & ~E_STRICT"	|					|
| php_display_errors			| "Off"	   		   		|					|
| php_display_startup_errors		| "Off"					|					|
| php_realpath_cache_size		| 16k					|					|
| php_realpath_cache_ttl		| 120					|					|
| php_max_input_vars			| 1000					|					|
| php_short_open_tag			| Off					|					|
| php_composer				| true					|					|
| php_composer_autoupdate		| true					|					|
| php_codeception			| true					|					|
| php_codeception_autoupdate		| true					|					|

Dependencies
------------

TODO

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: correcthorse.php }

License
-------

MIT

Author Information
------------------

* [Joshua Rusch](https://correct.horse/)
