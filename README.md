# What is LucidFrame?

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/cithukyaw/LucidFrame?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

PHPLucidFrame (a.k.a LucidFrame) is a mini application development framework - a toolkit for PHP developers. It provides logical structure and several helper utilities for web application development.
It uses a functional architecture to simplify complex application development. LucidFrame is especially designed for PHP, MySQL and Apache. It is simple, fast, lightweight and easy to install.

Almost zero configuration - just configure your database setting and you are ready to go. No complex JSON, XML, YAML or vHost configuration.

No template engine to eliminate overhead of template processing and to save your storage from template cache files.

Although it is stated as mini framework, it supports a wide range of web application development features:

- Datatase access API
- Security control
- URL routing
- Validation helpers
- Internationalization & Localization
- User authentication & authorization API
- Ajax

## Prerequisites

- Web Server (Apache with `mod_rewrite` enabled)
- PHP version 5.2.0 or newer (optional `mcrypt` extension enabled, but recommended)
- MySQL 5.0 or newer with MySQLi enabled.

## Installation

- Extract [the downloaded archive](https://github.com/cithukyaw/LucidFrame/releases/latest) in your local webserver document root, and you will get a folder named **LucidFrame-x.y.z** where **x.y.z** would be your downloaded version.
- Rename it as **LucidFrame** or your project name.
- Copy `/inc/config.default.php` and rename it to `/inc/config.php`
- Copy `/inc/site.config.default.php` and rename it to `/inc/site.config.php`.
- (Optional, but recommended) Copy `/inc/tpl/head.php` to `/app/inc/tpl/head.php` if you want to update it.
- Check `http://localhost/LucidFrame` or `http://localhost/YourProjectName` in your browser.

**Note:** If you have your own project folder name other than **LucidFrame**, you should change `$lc_baseURL` in `/inc/config.php` in accordance with your project name.

## Using Composer

You can also install LucidFrame using [Composer](http://getcomposer.org/).

    composer require lucidframe/phplucidframe:~1.5.0

OR

    php composer.phar require lucidframe/phplucidframe:~1.5.0

## Furthermore on Installation

**URL Rewrite** : Make sure you have `mod_rewrite` activated on your server / in your environment.
Some guidelines:

- [XAMPP for Windows](http://www.leonardaustin.com/blog/technical/enable-mod_rewrite-in-xampp/)
- [Ubuntu 14.04 LTS](http://www.dev-metal.com/enable-mod_rewrite-ubuntu-14-04-lts/)
- [Ubuntu 12.04 LTS](http://www.dev-metal.com/enable-mod_rewrite-ubuntu-12-04-lts/)
- [EasyPHP on Windows](http://stackoverflow.com/questions/8158770/easyphp-and-htaccess)
- [AMPPS on Windows/Mac OS](http://www.softaculous.com/board/index.php?tid=3634&title=AMPPS_rewrite_enable/disable_option%3F_please%3F)
- [MAMP on Mac OS](http://stackoverflow.com/questions/7670561/how-to-get-htaccess-to-work-on-mamp)

**Based URL** : You could have a folder whatever name you like or even virtual host in your development environment.
Just change the configuration variable `$lc_baseURL` in `/inc/config.php` in accordance with your folder name or virtual host name.

**Home Routing** : In your production environment, you may not have a folder and you could upload the framework files directly to your web server document root.
In this case, you have to set and leave `$lc_baseURL` empty.

By default, LucidFrame has home page routing which is defined as `$lc_homeRouting` in `/inc/config.php`. It maps to `/app/home/index.php`. You could have `home.php` or `welcome.php` or whatever you like. However, LucidFrame encourages a structured page organization. You can check the recommended structure in the sample page folders and codes `/app/home` and `/app/example/` of the release.

**Additional Site Settings** : You can also configure the other settings in `/inc/config.php` and `/inc/site.config.php` or `/app/inc/site.config.php` according to your requirement.

**Secret** : You can generate the application secret `/inc/.secret` at [phplucidframe.sithukyaw.com/hash-generator](http://phplucidframe.sithukyaw.com/hash-generator).

**CSS Template** : LucidFrame provides you a default site CSS template. The file is `/css/base.css`. No matter you want to use it or not, you may do one of the following two ways to make your site easily upgradable in the future:

 1. create your own file in `/css` or `/app/css` with whatever name you like and update your `/inc/tpl/head.php` or `/app/inc/tpl/head.php` by including your file. Then you can override the rules of `/css/base.css` or write your own rules in your file.
 2. copy `/css/base.css` to `/app/css/base.css` and update it to your need. Then you don't have to update `head.php`.

## Demo with Sample Administration Module

- To run and check the sample administration module, have a look at [the configuration guideline](https://github.com/cithukyaw/LucidFrame/wiki/Configuration-for-The-Sample-Administration-Module).
- This Github project are successfully running at [demo-phplucidframe.rhcloud.com](http://demo-phplucidframe.rhcloud.com) and [demo-phplucidframe.rhcloud.com/admin](http://demo-phplucidframe.rhcloud.com/admin) with default user *admin/password*.

## Documentation

- [PDF Cookbook](http://phplucidframe.sithukyaw.com/cookbook) - The complete PDF documentation is available to download.
- [API Documentation](http://phplucidframe.sithukyaw.com/api) - API documentation of every version is available and generated by [phpDocumentor](http://phpdoc.org).
- [Code Samples & Scaffold](https://github.com/cithukyaw/LucidFrame/releases/latest) - The quick reference and coding samples are also available in the release.

## Support & Resources

- [Community Forum](http://phplucidframe.sithukyaw.com/community)
- [Stackoverflow](http://stackoverflow.com/questions/tagged/phplucidframe)
- [GitHub issues](https://github.com/cithukyaw/LucidFrame/issues)
- [Gitter IM](http://gitter.im/cithukyaw/LucidFrame)
- [IRC channel](http://webchat.freenode.net/?channels=#phplucidframe) `#phplucidframe`
- [Roadmap](https://trello.com/b/zj5l6GP1/phplucidframe-development)
