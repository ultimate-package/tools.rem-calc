tools.rem-calc
==============

A calculator function that outputs rem/px values depending on browser support. This is a global tool designed to be used anywhere in a project, for example:

~~~scss
.component {
    margin-right: rem-calc(20);
}

h1 {
    margin: rem-calc(0 20 10 10);
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
