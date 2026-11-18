# Changelog

## 2.1.0

### Asset Library

- [Cut Groove](./mesh_tools/cut_groove.md):
	- Added [Cutter Alignment](./mesh_tools/cut_groove.md#cutter-geometry) option. Choose how the groove is positioned relative to the cutter.
- [Solidify Pro](./mesh_tools/solidify_pro.md):
	- New [Bevel Weights](./mesh_tools/solidify_pro.md#bevel-weights) panel. Control how edge and vertex bevel weights are carried over to the rim.
- [Boolean Pro](./mesh_tools/boolean_pro.md):
	- Removed the "Sequential" Float solver option. This fixes Boolean Pro being ~3x slower in Blender 5.2.
	- Fixed wrong results with Union, Intersect and Slice when cutter islands overlap each other.
	- Faster "Difference" operation with the Manifold solver.
	- "Merge by Distance" is now a menu: **None** (default), **Boundaries Only** or **All Vertices**.
	- Merging vertices no longer creates false sharp edges. Normals at merged points are re-averaged, and existing sharp edges are kept.
- [Repair Bevel Normals](./normal_tools/repair_bevel_normals.md):
	- "Bevel Loop Angle" and "Bevel Boundary Angle" Mark Sharp options are now off by default.
- [Symmetrize](./mesh_tools/symmetrize.md):
	- New "Center Points" output attribute.
- [Surface Insert](./mesh_tools/surface_insert.md):
	- Around 13% faster.
- Internal helper node groups are now hidden from the Add › Group menu. Turn on "Show Hidden" in Blender's search preferences to see them.

### Pro Add-on

- [Modifier Updates for Existing Scenes](./install.md#update-existing-scenes). Modifiers in scenes made with an older version can now be updated with one click from the sidebar or modifier header. Settings are kept and the update can be undone.
- [Asset Library Preferences](./add-on/preferences.md#asset-library):
	- The bundled asset library is now set up automatically when the add-on is installed or updated.
	- Choose between the **Bundled** library or a **Custom** one.
	- New **Import Method** option: **Packed** (default) or **Linked**.
	- Other normalMagic asset libraries (e.g. Base version) are listed so they can be disabled or removed.
- Preferences and [Modifier Defaults](./add-on/modifier_defaults.md) are now kept when updating the add-on.
- [Free Normals Warnings](./add-on/free_normals.md). New warnings when "Free" custom normals won't follow edits or deformation, with one-click fixes.
- [Modifier Header](./add-on/modifier_header.md):
	- New add-modifier buttons: [Solidify Pro](./mesh_tools/solidify_pro.md), Bevel (with [Repair Bevel Normals](./normal_tools/repair_bevel_normals.md)), [Smooth Normals](./normal_tools/smooth_normals.md), [Face Weighted Normals](./normal_tools/face_weighted_normals.md) and [Normal Transfer](./normal_tools/normal_transfer.md).
	- Modifiers added from the header only collapse their object inputs panel. Modifiers added from the sidebar are collapsed completely.
- [Modifier Defaults](./add-on/modifier_defaults.md):
	- New **Restore Defaults** button. Reset the active modifier to your saved defaults (or the built-in defaults). Object and collection inputs are kept.
	- "Restore Defaults" from 2.0 is now called **Delete Custom Defaults**.
	- Added support for Solidify Pro, Repair Bevel Normals, Smooth Normals and Face Weighted Normals.
	- Output attribute names are now saved and restored (Blender 5.2+).
- [Modifier References](./add-on/modifier_references.md):
	- "Apply Modifier" renamed to **Apply Single Modifier**.
	- New **Collapse to Selected** button. Apply all modifiers from the top of the stack down to the highlighted one.
	- When applying or deleting a modifier would delete objects used by other modifiers, a **Shared References** dialog lets you keep them.
	- Applying modifiers converts "Free" custom normals to "Tangent" normals and makes shared meshes single user.
	- Around 3.5x faster panel redraws.
	- New [Filter References](./add-on/modifier_references.md#filter-references) options: show or hide modifiers without references, checkpoint sources and instance sources.
	- Show, Select and Select All now reveal objects in hidden collections, with a [Force Show](./add-on/modifier_references.md#hidden-collections) dialog listing the collections first.
- [Instance Objects](./add-on/instance_objects.md):
	- New [Checkpoints](./add-on/instance_objects.md#checkpoints). Create instance "checkpoints" of an object and step back and forth between them.
	- [Select Source](./add-on/instance_objects.md#select-source) and checkpoint Previous/Next now show hidden objects, including those in hidden collections (with a [Force Show](./add-on/modifier_references.md#hidden-collections) dialog).
- [Boolean Pro Panel](./add-on/boolean_pro.md):
	- "Auto-Smooth" cutter option now defaults to **All**. Instances and checkpoints are skipped.
	- Cutter collections are now per scene, reused by name instead of creating a new one for every cutter.
	- [Convert Existing Booleans](./add-on/boolean_pro.md#convert-existing-booleans) keeps modifier names, on/off toggles and stack position. Collection Booleans use Boolean Pro's Collection mode.
	- The [Convert Existing Booleans](./add-on/boolean_pro.md#convert-existing-booleans) button is back. It shows when selected objects have Blender Boolean modifiers.
- [Project to Surface](./add-on/surface_integration.md#project-to-surface):
	- Fixed error when "Single Surface" is turned off in the "Adjust Last Operation" panel. The active object can now project onto any number of selected surfaces, more than 6 adds extra modifiers.
- [Shade Auto Smooth (First)](./other_tools/mark_sharp.md#shade-auto-smooth-first). New operator in the object right-click menu: adds the preferred smooth modifier at the start of the modifier stack.
- Fixed errors when the asset library is missing (Mark Sharp, Symmetrize, Project to Surface and Boolean Pro with no cutters).
- When the asset library is missing, operators now cancel without changing anything. Previously cutter settings were still applied and Split left a stray duplicate.

## 2.0.2

### Asset Library

- [Solidify Pro](./mesh_tools/solidify_pro.md):
	- Fixed bevel weights getting broken on resulting mesh (tooling to control this coming in 2.1).
- [Symmetrize](./mesh_tools/symmetrize.md):
	- Fixed incorrect normals when custom normals are stored as tangents.

## 2.0.1

### Asset Library

- [Cut Groove](./mesh_tools/cut_groove.md):
	- Groove depth now has even thickness.
	- Better preservation of sharp edges from the base mesh.
- [Boolean Pro](./mesh_tools/boolean_pro.md):
	- New "Internal Edges" output attribute.
- [Recalculate Normals](./manual_tools/recalculate_normals.md):
	- New "Normal Type" option, "Tangent" by default.

### Pro Add-on

- Fixed an error message when removing modifiers.

## 2.0.0

<iframe width="900" height="390" src="https://www.youtube.com/embed/0sf4ywieXwA?si=Nxh37v053igm-wQy" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### New Modifiers

- [Cut Groove](./mesh_tools/cut_groove.md): Cuts a V-shaped groove or gap where other meshes intersect.
- [Solidify Pro](./mesh_tools/solidify_pro.md): Solidify meshes with advanced profile control. Supports custom normals.
- [Offset Surface](./mesh_tools/offset_surface.md): Offset the surface of a mesh.
- [Boolean Extrude](./mesh_tools/boolean_extrude.md): Extrude area of Boolean intersection area in or out.
- [Boolean Trim](./mesh_tools/boolean_trim.md): Cut and 'trim' a mesh with single-sided cutter objects.

### Existing Modifiers
- Surface Project renamed to [Project to Surface](./mesh_tools/project_to_surface.md):
	- Added Color debug options for projection and normal masks.
- [Surface Insert](./mesh_tools/surface_insert.md):
	- Added "Instances" option to insert mesh panel. You can now:
		- Realize instances and insert using their local transform (if applicable).
		- Realize instances and insert using their parent insert object's transform (if applicable).
		- Keep instances, maintain their relative position to the nearest insert geometry.
	- Debug Color for projection and normal masks.
	- Surface Boolean is now optional.
	- Added "Boolean Caps" menu to help with certain edge cases.
- [Boolean Pro](./mesh_tools/boolean_pro.md):
	- Has multi-object input like other mesh modifiers.
	- New "Non-manifold fallback" solver option.
	- Output attributes for boundary edges and slice faces.
- [Face Weighted Normals](./normal_tools/face_weighted_normals.md):
	- Now takes into account corner angle. Triangulated meshes now have better weighting.
- [Symmetrize](./mesh_tools/symmetrize.md):
	- Added support for mirroring instances.
	- Added option to convert geometry to an instance before mirroring. This works well when using the object as an insert mesh with [Surface Insert](./mesh_tools/surface_insert.md).

### Pro Add-on
- Single file download/install for normalMagic Pro (Asset library is now packaged with the add-on)
- [Surface Integration](./add-on/surface_integration.md). New panel, contains operators for:
	- [Surface Insert](./mesh_tools/surface_insert.md)
	- [Project to Surface](./mesh_tools/project_to_surface.md)
- [Modifier References](./add-on/modifier_references.md). New panel: show/hide, select/deselect, apply/delete objects referenced by modfiers on the active object.
- [Object Display](./add-on/object_display.md). New panel to manage object visibility.
- [Boolean Pro Panel](./add-on/boolean_pro.md)
	- "Advanced Boolean" sub-panel contains new operators:
		- [Boolean Extrude](./mesh_tools/boolean_extrude.md)
		- [Boolean Trim](./mesh_tools/boolean_trim.md)
		- [Cut Groove](./mesh_tools/cut_groove.md)
	- Modifier Settings now handled by the [modifier defaults](./add-on/modifier_defaults.md) system.
- [Modifier Header Bar](./add-on/modifier_header.md). Quickly apply modifiers and manage modifier references from the modifier properties panel.
- [Modifier Defaults](./add-on/modifier_defaults.md). Save default settings for modifiers added via the add-on.
- Added [Symmetrize](./mesh_tools/symmetrize.md) and [Mark Sharp](./other_tools/mark_sharp.md) operators. They are in the modifier header bar by default.
- All operators now support more than 6 cutters/inserts at a time.


----


## 1.1

### Asset Library

- [Surface Project](./mesh_tools/surface_project.md): Complete refactor to better match the options on Surface Insert.
    - Introduced "Wrap" Mode.
    - Option to turn off normal transfer.
- [Surface Insert](./mesh_tools/surface_insert.md):
	- Renamed "Projection Origin" to "Base Height".
	- "Base Height" no longer shows when in "Blend to Surface" mode. 
	- Fixed Cases where cutters would be flipped when generated causing several bugs.
	- Refactored height calculation — should be no change to behavior.
	- Added Debug for projection direction.
    - Cleaned up all attributes created by modifier.
- New Modifier: [Symmetrize](./mesh_tools/symmetrize.md):
	- Mirror-like modifier for single axis symmetry.
	- Works with custom normals.
	- Local/Global/Object space mirroring.
- [Repair Mirrored Normals](./normal_tools/repair_mirrored_normals.md):
	- Added Mirror Object option.
- New Modifier: [Change Materials](./other_tools/change_materials.md):
    - Assign materials or material indices to face selections.
- New Modifier: [Lock Normals](./normal_tools/lock_normals.md):
    - Creates custom normals if none exist.
    - Allows converting normals to "Tangent Space" which allows for deformation after setting.
- New Manual Tool: [Add Custom Normals](./manual_tools/add_custom_normals.md):
    - Tool version of "Lock Normals" for Object and Edit Mesh modes.
- [Normal Transfer](./normal_tools/normal_transfer.md):
	- Improving sharp edges appearing when transferring normals on small meshes.
- [Smooth Normals](./normal_tools/smooth_normals.md):
	- Fixed broken normals on very small meshes.


### Add-on

- Moved "Link Split Mesh" next to the "Split" Button.
- Moved "Refresh" button above "Add Asset Library" to encourage use.
- "Add Asset Library" now runs the "Refresh" operator to avoid adding the same library twice.
- Fixed error when cutter collection is hidden/disabled.
- Added "No Change" option to cutter display options.
- Fixed cutters moving when using the redo panel. This occurred when parenting was on.
- Now allows example file to live in the same folder as the asset library.