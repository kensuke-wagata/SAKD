# Distill Only What is Reliable: Stability-based Adaptive Knowledge Distillation

This repository is an official PyTorch implementation of "[Distill Only What is Reliable: Stability-based Adaptive Knowledge Distillation]()" published in IJCNN2026. SAKD, an adaptive knowledge distillation method, which modulates distillation strength based on instance instability.

## Version

- Python 3.10.12
- Pytorch 2.91
- CUDA 12.1.1

## Training

Here is an example of how to train the student model, given a teacher-student network pair.
```
python train_cifar_student_sakd.py --path_t ./save/models/resnet32x4_vanilla/ckpt_epoch_240.pth --model_t resnet32x4 --model_s resnet8x4
```
where
- `--path_t`: specify the path of the pre-trained teacher model.
- `--model_t`: name of the pre-trained teacher model. Configurations of all teacher-student network pairs can be found in train_cifar_student.py and train_imagenet_student.py.
- `--model_s`: name of the target student model. Configurations of all teacher-student network pairs can be found in train_cifar_student.py and train_imagenet_student.py.
- `--trial`: the comments for each teacher-student network pair.
- other parameters are referred to train_cifar_student.py and train_imagenet_student.py.


## Acknowledgement

This repository is built based on [NORM](https://github.com/OSVAI/NORM). We thank the authors for releasing their amazing codes.







