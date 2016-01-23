If your site has been blocked by Google as Malicious then follow these steps to be relisted:

## To prevent your site from being blocked do the following ##

  1. Remove all old plugins and themes you aren’t using.
  1. Upgrade all your plugins and themes to the latest versions and make sure none of them use an old version of Timthumb.
  1. Clean any Timthumb cache directories.
  1. Upgrade your entire wordpress installation, even if it’s at the latest version. This overwrites all wordpress files.
  1. Search your directory tree for any remaining suspicious files that contain base64\_decode wrapped in an eval() statement or URL encoded data. More info on how to do this search here. Delete any files you find. NOTE: If you don’t find any additional infected files in this step, it’s highly likely that your site is not clean. Every attack that I’ve seen so far using Timthumb gets in by uploading a file into the cache directory and then uploads an additional file into a writeable directory on the blog to ensure continued access once the cache is cleaned. Make sure you find that additional file.
  1. Make sure the only directory that is writeable in your wordpress installation is wp-content/. Directories like wp-admin and wp-includes should be read only by the web server.

## To repair a blocked site ##

  1. complete the steps above
  1. request a relisting through Google webmaster tools.  [info on being relisted here](http://www.google.com/support/webmasters/bin/answer.py?answer=168328)
  1. the process takes 24 hours to be cleaned.
  1. You can find out [more about Google’s Malware list and safe browsing report on this page.](http://25yearsofprogramming.com/blog/2009/20091124.htm)

## To upgrade TimThumb using FTP ##

  1. open up your website in your favorite ftp application
  1. delete the **timthumb.php** file (may also be thumb.php, image.php or some other variation - if unsure please ask your webmaster/ theme provider for more information)
  1. download [the latest timthumb.php](http://timthumb.googlecode.com/svn/trunk/timthumb.php) saving it with the name of the file you deleted previously - most likely timthumb.php
  1. upload the newly created file to your web space in the same location as the file(s) you deleted