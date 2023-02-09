# Deemen17 dee1800FL PCB
![dee1800FL-front](https://user-images.githubusercontent.com/95753855/217714488-8f199941-adea-4f22-a586-95d7c693f6ab.png)
![z4095475175387_361c0af3d0ab31d3d8345491f15e48ab](https://user-images.githubusercontent.com/95753855/217714428-fb10f373-a566-44e7-9264-a3ad0ba5959e.jpg)

Layout available here: [KLE](http://www.keyboard-layout-editor.com/#/gists/2b73d56f989abd9a6dcb6a0afe722066) 

## Specification:
* 1.6mm thickness
* Layout 1800 function row less
* USB Type C
* Powered by RP2040 MCU
* Underglow RGB on left and right side
* Encoder supported (Num Lock Key)
* Programmable with QMK and VIA
* ESD protection
* Breakway USB area with JST for daughterboard
* PCB colour: Black

## QMK Firmware
You can find and modify source [here](https://github.com/Deemen17/qmk_firmware/tree/deelab_develop/keyboards/deelab/dee1800fl)

## Files detail:
* `deemen17_dee1800FL_via_v3.json` : for loading on [VIA](https://usevia.app/)
* `deemen17_dee1800FL_via.uf2` : firmware for flashing

### How to download files: 
Move your cursor to files above, right click then press **Save link as...**

## How to flash new firmware:
* **Step 1**: Enter the bootloader in 3 ways
    - Keycode in layout: Press the key mapped to `QK_BOOT` in **keymap.c** or `Reset` in VIA if it is available (Recommended)
    - Physical reset button: Press and hold the button BOOT (near Space Key) on the back of the PCB, then plug USB onto PC (Recommended)
    - Bootmagic reset: Hold down the Esc key and plug in the keyboard (Not recommended because EEPROM loss, you will lose saved keymap on VIA) (Factory reset)

* **Step 2**: *Copy and paste* or *drag and drop* the `deelab_dee1800FL_via.uf2` into **RPI-RP2** mass storage device appeared.

## How to factory reset:
Sometime you may make a mess keymap on VIA and want to make your PCB works like brand new one.

* **Step 1**: Enter bootloader via Bootmagic reset: Hold down the Esc key and plug in the keyboard.
By this bootmagic method, everything stores in EEPROM include saved VIA keymaped will be deleted.

* **Step 2**: *Copy and paste* or *drag and drop* the `deelab_dee1800FL_via.uf2` into **RPI-RP2** mass storage device appeared.
