# LobiCard

jQuery plugin for bootstrap 4 cards. It extends cards with several common and useful functions.

This is a fork of [Lobipanel](https://github.com/arboshiki/lobipanel), migrating the library from Bootstrap 3 to Bootstrap 4.

## Differences to LobiPanel

- Switched Less to SASS, giving compatibility with Bootstrap 4
- Glyphicons has been dropped from Bootstrap, LobiCard now uses Font Awesome by default
- Clean up usage of `""`, now more consistently uses `''`
- Improve support for use through NPM as well as Bower. **Note:** If using NPM this requires that you do `npm install napa --save-dev` in your project. This is due to 'jquery-ui-touch-punch-improved' not being an npm package. But hey, maybe it's not needed anymore...
- Updated the version of JQuery and JQuery UI
- Added JS/HTML hinting and beautification configs
- Less working files committed to Git
- Updated lib folder
- Added some margin between control icons
- Fix an issue using jquery's `load()`, which now assumes POST if the params is an object - params is now a string by default
- Tooltip `destroy` issue resolves as in Bootstrap 4 it is now `dispose`.
- When editing a card's title the contained HTML is retained. Previous behaviour was to allow a user to edit the text only and does a direct replacement, now the HTML is retrieved.

### Known issues

Since Bootstrap 4 has not been released yet there are still some issues that may well be related to other known issues. If in doubt, check [Bootstrap's Issue tracker](https://github.com/twbs/bootstrap/issues). Here are some I've found so far:

#### Uncaught Error: Tooltip is transitioning

This appears to be an issue in Bootstrap 4, e.g. [#21607](https://github.com/twbs/bootstrap/issues/21607). There is a fix for this that will become available with the first beta of Bootstrap 4. See [PR#21743](https://github.com/twbs/bootstrap/pull/21743) for more information. Until then [#21607](https://github.com/twbs/bootstrap/issues/21607) does give some workarounds, or just survive with the error until [Bootstrap 4 Beta](https://github.com/twbs/bootstrap/milestone/41) is released.

## Features

- Sort, drag, expand, resize, minimize bootstrap cards
- Specify url and load content in card from this url
- Change the name of the card
- Customize action icons and action tooltips
- Works for nested cards
- HTML5 localStorage support
  - Save card state: (pinned, unpinned, collapsed, fullscreen, minimized) and apply it on page load
  - Save card position among siblings and apply on next time

## Dependencies

LobiCard is depended on jQuery, jQuery UI and Bootstrap 4.

## Compiling

The package now uses sass rather than less. So, if you are developing on Windows you will need to install [Ruby](https://rubyinstaller.org/downloads/) making sure to add the executable to your path, and then install SASS by opening a new command window and executing `gem install sass`.

## Installation

Below demonstrates installation with bower, but npm can be used too by simply changing the directory `bower_components` to `node_modules`.

```html
<!DOCTYPE html>
<html>
   <head>
        <!--Installation using bower -->
        <link rel="stylesheet" href="bower_components/tether/dist/css/tether.min.css"/>
        <link rel="stylesheet" href="bower_components/bootstrap/dist/css/bootstrap.min.css"/>
        <link rel="stylesheet" href="bower_components/jquery-ui/themes/ui-lightness/jquery-ui.min.css"/>
        <link rel="stylesheet" href="bower_components/font-awesome/css/font-awesome.min.css"/>

        <link rel="stylesheet" href="dist/css/lobicard.min.css"/>
   </head>

    <body>
        ...
        <!--Installation using bower -->
        <script src="bower_components/jquery/dist/jquery.min.js"></script>
        <script src="bower_components/jquery-ui/jquery-ui.min.js"></script>
        <script src="bower_components/jquery-ui-touch-punch-improved/jquery.ui.touch-punch-improved.js"></script>
        <script src="bower_components/tether/dist/js/tether.min.js"></script>
        <script src="bower_components/bootstrap/dist/js/bootstrap.min.js"></script>

        <script src="dist/js/lobicard.js"></script>

   </body>
</html>
```

## Usage

`index.html` contains a series of examples of Lobicard's usage.

For more complete documentation and examples visit Lobipanels's [home page](http://lobianijs.com/site/lobipanel). This fork only tries to make this library more compatible with Bootstrap 4, not change the API.
