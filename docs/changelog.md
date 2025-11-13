# Changelog

## 1.1

### Asset Library

- Surface Project: Complete refactor to better match the options on Surface Insert.
    - Introduced "Wrap" Mode.
    - Option to turn off normal transfer.
- Surface Insert:
	- Renamed "Projection Origin" to "Base Height".
	- "Base Height" no longer shows when in "Blend to Surface" mode. 
	- Fixed Cases where cutters would be flipped when generated causing several bugs.
	- Refactored height calculation — should be no change to behavior.
	- Added Debug for projection direction.
    - Cleaned up all attributes created by modifier.
- New Modifier: Symmetrize:
	- Mirror-like modifier for single axis symmetry.
	- Works with custom normals.
	- Local/Global/Object space mirroring.
- Repair Mirrored Normals:
	- Added Mirror Object option.
- New Modifier: Change Materials:
    - Assign materials or material indices to face selections.
- New Modifier: Lock Normals:
    - Creates custom normals if none exist.
    - Allows converting normals to "Tangent Space" which allows for deformation after setting.
- New Manual Tool: Add Custom Normals:
    - Tool version of "Lock Normals" for Object and Edit Mesh modes.
- Normal Transfer:
	- Improving sharp edges appearing when transferring normals on small meshes.
- Smooth Normals:
	- Fixed broken normals on very small meshes.


### Add-on

- Moved "Link Split Mesh" next to the "Split" Button.
- Moved "Refresh" button above "Add Asset Library" to encourage use.
- "Add Asset Library" now runs the "Refresh" operator to avoid adding the same library twice.
- Fixed error when cutter collection is hidden/disabled.
- Added "No Change" option to cutter display options.
- Fixed cutters moving when using the redo panel. This occurred when parenting was on.
- Now allows example file to live in the same folder as the asset library.