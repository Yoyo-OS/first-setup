<div align="center">
    <img src="data/icons/hicolor/scalable/apps/org.yoyoos.FirstSetup.svg" height="128">
    <h1>Yoyo OS First Setup</h1>
    <p>This utility is meant to be used in <a href="https://github.com/yoyo-os">Yoyo OS</a>
    as a first-setup wizard. Its purpose is to help the user to configure the
    system to their needs, e.g. by configuring snap, flatpak, flathub, etc.</p>
    <hr />
    <a href="https://hosted.weblate.org/engage/yoyo-os/">
<img src="https://hosted.weblate.org/widgets/yoyo-os/-/control-center/svg-badge.svg" alt="Stato traduzione" />
</a>
    <br />
    <img src="data/screenshot-1.png">
</div>

## Copyright Notice
This project is forked from Vanilla os, the purpose is to adapt to the special functions of Yoyo os.
We follow the original GPLv3 agreement, modify and retain the original open source agreement, please note that if there are related vanilla trademarks or other vanilla logos, our organization (Yoyo OS team) has no commercial rights.

## Build
### Dependencies
- build-essential
- meson
- libadwaita-1-dev
- gettext
- desktop-file-utils

### Build
```bash
meson build
ninja -C build
```

### Install
```bash
sudo ninja -C build install
```

## Run
```bash
yoyo-first-setup
```

### Using custom recipes
Place a new recipe in `/etc/yoyo-first-setup/recipe.json` or launch the
utility with the `YOYO_CUSTOM_RECIPE` environment variable set to the path
of the recipe.
