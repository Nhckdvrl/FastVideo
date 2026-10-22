# Bernini-R video-editing comparison

Input: [Bernini's snowman example video](https://github.com/bytedance/Bernini/blob/e6c2cf11843470b08491745947abcba9c3c6b079/assets/testcases/v2v/source_case1.mp4).

Checkpoint: [ByteDance/Bernini-R-1.3B-Diffusers](https://huggingface.co/ByteDance/Bernini-R-1.3B-Diffusers/tree/ff4c5d4d2d31365c2ffeb30e9753065ee18f58ce).
Reference implementation: [bytedance/Bernini](https://github.com/bytedance/Bernini/tree/e6c2cf11843470b08491745947abcba9c3c6b079).
FastVideo implementation: [67933a1](https://github.com/Nhckdvrl/FastVideo/commit/67933a16646e67f6d49df0a95d8b034332bfcc6f).

The source, official, and FastVideo JPEG previews show the frame at 2.5 seconds.
The two MP4 files are the original saved outputs of the independently executed
official and FastVideo implementations.

Recipe: 480x848, 81 frames, 16 FPS, 40 steps, seed 42, guidance scale 4,
empty negative prompt, Torch SDPA. The instruction adds a snowman beside the
snowy trail while preserving the dog, its motion, and the scene.

Mean MP4 MS-SSIM against the official output: 0.9878277940514647.

| File | SHA-256 |
| --- | --- |
| official.mp4 | 0e611e65752e2586f6c28aeed4dd348b40968683b9dff7a013ec8171fb487939 |
| fastvideo.mp4 | 9c1c7d5c0f3505faea90b86f151d7473457da43348139001180077b73d3e6252 |
