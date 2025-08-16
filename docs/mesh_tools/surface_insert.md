# Surface Insert :warning:

**Surface Insert** will seamlessly "insert" one mesh into another mesh's surface.
The specified **Insert Mesh** will act as a "patch/decal/plug".

<div class="grid cards" markdown>
- ![Wrap to Surface](../assets/surface_insert/wrap_to_surface.gif)
**Wrap to Surface**  
Warp geometry to match the underlying surface.
- ![Mirrored Unflipped](../assets/surface_insert/blend_to_surface.gif)
**Blend to Surface**  
Keep world position of geometry and blend to surface via masking. This allows you to keep flat surfaces inside the insert mesh.
</div>

- Mesh Islands with open edges on the **Insert Mesh** will be projected, cut and welded into the surface.
- Manifold mesh islands can be projected but won't affect the underlying surface geometry.

## Requirements

1. A receiving mesh object. This will have the modifier on it.
2. An insert mesh with open edges. This will be projected, cut and welded into the surface of the receiving mesh.

## Features





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

### Projection Masking