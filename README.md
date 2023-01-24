# Test Filesystem for Godot Projects

## Considerations

Ability to save assets and source files for content produced in external editors to be paired to project files.

The `project.godot` file is saved a level deeper in scanned project directory under `project/`.

- Files can be saved one level up relative to Godot project root.
- Files saved in the main directory will not interfere with Godot's realtime filesystem monitoring at `res://`

Created `import_stage` directory in main directory to house saved files from external editors. Work produced in these editors can then be imported into the project root directories to be utilized in project.

### Tree View of Filesystem and Folder Structure

```bash
.
├── README.md
├── .gitignore
├── .github/
│   └── workflows/
│       └── godot_ci.yml
├── build/
│   └── win/
│       └── game.exe.test
├── docs/
│   └── filesystem.md
├── import_stage/
│   ├── effect.acd
│   ├── player.xcf
│   ├── player_tileset.xcf
│   └── song.sfas
└── project/
    ├── addons/
    │   └── godot-git-plugin/
    ├── default_env.tres
    ├── icon.png
    ├── icon.png.import
    ├── project.godot
    ├── src/
    │   ├── Level.tscn
    │   └── Level.tscn
    ├── assets/
    │   ├── sprites/
    │   │   ├── player.png
    │   │   └── player_tileset.png
    │   ├── music/
    │   │   └── song.ogg
    │   └── sounds/
    │       └── effect.wav
    └── test/
        └── unit/
            └── test_player.gd
```
