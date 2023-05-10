# iris-via-qmk
My Keebio Iris Rev7 layout with 6 layers, via support, custom qmk configurations and 6 layers.

# Introduction

The default Iris layout for QMK is very usable, especially 
since it comes with Via preinstalled. I particularily like
Via because allows you to change layouts on the fly, without 
having to flash the keyboard each time you want to make a change.

I particularily like being able to change my layout
on any computer that has chrome using Via, even without 
any custom software installed. 

However, there are some limitations to the stock layout.
First, it is limited to 4 layers, and second, you are
limited to only the settings available within Via.
There are many configurations in qmk that one might
want but are not configurable in Via.

The good news is that the stock firmware is the
compiled version of the `keyboards/keebio/iris/keymaps/via`
keyboard layout in the qmk repository. Knowing this, I 
copied and modified the keymap to feature the following:

* Via support
* 6 configurable layers that can be changed with Via
* Ability to set qmk configurations to help with 
    setups such as Home Row Modifiers.


# How to install:

1. Set up the [QMK environment](https://docs.qmk.fm/#/newbs_getting_started)

2. Add this repository as a git submodule in this location:


    ```
    keyboards/keebio/iris/keymaps/via6
    ```

3. Navigate to the `keymaps` directory and compile the code.

    ``` bash
    cd keyboards/keebio/iris/keymaps
    qmk compile -kb keebio/iris/rev7 -km via6
    ```

The compiled firmware will be located in the root directory of the qmk repository. 

4. Flash the firmware to both sides of your keyboard.

    I use the [QMK Toolbox](https://docs-gitbook.keeb.io/docs/flashing-firmware#using-qmk-toolbox)

    Remember to clear the EEPROM memory before flashing.

5. Open chrome, navigate to https://usevia.app/ and connect your Iris.

6. Confirm that you can see 6 layouts

# How to use:

## Modify your layout
1. Modify your layout as you see fit in Via.
2. Save your layout as a json file. You can then use this 
    json file to load your layout again if you decide
    to flash your keyboard again.


## Modify QMK configurations
1. Add the changes required in the `config.h`, `keymap.c` or `rules.mk` files
2. Recompile
3. Flash the boards again
4. Reload your via layout. 