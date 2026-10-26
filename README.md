# Infinity Nikki · ok-script-toolkit templates

This repository is the source of editable [ok-script Toolkit](https://github.com/AliceJump/ok-script-toolkit) Template / Rect / Point annotations. In the application repository it is mounted as the `ok_templates/` Git submodule.

## Current working format

- `0.png`, `1.png` — initial images copied byte-for-byte from Nikki's current runtime atlas.
- `coco_annotations.json` — editable Template annotations, 5 existing feature names preserved.
- `boxes.json` — editable Rect annotations.
- `points.json` — editable Point annotations.

The initial pictures are packed/sparse **runtime images**, not full original screenshots. For new authoring work, take fresh screenshots in Toolkit and annotate them using its integrated editor. Publishing templates writes `assets/coco_annotations.json` and `assets/images/` in the **application** repository; saving work files alone does not change application behavior. After editing or publishing, review the generated resources and app tests separately.

The historical X-AnyLabeling source PNG/JSON data is preserved in the existing Git history at commit `592f0adf22abf7509ea88670a6a51b00d7f17a92`. It is not the current working format, and no X-AnyLabeling conversion tool is required.
