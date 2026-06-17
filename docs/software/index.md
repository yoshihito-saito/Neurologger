# Software

Software documentation covers how to connect to the WILD device, configure recordings in WILD_console, export data from the device microSD card, and process recordings for analysis.

## Software Components

<div class="wild-grid wild-nav-grid">
  <a class="wild-card wild-card-link wild-card-compact" href="acquisition/">
    <div>
    <h3>WILD_console</h3>
      <p>Connect and export</p>
    </div>
  </a>
  <a class="wild-card wild-card-link wild-card-compact" href="artificial-intelligence/">
    <div>
      <h3>Embedded AI</h3>
      <p>Validated models</p>
    </div>
  </a>
  <a class="wild-card wild-card-link wild-card-compact" href="api-cli/">
    <div>
      <h3>Scripts</h3>
      <p>Batch tools</p>
    </div>
  </a>
  <a class="wild-card wild-card-link wild-card-compact" href="../analysis/">
    <div>
      <h3>Analysis</h3>
      <p>MATLAB and Python</p>
    </div>
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

WILD_console remains the stable public control and export workflow for BLE discovery, connection, synchronization support, status checks, selected preview, low-bandwidth commands, and SD-card export.

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
