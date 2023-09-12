# Multi-class Activation Functions


Two types of multi-class situations:
1. non-exclusive classes: a data point can have multiple classes/categories assigned to it
2. mutually exclusive classes: only one class per data point

(2) is more common.  

Example of (1): a photo can have multiple tags.  
Example of (2): a photo is in grayscale or full color 

How to organize multiple classes?
- have one output node per class 

I think we want to be able to do algebra on the output classes.  
Therefore we can use **one hot encoding**.  

i.e. you have a matrix, with one column per output value.  
The rows are data points.  
You set 1 for when the data point falls into that category.  

You can also use one hot encoding for non-exclusive classes, however you can have 1 for multiple categories!  

Now that we have our data correctly organized, we just need to choose the correct classification activation function that the last output layer should have.  

For organizing non-exclusive classes:
- you can use the sigmoid function 
- each neuron will output a value between 0 and 1  
- this output indicates the probability of having that class assigned to it!  
- you have an output neuron assigned to each class 
- each neuron ends up with a value between 0 and 1  


For organizing mutually exclusive classes:
- use a **softmax function** (activation)
- note: go back and write down the formula 
- i = 1 ... k 
- softmax function calculates the probabilities distribution of the event over K different events 
- this function will calculate the probabilities of each target class over possible target classes.  
- range is 0 to 1 
- the sum of all probabilities is equal to one! 
- the model returns the probabilities of each class and the target class chosen will have the highest probability... 
- [Red, Green, Blue]
- [0.1, 0.6, 0.3]
- so for this case, we choose green as the classification.



