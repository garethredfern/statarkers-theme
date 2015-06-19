# The Statarkers Theme

Born from the idea of a blank canvas for starting your Statamic sites this theme is loosely based on the popular [Starkers](http://viewportindustries.com/products/starkers/) theme for Wordpress. The idea being that you can load the theme into your Statamic themes folder, add the dummy content and fields to your Statamic install and get designing and building your Statamic sites in even less time than you were already.

## Versions
There are two versions of Statarkers which run on two different branches.

### Original Version
For those that just want the bare minimum (which was how things started) then there is the [original branch](https://github.com/statamicthemes/statarkers-theme/tree/original).

### Clothed Version
The master branch is what Statarkers has evolved into with its Bower, Grunt and Sass setup. Normalize is used to reset browser defaults and SASS is used to make your CSS life easy. Each template is marked up with some helpful user notes. [Bower](http://bower.io/) is used to manage all dependencies and you can edit the [bower.json](http://bower.io/docs/creating-packages/#bowerjson) file to add or remove resources that you may or may not want to use. To help with older browser support [DOMAssistant](http://www.domassistant.com/) and [Selectivir](http://selectivizr.com/) are conditionally loaded for IE8. DOMAssistant is not available on Bower so it is kept in the theme js libs folder. To finish off [Grunt](http://gruntjs.com/getting-started) is used for the front end automation. SASS and JS are compiled and compressed for you by simply navigating to the theme folder and in your terminal typing `grunt watch` (there's a bit more to it but its not hard I promise). For more information on installing and using Grunt I recommend reading and watching:

- [Grunt for People Who Think Things Like Grunt are Weird and Hard](http://24ways.org/2013/grunt-is-not-weird-and-hard/)
- [First Moments with Grunt](http://css-tricks.com/video-screencasts/130-first-moments-grunt/)

If you dont want to use Bower or Grunt just delete the following folders/files

- bower_components
- bower.json
- Gruntfile.js
- package.json

Out of the box Statarkers supports IE8 and all modern browsers. To provide a basic layout for older browsers (IE7 & below) we use Normalize with no other styles aplied. The scripts in the default layout template use conditional comments to stop them loading below IE8. If you would like to support IE7 & below you can remove these elements.

## Raven Forms
An example form template and partial are included with the theme, to make use of them you will need to have [Raven Forms](http://statamic.com/add-ons/raven) installed. To get the example working just change the `to` variable on line 42 of the _config/formsets/contact.yaml file. Then either add a [route](http://statamic.com/learn/advanced-features/routes) of `/contact : /contact` or set up a content page for your contact form in your _content folder and point the `_template` YAML to `contact` . If you don't want to use Raven just delete:

- _config/formsets
- _themes/statarkers/templates/contact.html
- _themes/statarkers/partials/forms/_contact_form.html
- _themes/statarkers/templates/emails/

## Theme Use
You can use Statarkers in any way you wish, please feel free to fork it on github. As the theme is offered for free, it’s also offered with limited support. If you find a bug, please let me know and I’ll fix it as soon as possible. Any improvements and feature requests can be asked through github.

Happy Statamic Themeing!

##Installing

To install the theme follow the instructions below.

1. [Install Statamic:](http://statamic.com/learn/digging-in/installing) **Don't forget to set up your .htaccess file**.
2. Copy the statarkers theme folder to your _themes folder. Please note if you have downloaded the statarkers-theme-master folder **the statarkers theme is located inside the _themes folder**.
3. Rename the Statarkers theme folder to the name of your theme. From now on we will still refer to the Statarkers theme folder but this will now be whatever you rename it to.
4. Change the name of the statarkers.js file (located in the js folder) and the starkers.js file located in the js/app folder  to the name of your theme.
5. In the Statarkers theme folder go to the css folder. Rename the statarkers.css and statarkers.css.map files to the name of your theme then find the sass folder and rename the statarkers.scss file to the name of your theme.
6. In the Statarkers theme folder open the package.json file and change the `"name": "statarkers"` to your theme name.
7. Delete the contents of your Statamic install fieldsets folder then copy the new fieldsets from the Statarkers folder (located in _config/fieldsets).
8. If you would like to use the dummy content provided with the Statarkers theme (recommended) then delete the contents of your existing _content folder and copy the files and folders from the Statarkers _content folder. Also delete the img folder inside of your assets folder and drop in the Statarkers img folder.
9. In your Statamic install go to `_config` settings YAML file and change the `_theme` name from acadia to the name you have given to your theme. If this is a clean install you should also change the site name and url to whatever you are using. We suggest also changing the `_taxonomy_slugify` to true as this gives you cleaner url's.
10. Add the gitignore file to the root of your project/site (remove sample from the front of the file name), in here there are some handy ignores for Statamic.
11. If you are using Grunt navigate to your theme folder, open up the terminal and type `npm install`. This will add all the required plugins from the package.json file.
12. If you are using Bower make sure you have added or removed the dependencies you require in the bower.json file and changed the name of the project etc. then navigate to your theme folder in the terminal and type `bower update` to pull in all the required dependencies.
13. Navigate to your theme folder and type `grunt watch` in your terminal to have Grunt compile and compress your Sass and JS files.
14. Add the dev.yaml to your _config/environments folder.

##More Information

The Gruntfile is set up to watch a JS file in your theme folder in js/app it then compresses the JS into the theme JS folder, it is important that these files are named the same as your theme.

### Additional Modules
- [Statarkers Membership](https://github.com/statamicthemes/statarkers-membership)
- [Statarkers Nav](https://github.com/statamicthemes/statarkers-nav)
