SegFormer for Semantic Segmentation 🐾

This repository demonstrates how to train SegFormer — NVIDIA’s state-of-the-art Transformer-based segmentation model — on the Oxford-IIIT Pet dataset.
The task is binary semantic segmentation:

Pet = foreground (class 1)

Background = class 0

Thin boundary pixels are ignored during training (label = 255)

SegFormer provides excellent performance with efficient computation — and this training pipeline can be easily adapted to any custom segmentation dataset.

Features included:
- MiT-B0 SegFormer backbone (pretrained encoder, fresh 2-class head)
- Custom dataset wrapper for images + masks (trimaps → labels)
- mIoU and pixel accuracy metric reporting
-  Mixed-precision (AMP) training support for faster GPU training
-  Easy to modify for multi-class segmentation

Requirements
- PyTorch 2.x
- Transformers
- CUDA GPU recommended for training

📌 Dataset

In this example, we use the Oxford-IIIT Pet dataset
(download handled automatically in the notebook / script).

You can replace the dataset load function with your own images + masks
to train SegFormer on any segmentation task.
