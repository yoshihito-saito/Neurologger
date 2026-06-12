# Software

WILD software covers acquisition, live visualization, data export, and post-processing entry points.

## Software Components

<div class="wild-grid two">
  <div class="wild-card">
    <h3>WILD_console</h3>
    <p>Windows GUI for BLE connection, recording setup, preview display, closed-loop configuration, and data download.</p>
  </div>
  <div class="wild-card">
    <h3>Analysis scripts</h3>
    <p>MATLAB and Python scripts for headers, timing, IMU processing, video decoding, and downstream analysis.</p>
  </div>
</div>

## Install

Download the latest WILD console installer from [Software](https://github.com/zifangzhao/Neurologger/tree/main/Software). Development builds should be documented under the WILD console name, even when internal source folders still use older names.

## Requirements

- Windows 10 or later.
- .NET Framework 4.8 for the current GUI.
- Bluetooth 4.0 or later.
- Administrator privileges for some SD formatting workflows.

## Optional Runtime Files

- `dll_upfirdn.dll` for resampling.
- WILD BLE backend DLL for BLE support in older installer layouts.
- `ffmpeg.exe` for some camera processing workflows.
