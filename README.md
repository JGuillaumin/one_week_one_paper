
# One Week, One Paper

Every week I will try to quickly implement a recent paper or make a review of a Deep Learning technique. 


### Week 46: Drop Activation 

- [DropActivation: Implicit Parameter Reduction and Harmonic Regularization](https://arxiv.org/abs/1811.05850), Submitted on 14 Nov 2018
- random non linear activation layer which improves generalization a DNNs
- implementation for Keras and TensorFlow 
- also contains implementation of [Randomized-ReLU]((https://arxiv.org/abs/1505.00853))
- from 92.47 to 93.36 (accuracy) with this new activation layer (ResNet56-v2, CIFAR10)