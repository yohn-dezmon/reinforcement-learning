# Neural Networks

A multi-layer perceptron model!  
Vertical layers of individual perceptrons.  
Take their output and feed them as input into another vertical layer of perceptrons.  

feed-forward = uni-directional (input --> output, left to right).  
fully connected: every neuron in one layer is connected to every neuron in the next layer!  

input layer: first layer.  
output layer: last layer.  
hidden layers: layers inbetween.  

The output can be more than one neuron, especially in the case of multi-class classification.  

hidden layers are difficult to interpret, due to their high connectivity and their distance away from known input and output values.  

When does a neural network become a deep neural network?
- when you contain two or more hidden layers...  

Deep neural network:
- a neural network (interconnected layers of perceptrons) with two or more hidden layers.  


network width:
- how many neurons are in the layer. 

network depth:
- how many layers there are total

The neural network framework can be used to approximate any continuous function.  
"universal approximation theorem"  

In our simple model we had a simple function within the perceptron, i.e. a summation function.  
For most usecases, we'll want to be able to set constraints to our output values, especially in classifiaction tasks.  

example constrain for classification tasks: 
- have all outputs fall between 0 and 1  
- these values can then present probability assignments for each class.  

in the next lecture we'll discuss **activation functions** to set boundaries to output values from the neuron.  



