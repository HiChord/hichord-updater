# HiChord Firmware Updater

Web-based firmware updater for HiChord synthesizers that already have the bootloader installed.

## Usage

This tool is for updating firmware on **commercial HiChords** that already have the bootloader installed. If you need to install the bootloader first, use the [HiChord Production Uploader](https://github.com/HiChord/hichord-uploader) instead.

### Update Firmware

1. Visit: https://hichord.github.io/hichord-updater
2. Follow the on-screen instructions to enter DFU mode and update firmware

### Enter DFU Mode

Press and hold all three menu buttons simultaneously: **FN1 + FN2 + FN3**

The HiChord display will show "Entering DFU Mode" and the LED will begin pulsing.

## Browser Compatibility

This tool uses WebUSB and requires:
- Google Chrome (recommended)
- Microsoft Edge
- Other Chromium-based browsers

**Not supported:** Firefox, Safari

## Technical Details

- Uses STM32 DFU protocol over WebUSB
- Firmware is uploaded to QSPI flash at address 0x90040000
- Based on Electro-Smith Programmer implementation
- No local installation required - runs entirely in the browser

## Development

To test locally:
```bash
python3 -m http.server 8000
```

Then visit: http://localhost:8000

## License

MIT License
