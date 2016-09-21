# Metal Image Recognition: Performing Image Recognition with Inception_v3 Network using Metal Performance Shaders Convolutional Neural Network routines

This sample code ports open source library, TensorFlow trained Inception_v3 network trained on ImageNet Dataset. We do inference using Metal Performance Shaders. 
We demonstrate how to encode different layers to the GPU and perform image recognition using trained parameters(weights and bias) we have fetched from,
pre-trained and saved network on TensorFlow.

The Network can be found at:
https://github.com/tensorflow/tensorflow/blob/master/tensorflow/models/image/imagenet/classify_image.py

Instructions to run this network on TensorFlow can be found at:
https://www.tensorflow.org/versions/r0.8/tutorials/image_recognition/index.html#image-recognition

The Original Network Paper is at:
http://arxiv.org/pdf/1512.00567v3.pdf

We have put network parameters in .dat files as binaries to be memory-mapped into memory when needed.

The weights for this particular network were batch normalized but for inference we may use :

w = 𝛄 / √(s + 0.001), b = ß - ( A * m )

s: variance
m: mean
𝛄: gamma
ß: beta

w: weights of a feature channel
b: bias of a feature channel 

for every feature channel separately to get the corresponding weights and bias

this comes from: 
https://arxiv.org/pdf/1502.03167v3.pdf

## Requirements

### Build

Xcode 8.0 or later; iOS 10.0 SDK or later

### Runtime

iOS 10.0 or later

### Device Feature Set
 
iOS GPU Family 2 v1
iOS GPU Family 2 v2
iOS GPU Family 3 v1

Copyright (C) 2016 Apple Inc. All rights reserved.
