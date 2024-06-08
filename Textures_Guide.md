# Custom Textures Guide
## Requirements
1. RawTex
2. HxD Editor

## Base knowledge
Stuff you should know before you start modding.
### Texture formats
1. Base color (_c): These textures define the base color of objects, they usually end in _c
2. Gloss maps (_g): These textures define the specular and gloss maps of an object, they are defined by the RGB and Alpha channels respectively.
3. Normal maps (_c): These textures define the relief of object, normally used to give them volume.
4. Mask maps (_mask): These textures are only used in certain suits and they define the type of detail array (type of fabric) the suit should use. Might be different for each suit.

## 1 - Convert from .texture to .dds
You can convert from .texture to .dds with RawTex, here are the most common settings:
1. a) "BC1" or "BC7" for color textures
   b) "BC7" for gloss textures
   c) "BC5" for normal maps.
3. "2048x2048" for HD textures - "256x256" for SD textures.
4. "Offset 0" for HD textures - "Offset 0x74" for SD textures.

## 2 - Convert from .dds to .texture
### HD Textures
1. Select the content of the .dds file until the content from the texture file starts, this might look slightly different depending on the format you saved your .dds file as. It's usually until 0x7F or 0x94.
2. Delete the selected content.
![Offset for Textures](https://raw.githubusercontent.com/okangel12345/SM2_Modding_Research/main/Resources/Offset_Textures_1.png)

### SD Textures
1. Select the content of the .dds file until the content from the texture file starts, this might look slightly different depending on the format you saved your .dds file as. It's usually until 0x7F or 0x94.
2. Paste the original .texture header from the SD .texture until 0x74.
