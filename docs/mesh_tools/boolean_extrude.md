# :construction: Boolean Extrude

![Boolean Extrude Icon](../assets/icons/boolean_extrude_5.png){ width=128 }

Cuts and extrude the intersection area of a Boolean operation. There are two operations this modifier can perform:

<div class="grid cards" markdown>
- ![TODO: gif]()
**Extrude**  
Slice mesh and extrude intersection faces.
- ![TODO: gif]()
**Panel**  
Perform an "Intersect" Boolean and extrude the result into a solid panel.
</div>

!!! tip "Equal and Opposite"
    These two operations are essentially the inverse of each other, combining them can create interesting details.

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