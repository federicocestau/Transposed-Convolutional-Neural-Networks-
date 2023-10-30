# Transposed-Convolutional-Neural-Networks
The goal of a Transposed Convolution is to do the opposite of a regular Convolution, i.e., to upsample the input feature map to a desired larger size output feature map.

To achieve this, Transposed Convolution goes through an iterative process of multiplying entries in the input feature map by the filter and adding them up together. Note that we also move along by the specified number of places (stride) within each step.

•	Take the first input entry and multiply it by the filter matrix. Temporarily store the result.

•	Then, take the second input entry and multiply it by the filter matrix. Temporarily store the result. Continue this process for the rest of the input matrix.

•	Finally, sum up all the partial outputs to get the final result.

For example we can move from a 2x2 input to a 3x3 output via a 2x2 filter using a stride of 1.

It is worth nothing that we are essentially generating additional data during the transposed convolution operation as we are upsampling the feature map from a smaller to a larger size.

However, this operation is not exactly the reverse of a Convolution. It is because some information is always lost during a Convolution, meaning that we can never precisely recreate the same data by applying a Transposed Convolution.

Lastly, we can experiment with a filter size or stride to achieve the desired size of an output feature map. E.g., we could increase the stride from 1 to 2 to avoid section overlaps and produce larger outputs images.

Transposed Convolutions are crucial for Semantic Segmentation and data generation in the Generative Adversarial Networks (GANs). One of the more straightforward examples would be a Neural Network trained to increase image resolution. 

