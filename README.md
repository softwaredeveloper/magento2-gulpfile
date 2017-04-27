# BITBULL MAGENTO2 GULPFILE #

Simple Gulpfile for Magento2

Why?
----

This project is originated from the need to make faster the frontend workflow of Magento 2.
More info here: http://www.bitbull.it/blog/la-compilazione-del-less-in-magento2/

Usage
-----

1. Place the gulpfile.js in the root of your project.

2. Install the following required modules:

        npm install gulp
        npm install gulp-less
        npm install gulp-util
        npm install chalk
        npm install gulp-clean
        npm install gulp-run

3. Create a configuration file **dev/tools/gulp/configs/themes.js** with the following contents.

        module.exports = {
        <Theme>: {
          "src": [
            "vendor/<Vendor>/<Theme-name>",
            "vendor/<Vendor>/<Module-name>"
            ],
          "dest": "pub/static/frontend/<Vendor>/<Theme-name>",
          "locale": [locale],
          "lang": "less",
          "area": "frontend",
          "vendor": <Vendor>,
          "name": <Theme-name>,
          "files": [
            "css/styles-m",
            "css/styles-l"
           ]
         }
        };
        
* src:  Array of theme and modules you want to compile in format "vendor/<Vendor>/<Module-name>"
* dest: Path in pub/static of your theme
* area: Area, one of (frontend|adminhtml|doc),
* name: Theme name in format theme-name,
* locale: Locale (ie. en_US),
* files: Array of files to compile


Commands
--------
 
1. Task watch.       
        
        gulp watch --<theme-name>
        
1. Task clean and build.       
        
        gulp build --<theme-name>


Nice to have
------------
- Update Magento2 **packege.json** with the required modules
- Compile different languages

Licence
-------
[OSL - Open Software Licence 3.0](http://opensource.org/licenses/osl-3.0.php)

Developer
---------
Irene Iaccio(@nuovecode) http://www.bitbull.it

Copyright
---------
(c) 2016 Bitbull Srl
