# DeepDream  
### The generagted images are not the real images for the past task.
1. Generator: use noise to generate image by use loss of L2 and loss of variance（先验约束，使图像看起来更像我们见过的，而不仅是让分类置信度高的我们看不懂的图产生，愚惑网络）.
2. the fine-trained model, give the noise images to the fine-trained model, and extract the feature map of certain layer. update noise image by loss, NOT MODEL PARAMETERS.
3. Distillation: use the generated image to distillation, but the differences between distributions of the generated images and real images is obvious. This decrease the effect of distillation.
4. Loss make the results: If the fine-trained model was trained mostly on images of animals, the noise image will turn into remix of learned feature of various animals. For the lower layer, just the pattern. For higher-level layers, complex features or even whole objects.
5. If input noise images, ouput the pure trained images. If input an natural image, then main color almost the same with natural image, but the content changed.
# DeepInversion
### Improve the quality of the generated images by adding new regularization
1. add the L2 loss of mean and variance in all BN layer 
# Adaptive  DeepInversion
### The above methods guarentee the distribution, but not the diversity.
# Data-Free Class-Incremental Learning (DFCIL)


# Global covariance pooling, substitude the mean or max pooling
compute covariance among channel-features.


# MTN
1. why soft attention
2. the number of task and attention block, the problem of memory

# the convolution
Note: the size of input feature map is B*C*W*H; the size of output feature map is B*P*W*H.

A convolution layer has P filters, each filter has 1 kernel whose size is C\*kernel_size*kernal_size. Set the certain channel-value to zero of output feature, the corresponding filter can not be updated.
1. If the image is 3 channels, the filter is 3-dimensionality, but output one channel feature map.
2.  Attention and reinforce-learning can be used to choose the desire part of layers.