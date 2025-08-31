# Sharp Edges to Attribute

![Sharp Edges to Attribute Icon](../assets/icons/sharp_to_attribute.png){width=128}

Write edge and point attributes based on sharp edges or other arbitrary edge attributes.

<div class="grid cards" markdown>

- Edge attributes can be used for:  
    - Mark sharp edges as UV seams.
    - Add a bevel weight to sharp edges.
    - Detect sharp edges from custom normals and mark them as sharp.

- Point attributes can be used for:  
    - Creating a vertex group for selection in another modifier from sharp edges.
    - Expanding selection with or without a falloff.

</div>

## Options

### Sharp Edge Detection

How to specify edges to write to attribute(s)

- **Detect From Markup.** Use smooth shading attributes to define sharp edges. This might miss sharp edges defined by custom normals.
- **Detect Custom.** Detect sharp edges from normals. This will detect sharp edges created from custom normals but can have a small amount of error.
- **Tolerance (When "Detect Custom" is on).** Change the normal angle difference at which edges will be marked as sharp.

### Expand Points

Expand point selection. Can be useful in [Selection Panel](../common_settings.md#selection) of other modifiers.

- **Point Values.** How selection is expanded:
    - **Float.** Each expansion gets a lower value creating a falloff.
    - **Bool.** Each expansion is set to 1.
- **Expand Iterations.** How many edges to expand point selection.
- **Falloff (When Point Values are "Float").** Falloff of point selection. similar to [mask falloff](../common_settings.md#base-falloff)

### Output Attributes

What to name Edge / Point attributes. **Leaving blank will not write to any attributes.**
