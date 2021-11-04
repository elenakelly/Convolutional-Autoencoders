An autoencoder (AE) is a neural network that is trained to copy its input to its output.  
It has one or more hiddenlayershthat each describe a code used to represent the input.  
The network may be viewed as consisting of two parts:an encoderh=f(x) that produces the code and a decoder that produces a reconstruction of the datar=g(h).The  encoder  is  tasked  with  finding  a  (usually)  reduced  representation  of  the  data,  extracting  the  most  prominentfeatures of the original data and representing the input in terms of these features in a way the Decoder can understand.The Decoder learns to read these codes and regenerate the data from them.  The entire AE aims to minimize a loss-function  while  reconstructing.  
In  their  simplest  form  encoder  and  decoder  are  fully-connected  feedforward  neuralnetworks.  When the inputs are images, it makes sense to use convolutional neural networks (CNNs) instead, obtaininga convolutional autoencoder (CAE).
A  CAE  uses  the  convolutional  filters  to  extract  features.   CAEs  learn  to  encode  the  input  as  a  combination  ofautonomously learned signals and then to reconstruct the input from this encoding.  CAEs learn in what can be seenas  an  unsupervised  learning  setup,  since  they  don’t  require  labels  and  instead  aim  to  reconstruct  the  input.   Theoutput is evaluated by comparing the reconstructed image by the original one, using a Mean Squared Error (MSE)cost function.


We will be using the CIFAR-10 dataset that you can find in the link below:
•CIFAR-10 dataset (https://www.cs.toronto.edu/ ̃kriz/cifar.html).

Reconstruction:

Colorization:
