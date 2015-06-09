<!--
slug: phalcon-2-released
date: Fri Apr 17 2015 16:02:46 GMT-0400 (EDT)
tags: zephir, php, phalcon, phalcon2
title: Phalcon 2 released!
id: 116664774400
link: http://blog.phalconphp.com/post/116664774400/phalcon-2-released
raw: {"blog_name":"phalconphp","id":116664774400,"post_url":"http://blog.phalconphp.com/post/116664774400/phalcon-2-released","slug":"phalcon-2-released","type":"text","date":"2015-04-17 20:02:46 GMT","timestamp":1429300966,"state":"published","format":"html","reblog_key":"i6M2CduM","tags":["zephir","php","phalcon","phalcon2"],"short_url":"http://tmblr.co/Z6Pumv1ifmoy0","highlighted":[],"note_count":10,"title":"Phalcon 2 released!","body":"<p>The wait is over! Phalcon 2.0 is here!</p>\n<p>After more than a year of development, we&rsquo;re extremely excited to announce the release of Phalcon 2.0 (final).</p>\n\n<p>\nThose that have been following the project closely, know that this has not been a small feat. \n</p><ul><li>We had to create a brand new language <a href=\"http://www.zephir-lang.com\">Zephir</a> which allows developers to write PHP extensions easily.</li>\n\n<li>We had to completely rewrite most of Phalcon 1.3.x, offering the same functionality as before so as to ensure that upgrading will be very easy.</li>\n\n<li>Zephir had to be adjusted and enhanced as we moved through the rewrite, offering more functions and options to developers.</li>\n<li>Additional features were implemented for 2.0, mostly thanks to our contributors!</li>\n</ul>\nThe results are something that we are very proud of:\n<ul><li>Phalcon 2.0, offering compatible functionality (and more) as before</li>\n<li>Zephir, allowing developers to write their own extensions easily without the need to know C.</li>\n</ul><h3>Installation</h3>\n<p>This version can be installed from the master branch, if you don’t have Zephir installed follow these instructions:</p>\n\n<pre class=\"sh_sh sh_sourceCode\">\ngit clone <a href=\"http://github.com/phalcon/cphalcon\">http://github.com/phalcon/cphalcon</a>\ngit checkout master\ncd ext\nsudo ./install\n</pre>\n\n<p>The standard installation method also works:</p>\n\n<pre class=\"sh_sh sh_sourceCode\">\ngit clone <a href=\"http://github.com/phalcon/cphalcon\">http://github.com/phalcon/cphalcon</a>\ngit checkout master\ncd build\nsudo ./install\n</pre>\n\n<p>If you have Zephir installed:</p>\n\n<pre class=\"sh_sh sh_sourceCode\">\ngit clone <a href=\"http://github.com/phalcon/cphalcon\">http://github.com/phalcon/cphalcon</a>\ngit checkout master\nzephir fullclean\nzephir build\n</pre>\n\n<p>Note that running the installation script will replace any version of Phalcon installed before.</p>\n\n<p>Windows DLLs are available in the <a href=\"http://phalconphp.com/en/download/windows\">download page</a>.</p>\n\n<p>See the <a href=\"http://blog.phalconphp.com/post/115773676765/guide-upgrading-to-phalcon-2\">upgrading guide</a> for more information about installing and updating to Phalcon 2.</p>\n\n<h3>What’s next</h3>\n<p>\nOur release schedule will be every one or two months (unless we need to issue a security fix, which will be near instant). \nThe target will be the most requested features by the community, although with Zephir, contributing to Phalcon will be a breeze. \nWe can&rsquo;t wait to see those pull requests coming in :)\n</p>\n<p>\nSmaller changes and fixes that can be bundled in a minor version will be released as soon as we can. We will also be working on \na LTS (Long Term Support) model for our community.\n</p>\n<p>\nFinally we are going to start the research on PHP 7, so that we can adjust Zephir accordingly and of course Phalcon. This \ntask will require a lot of preparation and work but we have our targets set on it due to the new functionality and features it offers.\n</p>\n\n<h3>Conclusion and acknowledgments</h3>\n<p>\nWe are super excited about this release and are looking forward to the future. A big thank you to all the contributors and donors! \nWe could not have done this without you. And of course, we would like to thank everyone that tested the alpha, betas and release candidates and finding, filing issues and providing feedback. \nWe really hope you enjoy this release.\n</p>\n<p>We would like to express our deep gratitude for tremendous efforts migrating and testing the code in this version, specially to:</p>\n\n<ul><li><a href=\"https://github.com/andresgutierrez\">Andres Gutierrez</a></li>\n <li><a href=\"https://github.com/niden\">Nikolaos Dimopoulos</a></li>\n <li><a href=\"https://github.com/sjinks\">Vladimir Kolesnikov</a></li> \n <li><a href=\"https://github.com/carvajaldiazeduar\">Eduar Carvajal</a></li>\n <li><a href=\"https://github.com/dreamsxin\">Dreamszhu</a></li>\n <li><a href=\"https://github.com/ovr\">Dmitry Patsura</a></li>\n <li><a href=\"https://github.com/quantum13\">Vladimir Khramov</a></li>\n <li><a href=\"https://github.com/WooDzu\">Piotr Gasiorowski</a></li> \n <li><a href=\"https://github.com/olivier-monaco\">Olivier Monaco</a></li> \n <li><a href=\"https://github.com/SidRoberts\">Sid Roberts</a></li> \n <li><a href=\"https://github.com/akaNightmare\">Ivan Zubok</a></li>  \n <li><a href=\"https://github.com/maxgalbu\">Max Galbusera</a></li>  \n <li><a href=\"https://github.com/dugwood\">Yvan Taviaud</a></li>  \n <li><a href=\"https://github.com/rianorie\">Rian Orie</a></li>  \n <li><a href=\"https://github.com/brainformatik\">Brainformatik GmbH</a></li>  \n <li><a href=\"https://github.com/mruz\">Mariusz Łączak</a></li>  \n <li><a href=\"https://github.com/xboston\">Nikolay Kirsh</a></li>  \n <li><a href=\"https://github.com/Cinderella-Man\">Kamil Skowron</a></li>  \n <li><a href=\"https://github.com/sergeyklay\">Serghei Iakovlev</a></li>\n <li><a href=\"https://github.com/rlaffers\">Richard Laffers</a></li>\n <li><a href=\"https://github.com/endeveit\">Nikita Vershinin</a></li>\n <li><a href=\"https://github.com/ogarbe\">Olivier Garbé</a></li>\n <li><a href=\"https://github.com/fogcity\">Robert Smolarek</a></li>\n <li><a href=\"https://github.com/zyxep\">Simon Karberg</a></li>\n <li><a href=\"https://github.com/souf\">Soufiane Ghzal</a></li>\n <li><a href=\"https://github.com/kenjis\">Kenji Suzuki</a></li>\n <li><a href=\"https://github.com/Green-Cat\">Vladimir Metelitsa</a></li>\n <li><a href=\"https://github.com/cvsguimaraes\">Carlos Guimaraes</a></li>\n</ul><p>Thanks again to all!<br/>\nEnjoy Phalcon 2 &lt;3</p>","reblog":{"tree_html":"","comment":"<p>The wait is over! Phalcon 2.0 is here!</p>\n<p>After more than a year of development, we&rsquo;re extremely excited to announce the release of Phalcon 2.0 (final).</p>\n\n<p>\nThose that have been following the project closely, know that this has not been a small feat. \n</p><ul><li>We had to create a brand new language <a href=\"http://www.zephir-lang.com\">Zephir</a> which allows developers to write PHP extensions easily.</li>\n\n<li>We had to completely rewrite most of Phalcon 1.3.x, offering the same functionality as before so as to ensure that upgrading will be very easy.</li>\n\n<li>Zephir had to be adjusted and enhanced as we moved through the rewrite, offering more functions and options to developers.</li>\n<li>Additional features were implemented for 2.0, mostly thanks to our contributors!</li>\n</ul>\nThe results are something that we are very proud of:\n<ul><li>Phalcon 2.0, offering compatible functionality (and more) as before</li>\n<li>Zephir, allowing developers to write their own extensions easily without the need to know C.</li>\n</ul><h3>Installation</h3>\n<p>This version can be installed from the master branch, if you don&rsquo;t have Zephir installed follow these instructions:</p>\n\n<pre class=\"sh_sh sh_sourceCode\">\ngit clone <a href=\"http://github.com/phalcon/cphalcon\">http://github.com/phalcon/cphalcon</a>\ngit checkout master\ncd ext\nsudo ./install\n</pre>\n\n<p>The standard installation method also works:</p>\n\n<pre class=\"sh_sh sh_sourceCode\">\ngit clone <a href=\"http://github.com/phalcon/cphalcon\">http://github.com/phalcon/cphalcon</a>\ngit checkout master\ncd build\nsudo ./install\n</pre>\n\n<p>If you have Zephir installed:</p>\n\n<pre class=\"sh_sh sh_sourceCode\">\ngit clone <a href=\"http://github.com/phalcon/cphalcon\">http://github.com/phalcon/cphalcon</a>\ngit checkout master\nzephir fullclean\nzephir build\n</pre>\n\n<p>Note that running the installation script will replace any version of Phalcon installed before.</p>\n\n<p>Windows DLLs are available in the <a href=\"http://phalconphp.com/en/download/windows\">download page</a>.</p>\n\n<p>See the <a href=\"http://blog.phalconphp.com/post/115773676765/guide-upgrading-to-phalcon-2\">upgrading guide</a> for more information about installing and updating to Phalcon 2.</p>\n\n<h3>What&rsquo;s next</h3>\n<p>\nOur release schedule will be every one or two months (unless we need to issue a security fix, which will be near instant). \nThe target will be the most requested features by the community, although with Zephir, contributing to Phalcon will be a breeze. \nWe can&rsquo;t wait to see those pull requests coming in :)\n</p>\n<p>\nSmaller changes and fixes that can be bundled in a minor version will be released as soon as we can. We will also be working on \na LTS (Long Term Support) model for our community.\n</p>\n<p>\nFinally we are going to start the research on PHP 7, so that we can adjust Zephir accordingly and of course Phalcon. This \ntask will require a lot of preparation and work but we have our targets set on it due to the new functionality and features it offers.\n</p>\n\n<h3>Conclusion and acknowledgments</h3>\n<p>\nWe are super excited about this release and are looking forward to the future. A big thank you to all the contributors and donors! \nWe could not have done this without you. And of course, we would like to thank everyone that tested the alpha, betas and release candidates and finding, filing issues and providing feedback. \nWe really hope you enjoy this release.\n</p>\n<p>We would like to express our deep gratitude for tremendous efforts migrating and testing the code in this version, specially to:</p>\n\n<ul><li><a href=\"https://github.com/andresgutierrez\">Andres Gutierrez</a></li>\n <li><a href=\"https://github.com/niden\">Nikolaos Dimopoulos</a></li>\n <li><a href=\"https://github.com/sjinks\">Vladimir Kolesnikov</a></li> \n <li><a href=\"https://github.com/carvajaldiazeduar\">Eduar Carvajal</a></li>\n <li><a href=\"https://github.com/dreamsxin\">Dreamszhu</a></li>\n <li><a href=\"https://github.com/ovr\">Dmitry Patsura</a></li>\n <li><a href=\"https://github.com/quantum13\">Vladimir Khramov</a></li>\n <li><a href=\"https://github.com/WooDzu\">Piotr Gasiorowski</a></li> \n <li><a href=\"https://github.com/olivier-monaco\">Olivier Monaco</a></li> \n <li><a href=\"https://github.com/SidRoberts\">Sid Roberts</a></li> \n <li><a href=\"https://github.com/akaNightmare\">Ivan Zubok</a></li>  \n <li><a href=\"https://github.com/maxgalbu\">Max Galbusera</a></li>  \n <li><a href=\"https://github.com/dugwood\">Yvan Taviaud</a></li>  \n <li><a href=\"https://github.com/rianorie\">Rian Orie</a></li>  \n <li><a href=\"https://github.com/brainformatik\">Brainformatik GmbH</a></li>  \n <li><a href=\"https://github.com/mruz\">Mariusz &#321;&#261;czak</a></li>  \n <li><a href=\"https://github.com/xboston\">Nikolay Kirsh</a></li>  \n <li><a href=\"https://github.com/Cinderella-Man\">Kamil Skowron</a></li>  \n <li><a href=\"https://github.com/sergeyklay\">Serghei Iakovlev</a></li>\n <li><a href=\"https://github.com/rlaffers\">Richard Laffers</a></li>\n <li><a href=\"https://github.com/endeveit\">Nikita Vershinin</a></li>\n <li><a href=\"https://github.com/ogarbe\">Olivier Garb&eacute;</a></li>\n <li><a href=\"https://github.com/fogcity\">Robert Smolarek</a></li>\n <li><a href=\"https://github.com/zyxep\">Simon Karberg</a></li>\n <li><a href=\"https://github.com/souf\">Soufiane Ghzal</a></li>\n <li><a href=\"https://github.com/kenjis\">Kenji Suzuki</a></li>\n <li><a href=\"https://github.com/Green-Cat\">Vladimir Metelitsa</a></li>\n <li><a href=\"https://github.com/cvsguimaraes\">Carlos Guimaraes</a></li>\n</ul><p>Thanks again to all!<br>\nEnjoy Phalcon 2 &lt;3</p>"},"trail":[{"blog":{"name":"phalconphp","theme":{"header_full_width":1117,"header_full_height":426,"header_focus_width":758,"header_focus_height":426,"avatar_shape":"square","background_color":"#FAFAFA","body_font":"Helvetica Neue","header_bounds":"0,937,426,179","header_image":"http://static.tumblr.com/be2b0380984b972b47699d457f4c0ffb/ivjir8a/815nn0qo7/tumblr_static_28z87js742xwowwo0kco04ogs.jpg","header_image_focused":"http://static.tumblr.com/be2b0380984b972b47699d457f4c0ffb/ivjir8a/laHnn0qo9/tumblr_static_tumblr_static_28z87js742xwowwo0kco04ogs_focused_v3.jpg","header_image_scaled":"http://static.tumblr.com/be2b0380984b972b47699d457f4c0ffb/ivjir8a/815nn0qo7/tumblr_static_28z87js742xwowwo0kco04ogs_2048_v2.jpg","header_stretch":true,"link_color":"#529ECC","show_avatar":true,"show_description":true,"show_header_image":true,"show_title":true,"title_color":"#444444","title_font":"Gibson","title_font_weight":"bold"}},"post":{"id":"116664774400"},"content":"<p>The wait is over! Phalcon 2.0 is here!</p>\n<p>After more than a year of development, we’re extremely excited to announce the release of Phalcon 2.0 (final).</p>\n\n<p>\nThose that have been following the project closely, know that this has not been a small feat. \n</p><ul><li>We had to create a brand new language <a href=\"http://www.zephir-lang.com\">Zephir</a> which allows developers to write PHP extensions easily.</li>\n\n<li>We had to completely rewrite most of Phalcon 1.3.x, offering the same functionality as before so as to ensure that upgrading will be very easy.</li>\n\n<li>Zephir had to be adjusted and enhanced as we moved through the rewrite, offering more functions and options to developers.</li>\n<li>Additional features were implemented for 2.0, mostly thanks to our contributors!</li>\n</ul>\nThe results are something that we are very proud of:\n<ul><li>Phalcon 2.0, offering compatible functionality (and more) as before</li>\n<li>Zephir, allowing developers to write their own extensions easily without the need to know C.</li>\n</ul><h3>Installation</h3>\n<p>This version can be installed from the master branch, if you don’t have Zephir installed follow these instructions:</p>\n\n<pre class=\"sh_sh sh_sourceCode\">\ngit clone <a href=\"http://github.com/phalcon/cphalcon\">http://github.com/phalcon/cphalcon</a>\ngit checkout master\ncd ext\nsudo ./install\n</pre>\n\n<p>The standard installation method also works:</p>\n\n<pre class=\"sh_sh sh_sourceCode\">\ngit clone <a href=\"http://github.com/phalcon/cphalcon\">http://github.com/phalcon/cphalcon</a>\ngit checkout master\ncd build\nsudo ./install\n</pre>\n\n<p>If you have Zephir installed:</p>\n\n<pre class=\"sh_sh sh_sourceCode\">\ngit clone <a href=\"http://github.com/phalcon/cphalcon\">http://github.com/phalcon/cphalcon</a>\ngit checkout master\nzephir fullclean\nzephir build\n</pre>\n\n<p>Note that running the installation script will replace any version of Phalcon installed before.</p>\n\n<p>Windows DLLs are available in the <a href=\"http://phalconphp.com/en/download/windows\">download page</a>.</p>\n\n<p>See the <a href=\"http://blog.phalconphp.com/post/115773676765/guide-upgrading-to-phalcon-2\">upgrading guide</a> for more information about installing and updating to Phalcon 2.</p>\n\n<h3>What’s next</h3>\n<p>\nOur release schedule will be every one or two months (unless we need to issue a security fix, which will be near instant). \nThe target will be the most requested features by the community, although with Zephir, contributing to Phalcon will be a breeze. \nWe can’t wait to see those pull requests coming in :)\n</p>\n<p>\nSmaller changes and fixes that can be bundled in a minor version will be released as soon as we can. We will also be working on \na LTS (Long Term Support) model for our community.\n</p>\n<p>\nFinally we are going to start the research on PHP 7, so that we can adjust Zephir accordingly and of course Phalcon. This \ntask will require a lot of preparation and work but we have our targets set on it due to the new functionality and features it offers.\n</p>\n\n<h3>Conclusion and acknowledgments</h3>\n<p>\nWe are super excited about this release and are looking forward to the future. A big thank you to all the contributors and donors! \nWe could not have done this without you. And of course, we would like to thank everyone that tested the alpha, betas and release candidates and finding, filing issues and providing feedback. \nWe really hope you enjoy this release.\n</p>\n<p>We would like to express our deep gratitude for tremendous efforts migrating and testing the code in this version, specially to:</p>\n\n<ul><li><a href=\"https://github.com/andresgutierrez\">Andres Gutierrez</a></li>\n <li><a href=\"https://github.com/niden\">Nikolaos Dimopoulos</a></li>\n <li><a href=\"https://github.com/sjinks\">Vladimir Kolesnikov</a></li> \n <li><a href=\"https://github.com/carvajaldiazeduar\">Eduar Carvajal</a></li>\n <li><a href=\"https://github.com/dreamsxin\">Dreamszhu</a></li>\n <li><a href=\"https://github.com/ovr\">Dmitry Patsura</a></li>\n <li><a href=\"https://github.com/quantum13\">Vladimir Khramov</a></li>\n <li><a href=\"https://github.com/WooDzu\">Piotr Gasiorowski</a></li> \n <li><a href=\"https://github.com/olivier-monaco\">Olivier Monaco</a></li> \n <li><a href=\"https://github.com/SidRoberts\">Sid Roberts</a></li> \n <li><a href=\"https://github.com/akaNightmare\">Ivan Zubok</a></li>  \n <li><a href=\"https://github.com/maxgalbu\">Max Galbusera</a></li>  \n <li><a href=\"https://github.com/dugwood\">Yvan Taviaud</a></li>  \n <li><a href=\"https://github.com/rianorie\">Rian Orie</a></li>  \n <li><a href=\"https://github.com/brainformatik\">Brainformatik GmbH</a></li>  \n <li><a href=\"https://github.com/mruz\">Mariusz Łączak</a></li>  \n <li><a href=\"https://github.com/xboston\">Nikolay Kirsh</a></li>  \n <li><a href=\"https://github.com/Cinderella-Man\">Kamil Skowron</a></li>  \n <li><a href=\"https://github.com/sergeyklay\">Serghei Iakovlev</a></li>\n <li><a href=\"https://github.com/rlaffers\">Richard Laffers</a></li>\n <li><a href=\"https://github.com/endeveit\">Nikita Vershinin</a></li>\n <li><a href=\"https://github.com/ogarbe\">Olivier Garbé</a></li>\n <li><a href=\"https://github.com/fogcity\">Robert Smolarek</a></li>\n <li><a href=\"https://github.com/zyxep\">Simon Karberg</a></li>\n <li><a href=\"https://github.com/souf\">Soufiane Ghzal</a></li>\n <li><a href=\"https://github.com/kenjis\">Kenji Suzuki</a></li>\n <li><a href=\"https://github.com/Green-Cat\">Vladimir Metelitsa</a></li>\n <li><a href=\"https://github.com/cvsguimaraes\">Carlos Guimaraes</a></li>\n</ul><p>Thanks again to all!<br>\nEnjoy Phalcon 2 <3</p>","content_raw":"<p>The wait is over! Phalcon 2.0 is here!</p>\n<p>After more than a year of development, we're extremely excited to announce the release of Phalcon 2.0 (final).</p>\n\n<p>\nThose that have been following the project closely, know that this has not been a small feat. \n</p><ul><li>We had to create a brand new language <a href=\"http://www.zephir-lang.com\">Zephir</a> which allows developers to write PHP extensions easily.</li>\n\n<li>We had to completely rewrite most of Phalcon 1.3.x, offering the same functionality as before so as to ensure that upgrading will be very easy.</li>\n\n<li>Zephir had to be adjusted and enhanced as we moved through the rewrite, offering more functions and options to developers.</li>\n<li>Additional features were implemented for 2.0, mostly thanks to our contributors!</li>\n</ul>\nThe results are something that we are very proud of:\n<ul><li>Phalcon 2.0, offering compatible functionality (and more) as before</li>\n<li>Zephir, allowing developers to write their own extensions easily without the need to know C.</li>\n</ul><h3>Installation</h3>\n<p>\n</p><p>This version can be installed from the master branch, if you don&rsquo;t have Zephir installed follow these instructions:</p>\n\n<pre class=\"sh_sh sh_sourceCode\">\ngit clone http://github.com/phalcon/cphalcon\ngit checkout master\ncd ext\nsudo ./install\n</pre>\n\n<p>The standard installation method also works:</p>\n\n<pre class=\"sh_sh sh_sourceCode\">\ngit clone http://github.com/phalcon/cphalcon\ngit checkout master\ncd build\nsudo ./install\n</pre>\n\n<p>If you have Zephir installed:</p>\n\n<pre class=\"sh_sh sh_sourceCode\">\ngit clone http://github.com/phalcon/cphalcon\ngit checkout master\nzephir fullclean\nzephir build\n</pre>\n\n<p>Note that running the installation script will replace any version of Phalcon installed before.</p>\n\n<p>Windows DLLs are available in the <a href=\"http://phalconphp.com/en/download/windows\">download page</a>.</p>\n\n<p>See the <a href=\"http://blog.phalconphp.com/post/115773676765/guide-upgrading-to-phalcon-2\">upgrading guide</a> for more information about installing and updating to Phalcon 2.</p>\n\n<h3>What&rsquo;s next</h3>\n<p>\nOur release schedule will be every one or two months (unless we need to issue a security fix, which will be near instant). \nThe target will be the most requested features by the community, although with Zephir, contributing to Phalcon will be a breeze. \nWe can't wait to see those pull requests coming in :)\n</p>\n<p>\nSmaller changes and fixes that can be bundled in a minor version will be released as soon as we can. We will also be working on \na LTS (Long Term Support) model for our community.\n</p>\n<p>\nFinally we are going to start the research on PHP 7, so that we can adjust Zephir accordingly and of course Phalcon. This \ntask will require a lot of preparation and work but we have our targets set on it due to the new functionality and features it offers.\n</p>\n\n<h3>Conclusion and acknowledgments</h3>\n<p>\nWe are super excited about this release and are looking forward to the future. A big thank you to all the contributors and donors! \nWe could not have done this without you. And of course, we would like to thank everyone that tested the alpha, betas and release candidates and finding, filing issues and providing feedback. \nWe really hope you enjoy this release.\n</p>\n<p>We would like to express our deep gratitude for tremendous efforts migrating and testing the code in this version, specially to:</p>\n\n<ul><li><a href=\"https://github.com/andresgutierrez\">Andres Gutierrez</a></li>\n <li><a href=\"https://github.com/niden\">Nikolaos Dimopoulos</a></li>\n <li><a href=\"https://github.com/sjinks\">Vladimir Kolesnikov</a></li> \n <li><a href=\"https://github.com/carvajaldiazeduar\">Eduar Carvajal</a></li>\n <li><a href=\"https://github.com/dreamsxin\">Dreamszhu</a></li>\n <li><a href=\"https://github.com/ovr\">Dmitry Patsura</a></li>\n <li><a href=\"https://github.com/quantum13\">Vladimir Khramov</a></li>\n <li><a href=\"https://github.com/WooDzu\">Piotr Gasiorowski</a></li> \n <li><a href=\"https://github.com/olivier-monaco\">Olivier Monaco</a></li> \n <li><a href=\"https://github.com/SidRoberts\">Sid Roberts</a></li> \n <li><a href=\"https://github.com/akaNightmare\">Ivan Zubok</a></li>  \n <li><a href=\"https://github.com/maxgalbu\">Max Galbusera</a></li>  \n <li><a href=\"https://github.com/dugwood\">Yvan Taviaud</a></li>  \n <li><a href=\"https://github.com/rianorie\">Rian Orie</a></li>  \n <li><a href=\"https://github.com/brainformatik\">Brainformatik GmbH</a></li>  \n <li><a href=\"https://github.com/mruz\">Mariusz &#321;&#261;czak</a></li>  \n <li><a href=\"https://github.com/xboston\">Nikolay Kirsh</a></li>  \n <li><a href=\"https://github.com/Cinderella-Man\">Kamil Skowron</a></li>  \n <li><a href=\"https://github.com/sergeyklay\">Serghei Iakovlev</a></li>\n <li><a href=\"https://github.com/rlaffers\">Richard Laffers</a></li>\n <li><a href=\"https://github.com/endeveit\">Nikita Vershinin</a></li>\n <li><a href=\"https://github.com/ogarbe\">Olivier Garb&eacute;</a></li>\n <li><a href=\"https://github.com/fogcity\">Robert Smolarek</a></li>\n <li><a href=\"https://github.com/zyxep\">Simon Karberg</a></li>\n <li><a href=\"https://github.com/souf\">Soufiane Ghzal</a></li>\n <li><a href=\"https://github.com/kenjis\">Kenji Suzuki</a></li>\n <li><a href=\"https://github.com/Green-Cat\">Vladimir Metelitsa</a></li>\n <li><a href=\"https://github.com/cvsguimaraes\">Carlos Guimaraes</a></li>\n</ul><p>Thanks again to all!<br>\nEnjoy Phalcon 2 &lt;3</p>","is_current_item":true,"is_root_item":true}]}
publish: 2015-04-017
-->


Phalcon 2 released!
===================

The wait is over! Phalcon 2.0 is here!

After more than a year of development, we’re extremely excited to
announce the release of Phalcon 2.0 (final).

Those that have been following the project closely, know that this has
not been a small feat.

-   We had to create a brand new language
    [Zephir](http://www.zephir-lang.com) which allows developers to
    write PHP extensions easily.
-   We had to completely rewrite most of Phalcon 1.3.x, offering the
    same functionality as before so as to ensure that upgrading will be
    very easy.
-   Zephir had to be adjusted and enhanced as we moved through the
    rewrite, offering more functions and options to developers.
-   Additional features were implemented for 2.0, mostly thanks to our
    contributors!

The results are something that we are very proud of:

-   Phalcon 2.0, offering compatible functionality (and more) as before
-   Zephir, allowing developers to write their own extensions easily
    without the need to know C.

### Installation

This version can be installed from the master branch, if you don’t have
Zephir installed follow these instructions:

~~~~ {.sh_sh .sh_sourceCode}
git clone http://github.com/phalcon/cphalcon
git checkout master
cd ext
sudo ./install
~~~~

The standard installation method also works:

~~~~ {.sh_sh .sh_sourceCode}
git clone http://github.com/phalcon/cphalcon
git checkout master
cd build
sudo ./install
~~~~

If you have Zephir installed:

~~~~ {.sh_sh .sh_sourceCode}
git clone http://github.com/phalcon/cphalcon
git checkout master
zephir fullclean
zephir build
~~~~

Note that running the installation script will replace any version of
Phalcon installed before.

Windows DLLs are available in the [download
page](http://phalconphp.com/en/download/windows).

See the [upgrading
guide](http://blog.phalconphp.com/post/115773676765/guide-upgrading-to-phalcon-2)
for more information about installing and updating to Phalcon 2.

### What’s next

Our release schedule will be every one or two months (unless we need to
issue a security fix, which will be near instant). The target will be
the most requested features by the community, although with Zephir,
contributing to Phalcon will be a breeze. We can’t wait to see those
pull requests coming in :)

Smaller changes and fixes that can be bundled in a minor version will be
released as soon as we can. We will also be working on a LTS (Long Term
Support) model for our community.

Finally we are going to start the research on PHP 7, so that we can
adjust Zephir accordingly and of course Phalcon. This task will require
a lot of preparation and work but we have our targets set on it due to
the new functionality and features it offers.

### Conclusion and acknowledgments

We are super excited about this release and are looking forward to the
future. A big thank you to all the contributors and donors! We could not
have done this without you. And of course, we would like to thank
everyone that tested the alpha, betas and release candidates and
finding, filing issues and providing feedback. We really hope you enjoy
this release.

We would like to express our deep gratitude for tremendous efforts
migrating and testing the code in this version, specially to:

-   [Andres Gutierrez](https://github.com/andresgutierrez)
-   [Nikolaos Dimopoulos](https://github.com/niden)
-   [Vladimir Kolesnikov](https://github.com/sjinks)
-   [Eduar Carvajal](https://github.com/carvajaldiazeduar)
-   [Dreamszhu](https://github.com/dreamsxin)
-   [Dmitry Patsura](https://github.com/ovr)
-   [Vladimir Khramov](https://github.com/quantum13)
-   [Piotr Gasiorowski](https://github.com/WooDzu)
-   [Olivier Monaco](https://github.com/olivier-monaco)
-   [Sid Roberts](https://github.com/SidRoberts)
-   [Ivan Zubok](https://github.com/akaNightmare)
-   [Max Galbusera](https://github.com/maxgalbu)
-   [Yvan Taviaud](https://github.com/dugwood)
-   [Rian Orie](https://github.com/rianorie)
-   [Brainformatik GmbH](https://github.com/brainformatik)
-   [Mariusz Łączak](https://github.com/mruz)
-   [Nikolay Kirsh](https://github.com/xboston)
-   [Kamil Skowron](https://github.com/Cinderella-Man)
-   [Serghei Iakovlev](https://github.com/sergeyklay)
-   [Richard Laffers](https://github.com/rlaffers)
-   [Nikita Vershinin](https://github.com/endeveit)
-   [Olivier Garbé](https://github.com/ogarbe)
-   [Robert Smolarek](https://github.com/fogcity)
-   [Simon Karberg](https://github.com/zyxep)
-   [Soufiane Ghzal](https://github.com/souf)
-   [Kenji Suzuki](https://github.com/kenjis)
-   [Vladimir Metelitsa](https://github.com/Green-Cat)
-   [Carlos Guimaraes](https://github.com/cvsguimaraes)

Thanks again to all!\
 Enjoy Phalcon 2 \<3
