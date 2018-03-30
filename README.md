## Fast Style Transfer in Pytorch
An implemenation of Johnson, Alahi and Fei-Fei's [fast style transfer algorithm](https://arxiv.org/abs/1603.08155).

My implementation was heavily inspired by by Fastai's [Deep Learning Course](http://course.fast.ai/), and I trained my models on a portion of ImageNet. 

You can check out the code in train.ipynb. The important classes are:
- FeatureExtractor: a wrapper for vgg-16 that extracts the activations of intermediate layers. This is our 'loss network' referred to in the paper above.
- FastTransNet: The residual convolutional network that is trained to minimize the weighted sum of the feature reconstruction loss and the style reconstruction loss
- WrapperModel: a wrapper for the classes above

Here's an example of the images I produced:

#### Original Image:
![Ravenel Bridge](https://raw.githubusercontent.com/ryankresse/fast_style_transfer_pytorch/master/data/bridge.jpg)


#### Style Image:
![The Peanuts](https://raw.githubusercontent.com/ryankresse/fast_style_transfer_pytorch/master/data/charlie_brown.jpg)


#### Transformed Image:
![Transformed Ravenel Bridge](https://raw.githubusercontent.com/ryankresse/fast_style_transfer_pytorch/master/output_img/bridge_peanuts.jpg)

