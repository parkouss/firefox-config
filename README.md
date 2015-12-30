# (my) firefox config

Some configuration to make **firefox** awesome to me.

I use the excellent [keysnail][] for emacs-like navigation.

Fork this repository and make your own changes if you find it useful and want to customize it.


## Brief tour

Once installed, restart **firefox**. Now you have emacs-like keybindings:

- `C-s` for incremental search
- `C-r` for incremental backward search
- Navigation with emacs keybindings, and the mark is supported (`C-<space>`)
- `C-x h` to select all
- ...

Tab navigation is like emacs buffer navigation:

- `C-x <left>` select previous tab
- `C-x <right>` select next tab
- `C-x b` choose your tab using Tanything

Feel free to look at the configuration file (.keysnail.js), and make your own changes!

[Find as you type][] is an awesome functionality of firefox. I find it really cool
to follow hyperlinks, just by typing the beginning of the title of the link.

Type `'` then start typing - the first matching link encountered will be highlighted - from
there, you can type `Return` to follow the link, or `C-s` / `C-r` to navigate to other matching
links!

This is enabled in user.js.

## Installation

Obviously you need firefox. Then install [keysnail][] and [the Tanything keysnail plugin][tanything].

I'm currently trying [uBlock Origin][] to block ads. So far I used [Adbblock Plus][adBlock]
which is also excellent. Install one of them to get rid of a ton of advertising stuff wile browsing.

After that:

```bash
# path to your firefox profile, you may have to change that.
PATH_TO_PROFILE=~/.mozilla/firefox/*.default

git clone https://github.com/parkouss/firefox-config ~/.firefox-config
ln -s ~/.firefox-config/.keysnail.js ~/.keysnail.js
ln -s ~/.firefox-config/user.js $PATH_TO_PROFILE/user.js
```

Or copy the files instead at the right locations.

[keysnail]: https://github.com/mooz/keysnail
[tanything]: https://github.com/mooz/keysnail/wiki/plugin
[uBlock Origin]: https://addons.mozilla.org/en-us/firefox/addon/ublock-origin/
[adBlock]: https://adblockplus.org/
[Find as you type]: http://website-archive.mozilla.org/www.mozilla.org/access/access/type-ahead/
