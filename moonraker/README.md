# Moonraker Configuration

This directory contains Moonraker configuration files.

## Files

- **moonraker.conf** - Main Moonraker configuration file

## About Moonraker

Moonraker is a web API server for Klipper that enables:
- Web-based control interfaces (Fluidd, Mainsail)
- File management
- Update management
- Webcam streaming
- Power control
- And more

## Usage

Copy your Moonraker configuration from your printer:

```bash
scp pi@<printer-ip>:~/printer_data/config/moonraker.conf ./
```

Or from the typical Moonraker config location:
```bash
scp pi@<printer-ip>:~/moonraker.conf ./
```

## Important

The Moonraker configuration may contain sensitive information such as:
- API keys
- Network settings
- Authorization tokens

Review the file before committing to ensure no sensitive data is included, or use environment variables/secrets for sensitive values.
