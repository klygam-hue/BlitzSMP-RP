# Blitz SMP Resource Pack

**Minecraft Java 26.3 · Format 97.1 · Custom resources only**

[Download VisualPack v5 + Cameras](https://raw.githubusercontent.com/klygam-hue/BlitzSMP-RP/v5-mc26.3/BlitzSMP26.3-VisualPack-v5-Cameras.zip)

This version contains **zero bundled vanilla texture files** and no unmodified
vanilla client assets. Minecraft supplies its default textures, models, shaders,
fonts and other standard resources. Existing mod visuals and all 20 BlitzCameras
asset files are retained. Download size: 9,207,359 bytes.

## Server setup

Stop the server, copy these settings into `server.properties`, and restart:

```properties
# Minecraft Java 26.3 - Blitz SMP VisualPack v5 + Cameras (custom resources only)
resource-pack=https://raw.githubusercontent.com/klygam-hue/BlitzSMP-RP/v5-mc26.3/BlitzSMP26.3-VisualPack-v5-Cameras.zip
resource-pack-sha1=95488d703326f8f5878972f75088a1d982e6c437
resource-pack-id=c07b09ae-2a8d-58a2-ae84-d0170ca64d87
resource-pack-prompt={"text":"Install the Blitz SMP resource pack for custom textures and security cameras.","color":"aqua"}
require-resource-pack=true
```

`require-resource-pack=true` makes accepting the pack mandatory; use `false`
for optional installation. The download URL is pinned to this version's tag.
The pack UUID stays the same as v4; the URL and SHA-1 have changed.

When distributing this combined pack through the server properties, leave
the separate BlitzCameras `resource-pack.url` empty.

## Manual installation

Enable this ZIP in place of the older full pack. A separate camera pack is
not required. Keeping an old full pack enabled would load its vanilla overrides.

## Included resources

The pack retains Create, Copycats, Flywheel, Ponder, Vanillin, Fabric,
BlitzSMPAeronautics and BlitzCameras resource namespaces from the previous
version. The Minecraft namespace contains only additional atlas sources and
the original mod's train hat attachment definitions, with no vanilla textures.
Atlas additions are merged with the client's default atlas sources at runtime.

Mod custom item types and mechanics require matching client mods for 26.3.
This resource pack does not install or port mod code.

## Validation

- Removed **11,602** unchanged standard client files.
- Zero files in `assets/minecraft/textures/` and zero unchanged vanilla assets.
- All camera and other custom namespace assets preserved byte-for-byte from v4.
- Minecraft 26.3 client decoders accepted 2,404 models,
  680 item definitions, 2 atlas files
  and 3 equipment assets, with no errors.
- All 16 tested custom shader variants compiled with ShaderC,
  using default Minecraft shader includes from the installed client.
- Parent model and palette references resolve against the pack plus the default client.
- 64 mod-specific item definitions require their corresponding mod registries.

Visual gameplay and mod renderer runtime testing were not performed. See
[VALIDATION.txt](VALIDATION.txt) and [validation.json](validation.json).

SHA-1: `95488d703326f8f5878972f75088a1d982e6c437`

SHA-256: `09c0af495c36326467ec216d4bc92a3f51f952947f32406d8f2a94e29a2af913`

Bundled third-party mod assets retain their respective authors' rights and licenses.
The repository license does not relicense those assets.
