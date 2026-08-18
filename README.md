# Face Mask Detection — Arduino Nano 33 BLE Sense

**EE 446: Tiny Machine Learning for Ultra Low-Power Edge Computing | University of Washington, Spring 2026**

Real-time face mask detection ("with mask" vs "without mask") from the onboard camera-equivalent image pipeline, built entirely in Edge Impulse Studio and deployed to an Arduino Nano 33 BLE Sense.

---

## What it does

Classifies a captured image as **With Mask** or **Without Mask** using an image classification model trained in Edge Impulse Studio, then compiled to firmware for the Nano 33 BLE Sense.

Unlike the other labs in this course, this project's full pipeline (data upload, transfer learning, model training, and firmware export) was built and run entirely within Edge Impulse Studio — there is no local Python notebook. The public Edge Impulse project is linked below.

---

## Repository contents

```
Lab4_EE446.pdf     ← Written report
firmware/           ← Edge Impulse-compiled firmware for Arduino Nano 33 BLE Sense
  firmware-arduino-nano-33-ble-sense.ino.bin
  firmware-arduino-nano-33-ble-sense.ino.with_bootloader.bin
  flash_windows.bat / flash_mac.command / flash_linux.sh
```

---

## Dataset

Trained on a face-mask image classification dataset (~11,800 images: 10,000 train / ~1,000 test / 800 validation, split evenly between `WithMask` and `WithoutMask` classes). The dataset is not included in this repo due to size — it's the widely-used public "Face Mask 12K Images" dataset available on Kaggle. To retrain, download a similarly-structured with-mask / without-mask image dataset and upload it to the Edge Impulse project below.

---

## Edge Impulse project

- **Project:** [sdadhich / EE446 Lab 4](https://studio.edgeimpulse.com/public/972594/live) (public — clone to retrain or redeploy)

---

## Quick start

### Flash the pre-built firmware

```bash
# Windows
firmware\flash_windows.bat

# Mac
firmware/flash_mac.command

# Linux
bash firmware/flash_linux.sh
```

### Retrain

1. Clone the [Edge Impulse project](https://studio.edgeimpulse.com/public/972594/live)
2. Upload your own with-mask / without-mask image dataset (or reuse the Kaggle dataset referenced above)
3. Retrain the impulse in Edge Impulse Studio
4. Deploy → build firmware for Arduino Nano 33 BLE Sense → flash using the scripts above

---

## Hardware

- **Arduino Nano 33 BLE Sense** (Nordic nRF52840, 256 KB flash, 64 KB RAM)

---

## Authors

Sparsh Dadhich — University of Washington, ECE / Neuroscience
