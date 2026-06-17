# Hardware Setup

This checklist covers the physical preparation required before connecting WILD to software.

## Device and Connectors

Connector images identify the stimulation, auxiliary, sensor, sync, and battery interfaces before board power-up.

![WILD connector overview](../images/WIrelessEphys_Github_8_connectors.jpg){ .wild-readable-figure }

The connector-orientation schematic below highlights the power, ground, and USB data-line positions used during the first hardware check. Confirm the actual connector orientation on the assembled WILD device before applying power.

![WILD connector orientation schematic](../images/WIrelessEphys_Github_6_Connectors.jpg){ .wild-readable-figure }

The WILD device uses these connectors to support local acquisition, storage, wireless control, synchronization, and optional stimulation in a compact head-mounted unit. Before powering the device, confirm which interfaces are required for the planned session.

## Preparation Checklist

1. Inspect the PCB and connectors for visible damage.
2. Confirm battery polarity on the JST-SH connector.
3. Insert a tested microSD card.
4. Confirm the recording probe or flexible-probe connection.
5. Confirm the stimulation output, IMU, microphone, camera, and external-sync connections needed for the experiment.
6. Confirm that the device is running the expected released device image.

## microSD Card

Format the card from WILD_console before recording. The microSD card affects both reliability and power draw.

![microSD power comparison](../images/WIrelessEphys_Github_10_SDcard_power.jpg){ .wild-readable-figure }

Battery and SD-card guidance are part of the experimental protocol, not optional accessory setup.

![Battery examples](../images/WIrelessEphys_Github_9_batteries.jpg){ .wild-readable-figure }

## Released Device Image

Public setup documentation is based on prebuilt WILD release images. Each release image is matched to a hardware revision and experimental configuration. Keep the release tag and image filename in dataset metadata.

Release images are distributed through the [latest GitHub release](https://github.com/ayalab1/Neurologger/releases/latest). Follow the release notes for the specific image used in the experiment.

Treat the released device image as part of the hardware setup record. The WILD device, WILD_console version, SD card, battery, and analysis scripts should all be traceable to the dataset.
