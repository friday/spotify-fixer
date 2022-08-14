# spotify-fixer

This small scripts does two things:

1. On X11 it attempts to activate (raise) Spotify if it's already running,
   instead of trying to open a new Window (Spotify should be a single window app)
   The fix only woirks for X11 (but the issue happens on Wayland too).
2. It checks for and tries to use your HiDPI settings from _your_ gsettings (dconf),
   including both screen and font scaling.

## Dependencies
* spotify
* python-gobject (aka python3-gi or pygobject)
* libwnck3 (aka gir1.2-wnck-3.0) - Optional, but required to have Spotify run as a single window app in X11

## Usage

* It should be placed in `$PATH`, in a location that overrules /usr/bin/ (preferably `/usr/local/bin/` and not anywhere in $HOME unless you are sure all the app launchers you use runs as your user.
* It expects spotify to be located in `/usr/bin/spotify` (so if it's not, you'll have to chanfge the script)

# Arch install
```sh
yay -S spotify-fixer
```

# Others Distros
Install the dependencies manually and run:
```
sudo wget -P /usr/local/bin/ https://raw.githubusercontent.com/friday/spotify-fixer/main/spotify
sudo chmod +x /usr/local/bin/spotify
```

## License

The code is licensed as MIT.
