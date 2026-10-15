# Blitz SMP Resource Pack

**Minecraft Java 26.3 · Format 97.1 · Custom resources only**

[Download VisualPack v6 + Cameras](https://raw.githubusercontent.com/klygam-hue/BlitzSMP-RP/v6-mc26.3/BlitzSMP26.3-VisualPack-v6-Cameras.zip)

This pack contains no standard vanilla textures. Minecraft provides its
default resources. The existing mod visual assets and camera/computer/control
models are included, along with six native head skin assets.

## Camera rendering fix

Use this release with **BlitzCameras 1.0.1**. Placed devices now texture the
real head block using a resource-pack skin patch. The old display model over
a default player head is removed. Existing devices are updated on chunk load.

The plugin update also locks camera viewers in place by setting client walk
and fly speeds to zero, disabling gravity, locking the movement attribute,
rejecting even tiny position changes and zeroing external velocity. Mouse
rotation remains available. Original movement settings are restored on exit.

**Update both the plugin and the resource pack.** Keep the existing plugin data.

## Server setup

Stop the server, copy these settings into `server.properties`, and restart:

```properties
# Minecraft Java 26.3 - Blitz SMP VisualPack v6 + BlitzCameras 1.0.1
resource-pack=https://raw.githubusercontent.com/klygam-hue/BlitzSMP-RP/v6-mc26.3/BlitzSMP26.3-VisualPack-v6-Cameras.zip
resource-pack-sha1=a2bf35d014a2b1b3ba6f45428ad5fbc6f38ba8a6
resource-pack-id=c07b09ae-2a8d-58a2-ae84-d0170ca64d87
resource-pack-prompt={"text":"Install the Blitz SMP resource pack for custom textures and security cameras.","color":"aqua"}
require-resource-pack=true
```

`require-resource-pack=true` makes accepting the pack mandatory; use `false`
for optional installation. This URL pins v6. The pack UUID is unchanged.
When using the server resource pack, leave the separate BlitzCameras
`resource-pack.url` empty.

## Validation

- No files in `assets/minecraft/textures/`; other custom mod assets preserved.
- All six native skin IDs resolve to 64x64 PNGs using the actual client asset mapping.
- Native skins have opaque head fronts and transparent outer hat layers.
- Minecraft 26.3 decoded 2404 models, 680 standard item
  definitions, 2 additive atlases and 3 equipment definitions without errors.
- All 16 tested custom shader variants compiled with ShaderC.
- BlitzCameras 1.0.1 passed 80 simulated-player assertions on real Paper 26.3,
  including native skull profiles, migration, wall facing, movement locking,
  original speed/gravity restoration, inventory recovery and recording/playback.

These are headless resource/API tests, not visual gameplay tests. The
64 mod-specific item definitions need matching client mods. This pack does
not install or port mod code. See [validation.json](validation.json).

SHA-1: `a2bf35d014a2b1b3ba6f45428ad5fbc6f38ba8a6`

SHA-256: `a25e166e99ef5adb599a769789851b6aeac63cd113d33daab64ac2bbe8b84bf4`

Third-party mod assets retain their authors' rights and licenses.
