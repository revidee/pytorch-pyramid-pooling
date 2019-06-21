# Pyramid Pooling implemented in PyTorch
This Module implements Spatial Pyramid Pooling (SPP) and Temporal Pyramid Pooling (TPP) as described in different papers.


![SPP-TPP Comparison](https://github.com/revidee/pytorch-pyramid-pooling/blob/master/comparison-spp-tpp.png "SPP-TPP Comparison")


Temporal Pyramid Pooling:
------
[Sudholt, Fink: Evaluating Word String Embeddings and LossFunctions for CNN-based Word Spotting](http://patrec.cs.tu-dortmund.de/pubs/papers/Sudholt2017-EWS.pdf "Sudholt, Fink: Evaluating Word String Embeddings and LossFunctions for CNN-based Word Spotting")

### Principle
Given an 2D input Tensor, Temporal Pyramid Pooling divides the input in **x** _stripes_ which **extend through the height** of the image and **width of roughly (input_width / x)**. These stripes are then each pooled with max- or avg-pooling to calculate the output.

### Animated Principle
![TPP Visualization](https://github.com/revidee/pytorch-pyramid-pooling/blob/master/pytorch-tpp-visual.gif "TPP Visualization")

Spatial Pyramid Pooling:
------
[He, et. al.: Spatial Pyramid Pooling in Deep Convolutional Networks for Visual Recognition](https://arxiv.org/abs/1406.4729 "He et. al.: Spatial Pyramid Pooling in Deep Convolutional Networks for Visual Recognition")

### Principle
Given an 2D input Tensor, Spatial Pyramid Pooling divides the input in **x²** _rectangles_ with **height of roughly (input_height / x)** and **width of roughly (input_width / x)**. These rectangles are then each pooled with max- or avg-pooling to calculate the output.

