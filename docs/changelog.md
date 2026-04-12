# Changelog

## 2.0

### New Modifiers

- [Cut Groove](./mesh_tools/cut_groove.md): Cuts a V-shaped groove or gap where other meshes intersect.
- [Solidify Pro](./mesh_tools/solidify_pro.md): Solidify meshes with advanced profile control. Supports custom normals.
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
	- New "Non-manifold fallback" solver option.
- [Face Weighted Normals](./normal_tools/face_weighted_normals.md):
	- Now takes into account corner angle. Triangulated meshes now have better weighting.
- [Symmetrize](./mesh_tools/symmetrize.md)
	- Added support for mirroring instances.
	- Added option to convert geometry to an instance before mirroring. This works well when using the object as an insert mesh with [Surface Insert](./mesh_tools/surface_insert.md).

### Pro Add-on
- Single file download/install for normalMagic Pro (Asset library is now packaged with the add-on)
- New Panel: [Surface Integration](./add-on/surface_integration.md). Contains operators for:
	- [Surface Insert](./mesh_tools/surface_insert.md)
	- [Project to Surface](./mesh_tools/project_to_surface.md)
	
- New Panel: [Modifier References](./add-on/modifier_references.md)
- New Panel: [Object Display](./add-on/object_display.md)
- [Boolean Pro Panel](./add-on/boolean_pro.md)
	- "Advanced Boolean" sub-panel contains new operators:
		- [Boolean Extrude](./mesh_tools/boolean_extrude.md)
		- [Boolean Trim](./mesh_tools/boolean_trim.md)
		- [Cut Groove](./mesh_tools/cut_groove.md)
	- Modifier Settings now handled by the [modifier defaults](./add-on/modifier_defaults.md) system
- [Modifier Header Bar](./add-on/modifier_header.md).
	- [Mark Sharp](./other_tools/mark_sharp.md). Available in the modifier header
- [Modifier Defaults](./add-on/modifier_defaults.md). Save default settings for modifiers added via the add-on


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