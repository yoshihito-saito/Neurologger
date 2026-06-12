# WILD Website Content Questions

This file collects the parts of the current documentation site that need your confirmation or more project-specific detail. Fill in answers directly under each item. I will use those answers to replace draft wording, add exact specs, and make the public site more credible.

This file is intentionally outside `docs/`, so it is not part of the published MkDocs website.

## Priority 1: Public Launch Blockers

### 1. Project naming and positioning

Current site uses:

- Public name: `WILD`
- Expansion: `Wireless Intelligent Logger`
- Repository/project URL: `zifangzhao/Neurologger`
- Site title: `WILD: Open-source Wireless Neurotechnology for Naturalistic Neuroscience`

Questions:

- Should the public-facing name always be `WILD` across device variants, software, firmware, and documentation?
- Should `Neurologger` appear only as the legacy repository name, or should the repository be renamed later?
- Should the headline keep "Open-source Wireless Neurotechnology" or use a narrower phrase such as "Wireless Neural Logger"?

Answer:


### 2. Hardware revision and supported device variants

The docs currently describe the platform generally, without exact revision names.

Questions:

- Which hardware revision should be documented first?
- What are the exact WILD hardware variant names or revision names we should use publicly?
- What are the exact channel counts and supported recording modes for each WILD variant?
- Which features are stable today, and which should be labeled experimental?

Answer:


### 3. Core specifications

The public site needs a compact specs table.

Questions:

- Device mass:
- Device dimensions:
- Battery range:
- Typical battery life by mode:
- Neural channel count:
- Sampling rates:
- ADC resolution:
- Storage type and recommended SD cards:
- BLE role and supported operating systems:
- IMU model and sampling modes:
- Audio/USV bandwidth:
- Camera support details:
- Stimulation output type and limits:

Answer:


### 4. Device images and figure policy

Your requirement is clear: no AI-generated device photographs or device illustrations.

Questions:

- Can we publicly use all current `docs/images/WIrelessEphys_*.jpg` images?
- Which images are real device photos?
- Which images are schematic, CAD, PCB, or hand-authored diagrams?
- Are there images that should be removed before public hosting?
- Should image captions include hardware revision, date, or source file?

Answer:


### 5. Publications and citation

The current site has a placeholder repository citation.

Questions:

- Is there a preferred author list for the repository citation?
- Is there a platform manuscript, preprint, protocol, conference abstract, or dataset DOI to cite?
- Should the citation year be 2026, or another year?
- Should the site include BibTeX, APA, and/or Nature-style citation text?

Answer:


### 6. GitHub community links

The homepage currently mentions GitHub Discussions, but the repository must have Discussions enabled for that link to be useful.

Questions:

- Should GitHub Discussions be enabled?
- Should support questions go to Discussions, Issues, or email?
- Do you want issue templates for bug reports, hardware questions, and documentation fixes?
- Is there a lab or project contact email that should appear publicly?

Answer:


## Priority 2: Page-Specific Content Gaps

### 7. Getting Started

Current pages give a general workflow.

Questions:

- What is the recommended first experiment for a new user?
- What hardware should a new user have before starting?
- What firmware binary should they flash first?
- What software should they install first?
- What sample dataset should they use to verify analysis?

Answer:


### 8. Hardware: device overview, PCB, mechanical, power

Questions:

- Which PCB files should be linked from the docs?
- Are KiCad, Altium, Gerber, or PDF schematic files available?
- What connector pinouts are ready for public release?
- What mechanical files should be documented: enclosure, headstage mount, battery holder, probe adapter?
- What battery sizes and vendors have been tested?
- What power modes should users understand before running long experiments?

Answer:


### 9. Firmware: architecture, build, BLE, DSP

Questions:

- What MCU or SoC should be named publicly?
- What toolchain should users use: STM32CubeIDE, Keil, CMake, vendor IDE, or another workflow?
- What are the exact bootloader and application flashing steps?
- Where are firmware releases or binaries stored?
- What BLE commands are stable enough to document?
- Which DSP modes are implemented: filters, ripple detection, Hilbert phase, thresholding, stimulation gating?
- What TinyML model format is supported today?

Answer:


### 10. Software: acquisition, visualization, data format

Questions:

- Is the acquisition app officially called `WILD_console`, or should another WILD-branded name be used?
- Which Windows version is supported?
- Are there Linux or macOS workflows?
- What screenshots should be added for connection, recording setup, live preview, and export?
- What file formats are guaranteed stable?
- Which files are Intan-compatible, and which are WILD-specific?

Answer:


### 11. Analysis: Python, MATLAB, spike sorting

Questions:

- What Python package or scripts should users start with?
- What MATLAB functions should be documented first?
- Should the docs recommend SpikeInterface, Kilosort, Mountainsort, or another sorting workflow?
- Are there small example recordings that can be distributed publicly?
- How should users process IMU, camera, and USV data?

Answer:


### 12. Examples

The current Examples page lists planned examples, but no full protocols yet.

Questions:

- Which example should be completed first?
- Do you have one real dataset or recording session suitable for a public tutorial?
- For ripple detection, what validation waveform or expected output should be shown?
- For theta phase stimulation, what timing or phase accuracy numbers can be reported?
- For multi-animal experiments, what synchronization method should be documented?

Answer:


## Priority 3: Credibility and Adoption Details

### 13. Research highlights

The homepage currently lists outdoor recording, multi-animal experiments, ripple detection, theta phase stimulation, and naturalistic behavior.

Questions:

- Which of these have completed validation data?
- Which should be described as demonstrated, in development, or planned?
- Do you have figures for each highlight?
- Should any claims be softened before public release?

Answer:


### 14. Open-source release scope

Questions:

- What is included in the first public release: PCB, BOM, firmware source, acquisition software, analysis scripts, CAD, datasets?
- Are there files that should remain private for now?
- Is the current `GPL-3.0` license intended for the whole project?
- Do hardware files need a separate license such as CERN-OHL or CC BY?

Answer:


### 15. Build and manufacturing guidance

Questions:

- Should the docs include a BOM and assembly guide?
- Should users fabricate PCBs themselves, contact the lab, or wait for a release package?
- Are there known parts that are hard to source?
- What soldering or inspection steps are essential?
- What calibration or acceptance test should be run after assembly?

Answer:


### 16. Safety, animal use, and limitations

Questions:

- Should the site include an animal-use disclaimer?
- Should stimulation limits, battery safety, implant safety, or waterproofing limitations be documented?
- Are there operating conditions where WILD should not be used?
- Should outdoor recording guidance include environmental limits?

Answer:


## Priority 4: Visual Assets to Add

Questions:

- Do you have a clean real device photo for the homepage hero?
- Do you have a labeled block diagram from source files?
- Do you have PCB top/bottom renders exported from the EDA tool?
- Do you have connector pinout diagrams?
- Do you have screenshots of the acquisition console?
- Do you have example plots: neural trace, IMU trace, spectrogram, ripple event, theta phase, camera frame alignment?

Answer:


## Suggested Next Update After Your Answers

After you fill this in, the next website pass should:

1. Replace general claims with confirmed specs.
2. Add a hardware revision table.
3. Add one complete quick-start path with exact commands and screenshots.
4. Replace publication placeholders with real citations.
5. Add provenance-aware captions for every device image.
6. Mark features as stable, experimental, or planned.
7. Add one complete example protocol with expected outputs.
