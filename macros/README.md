# Klipper Macros

This directory contains custom G-code macros for your Klipper printer.

## Common Macros

Typical macros you might store here:

- **print_start.cfg** - Start print macro (heating, homing, purging)
- **print_end.cfg** - End print macro (cooldown, park position)
- **pause_resume.cfg** - Pause and resume macros
- **filament_change.cfg** - Filament change procedures
- **bed_mesh.cfg** - Bed mesh calibration macros
- **calibration.cfg** - Calibration routines (PID, bed leveling, etc.)
- **utilities.cfg** - Utility macros (LED control, fans, etc.)

## Usage

Copy your macro files from `~/printer_data/config/` on your printer to this directory.

Example:
```bash
scp pi@<printer-ip>:~/printer_data/config/macros/*.cfg ./
```

Make sure these macro files are properly included in your main `printer.cfg` using:
```
[include macros/*.cfg]
```
