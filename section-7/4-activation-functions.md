# Activation Functions  

inputs x, have a weight w, and a bias term b, attached to them in the perceptron model.  
* `x*w + b`

w: the strength that we give to a given input.  
b: offset value. i.e. `x*w` has to reach a certain threshold before having an effect.  

^ because you can set the value of b to be negative!  
If you set b to be -10, then the effects of `x*w` won't overcome the bias until their product surpasses 10.  
After that, the effect is solely based on the value of w.  

We want to set boundary values for the overall output value of:
```
x*w + b
```

We can state:
```
z = x*w + b
```

Then pass z through some **activation function** to limit its value.  

For binary classification, we want an *output* of either 0 or 1.  
activation function = `f(z)`  
If you see `f(Z)` or `X` -- these denote tensor input consisting of multiple values.  

step function:
- always outputs 0 or 1 

sigmoid (logistic) function:
- also has upper and lower bound of 1 and 0
- but gradually increase from 0 to 1 as opposed to step function which immediately switches from 0 to 1 at a given threshold. 
- more sensitive to small changes
- you can use the sigmoid value as a probability of where the point will land  

Hyperbolic Tangent:
- `tanh(z)`
- lower bound is -1, upper bound is 1

Rectified Linear Unit (ReLU):
- a relatively simple function 
- `max(0, z)`
- good performance when dealing with **vanishing gradient**

Wikipedia page for activation functions is a good resource.  

