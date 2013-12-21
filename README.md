# CampusHash HTML5 Deck - [Demo](http://campushash.github.io/deck/)

## Editing the slides

The slides are compiled from `slides.md`, which is written in standard markdown with some alterations. Check out `slides.md` to get an overview. Upon editing, you can compile the slides by running

```
$ python render.py
```

which will output `presentation.html`.

To use this deck, clone this repo, and make the changes.

## Configuring the slides

Much of the deck is customized by changing the settings in [`slide_config.js`](slide_config.js).
Some of the customizations include the title, speaker
information (name, social urls, blog), web fonts to load, themes, and other
general behavior.

## Editing CSS

[Compass](http://compass-style.org/install/) is a CSS preprocessor used to compile
SCSS/SASS into CSS. We chose SCSS for the new slide deck for maintainability,
easier browser compatibility, and because...it's the future!

That said, if not comfortable working with SCSS or don't want to learn something
new, not a problem. The generated .css files can already be found in
(see [`/theme/css`](theme/css)). You can just edit those and bypass SCSS altogether.
However, our recommendation is to use Compass. It's super easy to install and use.

### Installing Compass and making changes

First, install compass:

    sudo gem update --system
    sudo gem install compass

Next, you'll want to watch for changes to the exiting .scss files in [`/theme/scss`](theme/scss)
and any new one you add:

```
$ compass watch
```

This command automatically recompiles the .scss file when you make a change.
Its corresponding .css file is output to [`/theme/css`](theme/css). Slick.

By default, [`config.rb`](config.rb) in the main project folder outputs minified
.css. It's a best practice after all! However, if you want unminified files,
run watch with the style output flag:
```
compass watch -s expanded
```

*Note:* You should not need to edit [`_base.scss`](theme/scss/_base.scss).

## Running the slides

The slides can be run locally from `file://` making development easy :)

### Running from a web server

If at some point you should need a web server, use [`serve.sh`](serve.sh). It will
launch a simple one and point your default browser to [`http://localhost:8000/presentation.html`](http://localhost:8000/presentation.html):
```
$ ./serve.sh
```

You can also specify a custom port:
```
$ ./serve.sh 8080
```

### Presenter mode

The slides contain a presenter mode feature (beta) to view + control the slides
from a popup window.

To enable presenter mode, add `presentme=true` to the URL: [http://localhost:8000/presentation.html?presentme=true](http://localhost:8000/presentation.html?presentme=true)

To disable presenter mode, hit [http://localhost:8000/presentation.html?presentme=false](http://localhost:8000/presentation.html?presentme=false)

Presenter mode is sticky, so refreshing the page will persist your settings.