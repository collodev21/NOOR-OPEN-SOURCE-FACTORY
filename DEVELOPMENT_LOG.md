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
- **Not tested:** Tkinter GUI launch (Tkinter is missing from the environment), full Windows 10/11 desktop workflow, printer driver scaling or physical print output, packaging or executable. No screenshot is included because the GUI could not be launched. The GitHub Actions core-test matrix completed successfully on Windows and Ubuntu with Python 3.10 and 3.12.
- **Status:** source published at https://github.com/collodev21/noor-id-layout; central portfolio and roadmap updated and pushed. No Windows executable or release is claimed.
- **Next:** Day 3 Noor RectoVerso, focused on a non-destructive front/back print workflow with independent alignment offsets and a test/calibration sheet; avoid assumed card dimensions.

## Day 3 — Noor RectoVerso (2026-11-11)

- **Problem:** manual front/back printing can misalign because of printer margins, paper feed direction and reloading. Shops need independent horizontal and vertical correction rather than repeated trial-and-error placement.
- **Implemented:** standalone Python/Pillow engine, Tkinter Windows GUI and CLI; ordered paired front/back image input; two-page PDF (front page, then back page); operator-supplied paper and image-box dimensions; independently adjustable page-2 X/Y offsets; bounds validation; local image preview; two-page calibration PDF with reference crosses; Windows installation, privacy and manual-duplex instructions.
- **Tests performed:** seven automated `unittest` tests passed locally with Python 3.12, Pillow and pypdf. Verified two-page PDF dimensions, independent X/Y movement on the back page while the front remains unchanged, calibration PDF structure, mismatch/overflow rejection, corrupt image handling, output collision protection and Unicode destination paths. Both modules passed `py_compile`; CLI help ran.
- **Not tested:** the Tkinter GUI was not launched because this Linux environment lacks Tkinter. No interactive Windows desktop GUI session, physical printer, manual paper reload, printer driver scaling, or actual front/back registration test was performed. GitHub Actions passed all four core-test jobs: Windows and Ubuntu on Python 3.10 and 3.12. No screenshot, Windows executable or release is claimed.
- **Status:** public source published at https://github.com/collodev21/noor-rectoverso. Central index and roadmap updated. No Windows executable or release is claimed.
- **Next:** Day 4 Four-Corner Cropper, with user-adjustable corners and tests for perspective warp boundaries; preserve source files and avoid identity-data extraction.

## Day 4 — Noor Four-Corner Cropper (2026-11-12)

- **Problem:** photos of paper documents taken at an angle need a simple way to select the page manually and correct its perspective without automatic recognition or cloud uploads.
- **Alternatives reviewed:** Perspec, Free Scanner, and LiteObject/doc-scanner provide adjacent desktop or phone scanning, automatic detection, corner adjustment, OCR or enhancement workflows. This Day 4 project is a small manual, Pillow-only cropper.
- **Implemented:** standalone Python/Pillow core, Tkinter GUI and CLI; four draggable corners in fixed clockwise order; projective transformation to a rectangle; output dimensions estimated from opposite-edge averages; corrected preview; PNG/JPEG/TIFF/BMP/WebP export; EXIF orientation handling; size limits; save-as-only with source preservation; Windows setup, usage, privacy and limitation documentation.
- **Tests performed:** seven automated `unittest` tests passed locally under Python 3.12 and Pillow 13.0.0. They cover rectangular and trapezoid transformations, output geometry, invalid/reversed/out-of-frame/crossing/too-small corners, Unicode paths, original preservation, corrupt input, unsupported extensions, and collision protection. Both modules passed `py_compile`; CLI help ran.
- **Not tested:** the GUI was not launched because Tkinter is unavailable in the Linux environment. A real Windows desktop interaction, camera/scanner hardware, and physical output were not tested. GitHub Actions is configured; no completed Day 4 CI run has been verified yet. No screenshot, Windows executable, installer, or release is claimed.
- **Status:** source published at https://github.com/collodev21/noor-four-corner-cropper. Central portfolio and roadmap are being updated.
- **Next:** Day 5 PDF Deskewer; estimate rotation without clipping content and test mixed/noisy inputs before batch-safe export.
