# Blitz SMP Resource Pack

Combined resource pack for **Minecraft Java 26.3**: updated vanilla resources,
the existing mod visual assets, and BlitzCameras camera/computer/control models.
Resource-pack format: **97.1**.

[Download VisualPack v4 + Cameras](https://raw.githubusercontent.com/klygam-hue/BlitzSMP-RP/v4-mc26.3/BlitzSMP26.3-VisualPack-v4-Cameras.zip)

## Server setup

Stop your server, copy these settings into `server.properties`, and start it again:

```properties
# Minecraft Java 26.3 - Blitz SMP VisualPack v4 + Cameras
resource-pack=https://raw.githubusercontent.com/klygam-hue/BlitzSMP-RP/v4-mc26.3/BlitzSMP26.3-VisualPack-v4-Cameras.zip
resource-pack-sha1=c72ea29e8b91ab778fad6c3701bde03a98ba4a22
resource-pack-id=c07b09ae-2a8d-58a2-ae84-d0170ca64d87
resource-pack-prompt={"text":"Install the Blitz SMP resource pack for custom textures and security cameras.","color":"aqua"}
require-resource-pack=true
```

`require-resource-pack=true` makes accepting the pack mandatory. Set it to `false`
if the pack should be optional. The tag in the download URL pins this version.

If you already distribute this combined pack through your server properties,
leave the separate BlitzCameras `resource-pack.url` setting empty.

## Manual installation

Put the downloaded ZIP in your client's `resourcepacks` folder and enable it.
Use this pack in place of the older 26.2 pack; a separate camera pack is not needed.

## What was updated

The vanilla layer was rebased on original 26.3 assets. Atlases, trim palettes,
equipment trim overrides, legacy cuboid shading and four mod shader programs
were updated for the new resource format. Existing mod namespaces, the pack
icon and all 20 BlitzCameras asset files were retained.

Validation used the actual Minecraft 26.3 client decoders: 6,596 models,
2,338 item definitions, 12 atlases and 48 equipment assets decoded without
errors. All 16 tested variants of the four updated shaders compiled with ShaderC.
ZIP integrity and camera resource references were also checked.

Visual gameplay testing and mod renderer runtime testing were not performed.
The 64 item definitions that use custom mod types/components need matching
client mods for 26.3. This resource pack does not install or port mod code.
See [VALIDATION.txt](VALIDATION.txt) for the detailed report.

## Checksums

SHA-1: `c72ea29e8b91ab778fad6c3701bde03a98ba4a22`

SHA-256: `f3afef2950d32309ffeb1643f86c40e0563aa5d02d11a00f4ce4933e5a3a59f9`

Vanilla and bundled mod assets retain their respective authors' rights and
licenses. The repository license does not relicense those third-party assets.
