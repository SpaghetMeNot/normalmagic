# Surface Insert :construction_site:


Seamlessly join **insert meshes** into a mesh's surface.  
An **insert mesh** can be thought of as a "decal", "patch" or "plug".

There are two primary ways of performing the insert operation:

<div class="grid cards" markdown>
- ![Wrap to Surface](../assets/surface_insert/wrap_to_surface.gif)
**Wrap to Surface**  
Warp geometry to match the underlying surface.
- ![Mirrored Unflipped](../assets/surface_insert/blend_to_surface.gif)
**Blend to Surface**  
Keep world position of geometry and blend to surface via masking. This allows you to keep flat surfaces inside the insert mesh.
</div>

The **Surface Insert** Modifier performs the following steps:

1. Insert meshes are projected to surface geometry using one of the above methods.
- Normals, materials and UVs are transferred from the original surface to the insert meshes.
- The surface is cut and removed where insert mesh open edges are.
- Vertices are matched on both sides of the seam and welded.

!!! info "Mesh Islands"
    Insert meshes are performed per mesh island. Only mesh islands with open edges will be cut and welded into the original surface.

    - Manifold (solid) mesh islands can be projected but won't affect the underlying surface geometry.
    - Mesh islands that miss a raycast will be skipped entirely and a warning will show on the modifier.


## Requirements

1. A receiving mesh object. This will have the modifier on it.
2. An insert mesh with open edges. This will be projected, cut and welded into the surface of the receiving mesh.


## Options

### Insert Meshes
This section specifies which meshes to insert

- **Objects/Collection.** Choose individual mesh objects or a collection containing mesh objects
- **Object Count.** How many mesh objects to insert (when in ***Objects*** mode)

### Insert Mesh Projection

- **Method.** How to project the insert meshes to the underlying surface
    - **Wrap to Surface.** Warp geometry to match the underlying surface.
    - **Blend with Surface.** Warp geometry to match the underlying surface.

- **Projection Direction.** Which direction to project insert mesh(es)
    - **Mesh Island Normal.** Use average mesh island normal
    - **Insert Direction.** Specify a direction in the space of each insert object
    - **Object Direction.** Specify a direction in the space of receiving object

- **Projection Origin.** Where to use as the origin of the insert object. This will affect how the objects height is calculated for re-projection.

- **Height Offset.** Offsets insert mesh away from surface by a specified height.

- **Ray Length.** Maximum distance an insert mesh can have an effect.

#### Projection Masking
This section controls masking the projection of insert meshes to the surface. This is most useful when using ***Blend with Surface***.
![falloff](../assets/surface_insert/falloff.gif)
Controlling falloff is covered [here](../tools_overview.md#falloff-options)

#### Normals
This section controls how much of the surface normals are transferred to the insert mesh. This is most useful when using ***Blend with Surface***.

- **Normal Masking**
    - **Projection Mask**. Use the same mask falloff as the projection
    - **New Mask**. Create a new mask for normals

- **Recalculate Blend Normals.** Only available when using **Blend with Surface**. This will recalculate the normals on the blended portion of the insert mesh before transferring any from the surface.
- **Match Boundary Normals.** When choosing ***New Mask*** this will make sure the boundary edge of the insert mesh matches the normals on the underlying surface. Turn off to create a hard edge.

If ***New Mask*** is chosen, the settings for the falloff will appear below. Controlling falloff is covered [here](../tools_overview.md#falloff-options)

### Surface Boolean
This section controls how the surface is cut for the insert mesh.

- **Weld Surface.** Welds vertices between the surface and insert mesh. Turning this off will leave them as separate mesh islands.
- **Weld Distance.** Distance at which to weld vertices, this takes effect at several points during the process, not just the final weld between surface and insert mesh.
- **Boolean Extrusion.** How far to extrude the cutter shape from the surface. You might need to increase this value if the insert mesh covers a large area of curvature. You can preview cutters in the [Debug](#debug) panel.
    ![Boolean Extrusion](../assets/surface_insert/boolean_extrusion.gif)

### Materials
TODO

### Debug
TODO