Cycles to other Render engines Converter Addon for Blender
This addon expands Blender's functionality by allowing you to convert Cycles shaders to other engines.

Latest Realese: 
https://github.com/zorianpl/Material_Converter_Main/releases

Luxcore Render module installed.

Accurate Node Connection Replication: Reads the Cycles node connections and meticulously rebuilds them using corresponding Luxcore nodes, ensuring a faithful translation of your material setups.

Three buttons for conversion:

Convert all Cycles material to Luxcore Material: Converts all Cycles materials to Luxcore materials (skipping those that already have Luxcore shaders).

Convert Single Material to Luxcore: Converts a single Cycles material to Luxcore (overwrites the Luxcore node tree with the Cycles node tree).

Convert all materials in selected Object to Luxcore Materials: Converts all materials in the selected object to Luxcore materials (if LuxCore shaders exist, the material is skipped).

Luxcore module translates the following nodes:

Textures
Color Mix Node
Shader Node Mix node
Bump Node
Invert Node (if it detects a texture connected to the invert node, it adds an additional auxiliary node that replicates the texture color settings to those from Cycles)
2D Mapping
Principled BDSF to Disney material / Glass Material depending on what it detects (Glass material may be read incorrectly in this case, I don't use Cycles very often)
If it detects Glass material in Cycles, it imports it as the main Glass material in Luxcore.
If it detects a Translucency node, it imports the Translucency material instead of Disney.
Color Ramp with color settings from Cycles and all inputs from Cycles
Hue/Saturation/Value
If there is UV mapping in Cycles connected to transform, it uses the same UV map.

Planned Features:

Material Presets: Add presets that transform a material into another type while preserving the existing node connections (except for the main material node). For example, convert a Disney material to a Translucent material with a single click, with the addon automatically connecting all existing textures to the new Translucent node.
Additional modules for converting shaders to Vray and Octane.
Expanding the list of supported nodes.
Improving conversion accuracy, especially for Glass Material.
Expanded Material Presets: Plan to include 6 material presets: Disney, Metal, Glass, Translucency, Two-sided Translucency, and Fabric (currently requires code adjustments for the new connection method).

[![Watch the video](https://img.youtube.com/vi/8kH7x_tLKQE/maxresdefault.jpg)](https://youtu.be/8kH7x_tLKQE)

### [Cycles to LuxCore Convert Video ](https://youtu.be/8kH7x_tLKQE)


