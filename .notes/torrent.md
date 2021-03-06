# How to Use Torrents on Linux and On the Commmand Line

> A valuable resource is [Brodie Robertson's tutorial][brodie_tutorial].

1. Install `transmission-cli`:
    ```sh
    sudo pacman -S transmission-cli
    ```
1. In order to run the command line interface properly, you're actually going to have to first enable/activate the daemon &mdash; some people put it on their `.xinitrc` &mdash;:
    ```sh
    transmission-daemon &
    transmission-remote-cli # this has actually been deprecated, use either `tremc` or `stig` instead
    ```
1. Install either `tremc` or `stig` from the AUR:
    ```sh
    yay -S tremc
    ```
1. Use `tremc` then `:a` to add a torrent.

Some other tips for `tremc`:

- `tremc` is a replacement for `transmission-remote-cli`, so you can access all of the older version with `transmission -- [--trc-old-options]`
    - For example, `transmission -- -a <torrent-link>` to add a torrent.
- Once the torrent is added, you can move its contents by pressing <kbd>m</kbd> inside the TUI.


[brodie_tutorial]: https://youtu.be/MXKGLTSS4Z0
