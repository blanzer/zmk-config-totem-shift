<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/TOTEM_logo_dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/TOTEM_logo_bright.svg">
  <img alt="TOTEM logo font" src="/docs/images/TOTEM_logo_bright.svg">
</picture>

<h1 align="center">T O T E M - S H I F T</h1>

# ZMK CONFIG FOR THE TOTEM-SHIFT SPLIT KEYBOARD

[Here](https://github.com/Endracion/TOTEM-SHIFT) you can find my updated TOTEM-SHIFT hardware files.\
[Here](https://github.com/GEIGEIGEIST/totem) you can find the original hardware files and build guide.

TOTEM-SHIFT is a modified 38 keys column-staggered split keyboard originally by GEIGEIGEIST running [ZMK](https://zmk.dev/). It's meant to be used with a SEEED XIAO BLE.

It includes these additional projects and features:
- caksoylar's [RGB LED Widget](https://github.com/caksoylar/zmk-rgbled-widget)
- carrefinho's [Prospector Dongle](https://github.com/carrefinho/prospector)
- Support for [ZMK Studio](https://zmk.studio/) for keyboard layout adjustment without flashing

![TOTEM layout](/docs/images/TOTEM_layout.svg)

## Index numbers

**Left Hand**
 0  1  2  3  4      (Top Row)
10 11 12 13 14      (Home Row)
20 21 22 23 24 25   (Bottom Row - 20 is Outer Pinky Tab)
         32 33 34   (Thumbs: Outer, Middle, Inner)


**Right Hand**
      5  6  7  8  9 (Top Row)
     15 16 17 18 19 (Home Row)
  26 27 28 29 30 31 (Bottom Row - 31 is Outer Pinky Minus)
  35 36 37          (Thumbs: Inner, Middle, Outer)

## HOW TO USE

- fork this repo
- `git clone` your repo, to create a local copy on your PC (you can use the [command line](https://www.atlassian.com/git/tutorials) or [github desktop](https://desktop.github.com/))
- adjust the totem.keymap file (find all the keycodes on [the zmk docs pages](https://zmk.dev/docs/codes/))
- `git push` your repo to your fork
- on the GitHub page of your fork navigate to "Actions"
- scroll down and unzip the `firmware.zip` archive that contains the latest firmware
- connect the left half of the TOTEM to your PC, press reset twice
- the keyboard should now appear as a mass storage device
- drag'n'drop the `totem_left-seeeduino_xiao_ble-zmk.uf2` file from the archive onto the storage device
- repeat this process with the right half and the `totem_right-seeeduino_xiao_ble-zmk.uf2` file.