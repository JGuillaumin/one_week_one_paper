
# Week 46: DropActivation: Implicit Parameter Reduction and Harmonic Regularization


[Original paper](https://arxiv.org/abs/1811.05850), Submitted on 14 Nov 2018


.... 

## Implemented features

I don't use `keras` python package, I use `tensorflow.keras` ! 
(I did not use Keras for 2 years ... it's so misleading to have Keras within TensorFlow). 
So If you use raw python package `keras`, please be sure that the version of `keras` is the same the version of Keras
in `tensorflow`. Today (Nov 2018), if you `pip install keras` it will be `keras==2.2.0` while the Keras branch in TensorFlow
is `keras==2.1.6` ..

So, in the future, I will write the layer with `keras` instead of `tensorflow.keras`.

**Implemented features:**

- `DropActivation` layer
- `RandomizedReLU` layer ([]())
- ResNet-56 on CIFAR-10 with Keras (TF backend), with MomentumSGD (0.9)
- data augmentation: random crop, horizontal flips and per sample standardization
- 3 notebooks (same code, just different networks) with seeded initialization (same initial random weights)


## Drop Activation 


## Randomized ReLU (RReLU)



## Comparision: ReLUxDropout, Drop Activation and Randomized ReLU



## Results (from my code)

Model & training configuration:
- ResNet56 for CIFAR10 (no bottleneck block)
- L2 regularization only on kernels (conv and final dense layer) with weight `0.0002`
- optimization with SGD and Momentum (`0.9`)
- learning rate scheduling : 0.1, 0.01, 0.001 and 0.0001 (changes at epochs 91, 136 and 182)
- `batch_size=128` and `epochs=200`
- Data augmentation (only train, no test time augmentation): sample wise normalization (mean and std), 
    random crop (5 pixels), random horizontal flips (no vertical)
- training set vs validation : 80/20 % of initial training set (shuffle and stratified split)
- test set from CIFAR-10 as final test set !
