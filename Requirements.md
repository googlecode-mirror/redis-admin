**Web Server**

A web server, with Rewrite module, is needed to install ReAdmin on (e.g., Apache, IIS etc.)

**.htaccess Rule**

This module uses a rule-based rewriting engine (based on a regular-expression parser) to rewrite requested URLs on the fly. Available in Apache 1.2 and later.

```
<IfModule mod_rewrite.c>

RewriteEngine On

RewriteBase /

RewriteCond %{REQUEST_FILENAME} !-f

RewriteCond %{REQUEST_FILENAME} !-d

RewriteRule . /index.php [L]

</IfModule>
```

**PHP**

PHP 5.2.0, or newer, with the Standard PHP Library (SPL) extension enabled.

**Redis**

Redis 1.2.0 or newer ([details](http://code.google.com/p/redis/))

**Web browser**

Any web browser with cookies enabled.