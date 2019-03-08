# World data structures

Chunk Stories has a concept of "worlds". Worlds are currently a fixed-sized in Chunk Stories, but they have a neat feature where they will wrap arround their borders: Walking long enough in the same direction means you'll reach your starting point. Worlds have a current max limit of 65x65km (1m = 1 block wide), and 1024 blocks of height.

## Voxel cells data format

### Voxel cell format version 2.0 (changed in API 106)

Stores all voxels in 32-bit signed ints ( Java won't allow unsigned :c )

![](../images/voxel_bits.png)

 * 0->15 16-bit block**I**D, allowing for 65536 different block types
 * 16->19 4-bit **S**unlight
 * 20->23 4-bit **B**locklight
 * 24->31 8-bit **M**eta data

The `VoxelFormat` helper class available in the api has methods to pack/unpack the raw cell data.