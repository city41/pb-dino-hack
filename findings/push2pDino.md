# Push 2P Dino

## Sprites

It uses 355, 356 and 213, 214

### Tiles/Palettes

| 355     | 356     |
| ------- | ------- |
| 8b99/92 | 8b90/92 |
| 8b91/92 | 8b97/92 |

ROM tile map

```
00E2D0: 8B99 0000 8B90 0000 8B91 0000 8B92 0000 ................

00E2F8:  8B99 0000 8B90 0000 8B96 0000 8B97 0000  ................
```

Palette 92

Palette RAM starts at $400,000 in main memory
Palette $92 then can be located by doing `$400000 + $92 * $20` which is `$401240`

Then from there, run MAME with the debugger. Pause the game once the dino is on screen, then
`dump palette.txt,401240,20`, and the resulting file will be:

```
401240: 0000 0111 7666 7ABD 7EEE 0048 106C 108E ....vfz.~..H.l..
401250: 54BF 39DF 2C50 6F60 7B7A 2840 6D80 6FC0 T.9.,Po`{z(@m.o.
```
