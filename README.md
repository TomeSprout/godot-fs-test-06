# Test Filesystem for Godot Projects

## Considerations

Ability to save assets and source files for content produced in external editors to be paired to project files.

The `project.godot` file is saved a level deeper in scanned project directory under `project/`.

- Files can be saved one level up relative to Godot project root.
- Files saved in the main directory will not interfere with Godot's realtime filesystem monitoring at `res://`

Created `import_stage` directory in main directory to house saved files from external editors. Work produced in these editors can then be imported into the project root directories to be utilized in project.

### Tree View of Filesystem and Folder Structure

![Filesystem Tree](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/755134b9-d2b1-47bf-95f5-5b61e9319a07/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220511%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220511T003700Z&X-Amz-Expires=86400&X-Amz-Signature=198c0b28fc716bd0703f78b57b59bcb2cd5c449d510dc00a1bcfbf2cfa6da12c&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)
