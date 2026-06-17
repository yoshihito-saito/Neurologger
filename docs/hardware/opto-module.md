# Opto Module

The WILD opto-module is the optional stimulation hardware path for optical manipulation experiments. It should be documented separately from the logger board because supported stimulation behavior depends on the opto-module hardware, release image, wiring, and validation procedure.

## Hardware Assets

| Asset | Repository path |
| --- | --- |
| PCB fabrication files | [PCB/Optomodule/GerberFiles](https://github.com/ayalab1/Neurologger/tree/main/PCB/Optomodule/GerberFiles) |
| Drill files | [PCB/Optomodule/DrillFiles](https://github.com/ayalab1/Neurologger/tree/main/PCB/Optomodule/DrillFiles) |
| Assembly files | [PCB/Optomodule/Assembly](https://github.com/ayalab1/Neurologger/tree/main/PCB/Optomodule/Assembly) |
| Prebuilt module image | [Firmware/Opto_module.hex](https://github.com/ayalab1/Neurologger/blob/main/Firmware/Opto_module.hex) |

## Supported Operations

| Operation | Purpose | Validation |
| --- | --- | --- |
| Manual stimulation test | Confirm optical output and wiring before closed-loop use. | Use a bench photodiode, optical power meter, or other approved output check. |
| Closed-loop stimulation output | Deliver stimulation in response to WILD DSP, threshold, or TinyML state when supported by the release image. | Compare event files, stimulation markers, and observed output timing. |
| External trigger stimulation | Drive stimulation from external timing equipment when the experiment requires external coordination. | Record the external trigger and WILD event path for later alignment. |
| Parameter review | Confirm pulse width, intensity, channel selection, and enable state before the animal session. | Save release image, WILD_console version, and stimulation settings with the dataset. |

## Bring-Up Checks

Before connecting the opto-module to an animal-mounted device:

1. Confirm the opto-module PCB revision and compatible release image.
2. Inspect connector orientation and solder joints.
3. Confirm current limit, load, and optical output path on the bench.
4. Run a manual test pulse and record the measured output.
5. Confirm that stimulation markers are exported with the recording when stimulation timing is part of the analysis.

## Metadata

Record the opto-module PCB revision, release image, stimulation channel, optical output calibration, cable or connector path, and validation file. For closed-loop studies, also record the DSP or model state that generated each stimulation event.
