# normalMagic Home

!!! warning "Site under construction :construction_site: :construction:"

Welcome to the normalMagic documentation. Here you'll find everything there is to know about the tools.
<div class="grid cards" markdown>

- [:octicons-download-16: Install normalMagic](install.md)
- [:material-run: Examples](examples.md)

</div>

**normalMagic** is a versatile Blender toolset designed to give you powerful control over mesh normals and enhance modeling workflows.

Controlling normals can be essential for creating high quality 3D art. Whether it's for hard surfaces, foliage, cel shading, hair/fur... The list goes on! Modifying normals is sometimes the only way to get surfaces behaving the way you want.

!!! info "Custom Normals"
    Most of these tools create or edit ***custom normals***.

    Once custom normals exist on a mesh, some default Blender tools/modifiers might not behave as expected. 
    Tools are included to fix situations such as [mirroring](normal_tools/repair_mirrored_normals.md) or [beveling](normal_tools/repair_bevel_normals.md) but it's something to be aware of.

## Tool Highlights

### **Perfect boolean normals**

- Completely avoid boolean normal issues with [Boolean Pro](mesh_tools/boolean_pro.md).
- Repair normals on previously cut geometry with [Repair Boolean Normals](normal_tools/repair_boolean_normals.md).

### **Seamlessly blend surfaces**

- Project positions, normals and UVs with [Surface Blend](mesh_tools/surface_blend.md).
- Merge, cut and weld projected meshes into a surface with [Surface Insert](mesh_tools/surface_insert.md).

Convenient auto-masking options means no need for creating and managing vertex groups. Sharp edges can be preserved and transferred.

### **Smooth Normals**

Smooth normals to improve shading, achieve good toon lighting or for cheap subsurface scattering effects.


## Contact

If anything is unclear or missing, please reach out!  
:material-email: <spaghetmenot@gmail.com>  
:fontawesome-brands-bluesky: [@spaghetmenot.bsky.social](https://bsky.app/profile/spaghetmenot.bsky.social)  
:fontawesome-brands-mastodon: [@SpaghetMeNot@mastodon.social](https://mastodon.social/@SpaghetMeNot)