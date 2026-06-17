# Hardware

Hardware documentation covers the WILD device architecture, board fabrication assets, mechanical assembly, power choices, and release-image compatibility for supported device revisions.

<div class="wild-grid wild-nav-grid">
  <a class="wild-card wild-card-link wild-card-compact" href="device-overview/">
    <div>
      <h3>Device</h3>
      <p>Architecture</p>
    </div>
  </a>
  <a class="wild-card wild-card-link wild-card-compact" href="onboard-sensors/">
    <div>
      <h3>Sensors</h3>
      <p>IMU, audio, camera</p>
    </div>
  </a>
  <a class="wild-card wild-card-link wild-card-compact" href="opto-module/">
    <div>
      <h3>Opto module</h3>
      <p>Stimulation</p>
    </div>
  </a>
  <a class="wild-card wild-card-link wild-card-compact" href="usb-board/">
    <div>
      <h3>USB-GPIO</h3>
      <p>Trigger alignment</p>
    </div>
  </a>
  <a class="wild-card wild-card-link wild-card-compact" href="pcb/">
    <div>
    <h3>PCB</h3>
      <p>Fabrication files</p>
    </div>
  </a>
  <a class="wild-card wild-card-link wild-card-compact" href="mechanical/">
    <div>
    <h3>Mechanical</h3>
      <p>Mounts and enclosures</p>
    </div>
  </a>
  <a class="wild-card wild-card-link wild-card-compact" href="power/">
    <div>
    <h3>Power</h3>
      <p>Battery and SD</p>
    </div>
  </a>
  <a class="wild-card wild-card-link wild-card-compact" href="https://github.com/ayalab1/Neurologger/releases/latest">
    <div>
      <h3>Releases</h3>
      <p>Firmware images</p>
    </div>
  </a>
</div>

## Hardware Asset Map

| Hardware area | Repository path |
| --- | --- |
| Datalogger PCB | [PCB/Datalogger](https://github.com/ayalab1/Neurologger/tree/main/PCB/Datalogger) |
| Opto module | [PCB/Optomodule](https://github.com/ayalab1/Neurologger/tree/main/PCB/Optomodule) |
| Camera unit | [PCB/CameraUnit](https://github.com/ayalab1/Neurologger/tree/main/PCB/CameraUnit) |
| USB-GPIO firmware | [Firmware/WILD_USB_GPIO.hex](https://github.com/ayalab1/Neurologger/blob/main/Firmware/WILD_USB_GPIO.hex) |
| Opto-module firmware | [Firmware/Opto_module.hex](https://github.com/ayalab1/Neurologger/blob/main/Firmware/Opto_module.hex) |
| Mechanical parts | [3Dprint](https://github.com/ayalab1/Neurologger/tree/main/3Dprint) |
| Battery table | [LipoBattery_selection.csv](https://github.com/ayalab1/Neurologger/blob/main/docs/LipoBattery_selection.csv) |
| Prebuilt device images | [Latest GitHub release](https://github.com/ayalab1/Neurologger/releases/latest) |

## Compatibility Record

Document the following for each supported WILD hardware build or dataset:

| Record | Why it matters |
| --- | --- |
| PCB or device revision | Distinguishes connector layout, sensor options, and supported release images. |
| Release tag and image filename | Ties behavior to a reproducible device image. |
| WILD_console version | Defines the export and control tool behavior used in the session. |
| SD-card model | Affects boot reliability and long-session write stability. |
| Battery model | Affects boot margin, runtime, and peak-load behavior. |
| Enabled modalities | States whether the session used ephys, IMU, audio, video, stimulation, or external sync. |

## Bring-Up Checklist

Before the first recording on a newly assembled WILD device:

1. Confirm that the intended release image and hardware revision match.
2. Confirm battery polarity and boot stability.
3. Confirm microSD insertion and basic discoverability.
4. Confirm BLE connection and synchronization state.
5. Run a short recording, export it, and verify the expected files before any animal session.

## Visual Asset Policy

Public hardware visuals should be traceable to real WILD material: device photographs, CAD or EDA exports, microscope images, measured drawings, software screenshots, or hand-authored diagrams derived from measured hardware. AI-generated device photographs or device-like renders are excluded from WILD hardware documentation.
