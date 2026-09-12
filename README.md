# Face Mask Detection

Edge Impulse firmware export for an EE 446 TinyML Lab 4 face-mask detection project.

The checked-in firmware identifies the model author as `sdadhich` and the model name as `Mask Detection`. The included report labels the task with `Without mask` and `With mask on` examples and links to the public Edge Impulse project.

## What Is Included

- `Lab4_EE446.pdf`: one-page project report.
- `firmware/firmware-arduino-nano-33-ble-sense.ino.bin`: prebuilt firmware image.
- `firmware/firmware-arduino-nano-33-ble-sense.ino.with_bootloader.bin`: prebuilt firmware image with bootloader.
- `firmware/flash_windows.bat`: Windows flashing script.
- `firmware/flash_mac.command`: macOS flashing script.
- `firmware/flash_linux.sh`: Linux flashing script.

This repository does not include local training notebooks, model source code, or the training image dataset.

## Hardware And Tools

- Arduino Nano 33 BLE Sense.
- Arduino CLI available on `PATH`.
- Arduino Mbed Nano core, installed by the flash scripts if missing.
- Edge Impulse CLI tools for running the flashed impulse from a computer.

The flash scripts expect Arduino CLI 0.33.x or newer and upload with the Arduino Nano 33 BLE board FQBN.

## Flash The Firmware

Connect the Arduino Nano 33 BLE Sense, then run the script for your platform:

```bash
# Windows
firmware\flash_windows.bat

# macOS
firmware/flash_mac.command

# Linux
bash firmware/flash_linux.sh
```

After flashing, the scripts print these Edge Impulse commands:

```bash
edge-impulse-daemon
edge-impulse-run-impulse
```

## Edge Impulse Project

The included report links to this public Edge Impulse project:

https://studio.edgeimpulse.com/public/972594/live

## Credits

- Sparsh Dadhich
- University of Washington EE 446 Tiny Machine Learning
- Firmware generated with Edge Impulse for Arduino Nano 33 BLE Sense

## License

This repository is licensed under the MIT License. See `LICENSE`.
