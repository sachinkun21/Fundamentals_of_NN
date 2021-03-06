## Introduction to Perceptron
In this segment, you will study a simple device called the perceptron which was the first step towards creating the large neural networks we have today. Let's take a quick example to understand how a perceptron works.

 

Consider a sushi place you plan to visit on the coming Saturday. There are various factors that would affect this decision, such as:

1. How far is it?
2. How costly is it?
3. How many people are accompanying you?

You take a decision based on multiple such factors. Also, each decision factor has a different ‘weight’ - for example, the distance of the place might be more important than the number of people. 

Perceptrons work in a similar way. They take some signals as inputs and perform a set of simple calculations to arrive at a decision. 
Let’s study perceptrons in some detail.
the perceptron takes a weighted sum of multiple inputs (along with a bias) as the cumulative input and applies a step function on the cumulative input, i.e. it returns 1 if the input is positive, else -1. In other words, the perceptron “fires” (returns 1) if the cumulative input is positive and "stays dormant" (returns 0) if the input is negative.

Note that there are different ways to define the step function. The professor has considered a step function defined in the following way, though one can rather use 1 and -1 as well instead of 1 and 0:

                              `y=1 if x>0`
                              `y=0 if x<=0`
                  
The input to a perceptron is the sum of weights multiplied with their respective inputs and the bias:                  
          
                      `Cumulative Input = w1x1+w2x2+....+wkxk+b`
                      
                   
Shortly, we will be talking about everything in terms of vectors and matrices, so let's start using the vector algebra lingo. Say w and x are vectors representing the weights and inputs as follows (note that, by default, a vector is assumed to be a column vector):

![Test Image 2](https://github.com/sachinkun21/Fundamentals_of_NN-/blob/master/Screenshot%202019-12-09%20at%203.48.20%20PM.png)

A neat and concise way to represent the weighted sum of w  and  x is using the dot product of wT and  x . The transpose of w is wT = [w1w2..wk] - a row vector of size 1 x k. Taking the dot product of wT with x:

![Test Image 3](https://github.com/sachinkun21/Fundamentals_of_NN-/blob/master/Screenshot%202019-12-09%20at%203.56.50%20PM.png)


Upon adding bias to wT.x, we have wT.x  + b = w1x1+w2x2+....+wkxk+b. Hence,

`Cumulative Input = w T . x + b = w 1 x 1 + w 2 x 2 + . . . . + w k x k + b`
 

Upon applying the step function, if this cumulative sum of input is > 0, the output is 1/yes else 0/no.



This is a simple exercise that will help you better understand how a perceptron works. 

 

Consider the decision of whether to go to the sushi place being taken by a perceptron model. You have the following factors affecting the decision to go/not go: Distance, Cost and Company. These three variables are inputs to the perceptron. Suppose the inputs can be only 0/1 and the weights you assign to each variable add up to 1.


For each of the inputs, the rules for deciding 1 and 0 are as follows - these are arbitrary mappings that you have decided to make your model simpler:
TABLE

Assume that the bias value is -0.7. The sushi place is 5 km away and 3 of your friends are ready to accompany you. Also, the cost for 2 is INR 2500.
