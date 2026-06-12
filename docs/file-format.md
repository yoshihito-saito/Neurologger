# File Format

Each WILD recording session produces a folder with neural data, auxiliary signals, metadata, and optional camera or audio data.

## Files

- `amplifier.dat` - neural signals as `int16`; sampling rate depends on recording settings.
- `analogin.dat` - auxiliary analog input at 1250 Hz, including digital inputs, IMU channels, time words, and DSP channels.
- `adc.dat` - raw ADC channels, including microphone workflows.
- `misc.dat` - raw camera data.
- `info.rhd` - Intan-compatible metadata.
- WILD parameter binary - system and DSP parameters. Confirm the final public filename before release.
