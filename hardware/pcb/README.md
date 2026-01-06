# PCB Layout Files

This directory contains PCB layout files for the BLE-Sensor board.

## File Types

Depending on the EDA tool used, this directory may contain:

### KiCad
- `*.kicad_pcb` - PCB layout file
- `*.kicad_pro` - Project file
- `fp-lib-table` - Footprint library table
- `gerbers/` - Gerber output files

### Altium Designer
- `*.PcbDoc` - PCB document
- `*.PrjPcb` - Project file
- `*.OutJob` - Output job file

### EAGLE
- `*.brd` - Board file
- `*.sch` - Schematic file (may also be here)

## Layout Guidelines

- Follow STM32WB reference design for RF section
- Maintain proper impedance for RF traces (typically 50Ω)
- Use ground planes on inner layers
- Keep analog and digital sections separate
- Place decoupling capacitors close to IC pins
- Follow manufacturer recommendations for antenna placement
- Maintain adequate clearance for high-voltage traces

## Manufacturing Files

### Gerber Files (gerbers/ subdirectory)
- Copper layers (GTL, GBL, G1, G2, etc.)
- Soldermask (GTS, GBS)
- Silkscreen (GTO, GBO)
- Drill files (TXT or DRL)
- Board outline (GKO or GM1)

### Additional Files
- Pick-and-place file (CSV or TXT)
- Bill of Materials (BOM.csv)
- Assembly drawing (PDF)
- Fabrication drawing (PDF)

## Design Rules

Typical PCB specifications:
- **Minimum track width**: 0.15mm (6 mil)
- **Minimum spacing**: 0.15mm (6 mil)
- **Minimum drill size**: 0.3mm (12 mil)
- **Via size**: 0.6mm hole / 1.0mm pad
- **Copper weight**: 1 oz (35 μm)

Adjust based on manufacturer capabilities.

## Getting Started

1. Open the PCB file in your EDA tool
2. Review the layout
3. Check design rule checks (DRC)
4. Generate manufacturing files
5. Review Gerber files before ordering

## Notes

- Always run DRC before generating manufacturing files
- Verify component footprints match actual parts
- Check silkscreen for component references
- Ensure proper fiducial markers for assembly
