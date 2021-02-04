# Binary_conv_CNN_models
Some CNN models where weights in the convolution layers are {-1,1} while weights in the output layers are fixed point integers (for finite number of bits) 

Inlcudes a model for MNIST giving an accuracy of 99.28% 

The convolutional layers used in Keras are defined as: 

example for 2'nd layer: 
(filtre1, filtre2, filtre3) are the numbers of filters per each of (1,2,3) conv. layers 
csize=3 in all cases  (here csize2)
psize=4 in all cases  (here psize2)
str=2 in all cases    (here str2) 

model.add(DepthwiseConv2D(kernel_size=csize2, padding=pad, depth_multiplier=filtre2, use_bias=False))
model.add(MaxPooling2D(pool_size=(psize2, psize2),strides=(str2,str2),padding=pad))

The model was first described in the following paper 
R. Dogaru and I. Dogaru, "BCONV - ELM: Binary Weights Convolutional Neural Network Simulator based on Keras/Tensorflow, for Low Complexity Implementations," 2019 6th International Symposium on Electrical and Electronics Engineering (ISEEE), Galati, Romania, 2019, pp. 1-6, doi: 10.1109/ISEEE48094.2019.9136102.

https://ieeexplore-ieee-org.am.e-nformation.ro/document/9136102
