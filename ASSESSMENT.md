# Recovered weapon assets

These are the existing saved assets recovered from the interrupted session. No modeling, material editing, new animation, or source/export resaving was performed during recovery. New renders were made by opening the saved Blender files.

## Quality assessment

Both assets remain unfinished studies. Successful reopening/export validation does not establish professional realism. The user-supplied firearm and katana photographs are the visual authority; no historical-accuracy claim is made.

- Firearm: the long barrel and swept stock are recognizable, but the lock assembly still reads as layered plates with simplified jaws, spring and screw details. Wood grain remains subdued and surface wear is limited. The reference has more nuanced fitted and rounded metalwork.
- Katana: the curved blade, collar, black crossed wrapping and independent saya are present. White underwrap openings remain large compared with the reference; the cord knot and fittings are simplified. Blade reflections and the hamon remain less convincing than the reference.
- No additional refinement was authorized during recovery, so these limitations were preserved.

## Verified recovery

Blender 4.3.2 opened both sources and rendered new 1600 x 1000 PNG side views and close-ups using Cycles, 64 samples, AgX, saved studio lighting, and denoising off. These new images are under each asset’s renders/recovered/ directory. The original five-angle render sets are retained under renders/previous/.

Both GLBs reimported successfully; their textures are embedded. Packed Blender images and external texture PNGs resolve. Object scales are one; source meshes have no nonfinite vertices, missing UVs, or zero-area faces. These checks do not prove absence of self-intersections or all topology issues. Open surfaces exist in decorative strips, curve ends, and the scabbard mouth; these are not watertight manufacturing models.

## Flintlock

- Evaluated triangles: 66,592; mesh objects: 47.
- World-space assembled/display bounds (X x Y x Z): 1.4840 x 0.0814 x 0.3232 m. The katana bounds include the separately displayed saya.
- Materials: BluedSteel, Brass, Flint, Walnut.
- External texture maps: 12 PNGs, each 1024 x 1024; base color, roughness and normal maps. Base color uses sRGB; roughness and normal use Non-Color. Maps are also packed in the blend.
- Source SHA-256, unchanged during recovery: `c4250a66e0bf24adaa4502107df810b115b4fcc571cc18b4df37fdd8e7ae7c68`.

- Preserved corrections: cock outline has 152 vertices after contour refinement; walnut specular IOR level is 0.1; normal-map strength is 0.07.
- Animation: Blender timeline frames 1–72 at 24 fps, cock/frizzen/trigger. GLB contains one combined animation with three rotation channels. Existing demonstration PNG frames are included; no new animation was created during recovery.
- Origin: root is at the butt datum, +X points toward the muzzle; moving components have local pivot origins. This is a visual flintlock asset, not a Tanegashima matchlock.

## Katana

- Evaluated triangles: 129,630; mesh objects: 27.
- World-space assembled/display bounds (X x Y x Z): 1.0200 x 0.0720 x 0.2496 m. The katana bounds include the separately displayed saya.
- Materials: Brass, Hamon | satin hardened edge, Iron, Lacquer, PolishedSteel, Same, Silk.
- External texture maps: 18 PNGs, each 1024 x 1024; base color, roughness and normal maps. Base color uses sRGB; roughness and normal use Non-Color. Maps are also packed in the blend.
- Source SHA-256, unchanged during recovery: `b1effbbf12f3e296664197eeb798351f79e9dddfae904efb96a05093ee463fc9`.

- Preserved corrections: blade-tip local Z is 0.087208 m; paired wrap ribbon width is 0.010400 m.
- Animation: none. No draw/sheath demonstration is claimed.
- Origin: sword assembly at grip, scabbard assembly at throat, under a common root. Components remain separately editable. +X points toward the tip.

## Existing export settings

glTF 2.0 binary GLB, selected asset objects and root empties, applied modifiers on export, +Y up conversion, embedded texture images, active actions merged and sampled. Studio cameras and lights are retained in Blender, excluded from GLB. Draco compression is disabled. Source modifiers remain editable. No engine integration or engine-specific import test was performed.

## Package and reproducibility

Open Flintlock/Flintlock.blend or Katana/Katana.blend in Blender 4.x. External textures sit in the adjacent textures/ folders, and each source also contains packed copies. The corresponding GLB can be imported independently. The manifest records SHA-256 hashes for every payload file. Source-generation scripts and stale .blend1 backups are intentionally excluded from this delivery to avoid confusing recovered assets with rebuild instructions or previous states.

Game repositories were not modified.
