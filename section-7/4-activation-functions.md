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

