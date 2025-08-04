# Repair Mirrored Normals

Mirroring a mesh with custom normals will not mirror the normals. This leads to incorrect normals on the mirrored geometry.

This modifier will detect mesh islands with flipped normals and what axis they need flipping on.

<div class="grid cards" markdown>
- ![Mirrored Flipped](../assets/mirrored_flipped.png)
Unmirrored Custom Normals
- ![Mirrored Unflipped](../assets/mirrored_unflipped.png)
Mirrored Custom Normals
</div>

## Options

- **Normal Domain.** Whether normals are stored on points (smooth) or face corners (allows sharp edges)
- **Method.** Choose which faces get mirrored normals:
    - **Detect.** Faces and axes will be determined automatically, this should work in most cases.
    - **Specify.** Specify which faces to flip normals and which axes to flip them on.