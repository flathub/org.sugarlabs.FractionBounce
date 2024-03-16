# FractionBounce Flatpak

FractionBounce is a game to nudge a bouncing ball to land at an estimate of a given fraction. For example, if "2/3" is displayed on the ball, then the ball must land 2/3 the distance along the bottom.

To know more refer: https://github.com/sugarlabs/fractionbounce

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.FractionBounce.git
cd org.sugarlabs.FractionBounce
flatpak -y --user install flathub org.gnome.{Platform,Sdk}//46
flatpak -y --user install org.sugarlabs.BaseApp//24.04
flatpak-builder --user --force-clean --install build org.sugarlabs.FractionBounce.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.FractionBounce
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.FractionBounce.json
```