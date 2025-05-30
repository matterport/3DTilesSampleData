# 3DTilesSampleData

A small set of example Matterport generated 3d-tiles tilesets

3d-tiles extensions required: `3DTILES_content_gltf`
GLTF extensions required: `KHR_draco_mesh_compression` `KHR_texture_basisu`
GLTF optional extension (not released yet): `MTTR_three_mesh_bvh` provides a in-line pre-processed buffer of a [three-mesh-bvh](https://github.com/gkjohnson/three-mesh-bvh) boundsTree.

LOD levels start at 0 being the lowest resolution, and increase in mesh and texture detail as the numbers increase. Only publishing up to a max of 4 levels here for simplicity sake, as the tilesets can get fairly large!

`mesh_tiles/#/` folders contain the mesh and texture data for a specific LOD level
the .ktx2 files are downscaled versions of the higher resolution .jpg texture using the same uv's.
Textures are externally referenced from the .glb files, since matterport re-uses the same texture atlas across multiple .glb files within an LOD level.

Matterport has an internal extenstion to 3d-tiles which identifies the tiles in view, and will prioritize streaming in higher resolution .jpg texture for a number of tiles. information about the content of the individual tiles, the texelSize of each texture and what the scale factor is between the .ktx2 minimal texture and the full resolution texture is included in the tile.extras.

# Models
