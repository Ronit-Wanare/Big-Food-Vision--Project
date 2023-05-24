# Big-Food-Vision--Project

Building Food Vision Big™, using all of the data from the Food101 dataset.
All 75,750 training images and 25,250 testing images.
## The goal of beating DeepFood, a 2016 paper which used a Convolutional Neural Network trained for 2-3 days to achieve 77.4% top-1 accuracy.
Note: Top-1 accuracy means "accuracy for the top softmax activation value output by the model" (because softmax ouputs a value for every class, but top-1 means only the highest one is evaluated). Top-5 accuracy means "accuracy for the top 5 softmax activation values output by the model", in other words, did the true label appear in the top 5 activation values? Top-5 accuracy scores are usually noticeably higher than top-1.

### Things that are covered
* Using TensorFlow Datasets to download and explore data.
* Creating preprocessing function for our data.
* Batching & preparing datasets for modelling (**making our datasets run fast**).
* Creating modelling callbacks.
* Setting up **mixed precision training**
* Building a feature extraction model.
* Fine-tuning the feature extraction model.

Alongside attempting to beat the DeepFood paper, we're going to learn about two methods to significantly improve the speed of our model training:
### 1. Prefetching
![image](https://github.com/Ronit-Wanare/Big-Food-Vision--Project/assets/85942512/d8ab068a-a12b-4007-a613-fc8bc309d386)
### 2. Mixed precision training
![image](https://github.com/Ronit-Wanare/Big-Food-Vision--Project/assets/85942512/f6c90f74-2404-4a51-9d5f-3b30018793c4)

## Following Typical order for using transfer learning is:

1. Build a feature extraction model (replace the top few layers of a pretrained model) 
2. Train for a few epochs with lower layers frozen
3. Fine-tune if necessary with multiple layers unfrozen

![image](https://github.com/Ronit-Wanare/Big-Food-Vision--Project/assets/85942512/160cdce0-fef1-4948-812c-bef60d81f0ad)
