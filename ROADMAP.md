# Noor Open Source Factory — 30-Day Roadmap

**Mission:** one independent, useful, documented Windows utility per day, designed around the real workflows of Noor Library in Collo, Algeria. Projects are offline-first, privacy-respecting, lightweight and open source. Dates are relative to the start of Day 1; a daily cadence is an objective, not a claim that unattended work will continue between sessions.

## Product principles

- Build complete, narrowly scoped utilities; never inflate the project count with empty or copied repositories.
- Keep sensitive customer documents on the local computer. No telemetry, ads, or mandatory account.
- Prioritize Windows 10/11, French UI, Arabic/RTL and English where practical, accessible controls, low-resource hardware, and clear error handling.
- Do not invent official document dimensions or automate protected government services.
- Test what is actually testable, label unverified platform workflows, and do not publish unstable binaries as stable releases.

## 30-day delivery plan

| Day | Project | Practical outcome | Initial implementation / acceptance focus |
|---:|---|---|---|
| 1 | **Noor SmartScan — Image-to-PDF Foundation** | Turn scanned or photographed pages into a clean multi-page PDF offline. | Import common image formats, reorder/remove/rotate, apply a safe document enhancement, choose DPI, export a PDF; tests for ordering, rotation, Unicode paths, invalid files and output readability. Hardware scanner acquisition and perspective correction are future work. |
| 2 | Noor ID Layout | Place provided card images on a printable sheet. | User-supplied dimensions only; custom paper, margins, spacing and preview. |
| 3 | Noor RectoVerso | Prepare front/back images for two-sided output. | Independent X/Y offsets, manual duplex instructions and a calibration sheet; no assumed card dimensions. |
| 4 | Four-Corner Cropper | Correct a photographed document. | Manual corner control and perspective transform; compare boundary handling on test images. |
| 5 | PDF Deskewer | Straighten scanned pages. | Rotation estimate, preview, batch-safe output and before/after tests. |
| 6 | Magic Color | Improve legibility of scanned pages. | Reversible color, grayscale and black/white presets with preview. |
| 7 | Batch Image-to-PDF | Convert image folders to PDFs. | Stable sorting, Unicode paths, output collision protection and progress/error report. |
| 8 | PDF Page Reorganizer | Reorder, rotate, remove and extract pages. | Preserve page content; test mixed sizes and invalid input. |
| 9 | Local OCR Assistant | Make a document searchable locally. | Optional local OCR backend, explicit install status and no uploads. |
| 10 | PDF Merger/Splitter | Combine or split customer PDFs. | Page-range validation and source preservation. |
| 11 | ID A4 Layout Generator | Lay out user-provided front/back images for printing. | Paper presets, adjustable margins and print preview. |
| 12 | Multiple Documents on One Page | Save paper on repetitive print jobs. | Fit, crop and spacing controls; predictable output dimensions. |
| 13 | Front/Back Alignment Calibrator | Measure printer-side offset. | Printable calibration marks and independent offset values. |
| 14 | Print Queue Viewer | Inspect local Windows print jobs. | Read-only first version; disclose platform permissions and limitations. |
| 15 | Printer Status Helper | Show locally available printer status. | Windows-native status discovery where accessible; no driver assumptions. |
| 16 | DPI & Print Size Calculator | Convert pixels, DPI and physical print size. | Unit tests, common paper presets and explicit rounding. |
| 17 | Photo Sheet Generator | Arrange photos for printing. | User-defined photo size, margins and crop/fill behavior. |
| 18 | Passport Photo Sheet | Prepare photo sheets. | User-entered official dimensions only; no claims of regulatory compliance without cited verification. |
| 19 | Document Margin Calculator | Calculate usable print area. | Paper, printer margin and scale calculations with sample cases. |
| 20 | Print Cost Calculator | Estimate copy/print prices. | Editable local price list, quantity tiers and printable estimate. |
| 21 | PDF Compressor | Reduce PDF file size. | Quality presets and size comparison; preserve original. |
| 22 | PDF Page Numberer | Add page numbers locally. | Position, format, start page and font options. |
| 23 | PDF to Images | Export pages as images. | DPI, format and collision-safe output. |
| 24 | PDF Form Filler | Add text to printable forms. | Position/preview workflow; do not imply digital signature. |
| 25 | PDF Watermark Tool | Add optional labels to PDFs. | Text/image watermark, opacity and preview. |
| 26 | Bulk File Renamer | Rename batches safely. | Preview, collision detection, reversible rename log. |
| 27 | Document Folder Organizer | Sort files into user-selected folders. | Dry-run plan, no destructive default, Arabic/French names. |
| 28 | Photocopy Price Calculator | Quote jobs quickly. | Service catalog, paper/color/side rules and printable totals. |
| 29 | Customer Job Ticket | Track jobs awaiting pickup. | Local-only data, simple status, backup/export and minimal personal data. |
| 30 | Local Backup Verifier | Verify local copies of business files. | Hash manifest, restore checklist and non-destructive verification. |

## Delivery gates (each day)

1. Inspect existing repositories and alternatives; choose a distinct, useful scope.
2. Implement a working application, not just a mockup; document dependencies and Windows installation.
3. Run available automated tests and meaningful workflow checks; identify any tests that require Windows hardware.
4. Review Unicode paths, long names, bad input and output collision behavior where relevant.
5. Provide source, README, license, `.gitignore`, contribution/security guidance as appropriate, and a concise development log.
6. Publish only when repository access and actual validation permit it. Create a release only after a Windows build has been produced and tested.

## Status

- Day 1 source published: [Noor SmartScan](https://github.com/collodev21/noor-smartscan); 5 core tests passed on Linux. Windows GUI, scanner/printer workflows and executable remain unverified/not delivered.
- Day 2 source published: [Noor ID Layout](https://github.com/collodev21/noor-id-layout); 7 core tests passed on Linux. Windows GUI and physical print output remain unverified; no executable/release is claimed.
- The initial build environment is Linux with Python and Pillow; it has no .NET SDK or Tkinter. Windows GUI packaging and physical scanner/printer tests therefore require a Windows host. Python core processing can be tested here.
- The central roadmap and Day 1 source repositories were created publicly and their `main` branches were verified on GitHub. No Windows executable or release is claimed.
