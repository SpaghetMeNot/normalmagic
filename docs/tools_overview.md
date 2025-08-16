# Tools Overview

normalMagic is comprised of several tools. Some modify normals, some modify geometry and normals, and some visualize normals and related attributes.

!!! warning "Custom Normals"
    Most of these tools create or edit ***custom normals***. These can be unintuitive to work with if you're unfamiliar
    Once custom normals exist on a mesh, some default Blender tools/modifiers might not behave as expected. 
    Tools are included to fix situations such as [mirroring](normal_tools/repair_mirrored_normals.md) or [beveling](normal_tools/repair_bevel_normals.md) but it's something to be aware of.

## Common Tool Options
Many tools share common options, for reference they are listed in this section

### Mask Falloff Options
When two sets of data blend together there are often falloff controls. These can be found across normalMagic in tools such as [Normal Transfer](normal_tools/normal_transfer.md), [Surface Insert](mesh_tools/surface_insert.md) and [Surface Blend](mesh_tools/surface_blend.md).


#### Boundary Edge Expand
TODO

#### Boundary Edge Distance
TODO

#### Surface Distance
TODO


