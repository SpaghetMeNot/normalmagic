# :construction: Boolean Extrude

![Boolean Extrude Icon](../assets/icons/boolean_extrude_5.png){ width=128 }

Cuts and extrudes where cutter meshes intersect.

## Extrusion Operation

<div class="grid cards" markdown>
- ####**Emboss**   
![emboss](../assets/booleans/boolean_extrude_emboss.gif)
Slice mesh and extrude intersection faces in or out.
- ####**Panel** 
![panel](../assets/booleans/boolean_extrude_panel.gif)
Perform an "Intersect" Boolean and extrude the result into a solid panel.
</div>

!!! tip "Equal and Opposite"
    These two operations are essentially the inverse of each other. Duplicating the object and using opposite operations with different outsets can create interesting effects.

    ![Boolean Extrude Combined](../assets/booleans/bool_extrude_combined.png)

## Options

### Cutters
This section specifies which cutters to use.

- **Objects/Collection:** Choose individual mesh objects or a collection containing mesh objects.
- **Object Count:** How many cutter mesh objects to use (when in ***Objects*** mode).
- **Cutter Outset:** Expands the cutter mesh with options for even thickness.

### Extrude
This section details the extrude operation

### Inset (When Extrusion Mode = ***Extrude Faces***)
Inset the front of the extrude operation.

### Normals

### Weld