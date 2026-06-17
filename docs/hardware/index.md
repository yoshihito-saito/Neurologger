# Hardware

Hardware documentation covers the WILD device architecture, board fabrication assets, mechanical assembly, power choices, and release-image compatibility for supported device revisions.

<div class="wild-grid two">
  <a class="wild-card wild-card-link" href="device-overview/">
    <h3>Device Overview</h3>
    <p>Core device specifications, supported modalities, local storage, wireless control, and closed-loop output paths.</p>
  </a>
  <a class="wild-card wild-card-link" href="onboard-sensors/">
    <h3>Onboard Sensors</h3>
    <p>IMU, camera, microphone, digital inputs, camera working distance, and microphone ribbon-amplifier notes.</p>
  </a>
  <a class="wild-card wild-card-link" href="opto-module/">
    <h3>Opto Module</h3>
    <p>Optional stimulation-module assets, supported stimulation operations, and bench validation checks.</p>
  </a>
  <a class="wild-card wild-card-link" href="usb-board/">
    <h3>USB Board</h3>
    <p>USB-GPIO board picture, supported input/output operations, and trigger-alignment metadata.</p>
  </a>
  <a class="wild-card wild-card-link" href="pcb/">
    <h3>PCB</h3>
    <p>Board packages, fabrication outputs, assembly files, revision notes, and inspection points for manufactured boards.</p>
  </a>
  <a class="wild-card wild-card-link" href="mechanical/">
    <h3>Mechanical</h3>
    <p>Printable parts, baseplates, camera mounts, enclosure orientation, and fit checks for head-mounted assemblies.</p>
  </a>
  <a class="wild-card wild-card-link" href="power/">
    <h3>Power</h3>
    <p>Battery and microSD guidance for boot current, recording runtime, preview load, stimulation, and camera use.</p>
  </a>
  <a class="wild-card wild-card-link" href="https://github.com/ayalab1/Neurologger/releases/latest">
    <h3>Release Images</h3>
    <p>Validated WILD device images linked to compatible hardware revisions and experiment metadata.</p>
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
