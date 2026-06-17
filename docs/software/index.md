# Software

Software documentation covers how to connect to the WILD device, configure recordings in WILD_console, export data from the device microSD card, and process recordings for analysis.

## Software Components

<div class="wild-grid two">
  <a class="wild-card wild-card-link" href="acquisition/">
    <h3>WILD_console</h3>
    <p>Windows GUI for connecting to WILD over BLE, synchronizing the session, setting up recordings, previewing selected signals, configuring closed-loop behavior, and exporting SD-card data.</p>
  </a>
  <a class="wild-card wild-card-link" href="acquisition/#wireless-connection-model">
    <h3>iOS controller</h3>
    <p>In-development app for device discovery, BLE connection, synchronization support, status checks, and low-bandwidth control.</p>
  </a>
  <a class="wild-card wild-card-link" href="artificial-intelligence/">
    <h3>Embedded inference</h3>
    <p>Curated embedded models for validated closed-loop releases. Generic model loading is not yet part of the stable workflow.</p>
  </a>
  <a class="wild-card wild-card-link" href="api-cli/">
    <h3>Programmatic workflows</h3>
    <p>Documented operations for data export, batch post-processing, video/audio decoding, GPIO logging, and validation utilities.</p>
  </a>
  <a class="wild-card wild-card-link" href="../analysis/">
    <h3>Analysis scripts</h3>
    <p>MATLAB and Python scripts for headers, timing, IMU processing, video decoding, and downstream analysis.</p>
  </a>
</div>

## Install

Download WILD_console from the [latest GitHub release](https://github.com/ayalab1/Neurologger/releases/latest). The link always opens the newest published WILD release.

## Public Workflow Boundary

The current public software path is:

1. Connect and record with WILD_console.
2. Export from the device microSD card.
3. Run documented MATLAB or Python post-processing.

The public documentation does not treat BLE as a continuous high-bandwidth acquisition path, and it does not promise a stable general-purpose SDK yet.

## Wireless Control

WILD_console remains the stable public control and export workflow. The iOS-based controller app is being developed as a lighter wireless-control path for BLE discovery, connection, synchronization support, status checks, and low-bandwidth commands.

Full-resolution WILD recordings remain local to the device microSD card and are exported after the session.

## Requirements

- Windows 10 or later.
- .NET Framework 4.8 for the current GUI.
- Bluetooth 4.0 or later.
- Administrator privileges for some SD-formatting workflows.

## Optional Runtime Files

- `dll_upfirdn.dll` for resampling.
- WILD BLE backend DLL for BLE support in older installer layouts.
- `ffmpeg.exe` for some camera processing workflows.
