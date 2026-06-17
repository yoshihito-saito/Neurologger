# Getting Started

Start here if you are setting up a WILD device for the first time or reproducing the public workflow from the Nature Methods platform paper.

<div class="wild-grid two">
  <a class="wild-card wild-card-link" href="hardware-setup/">
    <h3>1. Hardware setup</h3>
    <p>Prepare the WILD device, connector, microSD card, battery, probe or sensor cabling, and release image before recording.</p>
  </a>
  <a class="wild-card wild-card-link" href="data-acquisition/">
    <h3>2. Data acquisition</h3>
    <p>Use WILD_console for BLE discovery, synchronization support, recording configuration, closed-loop control, and SD-card export.</p>
  </a>
  <a class="wild-card wild-card-link" href="data-analysis/">
    <h3>3. Data analysis</h3>
    <p>Generate compatible headers, timing files, decoded camera streams, processed IMU data, and spike-sorting inputs.</p>
  </a>
</div>

## Before You Begin

- Windows 10 or later for WILD_console.
- Bluetooth 4.0 or later for BLE control.
- A tested microSD card installed in the WILD device. Use Samsung EVO series or tested Lexar cards for first recordings; some SanDisk cards may be unreliable in specific WILD operating modes.
- A battery that can boot the WILD device and sustain the planned recording mode.
- The correct release image for the hardware revision and experiment mode.

## Repository Assets

| Asset | Location |
| --- | --- |
| Prebuilt device images | [Latest GitHub release](https://github.com/ayalab1/Neurologger/releases/latest) |
| WILD_console installers | [Latest GitHub release](https://github.com/ayalab1/Neurologger/releases/latest) |
| PCB fabrication files | [PCB](https://github.com/ayalab1/Neurologger/tree/main/PCB) |
| 3D-print files | [3Dprint](https://github.com/ayalab1/Neurologger/tree/main/3Dprint) |
| MATLAB and Python analysis scripts | [Code](https://github.com/ayalab1/Neurologger/tree/main/Code) |

!!! tip "Recommended first path"
    Start with Hardware Setup, then Data Acquisition, then Data Analysis. The SD card, battery, release image, and boot state provide the baseline for troubleshooting.

## First Successful Dry Run

**Goal:** complete a short bench recording and confirm that the public export and analysis path works before changing advanced settings.

**Minimum output folder:**

- `amplifier.dat`
- `analogin.dat`
- `time.dat`
- `info.rhd`
- `CE_params.bin`

**Optional outputs, depending on mode:**

- `adc.dat` for audio workflows.
- `misc.dat` for camera workflows.
- `device_event.*.evt` files after MATLAB preprocessing.
- `IMU.mat` after IMU processing.

**Success criteria:**

1. The WILD device is discovered and connected in WILD_console.
2. A short recording starts and stops cleanly.
3. SD-card export completes without missing-core-file errors.
4. The exported folder contains the expected files for the recording mode.
5. MATLAB or Python post-processing runs without manual file repair.
