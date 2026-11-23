# Preferences

These options show up under ***Edit/Preferences/Add-ons/normalMagic***

!!! info "Kept Through Updates"
    Preferences and [Modifier Defaults](./modifier_defaults.md) are kept when you update the add-on.

## UI Preferences

- **Show Sidebar Panel.** Enable/disable the add-on's sidebar panel. Expand to specify it's category (default is "Normal Magic")
- **Show Modifier Header.** Enable/disable the [modifier header](../add-on/modifier_header.md). Expand to choose which add-modifier buttons show in the header.

## Auto Smooth

- **Preferred Smooth Modifier.** Which smooth modifier (**Mark Sharp** or **Smooth by Angle**) gets added with Boolean Pro's cutter "Auto-Smooth" option and [Shade Auto Smooth (First)](../other_tools/mark_sharp.md#shade-auto-smooth-first).
- **Shade Auto Smooth (First) in Object Menu.** (On by default) Show [Shade Auto Smooth (First)](../other_tools/mark_sharp.md#shade-auto-smooth-first) in the object right-click menu.

## Normal Warnings

- **Warn About Free Source Normals.** Show a warning in the tool header when selected meshes store "Free" custom normals. See [Free Normals Warnings](./free_normals.md).
- **This Scene.** Turn hidden warnings back on for the current scene:
    - **Hide Free Source Normals Warning.**
    - **Hide Deform Normals Warning.**

## Asset Library

Shows the asset library the add-on is using, its version and its location. If there is a problem with the library (missing, disabled, or a version that doesn't match the add-on) it is shown here with a button to fix it.

- **Location.** Which asset library to add modifiers from:
    - **Bundled.** (Default, recommended) Use the asset library that comes with the add-on. It is set up automatically when the add-on is installed or updated, so it always matches the add-on's version.
    - **Custom.** Use one of your own asset libraries. Choose the library from the list, or press ++"Manage Libraries"++ to open Blender's asset library preferences.
- **Import Method.** How normalMagic node groups are added to files:
    - **Packed.** (Default) Pack node groups into each file. Files work anywhere and keep their version until you update them.
    - **Linked.** Link node groups from the asset library. Files always use the installed version, but need the asset library to open correctly.
- **Offer to Update Existing Modifiers.** Show a button to update normalMagic modifiers in files made with an older version. See [Update Existing Scenes](../install.md#update-existing-scenes).

### Other normalMagic Libraries

If other normalMagic asset libraries are installed (for example the [Base version](../install.md#base-version-asset-library) or an older version), they are listed here. While enabled, their modifiers will also show up in Blender's "Add Modifier" menu. You can disable them (Blender 5.2+), or remove them from Blender's preferences with the ++"Remove Asset Library"++ button (the files aren't deleted).
