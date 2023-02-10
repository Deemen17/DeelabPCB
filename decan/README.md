# Deemen17 Decan PCB
![Decan_back](https://user-images.githubusercontent.com/95753855/218182309-5900a36c-d996-4780-948e-a1f92b90ae09.png)

## Specification:
* Zodiac - Mechlovin' Pisces PCB compatible
* 1.6mm thickness
* Layout 65% available here: [KLE](http://www.keyboard-layout-editor.com/#/gists/c0c59d30865d535b082bd34e2c76114a) 
* Solder only
* USB Type C
* PCB colour: Purple
* ESD protection
* Powered by ATmega32u4 MCU
* Programmable with QMK and VIA
* Upper RGB LEDs around (Need to short the JP1 near Backspace Key)
* Caps Lock LED indication

## QMK Firmware
You can find and modify source [here](updating)

## Files detail:
* `deemen17_decan_via.hex` : firmware for flashing

### How to download files: 
Move your cursor to files above, right click then press **Save link as...**

## How to flash new firmware:
* **Step 1**: Enter the bootloader in 3 ways
    - Keycode in layout: Press the key mapped to `QK_BOOT` in **keymap.c** or `Reset` in VIA if it is available (Recommended)
    - Physical reset button: Plug USB onto PC, double press the button BOOT (Recommended)
    - Bootmagic reset: Hold down the Esc key and plug in the keyboard (Not recommended because EEPROM loss, you will lose saved keymap on VIA) (Factory reset)

* **Step 2**: *Copy and paste* or *drag and drop* the `deelab_dee1800FL_via.uf2` into **RPI-RP2** mass storage device appeared.

## How to factory reset:
Sometime you may make a mess keymap on VIA and want to make your PCB works like brand new one.

* **Step 1**: Enter bootloader via Bootmagic reset: Hold down the Esc key and plug in the keyboard.
By this bootmagic method, everything stores in EEPROM include saved VIA keymaped will be deleted.

* **Step 2**: *Copy and paste* or *drag and drop* the `deelab_dee1800FL_via.uf2` into **RPI-RP2** mass storage device appeared.
