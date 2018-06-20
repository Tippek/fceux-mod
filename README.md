# fceux-mod
Changes from fceux 2.2.3:

- RAM: 0x0000-0x7FFF;
- 16 palettes for sprites and 4 for background(0x3f20 not mirrored, unused bits in sprite attribute)
- 256 sprites on screen(instead 64, activated by header)
- VT03 mode(activated by header): based on vt03 mapper. 4bpp color mode. Many limits and conditions. 16 colors on palette, only 12 palettes for sprites and 4 on background.
- 512 sprites (activated by header and unused bit sprite attribute)
- Overclock DPCM 7bit fix(but make sound some dirty, fix ideally working on mednafen)
- New CPU register "Z" and new opcodes with Z and other opcodes(example DVA - division A or DMA - dimension A)
- Extra background with own $3005-$3007 registers. Have low priority(behind background)
- 127 color mode(allow to use 127 color for palette instead 64)
- $401C register - stop timestamp increasing(any value to stop, 0 to continue). Allow to insert code without break timings.
- 10 Players(not finished)



TODO:
- MMC5 and 16x8 sprites mode probably broken(?).
- Allow Sprites using background palette(?).
- Color #00 in palette now broken, dirty fix(!).
- Most changes works only with 256 sprites(?).
- All changes presents in debugger(?).
- New PPU(??).
