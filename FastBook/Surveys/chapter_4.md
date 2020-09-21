1. How is a grayscale image represented on a computer? How about a color image?

	As a multi-dimensional array of numbers. For color it's slightly different where each cell has a respective red green and blue value, each ranging from 0 to 255.

1. How are the files and folders in the MNIST_SAMPLE dataset structured? Why?

	It has separate folders for the training set and validation set. Further, it has individual folders for each label.

1. Explain how the "pixel similarity" approach to classifying digits works.

	Average every pixel of each image. This should give us the "ideal" version of the number.
	We can then take that "ideal" version of the number, and compare it to our data. It should be possible to obtain a decent accuracy for our "ideal" number compared to our sample.

1. What is a list comprehension? Create one now that selects odd numbers from a list and doubles them.

	A list comprehension is just a convenient syntax for handling list operations. It effectively combines functional programming items such as `map` and `filter` into one simple syntax.

	`odd_double = [x * 2 for x in arr if x % 2 == 1]`

1. What is a "Rank-3 tensor"?

	A 3-dimensional tensor

1. What is the difference between tensor rank and shape? How do you get the rank from the shape?

	The rank is the number of dimensions. The shape is the respective value for each of those dimensions.

1. What is RMSE and L1 norm?

	L1 norm is the absolute value of the differences between one sample and the mean.

	Root mean square error (RMSE) is the square root of the mean of the square of differences.

1. How can you apply a calculation on thousands of numbers at once, many thousands of times faster than a Python loop?

	By utilizing numpy arrays and/or pytorch tensors. They (generally) compile to C.

1. Create a 3x3 tensor or array containing the numbers from 1 to 9. Double it. Select the bottom-right four numbers.

	```
		tens = tensor([[1,2,3], [4, 5, 6], [7, 8, 9]])
		tens2 = tens * 2
		tens2[1:, 1:]
	```

1. What is broadcasting?

	Where when given two tensors of different ranks, it automatically expands the tensor with the smaller rank to have the same size as the one with the larger rank.

1. Are metrics generally calculated using the training set, or the validation set? Why?

	

1. What is SGD?
1. Why does SGD use mini-batches?
1. What are the seven steps in SGD for machine learning?

	- Initialize the weights.
	- Use those weights to predict the value.
	- Based on those predictions, calculate the loss.
	- Calculate the gradient and see how much it would change the loss.
	- Step.
	- Go repeat the process of prediction and recalculating the gradient.
	- Iterate until the model is good enough, or you stop.

1. How do we initialize the weights in a model?

	We initialize all of the weights to random values. It turns out that because the model is continually being modified, it works out well regardless.

1. What is "loss"?

	How good the model is. Or how effective the current weight assignment is in terms of performance.

1. Why can't we always use a high learning rate?

	A high learning rate can lead to loss getting worse instead of getting better.

1. What is a "gradient"?
1. Do you need to know how to calculate gradients yourself?

	No. Couldn't hurt though.

1. Why can't we use accuracy as a loss function?

	

1. Draw the sigmoid function. What is special about its shape?
1. What is the difference between a loss function and a metric?
1. What is the function to calculate new weights using a learning rate?
1. What does the `DataLoader` class do?
1. Write pseudocode showing the basic steps taken in each epoch for SGD.
Create a function that, if passed two arguments `[1, 2, 3, 4]` and `abcd`, returns [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd')]. What is special about that output data structure?
1. What does `view` do in PyTorch?
1. What are the "bias" parameters in a neural network? Why do we need them?
1. What does the `@` operator do in Python?
1. What does the `backward` method do?
1. Why do we have to zero the gradients?
1. What information do we have to pass to `Learner`?
1. Show Python or pseudocode for the basic steps of a training loop.
1. What is "ReLU"? Draw a plot of it for values from -2 to +2.
1. What is an "activation function"?
1. What's the difference between F.relu and nn.ReLU?
1. The universal approximation theorem shows that any function can be approximated as closely as needed using just one nonlinearity. So why do we normally use more?
