Olivero sub-theme which provides dark mode colours.

Note that this does not provide any sort of UI; instead it automagically
switches to dark mode colours when the CSS [`prefers-color-scheme`
media query](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme)
matches. This means that when your browser and operating system are set to light
mode, this theme will display the light mode colours that ship with Drupal core;
when your browser and operating system are set to dark mode, the dark mode
colours will be used.

Also note that this requires Drupal core 10.1.x, and will not be installable on
previous major core versions due to [lack of CSS custom property
support](https://www.drupal.org/project/drupal/issues/3257274#comment-14567683),
nor on Drupal core 10.2.x or later because the Olivero CSS is marked as internal
and thus not guaranteed to obey semantic versioning rules so it could change
drastically at any time. When new, stable core versions are tested and verified
to work, the version constraint will be increased to allow them.

# Installation

First step is to make Composer aware of this repository. Your root
`composer.json` should already have a `repositories` section that has the
drupal.org Composer repository like so:

```json
  "repositories": [
    {
      "type": "composer",
      "url": "https://packages.drupal.org/8"
    }
  ],
```

You'll need to edit the section to include this theme's repository like so:

```json
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/Ambient-Impact/drupal-olivero-dark.git"
    },
    {
      "type": "composer",
      "url": "https://packages.drupal.org/8"
    }
  ],
```

Save the file and then run
`composer require "drupal/olivero_dark:^10.1@dev"` which should download
the theme. Log into Drupal, find the theme in the themes list (under
`/admin/appearance`), install it, and configure the default colour scheme if
needed.
