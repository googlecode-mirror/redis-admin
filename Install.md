**Download**

Choose a last stable version from the [downloads](http://code.google.com/p/redis-admin/downloads/list) page.

**Extract files**

Untar the stable package in your web server's document root (e.g., /var/www/).:

```
tar -xzvf readmin-*.*.*.tar.gz
```

If you don't have direct access to your document root or don't have shell access, put the files in a directory on your local machine, and, after, transfer the directory on your web server using, for example, FTP.

Ensure that all the scripts have the appropriate owner (if PHP is running in safe mode, having some scripts with an owner different from the owner of other scripts will be a problem).

**Configuration**

Simply use a plain text editor to edit a file named config.php in the main (top-level) ReAdmin directory (the one that contains index.php)

You'll need a few directives to get going, a simple configuration may look like this:

```
/* set redis variables */
$config['redis']['host'] = "localhost";
$config['redis']['port'] = "6379";	

/* default admin variables */			
$config['admin']['user'] = "username";
$config['admin']['pass'] = "password";
	
/* default dir */
$config['dir']['home']	 = "/var/www/readmin-x.x.x";
```

**Finish**

For Apache you can use supplied .htaccess file in that folder, for other web servers, you should configure this yourself. Such configuration prevents from possible path exposure and cross side scripting vulnerabilities that might happen to be found in that code.