# Doors Ransom - GDI Effects Edition

A fan-made visual simulation of the A-90 Ransom with GDI screen effects sourced from open source GDI visual projects.

**This is NOT real malware.** It is a harmless visual simulator with no destructive capabilities. No files are encrypted, no MBR is overwritten, no system damage occurs.

## What's New (GDI Effects)

Added 25 real Win32 GDI screen effects using API calls:

| # | Effect | Source |
|---|--------|--------|
| 1 | Screen shake (SRCCOPY offset) | Custom |
| 2 | Negative boxes (DSTINVERT) | Custom |
| 3 | Tunnel zoom (StretchBlt) | Custom |
| 4 | Vertical strip copy | Custom |
| 5 | Horizontal band shift | Custom |
| 6 | Sine wave wobble | Custom |
| 7 | Psychedelic blend (SRCPAINT) | Custom |
| 8 | Ghost trail (SRCAND) | Custom |
| 9 | Full invert (SRCINVERT) | Custom |
| 10 | Block scatter | Custom |
| 11 | Magnifier zoom | Custom |
| 12 | Horizontal flip | Holzer |
| 13 | Vertical flip | Holzer |
| 14 | Rainbow PatBlt | Holzer Rainbow |
| 15 | Dark stretch (0x999999) | Thallium |
| 16 | Expanding circle/rect (NOTSRCCOPY) | Holzer CircleSquare |
| 17 | Horizontal melter | Holzer Melter3 |
| 18 | Color shift (0x666666/0x999999) | Holzer Colors |
| 19 | Diagonal stretch zoom | Thallium |
| 20 | Bright stripe (SRCPAINT) | Holzer Bright |
| 21 | SRCERASE blend | dlwxzypwwzdtd |
| 22 | Rainbow text scatter | Thallium TextOut |
| 23 | Fast invert+shift | Holzer Invert |
| 24 | Border wrap + PatBlt | salinewin profect |
| 25 | Subtle shake | Custom |

### Chain System

Each effect triggers a chain multiplier:
- Starts at 1 effect
- Each step: 50% stay / 50% add +1
- Max 25 effects per frame
- Average: ~2-3 effects per frame
- Rare jackpot: 15+ effects (~2.7% chance in 90secs.)

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
