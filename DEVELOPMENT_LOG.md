# Development Log

## Day 1 — Noor SmartScan (2026-11-10)

- **Problem:** small copy/print shops need a quick offline way to assemble scanned or photographed pages into a multi-page PDF.
- **Implemented:** Python/Pillow processing core; Tkinter Windows interface; image import, list ordering, removal, rotation, preview, three enhancement presets, DPI selection, multi-page PDF export, CLI export, installation and privacy documentation.
- **Tests performed:** five automated `unittest` cases passed on Linux with Python 3.12 and Pillow 13.0.0. Covered Unicode/Arabic path loading, enhancement modes, multipage PDF order and dimensions, validation, corrupt images, and no partial output.
- **Not tested:** GUI launch (Tkinter is absent from the sandbox), Windows 10/11 execution, scanner acquisition, printer output, packaging or installer.
- **Status:** source published at https://github.com/collodev21/noor-smartscan; central roadmap published at https://github.com/collodev21/NOOR-OPEN-SOURCE-FACTORY. No Windows executable or versioned release was produced.
- **Next:** prepare Windows validation; build a non-destructive crop/perspective editing workflow and maintain in-memory edits before adding scanner hardware support.

## Day 2 — Noor ID Layout (2026-11-10)

- **Problem:** copy/print shops need a quick way to place supplied document images on a print sheet without guessing physical card sizes.
- **Research:** reviewed the public READMEs for [Photo ID Creator](https://github.com/dpar39/ppp), [Idify](https://github.com/zhbhun/idify) and [Passport Photo Generator](https://github.com/rizwansoaib/passport-photo-generator). They address adjacent photo-ID/photo-editing needs. This project focuses on offline placement of supplied images using operator-entered dimensions, not face/photo standardization or country-size databases.
- **Implemented:** Python/Pillow core, Tkinter Windows GUI and CLI; custom sheet and image-box dimensions in mm; A4/A5/A6 paper presets; margins, gaps, copies per input image, placement preview and one-page PDF output; fit-without-cropping; rendering limits; Windows install and privacy documentation.
- **Tests performed:** seven automated `unittest` tests passed on Linux with Python 3.12, Pillow and pypdf. Covered grid capacity/centering, image sequence/copies, PDF physical dimensions, Arabic/Unicode and long paths, invalid/oversized layouts, corrupt input and output collision protection. Python modules passed syntax compilation; CLI help executed.
- **Not tested:** Tkinter GUI launch (Tkinter is missing from the environment), Windows 10/11 execution, printer driver scaling or physical print output, packaging or executable. No screenshot is included because the GUI could not be launched. The GitHub Actions workflow is configured; a completed CI result is not yet verified.
- **Status:** source published at https://github.com/collodev21/noor-id-layout; central portfolio and roadmap updated and pushed. No Windows executable or release is claimed.
- **Next:** Day 3 Noor RectoVerso, focused on a non-destructive front/back print workflow with independent alignment offsets and a test/calibration sheet; avoid assumed card dimensions.
