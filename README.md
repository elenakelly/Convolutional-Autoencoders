### Autoencoder

An autoencoder (AE) is a neural network that is trained to copy its input to its output.  <br />
It has one or more hidden layers that each describe a code used to represent the input.  <br/>
The network may be viewed as consisting of two parts:an encoderh=f(x) that produces the code and a decoder that produces a reconstruction of the datar=g(h).The  encoder  is  tasked  with  finding  a  (usually)  reduced  representation  of  the  data,  extracting  the  most  prominentfeatures of the original data and representing the input in terms of these features in a way the Decoder can understand.The Decoder learns to read these codes and regenerate the data from them.  The entire AE aims to minimize a loss-function  while  reconstructing.  

In  their  simplest  form  encoder  and  decoder  are  fully-connected  feedforward  neuralnetworks.  When the inputs are images, it makes sense to use convolutional neural networks (CNNs) instead, obtaininga convolutional autoencoder (CAE).

A  CAE  uses  the  convolutional  filters  to  extract  features.   CAEs  learn  to  encode  the  input  as  a  combination  ofautonomously learned signals and then to reconstruct the input from this encoding.  CAEs learn in what can be seenas  an  unsupervised  learning  setup,  since  they  don’t  require  labels  and  instead  aim  to  reconstruct  the  input.   Theoutput is evaluated by comparing the reconstructed image by the original one, using a Mean Squared Error (MSE)cost function.

We will be using the CIFAR-10 dataset:
•CIFAR-10 dataset (https://www.cs.toronto.edu/ ̃kriz/cifar.html).

## Architecture
And the architect we are using is:

<img width="1048" alt="download" src="https://user-images.githubusercontent.com/59971317/140607664-6a79a4e1-24a1-4eb8-9df7-206c9a111c84.png">

1. Reconstruction:<br/>
  Dividing the dataset into training (80%), validation (10%) and test (10%).  
  Normaling the data. 
  Implementing  the  autoencoder  network  specified  above.   
  Runing  the  training and  ploting the evolution of the error with epochs.  
  Reporting also the test error.

2. Colorization:<br/>
  Adapt the  network  from  the  previous  part  such  that  it  learns  to  reconstruct  colors  by  feeding  in  grayscaleimages but predicting all RGB channels.  
  As a starting point, use the hyperparameters (including the networkarchitecture) that you identified to yield the best performance.  
  Report  the results  and  reason  about  potential  shortcomings  of  the  network. 

  ## Installation
The program is in Jupyter Notebook <br />
In order to use the code you need to install the following packages
1. Typical libraries
   ```sh
    import numpy as np
    import matplotlib.pyplot as plt
    import tensorflow
   ```
2. For the dataset 
```sh
    from keras.datasets import cifar10
   ```
3. For the neural network
   ```sh
    from keras.utils import np_utils #for the encoding to transform the labels in categorical
    from keras.layers import Input, Dense, Conv2D, MaxPooling2D, Dropout, Flatten, UpSampling2D #import the layers  
    from keras.models import Sequential #import the model
    from tensorflow.keras import optimizers #import the optimizer
    from keras.preprocessing import image #for visualisation of the image data
    from keras import backend as K #for cleaning the memory
    from keras.callbacks import Callback #import the callback
   ```
   


