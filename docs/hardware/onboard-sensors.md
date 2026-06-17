# Onboard Sensors

WILD sensor documentation describes the auxiliary channels recorded alongside neural data or used during bench validation. Treat each enabled sensor as part of the experiment configuration: record the release image, sampling mode, connected module, and whether the output was used for monitoring, downstream analysis, or both.

## IMU

The WILD device includes a 9-axis motion-sensor path for acceleration, gyroscope, and magnetic-field measurements. IMU data support motion-state review, behavioral segmentation, artifact inspection, and alignment with external tracking systems.

For reproducible datasets, document:

- IMU enable state.
- Configured sample rate.
- Axis orientation relative to the mounted device.
- Whether IMU channels were exported in `analogin.dat` or processed into `IMU.mat`.
- Any filtering, resampling, or coordinate transform applied after export.

## Camera

The head-mounted camera path supports synchronized behavioral context when video is enabled in the release image and hardware configuration. Camera payloads are recovered from local device storage during export; live preview is used for setup and focus checks rather than as the full-quality data source.

Record the camera hardware, release image, frame rate, working distance, illumination condition, and decode script version with each dataset.

### Camera Imaging Profile

![Camera imaging profile at 4 mm, 8 mm, and 12 mm working distances](../images/WIrelessEphys_Github_11_cameraProfile.jpg){ .wild-readable-figure }

Use the camera imaging profile during bench setup to choose the working distance and focus range before mounting the camera module. Confirm the expected target distance with live preview before treating camera data as part of the experiment record.

## Microphone

The WILD microphone path uses the SPH6611LR5H ultrasonic microphone for vocalization and high-frequency acoustic recordings. In the documented WILD workflow, microphone data are sampled at 160 kHz, supporting acoustic content up to approximately 80 kHz when the analog path, sampling mode, and export settings are configured for USV recording.

The microphone ribbon assembly includes an embedded 10x amplifier stage before the logger input. Record whether the microphone ribbon and amplifier stage are present, the microphone orientation, and the release image used for acquisition.

For microphone sessions, document:

- Microphone model: SPH6611LR5H.
- Sampling rate: 160 kHz in the USV recording workflow.
- Approximate frequency response target: up to 80 kHz.
- Ribbon/amplifier configuration, including the embedded 10x amplifier stage.
- Audio export file path, decode script version, and any filtering or gain applied after export.

## Digital Inputs

Digital input channels are used for synchronization pulses, behavioral event markers, camera triggers, stimulation markers, or bench validation signals. These inputs are most useful when the same physical pulse is also recorded by the external system being aligned.

For timing-sensitive work, keep the raw digital input record and any generated event files. Post-export correction should preserve both raw event times and the corrected WILD-time event table.
