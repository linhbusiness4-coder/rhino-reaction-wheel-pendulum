# Contributing to RWIP — Physical Design

Thanks for your interest in improving the Reaction-Wheel Inverted Pendulum design!

## How to propose a change

1. **Fork** the repo (or create a branch if you have write access):
   ```bash
   git checkout -b my-part-revision
   ```
2. Keep file naming consistent: `Part Name.stl` (spaces allowed) with a
   matching entry in the README table.
3. **Regenerate STLs from the `.3dm` master** — don't hand-edit meshes.
   Keep Rhino units in millimeters.
4. Update the README **Repository Layout** table (size / triangles / bounding
   box) so the docs stay in sync with the parts.
5. Open a Pull Request describing:
   - what changed physically (dimensions, mounting, material),
   - print settings used (material, layer height, infill),
   - whether the part was test-printed and how it fit.

## CAD conventions

- The `.3dm` file is the **single source of truth** for geometry.
- STLs are exports; never the other way around.
- Shared origin across parts so assemblies import in place.

## Issues

Use Issues for fit problems, print failures, or design suggestions. Include
photos when possible and your printer/material if relevant.

## License

By contributing you agree that your contributions are licensed under the
MIT License that covers this repository.
