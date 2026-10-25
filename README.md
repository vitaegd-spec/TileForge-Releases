# TileForge 1.13

**Search. Drag. Snap. Build. Animate. Export.**

TileForge is a Windows desktop scene builder for turning ordinary transparent PNG assets into finished **2D, isometric and one-point-perspective game scenes**, with a workflow designed around fast visual composition and direct **Godot 4** export.

Instead of forcing every prop into a conventional tileset, TileForge lets you mix **grid-fitted surfaces, upright props and completely free overlays** in the same scene, then add terrain rules, animation, collision, navigation, markers, lighting and room links.

## Why TileForge?

- **Four scene modes**: Square 2D, Isometric 2:1, true 60-degree isometric and one-point Perspective.
- **PNG-first asset library** with search, categories, tags, favourites, placement metadata and reusable prefabs.
- **Smart placement**: face-aware surfaces, upright snapped props, stick-to-face props, free overlays and arrow-key face targeting.
- **Real editing freedom**: grouping, resize/stretch, flip, rotation, draw-order control, free-form four-corner distortion and roof/ramp slopes.
- **Sheet Cutter** with background detection, editable boxes and pixel ownership so overlapping sprites do not contaminate each other.
- **Built-in Tile Editor** for cleanup, erasing, colour work and trimming.
- **Animated tiles** from sprite strips/grids with live preview.
- **Animated Strip Builder** for repairing AI-generated animation strips by locking a master body while allowing only a horizontal/vertical/rectangle/ellipse region to move.
- **Terrain Brush** with 16 edge-connectivity masks, fallback tiles and stable random variants.
- **Scatter Brush** for natural prop distribution with radius, density, spacing, scale variation and flipping.
- **Collision & navigation painting** for blocked, walkable, water and ladder cells plus collision footprints on props.
- **Gameplay markers**: spawn, NPC, chest/item, trigger, door/room link, light and custom metadata.
- **Lighting preview** with ambient presets and coloured light markers.
- **Multi-room projects** with door links and a navigable minimap.
- **Large-map chunk rendering** for smoother zoomed-out editing.
- **Commercial Asset Pack Builder** creates packaged PNGs, normalized assets, sprite sheets, contact sheets, marketplace thumbnail, inventories, licence, TileForge metadata and a Godot sample.

## Godot 4 export

TileForge can export complete Godot scenes with:

- TileMapLayer/TileSet floors for eligible Square 2D and Isometric 2:1 ground tiles
- Sprite2D and AnimatedSprite2D objects
- Y-sorted world sprites
- collision polygons
- water and ladder areas
- NavigationRegion2D data
- gameplay markers and metadata
- CanvasModulate + PointLight2D lighting
- optional chunk nodes and ChunkStreamer for large scenes

## Built for custom and AI-generated artwork

TileForge is especially useful when the source art is not a neat traditional tileset. Import individual PNGs, generated prop sheets, hand-painted textures or AI-created animation strips, clean them up inside TileForge and compose the playable scene visually.

## Project philosophy

TileForge focuses on the gap between **making artwork** and **building the actual game level**. The goal is simple: make loose game art immediately useful, keep composition visual, and export practical scene data without forcing the artist through a heavyweight 3D workflow.

## Current version

TileForge **1.13.0**

## License

Add the project license here before a public release. The Asset Pack Builder includes its own generated standard asset licence for packs you create; that is separate from the licence of the TileForge application itself.
