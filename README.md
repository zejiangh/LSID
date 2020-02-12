# Learning to See in the Dark

In this repository, we reimplement the algorithm in paper "Learning to See in the Dark". The code is in parallel to the original Tensorflow implementation provided by the authors.

### Requirements
1. Platform: PyTorch-0.4.1, Scipy, Numpy, Rawpy
2. Tested in Tesla P100 GPU with Cuda (>=8.0) and CuDNN (>=5.0).

### Training
```Shell
python train_Sony.py --gpu 0 --num_epoch 100
```

### Predicting
```Shell
test_Sony.py --model ./result_sony/model_99.pl --gpu 0
```

### Evaluating PSNR and SSIM
```Shell
python metrics.py --imgdir ./result_Sony/eval
```

The pretrained model has been released in './baseline'

### Todo list

