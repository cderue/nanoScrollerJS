# nanoScroller.js
[nanoScroller.js](http://jamesflorentino.com/jquery.nanoscroller) is a jQuery plugin that offers a simplistic way of implementing Mac OS X Lion-styled scrollbars for your website.
It uses minimal HTML markup being `.nano > .content`. The other scrollbar div elements `.pane > .slider` are added during run time to prevent clutter in templating. The latest version utilizes native scrolling and works with the iPad, iPhone, and some Android Tablets.

Please visit the [downloads](https://github.com/jamesflorentino/nanoScrollerJS/downloads) section to get the js and css template file (.zip).

To start using, you to do three basic things:

### 1. Mark Up

    <div id="about" class="nano">
     <div class="content"> ... content here ...  </div> 
    </div>

Copy the HTML mark-up. Change `#about` into something related to your content. Though you can also remove that attribute as long as you have a parent div with an ID reference. e.g. `#parent > .nano`

### 2. CSS

Link to the `nanoscroller.css` file inside your page's `<head>` section (...or copy the contents from it to your page's main stylesheet file).

    <link rel="stylesheet" href="nanoscroller.css"> 

You should specify a width and a height to your container, and apply some custom styling for your scrollbar. Here's an example:

    .nano { background: #bba; width: 500px; height: 500px; }
    .nano .content { padding: 10px; }
    .nano .pane   { background: #888; }
    .nano .slider { background: #111; }

### 3. JavaScript

    $("#about").nanoScroller();

### Additional Methods


#### scroll:

To scroll at the top:

    $("#about").nanoScroller({ scroll: 'top' });

To scroll at the bottom:

    $("#about").nanoScroller({ scroll: 'bottom' });

To scroll to an element:

    $("#about").nanoScroller({ scroll: $('#a_node') });


#### stop:

To stop the operation:

    $("#about").nanoScroller({ stop: true });


#### nanoScroller();    

Refresh the scrollbar:

    $("#about").nanoScroller();


### Advanced methods

To scroll at the top with an offset value:

    $("#about").nanoScroller({ scrollTop: value });

To scroll at the bottom with an offset value:

    $("#about").nanoScroller({ scrollBottom: value });

To scroll to an element:

    $("#about").nanoScroller({ scrollTo: $('#a_node') });

### Development

To build nanoScroller from source you need the following libraries installed:

* Node.js and npm: [homepage / download](http://nodejs.org/)
* Coffeescript: [homepage](http://coffeescript.org/) | `npm install -g coffee-script`

To allow the build process to convert the README file to HTML you also need:

* Ruby (pre-installed in OS X): [homepage](http://www.ruby-lang.org/en/) | [download](http://www.ruby-lang.org/en/downloads/)
* GCC: [homepage](http://gcc.gnu.org/) | [download for OS X](https://github.com/kennethreitz/osx-gcc-installer)
* Redcarpet: [homepage](https://github.com/tanoku/redcarpet) | `gem install redcarpet` (add `sudo` if needed)

#### How to build & contribute

1. Make all JS changes in Coffeescript file(s), CSS changes in CSS file(s).
2. In terminal move to nanoscroller folder and run `cake build`
3. Make sure that all changes are valid and open a pull request.

### Features
- It has been tested to work in the following desktop browsers: IE7+ (_does not work in IE6_), Firefox 3+, Chrome, Safari 4+ and Opera 11.60+. If you find a bug, please report here at the [issues section](https://github.com/jamesflorentino/nanoScrollerJS/issues)
- It currently works with iOS5 (iPhone, iPad and iPod Touch). If you see it's broken on other tablets and mobile devices, please file a ticket in the git repo. Along with model name, and OS of the device.

### Contributors
- @jamesflorentino
- @kristerkari

### From the author
I wrote this plugin out of necessity for a JavaScript project with designers and front-end developers in mind. Please also note that I will not be liable to fix your problem just in case you plan to use this commercially and some unforseen event arises. However, I will do what I can to immediately patch a solution.

### Credits
- Initially written by [James Florentino](http://jamesflorentino.com) in [CoffeeScript](http://coffeescript.org)
- Released under [MIT License](http://www.opensource.org/licenses/mit-license.php)
- If you write CoffeeScript and you wish to improve the code, please feel free to fork the project.
