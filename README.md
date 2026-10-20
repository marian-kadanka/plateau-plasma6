# Plateau (Plasma 6)

Plateau Plasma Style by Jamboarder, updated for KDE Plasma 6.

## Original

The original theme is Plateau by Jamboarder (jamboarder@yahoo.com), published in 2009 on the KDE Store: https://store.kde.org/p/998864

The artwork in `dialogs/` and `widgets/` is Jamboarder's, except for the changes listed below and `widgets/actionbutton.svgz`, which comes from the Breeze Plasma Style in KDE's libplasma 6.8 (KDE Visual Design Group, LGPL).

## Changes

Plasma 6 treats a theme that does not declare `X-Plasma-API` 5 or later as a KDE 4 theme and draws everything except window backgrounds with the theme's button colours. In Plateau those had black text, so the application launcher's search bar and header, the tab bars in popups and text fields showed black text on a black background. Several other parts that Plasma 6 draws differently from KDE 4 were also dark on black.

- `metadata.desktop` is replaced by `metadata.json`, which declares `"X-Plasma-API": "5.0"`. The theme Id is `plateau-plasma6`, so it installs alongside the original instead of replacing it.
- Buttons: push buttons in `widgets/button.svgz` are dark warm brown (`#534932`) instead of cream, and button text is cream, because Plasma 6 gives flat buttons on the black popups the same text colour as push buttons.
- Radio buttons: Plateau has no radio button artwork, so Plasma draws them with `widgets/actionbutton.svgz`. The Breeze version added here has a cream outline instead of a dark one, so unselected radio buttons show on black.
- Progress bars: the unfilled track in `widgets/bar_meter_horizontal.svgz` was transparent and is now `78,70,49`.
- Pager: the current and the hovered desktop in `widgets/pager.svgz` are filled `115,102,69` and `83,73,50` instead of a faint white tint.
- `colors`: every text colour reaches at least 4.5:1 contrast on the surface it is drawn on. Tooltips have cream text on black, switch knobs and radio button fills use `115,102,69`, error, warning and success colours are bright enough for black backgrounds and the dark buttons, the selection blue is `46,115,190`, and placeholder text in text fields is dark cream `153,139,105` instead of white.

## Installation

System Settings › Plasma Style › Install from File…, then pick the `.tar.gz` from the KDE Store, or clone this repository into a folder named exactly after the theme Id:

```
git clone https://github.com/marian-kadanka/plateau-plasma6 ~/.local/share/plasma/desktoptheme/plateau-plasma6
```

## Licence

GNU General Public License, version 2 or later (GPL-2.0-or-later). The original theme declares its licence as GPL without a version number (`X-KDE-PluginInfo-License=GPL`), which under the GPL's own terms allows any published version to be chosen. `widgets/actionbutton.svgz` is LGPL, as part of KDE's Breeze Plasma Style.

Plasma 6 changes (c) Marian Kadanka, https://kadanka.net/
