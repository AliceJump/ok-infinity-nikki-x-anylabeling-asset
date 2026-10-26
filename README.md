# Infinity Nikki · Toolkit template sources

The application mounts this repository as the `ok_templates` submodule. Edit Template annotations in `coco_annotations.json`, Rect annotations in `boxes.json`, and Point annotations in `points.json` using ok-script Toolkit.

The four active template names are `dialog_icon`, `skip_choose` (the W/S choice-screen marker), `chat_icon`, and `skip_f`. Their boxes follow the user's local Toolkit annotations. `skip_b` and the task-item marker have been removed along with the unreferenced original 0.png and 1.png atlases.

- `screenshot_20261026_184825.png`: source of the dialogue marker, W/S hint and chat-option icon.
- `screenshot_20261026_184802.png`: another background used to verify matching and text-band measurement.
- `screenshot_20261026_200542.png`: source of the user's new F template, also used to verify that task-item popups receive no automatic input.

The parent app requires dialogue and W/S markers before counting chat icons. It measures the text band to the right of each chat icon and remembers selection progress independently for each option-count/text-length fingerprint. Task-item popups and B-key fallback handling are disabled.

Publishing writes the parent app's `assets/coco_annotations.json`, sparse `assets/images` atlas files and `src/data/FeatureList.py`. Saving source annotations alone does not publish runtime changes. Each template category must have exactly one annotation.

The historical X-AnyLabeling files remain available in Git history at `592f0adf22abf7509ea88670a6a51b00d7f17a92`.
