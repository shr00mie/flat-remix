# Flat Remix icons on Ubuntu (GNOME 50+)

## Dependencies

```bash
sudo apt update
sudo apt install -y make gtk-update-icon-cache
```

## Install all icon variants

```bash
git clone https://github.com/shr00mie/flat-remix.git
cd flat-remix
sudo make install PREFIX=/usr
```

This fork removes existing `/usr/share/icons/Flat-Remix-*` directories before
installing, which avoids failures when upgrading over older packages that left
dangling symlinks (for example `jadx-gui.svg`).

## Apply Red icon theme

```bash
gsettings set org.gnome.desktop.interface icon-theme 'Flat-Remix-Red-Dark'
```

## Pair with GNOME Shell theme

See [flat-remix-gnome](https://github.com/shr00mie/flat-remix-gnome):

```bash
git clone https://github.com/shr00mie/flat-remix-gnome.git
cd flat-remix-gnome
./install-user-themes.sh
gsettings set org.gnome.shell.extensions.user-theme name 'Flat-Remix-Red-Dark-fullPanel'
```

Log out and back in after changing the shell theme on Wayland.
