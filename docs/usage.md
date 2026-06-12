# Usage Guide

## Pre-recording Preparations

1. Prepare or recharge the battery. WILD includes a DC/DC buck-boost converter and accepts a wide input range from 2 V to 4.5 V. The battery must supply the minimum power required by the selected recording mode and should support more than 30 mW peak power during boot.

   ![Battery](images/WIrelessEphys_Github_9_batteries.jpg)

   [Battery selection table](https://github.com/zifangzhao/Neurologger/tree/main/docs/LipoBattery_selection.csv)

2. Format the microSD card using WILD_console. Make sure WILD_console has administrator privileges. Some SanDisk microSD cards may not be supported; Samsung EVO series or Lexar cards are recommended. Avoid unnecessarily high-speed cards because they can consume more power.

   ![SD card](images/WIrelessEphys_Github_10_SDcard_power.jpg)

3. Insert the microSD card into WILD.

4. Connect the battery. The device will start booting. A blue LED turns on when the device starts correctly, then turns off when the device enters low-power mode. If a firmware image is loaded on the microSD card, the device checks the image and starts upgrading. The LED blinks during upgrade, which takes about 10 seconds depending on image size.

   ![IO configuration](images/WIrelessEphys_Github_6_Connectors.jpg)

## Connecting

1. Launch `WILD_console.exe`.
2. Select the device from the port dropdown after BLE scan.
3. Connect and wait for synchronization. A number at the bottom of the panel should increase when communication is working.

If connection succeeds but synchronization does not start, or the TX number does not increase, check the microSD card.

## Recording

1. Configure closed-loop functions in the closed-loop panel.
2. Configure recording speed with the custom speed dropdown.
3. For multi-device recording, use **Wait for start** to coordinate multiple WILD_console instances. Bluetooth start jitter is expected to be below 50 ms, while the recording start timestamp is recorded from the calibrated high-precision clock.
4. Click **Recording Start**. Data streaming starts after about 1 second.
5. Click **Recording Stop** when the experiment is finished. If the battery dies during recording, completed recording files should remain available on the microSD card.

## Real-time Display

- Preview streaming is enabled by default when recording starts.
- Preview channels can be selected through **Display Channel**.
- Auxiliary signals from IMU and DSP can be selected through **Display Auxiliary**.
- Preview can be turned off to save power and host BLE bandwidth.
- Internal state display shows closed-loop detection, stimulation trigger, DSP states, and TinyML model states.
- Display length options include 1 s, 2 s, 5 s, and 10 s.
- Gain options range from 10 uV to 5 mV.
- Threshold overlays are available during closed-loop operation when the corresponding DSP channels are selected.

![Real-time control](images/WIrelessEphys_Github_4_onlineAPI.jpg)

## Data Download

1. Insert the microSD card into the host computer.
2. Click **Save to Disk** and select the target folder.
3. Data will be organized by recording ID and recording start timestamp.

![Offline interface](images/WIrelessEphys_Github_5_offlineAPI.jpg)

## Post Processing

Processing scripts are available in [Code](https://github.com/zifangzhao/Neurologger/tree/main/Code).

1. Run `WILD_PreProcess.m` to generate corrected headers and `time.dat`. This also generates FMAToolbox-style event files from digital input signals.
2. For recordings with camera data, decode `misc.dat` with `WILD_VideoDecodewAudio.py`.
3. For IMU sensor fusion, run `WILD_processIMU.m`.
