
## Day 3 — Noor RectoVerso (2026-11-11)

- **Problem:** manual front/back printing can misalign because of printer margins, paper feed direction and reloading. Shops need independent horizontal and vertical correction rather than repeated trial-and-error placement.
- **Implemented:** standalone Python/Pillow engine, Tkinter Windows GUI and CLI; ordered paired front/back image input; two-page PDF (front page, then back page); operator-supplied paper and image-box dimensions; independently adjustable page-2 X/Y offsets; bounds validation; local image preview; two-page calibration PDF with reference crosses; Windows installation, privacy and manual-duplex instructions.
- **Tests performed:** seven automated `unittest` tests passed locally with Python 3.12, Pillow and pypdf. Verified two-page PDF dimensions, independent X/Y movement on the back page while the front remains unchanged, calibration PDF structure, mismatch/overflow rejection, corrupt image handling, output collision protection and Unicode destination paths. Both modules passed `py_compile`; CLI help ran.
- **Not tested:** the Tkinter GUI was not launched because this Linux environment lacks Tkinter. No Windows desktop GUI session, physical printer, manual paper reload, printer driver scaling, or actual front/back registration test was performed. GitHub Actions had been configured; its run result still needs checking. No screenshot, Windows executable or release is claimed.
- **Status:** public source pushed to https://github.com/collodev21/noor-rectoverso. The central index and roadmap are being updated.
- **Next:** Day 4 Four-Corner Cropper, with user-adjustable corners and tests for perspective warp boundaries; preserve source files and avoid identity-data extraction.
