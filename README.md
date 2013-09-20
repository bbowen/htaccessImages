htaccessImages
==============

##Specify responsive images using .htaccess

The web development industry hasn't found a great solution for responsive images yet. We have a lot of potential solutions which involve server tricks or additional client-side processing. **I think we can do better using existing technology.**

####.htaccess to the rescue!

1. Use RewriteCond filtering on HTTP_USER_AGENT to specify high-level UA strings (Android, iPad, iPhone, etc).
2. Use RewriteRule to append a modifier to the image path (e.g. *.png becomes *.mobile.png)

####Hi DPI support

[Shaun Inman](http://github.com/shauninman/) has written up some [Apache mods for Retina images](http://shauninman.com/tmp/retina/). These could be easily added into your .htacess to serve images of appropriate resolution.

####Test link:
Check the results at [this page](http://goo.gl/D8LxAL). The page uses png, gif and jpg image types in `<img>` tags and CSS background images.