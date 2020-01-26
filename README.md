# MFL-Educlub
This repository contains all the required resources for workshops at MFL educlub

#### How does an computer understand an image
![](https://cdn-images-1.medium.com/max/1600/1*ccVO7341XIh7GfvzQS1IGw.png)

### The Big picture : a convolutions network
[Link to video](https://youtu.be/Oqm9vsf_hvU?t=266)

#### This is a 1 convolution layer
![](https://github.com/vdumoulin/conv_arithmetic/raw/master/gif/no_padding_no_strides.gif)

#### Filter/Kernel in action
[Image Kernels explained visually](http://setosa.io/ev/image-kernels/)
##### NOTE : weights in the filter are the result of training.

<br />

##### Convolution network = a stack of convolutions layers
And if this set is big one, it's **Deep Convolution networks**, the deep learning part counterpart of convolution network. Eg: RESNET.

#### Excelsheet example of convolutions
[Link to excel sheet](https://docs.google.com/spreadsheets/d/1rXJ_tmMAePh07nBdMBc18kfaANP02vL0E9ii-kSRsnA/)


## Convloutions in-depth: We'll look at a single convolution in action. Combinations of various of these convolutions results in various architectures.

> ### Convolutions in-detail: 
- #### Input : how do we take it?
  - What does resnet take as input
- #### strides & Padding
  - ##### Strides concept : 
    ![](https://github.com/vdumoulin/conv_arithmetic/raw/master/gif/no_padding_strides.gif)
  - ##### Padding concept:
    ![](https://github.com/vdumoulin/conv_arithmetic/raw/master/gif/same_padding_no_strides.gif)
    - Why:
      - Without padding, reduction in size would converge the network quickly and network might not get deep enough.
      - doesnt discard information at the borders
- #### Channels
  - What are channels
    ![](http://xrds.acm.org/blog/wp-content/uploads/2016/06/Figure1.png)
  - example RGB, medical, satellite, etc
- #### Kernel/filter 
  ![](https://i.stack.imgur.com/9Iu89.gif)
  - DIFF b/w parameters and hyper-parameters
- #### Feature maps : 
  - what
  - how to calculate the no. of feature maps produced : no. of filters
  - Dimension of produced feature maps ; (N+2P-F)/S + 1 
- #### No. of filters/kernels 
  - dimensions we consider of the filter.
- #### Activations : sigmoid, tanh, relu, leaky relu, elu 
![](https://cdn-images-1.medium.com/max/1600/1*DRKBmIlr7JowhSbqL6wngg.png)
  - what
  - why
  - their adv and disadv and 
  - when to use what.
- #### Pooling layers : Maxpool, avgpool, minpool
![](http://cs231n.github.io/assets/cnn/maxpool.jpeg)
  - what
  - why
  - adv and disadv
  - when to use what : In classifying cats vs. dogs, averaging over the image tells us "how doggy or catty is this image overall." Since a large part of these images are all dogs and cats, this would make sense. If you were using max pooling, you are simply finding "the most doggy or catty" part of the image, which probably isn't as useful. However, this may be useful in something like the fisheries competition, where the fish occupy only a small part of the picture.

> ### 1x1 Conv:
![](https://raw.githubusercontent.com/iamaaditya/iamaaditya.github.io/master/images/conv_arithmetic/full_padding_no_strides_transposed_small.gif)

> ### Combining CNNs and FCNNs to do what we do : example of a deep CNN:
![](https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/4e2c0880b1c224d3bd88f52805f620c4c3dc882c/3-Figure1-1.png)
