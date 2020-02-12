# Learning to See in the Dark

In this repository, we reimplement the algorithm in paper "Learning to See in the Dark" in PyTorch. The code is in parallel to the original Tensorflow implementation provided by the authors.

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

The pretrained model has been released in [here](https://drive.google.com/file/d/1Vjop6FnQ79ngJQORHqUUDZtiYXxDicRR/view?usp=sharing). The default training epochs reported in the paper is 2000. This would take more than 5 days on a single Tesla P100 GPU. Given limited GPU resources at hand, the released pretrained model in this repo is trained for 100 epochs only.

### Todo list
1. Pubish our pruned model. More specifically, the pruned model will be funetuned for only 100 epochs as well.
2. Release our pruning code, so that all results can be reproduced by this repo.
