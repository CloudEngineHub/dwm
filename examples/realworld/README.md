# Real-World Examples

- `realworld_fixed/`: raw fixed-view examples for the custom preprocessing path, including `pour_coke.mp4` and `lift_tumbler.mp4`.
- `realworld_dynamic/`: a small released dynamic-viewpoint subset with processed videos, hand videos, static videos, and rewritten prompts.

The dynamic-viewpoint data was created with ARIA. For details, please refer to the paper.

The full dynamic-viewpoint evaluation set used in the paper (48 samples, same layout) is available on Hugging Face: [byungjun-kim/DWM-RealWorld-Dynamic](https://huggingface.co/datasets/byungjun-kim/DWM-RealWorld-Dynamic).

```bash
hf download byungjun-kim/DWM-RealWorld-Dynamic --repo-type dataset --local-dir /path/to/dwm_realworld
```

To run the evaluation, pass `--data_root /path/to/dwm_realworld --dataset_file /path/to/dwm_realworld/realworld_selected_48.txt` to `training/wan/examples/infer_realworld.sh` or `training/cogvideox/examples/infer_realworld.sh`.
