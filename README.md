# pytorch-gotchas

1. CUDA OOM errors:
  - If dynamic batch size is used (ege audios of different lengths), start from the largest possible batch. See [this thread](https://discuss.pytorch.org/t/how-to-debug-causes-of-gpu-memory-leaks/6741/11?u=jan_vainer).
