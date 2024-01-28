# cc-desktop-theme
My CrossCode desktop theme, because a bunch of people on Reddit liked it. It includes:

- An animated (or non-animated) background.
- CPU, GPU, and RAM meters styled after the CrossCode HUD.
- A "Now Playing" tab, also styled after the CrossCode HUD.
- A shortcuts menu with collapsible sub-menus, and a python script to generate them.

### Notes
- Getting the Now Playing tab to work with Spotify is painful and annoying. More on that later.
- This was tested exclusively on Windows 10. Windows 11/Mac/Linux users, you're on your own (sorry).
  If you get this working on another OS and have to do things differently, submit a pull request
  with instructions and I'll probably add them.
- I have no intention of making a Wallpaper Engine version of this, but anyone who wants to has my
  blessing. All the images are in the `@Resources` folder if you decide to give it a shot.
- If you use the python script or decide to manually edit any of the config files, download a decent
  text editor if you haven't already. [VSCode](https://code.visualstudio.com/) is my daily driver.

# Installation
1. Download and install [Rainmeter](https://www.rainmeter.net/).
2. Download `CCDesktopTheme_1.0.rmskin` from the latest release.
3. Double-click the file, click Install.

# Skins
## Background
There are 2 background skins:
- `animated.ini` is an animated background taken from the CrossCode title screen.
- `static.ini` only displays the first frame of the animation.

Assuming you're on Windows 10, the background will try to cover up your taskbar. By default, the
config will crop it to fit the standard Windows 10 taskbar, at the bottom of the screen. If your
taskbar is a different size or is in a different place, you'll need to edit the config file to
change where it crops (don't worry, this one isn't hard).

## ystem
There are three resource monitors - `CPU`, `GPU`, and `RAM` - each in their own sub-folders. To load
one, open the folder and load `main.ini`.

## shortcuts
The default file here, `main_sample.ini`, will probably be useless for you. If you want to add your
own shortcuts, there are 2 ways to do it:
### Use the Python Script
1. Download and install [Python](https://www.python.org/)
2. Download `cctheme-shortcut-generator.py` from the latest release.
3. Open the file and run it (if you open it in vscode, use the play button in the top right). If it
   crashes and says something about PYSimpleGUI not being installed, type `pip install PYSimpleGUI`
   in the terminal it just crashed in and hit enter to fix it.
4. When you're done, save the new file to the same place as `main_sample.ini`. On Windows 10, the
   default location will be `Document/Rainmeter/Skins/crosscode/shortcuts`.

### Edit the Files Manually
There are instructions at the top of `main_sample.ini`. Good luck.

# Now Playing
Note: The Now Playing tab will only be visible if a music player is currently running. This is intentional.

If you're playing music stored locally on your computer, just load `local.ini`. You'll need to
be using a supported player for it to work - the default config uses [AIMP](https://www.aimp.ru/),
but you can edit it to use any of the
[supported players](https://docs.rainmeter.net/manual/measures/nowplaying/).

If you're playing music through a streaming player, install the
[WebNowPlaying](https://github.com/keifufu/WebNowPlaying-Rainmeter) plugin, load `web.ini`, and
get ready to have a mild headache over how annoying getting this working is. If you're using
Spotify, here's the process:
1. Make sure you're using the [desktop client](https://open.spotify.com/download), and not the
   Windows Store version.
2. Install [Spicetify](https://spicetify.app/docs/getting-started/) and the Spicetify marketplace.
3. Install the
   [WebNowPlaying extension](https://spicetify.app/docs/advanced-usage/extensions/#web-now-playing)
   for Spicetify - if it's not on the marketplace (it wasn't when i made this), you can download the
   file manually
   [here](https://github.com/keifufu/WebNowPlaying-Spicetify/blob/main/dist/webnowplaying-redux.js).
4. Pray.

If you're not using Spotify, you're on your own. If you get things working, submit a pull request
with instructions and I'll probably add them.
