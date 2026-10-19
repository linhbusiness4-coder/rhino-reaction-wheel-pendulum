# RWIP — Physical Design

CAD and 3D-printable part files for a **Reaction-Wheel Inverted Pendulum (RWIP)** —
a control-systems test rig that balances an inverted pendulum by spinning a
reaction wheel at its tip instead of driving the base.

![Platform](https://img.shields.io/badge/Platform-RWIP-blue) ![CAD](https://img.shields.io/badge/CAD-Rhinoceros--STL-green) ![Units](https://img.shields.io/badge/Units-mm-orange)

## Repository Layout

| File | Part | Size | Triangles | Bounding box (mm: X × Y × Z) |
|---|---|---|---|---|
| `Shaft & Sensor Holder.stl` | Shaft and sensor mount | 27.4 MB | 548,310 | 80.00 × 100.25 × 119.34 |
| `Stand 1.stl` | Main stand column | 23.6 MB | 471,258 | 28.29 × 43.13 × 260.00 |
| `link sensor.stl` | Sensor link (pendulum) | 10.0 MB | 200,628 | 74.11 × 44.15 × 99.66 |
| `ring.stl` | Stabilizer ring | 7.8 MB | 155,970 | 20.00 × 140.00 × 140.00 |
| `Stand 2.stl` | Secondary stand piece | 5.0 MB | 100,408 | 43.08 × 54.00 × 250.27 |
| `Physical.3dm` | Master Rhino CAD model | 1.85 MB | — | — |
| `Physical.3dmbak` | Rhino auto-backup of the above | 1.82 MB | — | — |

All STL bounding boxes assume **millimeters** (standard for Rhino exports).

## How to Use

- **CAD origins**: import all STLs into your slicer or CAD tool with the same
  origin — their coordinates above are already in a shared reference frame from
  the Rhino export, respecting each part's X/Y/Z placement.
- **Assembly order** (from the file names):
  1. `Stand 1.stl` + `Stand 2.stl` — build the base/frame.
  2. `Shaft & Sensor Holder.stl` — mounts the rotating shaft + sensor to the stand.
  3. `link sensor.stl` — attaches the measured pendulum link + sensor.
  4. `ring.stl` — reaction wheel hoop that spins to balance the assembly.
- **Printing**: all parts are STL-ready; the `.3dm` file is the authoritative
  source model in case a modification is needed.

## Requirements

- **Software**: any slicer (Cura, PrusaSlicer, Bambu Studio, etc.) or CAD
  viewer that reads STL (MeshLab, Fusion 360, Rhino) — plus Rhino for the `.3dm` file.
- **Hardware to build**: this repo only covers the physical design. You'll need
  a motor + IMU/encoder driver and control loop separately (not included here).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to propose changes
(new part revisions, tolerances, alternative sensor mounts…).

## License

MIT — see [LICENSE](LICENSE).
