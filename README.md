tools.rem-calc
==============

A calculator function that outputs rem/px values depending on browser support. This is a global tool designed to be used anywhere in a project, for example:

~~~scss
.component {
	margin-right: rem-calc(20);
}
~~~

### Set up

1. `rem-calc` requires the `$font-base-size` variable to have a default value. Set this in the same file that you set default typographic settings.
2. This function depends on a `$supports` map being set before this function is imported, like so:

~~~scss 
$supports: (
    rem: true,
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


| [![twitter/mathaywarduk](https://gravatar.com/avatar/3232e4cdc4a5e51c4bfb3bbed0d6abd5)](http://twitter.com/mathaywarduk "Follow @mathaywarduk on Twitter") |
|---|
| [Mat Hayward](http://www.mathayward.com/) |