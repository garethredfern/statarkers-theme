# The Statarkers Theme

Born from the idea of a blank canvas for starting your Statamic sites this theme is loosely based on the popular [Starkers](http://viewportindustries.com/products/starkers/) theme for Wordpress. The idea being that you can load the theme into your Statamic themes folder, add the dummy content and fields to your Statamic install and get designing and building your Statamic sites in even less time than you were already.

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
3. Rename the Statarkers theme folder to the name of your theme. From now on I will still refer to the Statarkers theme folder but this will now be whatever you rename it to.
4. Change the name of the statarkers.js file (located in the js folder) to the name of your theme.
5. In the Statarkers theme folder go to the css folder. Rename the statarkers.css file to the name of your theme.
6. Delete the contents of your Statamic install fieldsets folder then copy the new fieldsets from the Statarkers folder (located in _config/fieldsets).
7. If you would like to use the dummy content provided with the Statarkers theme (recommended) then delete the contents of your existing _content folder and copy the files and folders from the Statarkers _content folder. Also delete the img folder inside of your assets folder and drop in the Statarkers img folder.
8. In your Statamic install go to `_config` settings YAML file and change the `_theme` name from acadia to the name you have given to your theme. If this is a clean install you should also change the site name and url to whatever you are using. I suggest also changing the `_taxonomy_slugify` to true as this gives you cleaner url's.
9. Add the gitignore file to the root of your project/site (remove sample from the front of the file name), in here there are some handy ignores for Statamic.
10. Add the dev.yaml to your _config/environments folder.

### Additional Modules
- [Statarkers Membership](https://github.com/statamicthemes/statarkers-membership)
- [Statarkers Nav](https://github.com/statamicthemes/statarkers-nav)
