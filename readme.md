Olivero sub-theme which provides dark mode colours.

Note that this does not provide any sort of UI; instead it automagically
switches to dark mode colours when the CSS [`prefers-color-scheme`
media query](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme)
matches. This means that when your browser and operating system are set to light
mode, this theme will display the light mode colours that ship with Drupal core;
when your browser and operating system are set to dark mode, the dark mode
colours will be used.

Also note that this requires Drupal core 10.0.x, and will not be installable on
previous versions due to [lack of CSS custom property
support](https://www.drupal.org/project/drupal/issues/3257274#comment-14567683),
nor on Drupal core 10.1.x or later because the Olivero CSS is marked as internal
and thus not guaranteed to obey semantic versioning rules so it could change
drastically at any time. When new, stable core versions are tested and verified
to work, the version constraint will be increased to allow them.
