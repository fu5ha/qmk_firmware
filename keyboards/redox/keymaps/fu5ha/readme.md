# `fu5ha`'s keymap

Uses the 42keebs.io Frood rev7 (RP2040 based pro micro pinout MCU).

Also uses 1000hz usb polling rate and eager per-key debouncing.

Setup with:

```
qmk config user.keyboard=redox/rev1/base
qmk config user.keymap=fu5ha
```

Update `keymap.c` by downloading new `fu5ha.json` then running:

```
qmk json2c -o keyboards/redox/keymaps/fu5ha/keymap.c keyboards/redox/keymaps/fu5ha/fu5ha.json
```

Docker/Podman setup prepend with `util/docker_cmd.sh`

If `config.h` is set to `EE_HANDS`, then you need to flash twice, left then right.

```
qmk flash -bl uf2-split-left
qmk flash -bl uf2-split-right
```

Otherwise just build once then drag to the USB when each side is in bootloader mode.

