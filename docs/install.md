# WILD API Installation

## Requirements

- Windows 10 or later.
- .NET Framework 4.8.
- Visual Studio 2022 for development builds.

## Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/zifangzhao/Neurologger
   cd Neurologger
   ```

2. Navigate to `Software/` and install the latest WILD console package.

## For Development

1. Open the WILD console solution in Visual Studio.
2. Restore NuGet packages and build.

## Dependencies

- Windows Bluetooth APIs.
- System.Windows.Forms.
- Microsoft.Win32.SafeHandles.

## Optional Runtime Files

- `dll_upfirdn.dll` - resampling backend.
- WILD BLE backend DLL, if required by the selected installer.

Place runtime DLLs in the same folder as the WILD console executable.
