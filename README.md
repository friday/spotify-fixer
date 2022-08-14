# spotify-fixer

This small scripts does two things:

1. On X11 it attempts to activate (raise) Spotify if it's already running,
   instead of trying to open a new Window (Spotify should be a single window app)
   The fix only woirks for X11 (but the issue happens on Wayland too).
2. It checks for and tries to use your HiDPI settings from _your_ gsettings (dconf),
   including both screen and font scaling.

## Usage

* It should be placed in PATH, in a location that overrules /usr/bin/.
* It expects spotify to be located in /usr/bin/spotify

## License

The code is licensed as MIT.
