### Chapter 1 questionnaire

1: Do you need these for deep learning?

- Lots of Math T/**F**
- Lots of data T/**F**
- Lots of expensive computers T/**F**
- A PhD T/**F**

2: Name five areas where deep learning is now the best in the world.

- Natural language processing
- Recommendation systems
- Image generation
- Computer Vision
- Medicing

3: What was the name of the first device that was based on the principle of the artificial neuron?

The Mark I Perceptron.

4: Based on the book of the same name, what are the requirements for parallel distributed processing (PDP)?

- A set of processing units
- A state of activation
- An output function for each unit
- A pattern of connectivity among units
- A propagation rule for propagating patterns of activities through the network of connectivities
- An activation rule for combining the inputs impinging on a unit with the current state of that unit to produce an output for the unit
- A learning rule whereby patterns of connectivity are modified by experience
- An environment within which the system must operate

5: What were the two theoretical misunderstandings that held back the field of neural networks?

	1: that despite a single layer of neurons being unable to learn simple critical mathematical functions, multiple layers of neural networks would address those concerns.

	2: In theory, just adding a single layer would approx any mathematical function, but in practice they were too big and slow to be practical.

6: What is a GPU?

	A graphical processing unit, or graphics card. They're really good at handling multiple tasks at a single time.

7: Open a notebook and execute a cell containing: 1+1. What happens?

	Below the cell you receive an output of 2.

8: Follow through each cell of the stripped version of the notebook for this chapter. Before executing each cell, guess what will happen.

9: Complete the Jupyter notebook online appendix.

10: Why is it hard to use a traditional computer program to recognize images in a photo?
	
	- The exact steps required to recognize an object in a picture aren't totally clear.
	- You would somehow need to spell out every single detail to an extreme level of minutiae to manage to create a program that could do so.

11: What did Samuel mean by "weight assignment"?

	The value of a given variable.

12: What term do we normally use in deep learning for what Samuel called "weights"?

	Model Parameters

13: Draw a picture that summarizes Samuel's view of a machine learning model.

14: Why is it hard to understand why a deep learning model makes a particular prediction?

	At least until recently, it was hard to see what the model was doing. It was treated as a black box that just did a random task assigned to it.

15: What is the name of the theorem that shows that a neural network can solve any mathematical problem to any level of accuracy?

	The Universal approximation theorem.

16: What do you need in order to train a model?

	data(inputs)

17: How could a feedback loop impact the rollout of a predictive policing model?

	If for instance you have initially biased data, and then you follow through with an action based on that data, and then use data generated from that action to feed into the model. You can heavily bias your model via your real-world actions.

18: Do we always have to use 224x224 pixel-images with the cat recognition model?

	No. It's just a standard. Increasing the size comes with a potential increase in results at the cost of speed and memory, and vice-versal.

19: What is the difference between classification and regression?

	Classification is for discrete classes, regression is for more continuous data.

20: What is a validation set? What is a test set? Why do we need them?

	A test set is a chunk of your data sectioned off to avoid overfitting. It is used to test the validity of your model.

	A validation set is essentially a "super" test set, where it's data you have set aside to avoid any kind of overfitting with regards to the test set. The validation set is closer to the "real world" than the test set should be and is used as the ultimate measure of the validity of a model.

21: What will fastai do if you don't provide a validation set?

	fastai defaults valid_pct to 0.2. It takes care of it for you.

22: Can we always use a random sample for a validation set? Why or why not?

	You can, but probably shouldn't. If you keep randomizing it you don't know whether your improvement was due to the changes in the model or due to having a different random validation set.

23: What is overfitting? Provide an example.

	When your model too closely matches the data and can no longer generalize. If for example I have a model that is trained on the entirety of my data, then it'll only ever work on my data, and won't work on similar but different data.

24: What is a metric? How does it differ from "loss"?

	A metric is a function that measures the quality of the model's predictions using the validation set.
	The metric is printed at the end of each epoch.

25: How can pretrained models help?

	Pretrained models are already capable. It can save you time and effort in training something you do not need to. Further, pretrained models are already good at detecting shapes, edges, etc.

26: What is the "head" of a model?

	The part that is newly added to be specific to the new dataset.

27: What kinds of features do the early layers of a CNN find? How about the later layers?

	Early layers tend to find shapes and colors.
	Later layers tend to find more fine-grained details.

28: Are image models only useful for photos?

	Not necessarily. They work well for pretty much anything that can be recorded and turned into an image.

29: What is an "architecture"?

	The functional form of the model.

30: What is segmentation?

	Creating a model that can recognize the content of every individual pixel.

31: What is `y_range` used for? When do we need it?

	It refers to a continuous range of values that the dependent variable is allowed to have. It is useful for when you are doing a regression problem.

32: What are "hyperparameters"?

	Modeling choices ranging from network architecture, augmentation strategies, etc. Parameters about parameters. They're higher level choices that govern the meaning of weight parameters.

33: What is the best way to avoid failures when using AI as an organization?

	Understand what test and validation sets are and why they're important.
