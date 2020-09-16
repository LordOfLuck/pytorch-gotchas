# pytorch-gotchas

1. CUDA OOM errors:
  - If dynamic batch size is used (ege audios of different lengths), start from the largest possible batch. See [this thread](https://discuss.pytorch.org/t/how-to-debug-causes-of-gpu-memory-leaks/6741/11?u=jan_vainer).

2. Speeding up:
  - If your input shapes remain the same during training, try setting [torch.backends.cuddn.benchmark = True](https://discuss.pytorch.org/t/what-does-torch-backends-cudnn-benchmark-do/5936/2) - it finds the best algorithm for your hardware to use
