# Deelab dee1800FL PCB

![dee1800FL](updating image)

Layout available here: [KLE](http://www.keyboard-layout-editor.com/#/gists/2b73d56f989abd9a6dcb6a0afe722066) 

## Specification:
* Layout 1800 without function row
* USB Type C
* Powered by RP2040 MCU (ARM-Based)
* Underglow RGB on left and right side
* Encoder supported (Num Lock Key)
* Programmable with QMK and VIA
* ESD protection
* PCB colour: Black

## QMK Firmware
You can find and modify source [here](https://github.com/Deemen17/qmk_firmware/tree/deelab_develop/keyboards/deelab/dee1800fl)

## File detail:
* `deelab_dee1800FL_via_v3.json` : for loading on [VIA](https://usevia.app/)
* `deelab_dee1800FL_via.uf2` : firmware for flashing

## How to flash new firmware:
* **Step 1**: Enter the bootloader in 3 ways
    - Bootmagic reset: Hold down the Esc key and plug in the keyboard (not recommended because EEPROM loss)
    - Physical reset button: Press and hold the button BOOT (near Space Key) on the back of the PCB, then plug USB onto PC
    - Keycode in layout: Press the key mapped to `QK_BOOT` if it is available
* **Step 2**: *Copy and paste* or *click hold and move* the `deelab_dee1800FL_via.uf2` into **RPI-RP2** mass storage device appeared.
