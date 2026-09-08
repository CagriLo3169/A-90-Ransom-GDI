# Doors Ransom - GDI Effects Edition

A fan-made visual simulation of the A-90 Ransom with GDI screen effects sourced from open source GDI visual projects.

**This is NOT real malware.** It is a harmless visual simulator with no destructive capabilities. No files are encrypted, no MBR is overwritten, no system damage occurs.

## What's New (GDI Effects)

Added 25 real Win32 GDI screen effects using API calls:

| # | Effect | ROP Code | Source |
|---|--------|----------|--------|
| 1 | Heavy Screen Shake | SRCCOPY | Original |
| 2 | Negative Boxes | DSTINVERT | Original |
| 3 | Tunnel Zoom | SRCCOPY StretchBlt | Original |
| 4 | Vertical Strip Copy | SRCCOPY | Original |
| 5 | Horizontal Band Shift | SRCCOPY | Original |
| 6 | Sine Wave Wobble | SRCCOPY | Original |
| 7 | Psychedelic Blend | SRCPAINT | Original |
| 8 | Ghost Trail | SRCAND | Original |
| 9 | Full Invert | SRCINVERT | Original |
| 10 | Block Scatter | SRCCOPY | Original |
| 11 | Magnifier Zoom | SRCCOPY StretchBlt | Original |
| 12 | Horizontal Flip | SRCCOPY StretchBlt | Holzer |
| 13 | Vertical Flip | SRCCOPY StretchBlt | Holzer |
| 14 | Rainbow PatBlt | PATINVERT | Holzer Rainbow |
| 15 | Dark Stretch | 0x999999 | Thallium |
| 16 | Expanding Circle/Rect | NOTSRCCOPY | Holzer CircleSquare |
| 17 | Heavy Melt Rows | SRCCOPY | Holzer Melter3 |
| 18 | Color Shift | 0x666666/0x999999 | Holzer Colors |
| 19 | Diagonal Stretch | SRCCOPY StretchBlt | Thallium |
| 20 | Bright Stripe | SRCPAINT | Holzer Bright |
| 21 | SRCERASE Blend | 0x00440328 | dlwxzypwwzdtd |
| 22 | Text Scatter | TextOutW | Thallium TextOut |
| 23 | Fast Invert+Shift | NOTSRCCOPY | Holzer Invert |
| 24 | Border Wrap + PatBlt | SRCCOPY + PATINVERT | salinewin |
| 25 | **Melt (1px drip)** | SRCCOPY | **Python-gdi-repo** |
| 26 | **Expanding Circles** | NOTSRCCOPY + EllipticRgn | **Python-gdi-repo** |
| 27 | **Rainbow Hell** | PATINVERT HSV | **Python-gdi-repo** |
| 28 | **NOTSRCCOPY Shake** | NOTSRCCOPY | **BwHell** |
| 29 | **Sine Wave** | SRCCOPY | **Python-GDI-Screen-Effects** |
| 30 | **Tunnel Zoom** | SRCCOPY StretchBlt | **Python-gdi-repo** |
| 31 | **Melt Wide** | SRCCOPY | **Python-gdi-repo** |
| 32 | **Diagonal Stretch** | SRCCOPY StretchBlt | **Python-gdi-repo** |
| 33 | **Multi Band Shift** | SRCCOPY | **Python-GDI-Screen-Effects** |
| 34 | **Heavy Invert+Shift** | SRCINVERT | Original variant |
| 35 | **Big Region Invert** | NOTSRCCOPY | **Python-gdi-repo** |

### Chain System

- **Max chain limit increased**: 25 → 35
- 50% chance to add +1 effect each step, starts at 1
- Average ~3-4 effects per frame, rare jackpot 20+ effects

## How to Run

### Portable EXE (recommended)
```
dist\ransom.exe
```

### From Source
```
pip install pygame Pillow
python doors_ransom.py
```

### Hotkeys
- `+` / `=` : Trigger immediate encounter
- `-` : Restore system effects
- `*` : Exit application
- `ESC` : Force quit

## Controls

- Drag/throw coins to the ransom note to pay
- Collect all coins to "pay" the ransom
- Miss the STOP screen and GDI effects activate
- After attack phase, downloading animation plays
- Finally the ransom note appears with coin game

## Credits

- **Original Project**: [Doors-Ransom-A-90-Simulation](https://github.com/masashira0212-stack/Doors-Ransom-A-90-Simulation/releases/tag/v1.2.0.2) by masashira0212-stack
- **GDI Effects inspired by**:
  - [Holzer](https://github.com/pankoza2-pl/Holzer-safety/releases) - Flip, Rainbow, Melter, CircleSquare, Colors, Bright, Invert effects
  - [Thallium](https://github.com/pankoza2-pl/Thallium.exe/) - Dark stretch, TextOut, diagonal zoom effects
  - [dlwxzypwwzdtd](https://github.com/pankoza2-pl/dlwxzypwwzdtd.exe-Malware) - SRCERASE, gradient, shader effects
  - [salinewin](https://github.com/pankoza2-pl/salinewin.exe-Malware) - Bouncing balls, bezier, sine wave, profect effects

## Requirements

- Windows 10/11
- Python 3.11+ (for source)
- pygame, Pillow

## Disclaimer

This project is for educational and entertainment purposes only. The GDI effects are purely visual and do not damage any files, system data, or hardware. Always use virtual machines for testing.

## License
MIT LICENSE

Original project: See [Doors-Ransom-A-90-Simulation](https://github.com/masashira0212-stack/Doors-Ransom-A-90-Simulation) repository.
GDI effects: Public domain techniques from the GDI malware research community.
