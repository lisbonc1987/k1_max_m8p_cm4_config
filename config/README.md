# Klipper Configuration Files

This directory contains the main Klipper configuration files for the K1 Max M8P CM4 setup.

## Files

Place your Klipper configuration files here:

- **printer.cfg** - Main printer configuration file
- **stepper.cfg** - Stepper motor configurations (if separated)
- **extruder.cfg** - Extruder settings (if separated)
- **bed.cfg** - Heated bed configuration (if separated)
- **input_shaper.cfg** - Input shaper calibration data (if separated)
- ***.cfg** - Any other configuration files included in your printer.cfg

## Usage

Copy your configuration files from `~/printer_data/config/` on your printer to this directory.

Example:
```bash
scp pi@<printer-ip>:~/printer_data/config/*.cfg ./
```
