# K1 Max M8P CM4 Klipper Configuration Backup

This repository serves as a backup and version control system for Klipper configuration files used on the K1 Max printer with M8P and CM4 (Compute Module 4) conversion.

## About

This repository contains all configuration files for my Klipper 3D printer setup:
- **Printer:** Creality K1 Max
- **Control Board:** BTT M8P (Manta M8P)
- **Computing Module:** Raspberry Pi CM4

## Directory Structure

```
k1_max_m8p_cm4_config/
├── config/              # Main Klipper configuration files
│   ├── printer.cfg      # Main printer configuration
│   └── ...              # Additional config files
├── macros/              # Custom G-code macros
├── moonraker/           # Moonraker configuration
└── README.md            # This file
```

## Backup Instructions

### Manual Backup

To backup your configuration files to this repository:

1. Copy your configuration files from your Klipper instance:
   ```bash
   # SSH into your printer
   ssh pi@<printer-ip>
   
   # Navigate to Klipper config directory (usually ~/printer_data/config)
   cd ~/printer_data/config
   ```

2. Copy the files to your local machine and then to this repository:
   ```bash
   scp pi@<printer-ip>:~/printer_data/config/*.cfg ./config/
   ```

3. Commit and push changes:
   ```bash
   git add .
   git commit -m "Update Klipper configuration - $(date +%Y-%m-%d)"
   git push
   ```

### Automated Backup

Consider setting up a cron job or script to automatically backup configurations periodically.

## Restore Instructions

To restore configuration files from this repository:

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/lisbonc1987/k1_max_m8p_cm4_config.git
   cd k1_max_m8p_cm4_config
   ```

2. Copy files to your printer:
   ```bash
   scp config/*.cfg pi@<printer-ip>:~/printer_data/config/
   ```

3. Restart Klipper:
   ```bash
   ssh pi@<printer-ip>
   sudo systemctl restart klipper
   ```

## Important Files

- **printer.cfg** - Main Klipper configuration file
- **moonraker.conf** - Moonraker web API configuration
- **macros/** - Custom macros for print start/end, bed mesh, etc.

## Safety Notes

⚠️ **Important:**
- Always review configuration files before applying them to your printer
- Test configuration changes carefully
- Keep backups of working configurations
- Document any hardware changes that require config updates

## Contributing

This is a personal backup repository, but feel free to reference these configurations for your own K1 Max M8P CM4 conversion.

## License

These configuration files are provided as-is for personal use and reference.
