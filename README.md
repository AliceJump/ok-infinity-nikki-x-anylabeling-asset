# Infinity Nikki · ok-script-toolkit templates

This repository is the source of editable [ok-script Toolkit](https://github.com/AliceJump/ok-script-toolkit) Template / Rect / Point annotations. In the application repository it is mounted as the `ok_templates/` Git submodule.

## Current working format

- `0.png`, `1.png` — initial images copied byte-for-byte from Nikki's current runtime atlas.
- `coco_annotations.json` — editable Template annotations, 5 existing feature names preserved.
- `screenshot_20261026_184825.png` — 3392×2400 choice scene used for `dialog_icon` and `skip_choose`.
- `screenshot_20261026_184802.png` — another background for replay validation, intentionally without duplicate template annotations.
- `boxes.json` — editable Rect annotations.
- `points.json` — editable Point annotations.

The initial pictures are packed/sparse **runtime images**, not full original screenshots. The new screenshots replace the history icon and W/S choice hint with native-resolution annotations. `skip_f` still represents the ordinary dialogue continuation prompt; the F beside the choice list is a different location and must not replace it, or the ordinary-skip branch would bypass choice scrolling. `skip_b` and `task_icon` retain their verified original crops because neither appears in the two new choice scenes. `1.png` remains as an original authoring reference.

Publishing templates writes `assets/coco_annotations.json` and `assets/images/` in the **application** repository; saving work files alone does not change application behavior. After editing or publishing, review the generated resources and app tests separately. Do not add a second annotation of the same category on the validation image: the runtime requires one box per template category.

The historical X-AnyLabeling source PNG/JSON data is preserved in the existing Git history at commit `592f0adf22abf7509ea88670a6a51b00d7f17a92`. It is not the current working format, and no X-AnyLabeling conversion tool is required.
