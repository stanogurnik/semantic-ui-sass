# Semantic UI for Sass

`semantic-ui-sass` is an Sass-powered version of [Semantic UI](https://github.com/jlukic/Semantic-UI) and ready to drop into Rails & Compass.

## Installation and Usage

```ruby
gem 'semantic-ui-sass', '~> 0.0.3'
```
or

```ruby
gem 'semantic-ui-sass', github: 'doabit/semantic-ui-sass'
```

`bundle install` and restart your server to make the files available through the pipeline.

# semantic-ui-sass with Rails

## CSS

Import Semantic in an SCSS file (for example, `application.css.scss`) to get all of Semantic's styles

```css
@import "semantic-ui";
```

You can also include modules

```css
@import "semantic-ui/collections/menu";
```

## Javascripts

We have a helper that includes all Semantic javascripts. Put this in your Javascript manifest (usually in `application.js`) to

```js
// Loads all Semantic javascripts
//= require semantic-ui
```

You can also load individual modules, provided you also require any dependencies.

```js
//= require semantic-ui/modal
//= require semantic-ui/dropdown
```

# semantic-ui-sass with Compass

## New project

Install the gem and create a new project using the gem.

```console
gem install semantic-ui-sass
compass create compass-project -r semantic-ui-sass --using semantic-ui
```

This will sort a few things out:

* You'll get a starting `styles.scss`
* You'll get a compiled stylesheet compiled & ready to drop into your application
* We'll also copy the Semantic javascripts & images & fonts into their respective folders for you

## Existing project

Install the gem, add the require statement to the top of your configuration file, and install the extension.

```console
gem install semantic-ui-sass
```

```ruby
# In config.rb
require 'semantic-ui-sass'
```

```console
compass install semantic-ui
```

## TODO

* Add global variables
* Add rails helpers like `render_flash`?

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request