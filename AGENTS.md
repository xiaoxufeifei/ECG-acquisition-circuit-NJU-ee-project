# Repository Guidelines

## Project Structure & Module Organization

This workspace contains an ECG analog front-end hardware project, not an application codebase. Files currently live at the root:

- `电子实验心电测量.eprj2`: native EDA project for schematic and PCB work.
- `Design1.ms14`: Multisim simulation project.
- `Design1.ms14 (Security copy)`: existing simulation backup; preserve it.
- `ECG_AFE_可行性设计.md`: requirements, circuit calculations, proposed values, and validation notes.
- `0205组第一阶段实验报告.pdf`: experiment report.
- `*.png`: supporting image assets.

There are no source-code or test directories. The design notes reference `ecg_afe_verify.py`, but that script is absent from this snapshot.

## Build, Test, and Development Commands

Use PowerShell from the project root:

```powershell
Get-ChildItem -File
Start-Process '.\Design1.ms14'
Start-Process '.\电子实验心电测量.eprj2'
```

The first command lists artifacts; the others open projects through their installed Windows file associations. Install or configure Multisim and the compatible EDA application before using those commands. Run simulations and schematic/PCB checks inside those applications. No automated build, package manager, or CLI test runner is configured.

## Style & Naming Conventions

Preserve existing Chinese document titles and circuit identifiers such as `VIN_N`, `VNOTCH`, and `P_GAIN`. Write Markdown as UTF-8 with descriptive headings and fenced calculation examples. Include units and distinguish peak, peak-to-peak, and RMS measurements. Name new evidence descriptively, for example `notch_50Hz_rev02.png`. No formatter or linter is configured.

## Validation Guidelines

Check affected stages and end-to-end behavior after component changes. Record gain, bandwidth, input impedance, CMRR, notch response, output offset, and noise as relevant. Identify test points, supply voltages, component revision, and instrument settings. Keep theoretical, simulated, and measured results distinct. There is no automated coverage target; provide reproducible manual evidence. Do not treat older calculations as validation of revised hardware.

## Commit & Pull Request Guidelines

This snapshot has no Git metadata, so no established commit convention is available. If version control is introduced, use focused messages such as `docs: clarify high-pass component revision`. PRs should describe changed artifacts, affected circuit stages, validation results, and unresolved discrepancies. Include before/after screenshots for schematic or PCB changes.

## Artifact Handling

Edit native circuit files with their intended applications. Preserve original measurements and backups; document corrections and regenerate affected exports. Use the circuit only with laboratory signal sources or an ECG simulator, as specified in the design notes.
