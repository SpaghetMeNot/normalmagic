# Tools Overview
!!! info "Custom Normals"
    Most of these tools create or edit ***custom normals***. These can be unintuitive to work with if you're unfamiliar with them.

    Once custom normals exist on a mesh, some default Blender tools/modifiers might not behave as expected. 
    Tools are included to fix situations such as [mirroring](normal_tools/repair_mirrored_normals.md) or [beveling](normal_tools/repair_bevel_normals.md) but it is something to be aware of.

## Pro Add-on
The Pro add-on is the fastest way to work with normalMagic:

- Set up modifiers, cutters and inserts in one click.
- Manage complex scenes with modifier/object dependencies.
- Work destructively without worrying about custom normal types.
- Use checkpoints to keep working with heavy modifier stacks without slowdown.

??? example "Add-on features"

    <div class="grid cards tool-grid side" markdown>

    -   :material-select-multiple:{ .tool-icon }

        [Boolean Pro](./add-on/boolean_pro.md)

        Select cutters, then the object, and click. Cutters are set up for you.

    -   :material-wave-arrow-down:{ .tool-icon }

        [Surface Integration](./add-on/surface_integration.md)

        Insert or project meshes onto a surface in one click.

    -   :material-file-tree-outline:{ .tool-icon }

        [Modifier References](./add-on/modifier_references.md)

        Show, hide, select or apply every object your modifiers reference.

    -   :octicons-link-16:{ .tool-icon }

        [Instance Objects](./add-on/instance_objects.md)

        Duplicate as instances, or use checkpoints to keep heavy stacks responsive.

    -   :material-monitor-eye:{ .tool-icon }

        [Object Display](./add-on/object_display.md)

        Make cutters and helpers "Viewport Only" so they never show in renders.

    -   :material-dock-top:{ .tool-icon }

        [Modifier Header](./add-on/modifier_header.md)

        Add common modifiers from a button bar above the modifier stack.

    -   :material-content-save-cog-outline:{ .tool-icon }

        [Modifier Defaults](./add-on/modifier_defaults.md)

        Save your preferred settings for any modifier. Kept through updates.

    -   :material-alert-outline:{ .tool-icon }

        [Free Normals Warnings](./add-on/free_normals.md)

        Get warned before edits or deformation break custom normals, with one-click fixes.

    </div>

[Add-on Documentation](./add-on/index.md)

## Asset Library
The core of normalMagic is an asset library of modifiers. You'll also find all of these tools in the sidebar.

### Mesh Modifiers
These modifiers affect normals, underlying geometry and other attributes such as UVs.

<div class="grid cards tool-grid side" markdown>

-   ![Boolean Pro Icon](./assets/icons/boolean_cut_7_sparkles.png){ .tool-icon .off-glb }

    [Boolean Pro](./mesh_tools/boolean_pro.md)

    Replacement for Blender's built-in Boolean modifier with extra options and accurate normals.

-   ![Boolean Trim Icon](./assets/icons/boolean_trim.png){ .tool-icon .off-glb }

    [Boolean Trim](./mesh_tools/boolean_trim.md)

    Cut and 'Trim' a mesh using single-sided cutter objects.

-   ![Boolean Extrude Icon](./assets/icons/boolean_extrude_5.png){ .tool-icon .off-glb }

    [Boolean Extrude](./mesh_tools/boolean_extrude.md)

    Cuts and extrudes where cutter meshes intersect.

-   ![Project to Surface Icon](./assets/icons/surface_blend_9.png){ .tool-icon .off-glb }

    [Project to Surface](./mesh_tools/project_to_surface.md)

    Project and blend geometry onto other mesh surfaces.

-   ![Surface Insert Icon](./assets/icons/surface_insert6.png){ .tool-icon .off-glb }

    [Surface Insert](./mesh_tools/surface_insert.md)

    Project, cut, blend and weld insert meshes into the surface of a mesh.

-   ![Symmetrize Icon](./assets/icons/symmetrize.png){ .tool-icon .off-glb }

    [Symmetrize](./mesh_tools/symmetrize.md)

    Single axis mirror with extra options that works with custom normals.

-   ![Solidify Pro Icon](./assets/icons/solidify_pro_5.png){ .tool-icon .off-glb }

    [Solidify Pro](./mesh_tools/solidify_pro.md)

    Solidify meshes with advanced profile control. Supports custom normals.

-   ![Offset Surface Icon](./assets/icons/offset_surface.png){ .tool-icon .off-glb }

    [Offset Surface](./mesh_tools/offset_surface.md)

    Offset the surface of a mesh with options for even thickness.

-   ![Cut Groove Icon](./assets/icons/cut_groove_2.png){ .tool-icon .off-glb }

    [Cut Groove](./mesh_tools/cut_groove.md)

    Cut a v-shaped groove or gap into a surface where cutter objects intersect.

</div>

### Normal Modifiers
These modifiers affect the normals of a mesh and nothing else.

<div class="grid cards tool-grid side" markdown>

-   ![Normal Transfer Icon](./assets/icons/normal_transfer_4.png){ .tool-icon .off-glb }

    [Normal Transfer](./normal_tools/normal_transfer.md)

    Transfer normals from other mesh objects.

-   ![Smooth Normals Icon](./assets/icons/smooth_normals_1.png){ .tool-icon .off-glb }

    [Smooth Normals](./normal_tools/smooth_normals.md)

    Smooth normals without smoothing mesh topology.

-   ![Face Weighted Normals Icon](./assets/icons/weighted_normals2.png){ .tool-icon .off-glb }

    [Face Weighted Normals](./normal_tools/face_weighted_normals.md)

    Face weighted normals with selection control.

-   ![Bent Normals Icon](./assets/icons/bent_normals_1.png){ .tool-icon .off-glb }

    [Bent Normals](./normal_tools/bent_normals.md)

    Calculate bent normals directly on geometry for better ambient lighting.

-   ![Repair Bevel Normals Icon](./assets/icons/repair_bevel.png){ .tool-icon .off-glb }

    [Repair Bevel Normals](./normal_tools/repair_bevel_normals.md)

    Fix the normals of bevels on meshes with custom normals.

-   ![Repair Boolean Normals Icon](./assets/icons/repair_boolean_normals_1.png){ .tool-icon .off-glb }

    [Repair Boolean Normals](./normal_tools/repair_boolean_normals.md)

    Fix bad normals caused by applied Booleans.

-   ![Repair Mirrored Normals Icon](./assets/icons/repair_mirrored.png){ .tool-icon .off-glb }

    [Repair Mirrored Normals](./normal_tools/repair_mirrored_normals.md)

    Flip custom normals on mirrored geometry so they point the right way.

-   ![Lock Normals Icon](./assets/icons/lock_normals.png){ .tool-icon .off-glb }

    [Lock Normals](./normal_tools/lock_normals.md)

    Create custom normals, or convert between "Free" and "Tangent Space" normals.

</div>

### Visualize Modifiers
These modifiers produce geometry to visualize normals and related attributes.

<div class="grid cards tool-grid side" markdown>

-   ![View Normals Icon](./assets/icons/view_normals_eye_1.png){ .tool-icon .off-glb }

    [View Normals](./visualize_tools/view_normals.md)

    Visualize mesh normals in the viewport.

-   ![View Sharp Icon](./assets/icons/view_sharp.png){ .tool-icon .off-glb }

    [View Sharp](./visualize_tools/view_sharp.md)

    Visualize sharp edges in the viewport.

</div>

### Other Modifiers
These modifiers change things related to normals, such as sharp edges or face orientation.

<div class="grid cards tool-grid side" markdown>

-   ![Instance Object Icon](./assets/icons/instance_object1.png){ .tool-icon .off-glb }

    [Instance Object](./other_tools/instance_object.md)

    Instance another object to replace or append to the current geometry.

-   ![Mark Sharp Icon](./assets/icons/mark_sharp.png){ .tool-icon .off-glb }

    [Mark Sharp](./other_tools/mark_sharp.md)

    Mark sharp edges by angle, with options to add or remove custom normals.

-   ![Sharp Edges to Attribute Icon](./assets/icons/sharp_to_attribute.png){ .tool-icon .off-glb }

    [Sharp Edges to Attribute](./other_tools/sharp_edges_to_attribute.md)

    Write edge and point attributes based on sharp edges.

-   ![Auto-Flip Faces Icon](./assets/icons/auto-flip.png){ .tool-icon .off-glb }

    [Auto-Flip Faces](./other_tools/auto-flip_faces.md)

    Detect and fix flipped faces automatically.

-   ![Change Materials Icon](./assets/icons/change_materials.png){ .tool-icon .off-glb }

    [Change Materials](./other_tools/change_materials.md)

    Assign materials or material indices to face selections.

</div>

### Manual Tools
These tools are available as destructive operations. There isn't much here yet, if you wish to see more modifiers become manual tools please reach out!

<div class="grid cards tool-grid side" markdown>

-   ![Recalculate Normals Icon](./assets/icons/recalculate_normals.png){ .tool-icon .off-glb }

    [Recalculate Normals](./manual_tools/recalculate_normals.md)

    Weighted normals and mark sharp for selected geometry in Edit Mode.

-   ![Add Custom Normals Icon](./assets/icons/add_custom_normals_object.png){ .tool-icon .off-glb }

    [Add Custom Normals](./manual_tools/add_custom_normals.md)

    Add custom normals to selected mesh objects.

</div>
