tools.rem-calc
==============

A calculator function that outputs rem/px values depending on browser support. This is a global tool designed to be used anywhere in a project, for example:

~~~scss
.component {
	margin-right: rem-calc(20);
}
~~~

## Set up

This function requires the `$font-base-size` variable to have a default value. Set this in the same file that you would the default typographic settings. For rem values to work effectively you need to then apply the `$font-base-size` to the `html` element in px, like so:

~~~scss

$font-base-size: 16;

html {
    font-size: ($font-base-size * 1px);
}

~~~

This function also depends on a `$supports` map being set before this function is imported. This allows us to export a separate CSS file for specific browsers (such as IE8):

~~~scss 
$supports: (
    svg: true
);

@import 'tools/rem-calc';
~~~



## Authors

| [![twitter/robinrendle](https://gravatar.com/avatar/3232e4cdc4a5e51c4bfb3bbed0d6abd5)](http://twitter.com/robinrendle "Follow @robinrendle on Twitter") |
|---|
| [Robin Rendle](http://robinrendle.com) |


| [![twitter/metadaptive](https://gravatar.com/avatar/3232e4cdc4a5e51c4bfb3bbed0d6abd5)](http://twitter.com/metadaptive "Follow @metadaptive on Twitter") |
|---|
| [Tom Davies](http://metadaptive.com) |


| [![twitter/mathaywarduk](http://www.gravatar.com/avatar/f38afd846cb1a7a8e4b5d16c14188fc2.png)](http://twitter.com/mathaywarduk "Follow @mathaywarduk on Twitter") |
|---|
| [Mat Hayward](http://www.mathayward.com/) |