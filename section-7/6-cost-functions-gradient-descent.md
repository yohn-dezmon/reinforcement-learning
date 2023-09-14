# Cost Functions and Gradient Descent

y_hat == model output.  
After the network creates a prediction, how do we evaluate it?  
- compare the outputs of the network to the real values of the label.  
- this happens during training of the learning process. 


Cost function:
- loss function, error function
- it should be an average, so it can output a single value
- you want the cost function value to go down throughout training 

`a`: holds a lot of info about (activation function, weights, biases, input value).  
`a` is the result of putting `z` into an activation function, where `z` is  
equal to `w*x + b`.


Quadratic Cost Function:
- basically RMSE 
- however can be used for multidimensional data  

`L` == last layer.


`C(W, B, S^r, E^r)`: cost function. 

Cost functions often become complex with big neural networks, as they contain huge vectors of weights and biases.  

So how do we calculate the cost function and figure out how to minimize it?  

`C(w1, w2, w3, ..., wn)`  
How do we figure out which weights lead us to the lowest cost?  
- i.e. for each weight, how do I change it such that it will minimize the cost function at the very end?  
- for simplicity imagine we have a network with a single neuron
- we want to minimize the error by setting `w` to a particular value
- we want to minimize `C(w)`
- sometimes you can just take the derivative and solve for 0
- our cost function will be `n-dimensional` :D 
- where the number of dimensions is determined by how many neurons there are.  
- 


Gradient Descent:  
gradient: vector of partial derivatives.  
In gradient descent, you're trying to minimize the gradient of a cost function.  
Each parameter has a partial derivative within the vector.  
The gardient points in teh direction of the steepest increase of the function.  
You iteratively move in the opposite direction of the function.  

Simple Version of Gradient Descent:
- `C(w)` 
- choose random point
- calucluate the slope of that point
- move in downward direction of the slope 
- converge to 0, this is a minimum. 
- we took equal step sizes
- if you take smaller step sizes, it takes longer to reach the minimum
- if you take larger step sizes, you may overshoot the minimum
- 

**adaptive gradient descent**: start with larger steps and get smaller as the slope gets closer to 0.  

"Adam: A Method for Stochastic Optimization": Adam is a much more efficient way for searching for minimums.  


Stochastic Gradient Descent:
- computes the gradient usin randomly selected subset (mini-batch) of the data. 
- introduces randomness to the optimization process, which can lead to faster convergence and better generalization


For an N-dimensional vector (`tensor`) we denote the cost function as a gradient.

For classification problems, we end up using the **cross entropy** loss function.  
- it assumes that your model predicts a probability distribution `p(y=i)` for each class `i=1, 2, ..., C`


