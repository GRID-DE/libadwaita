This is the patched version of libAdwaita which allows themes.

It is based on libAdwaita 1.5 and adds theme support.

CSS support
-----------

The library uses the current GTK3 theme. If it provides a `libadwaita-1.0` directory, it uses the theme's stylesheets. Otherwise it fallsback to the library's own stylesheet, which looks exactly the same as upstream libadwaita.

Inside the theme's `libadwaita-1.0` directory, there should be the following CSS files:

- `defaults-light.css` defines the colors in Light mode
- `defaults-dark.css` defines the colors in dark mode
- `base.css` defines the widgets style
- `base-hc.css` defines the widgets style in high-contrast mode
- `assets` provide pictures used by the stylesheet

You can find these files in `/usr/share/themes/LibAdwaita-Example/libadwaita-1.0` after installing the `libadwaita-1-examples` package.

To minimize potential issues it is recommended to only change the colors and the style of the window controls.

The best place to modify the window controls is at the bottom of `base.css`.

SASS support
------------

If your theme uses SASS you can work from the SASS files directly and get greater control.

In this case, you can find the stylesheet here in the `src/stylesheet` directory.

Examples
--------

Mint-X and Mint-Y implement support for this library.

You can find their stylesheets in `/usr/share/themes/Mint-X/libadwaita-1.0` and `/usr/share/themes/Mint-Y/libadwaita-1.0`, or on github at https://github.com/linuxmint/mint-themes/pull/503.

Below is the libadwaita README
------------------------------

# Adwaita

Building blocks for modern GNOME applications.

## License

Libadwaita is licensed under the LGPL-2.1+.

## Building

We use the Meson (and thereby Ninja) build system for libadwaita. The quickest
way to get going is to do the following:

```sh
meson setup _build
ninja -C _build
ninja -C _build install
```

For build options see [meson_options.txt](./meson_options.txt). E.g. to enable documentation:

```sh
meson setup _build -Ddocumentation=true
ninja -C _build
```

## Usage

There's a C example:

```sh
_build/run _build/demo/adwaita-1-demo
```

## Documentation

The documentation can be found online
[here](https://gnome.pages.gitlab.gnome.org/libadwaita/doc/).

## Getting in Touch

Matrix room: [#libadwaita:gnome.org](https://matrix.to/#/#libadwaita:gnome.org)´