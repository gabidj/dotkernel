# Server Requirements

- [Server Requirements](#server-requirements)
    - [Webserver](#webserver)
    - [PHP >= 7.1](#php-71)
        - [Required Settings and Modules & Extensions](#required-settings-and-modules-extensions)
    - [RDBMS](#rdbms)
        - [Recommended extensions](#recommended-extensions)

For production we highly recommend a *nix based system.

## Webserver

- Apache >= 2.2
  - mod_rewrite
  - .htaccess support (`AllowOverride All`)
- Nginx

## PHP >= 7.1

Both **mod_php** and **FCGI (FPM)** are supported.

### Required Settings and Modules & Extensions

- memory_limit >= 128M
- upload_max_filesize and post_max_size >= 100M (depending on your data)
- mbstring
- CLI SAPI (for Cron Jobs)
- Composer (added to $PATH)

## RDBMS

- MySQL / MariaDB >= 5.5.3

### Recommended extensions

- opcache
- pdo_mysql or mysqli (if using MySql or MariaDb as RDBMS)
- dom - if working with markup files structure (html, xml, etc)
- simplexml - working with xml files
- gd, exif - if working with images
- zlib, zip, bz2 - if compessing files
- [curl](http://php.net/curl) (required if API's are used)
