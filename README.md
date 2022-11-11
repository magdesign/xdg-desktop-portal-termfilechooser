# xdg-desktop-portal-termfilechooser

[xdg-desktop-portal] backend for choosing files with your favorite file
chooser.
By default, it will use the [ranger] file manager, but this is customizable.
Based on [xdg-desktop-portal-wlr] (xpdw).

## NOTE: for [lf](https://github.com/boydaihungst/xdg-desktop-portal-termfilechooser/tree/fix-for-lf) user. Use branch [fix-for-lf](https://github.com/boydaihungst/xdg-desktop-portal-termfilechooser/tree/fix-for-lf)

To change default_dir, edit `$default_dir` in lf-wrapper.sh. For example: `$default_dir="$HOME/Downloads"`

```sh
git clone -b fix-for-lf https://github.com/boydaihungst/xdg-desktop-portal-termfilechooser.git
```
## Step for step guide

[Read here](https://github.com/GermainZ/xdg-desktop-portal-termfilechooser/issues/3#issuecomment-1304607788)

## Building

```sh
meson build
ninja -C build
```

## Installing

### From Source

```sh
ninja -C build install
```


## Running

Make sure `XDG_CURRENT_DESKTOP` is set and imported into D-Bus.

When correctly installed, xdg-desktop-portal should automatically invoke
xdg-desktop-portal-termfilechooser when needed.

For example, to use this portal with Firefox, launch Firefox as such:
`GTK_USE_PORTAL=1 firefox`.

### Configuration

See `man 5 xdg-desktop-portal-termfilechooser`.

### Manual startup

At the moment, some command line flags are available for development and
testing. If you need to use one of these flags, you can start an instance of
xdpw using the following command:

```sh
xdg-desktop-portal-termfilechooser -r [OPTION...]
```

To list the available options, you can run `xdg-desktop-portal-termfilechooser
--help`.

## License

MIT

[xdg-desktop-portal]: https://github.com/flatpak/xdg-desktop-portal
[xdg-desktop-portal-wlr]: https://github.com/emersion/xdg-desktop-portal-wlr
[ranger]: https://ranger.github.io/
