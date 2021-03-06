1. Provide an example of where the bear classification model might work poorly in production, due to structural or style differences in the training data.

	- If for example you were trying to recognize bears from uncommon positions. I.E. From behind, above, or underneath. Generally our data tends to bias towards being pretty photographically. This means that most data would be front-facing beauty shots.

1. Where do text models currently have a major deficiency?
	
	- Generating _correct_ responses is difficult for deep learning models. For example generating natural language responses with a given set of information.

1. What are possible negative societal implications of text generation models?

	- Context-appropriate responses on social media could be used at massive scale to spread disinformation.

1. In situations where a model might make mistakes, and those mistakes could be harmful, what is a good alternative to automating a process?

	- Use deep learning instead as part of a process in which the model and a human user interact closely. I.E. A deep learning model can be used to inform the human that something has occurred, and the human user can then decide what to do.

1. What kind of tabular data is deep learning particularly good at?

	Time series.

1. What's a key downside of directly using a deep learning model for recommendation systems?

	- They only tell you what a user may like, not what may be useful.
	- For example, if a user has read all books by an author the deep learning model has no way of knowing if they're already familiar with the products, or if it's just a new edition of the same book they may have already read.

1. What are the steps of the Drivetrain Approach?

	- Start by defining a clear objective.
	- Consider what actions you can take to better achieve a given objective.
	- Consider what new data you would need to complete the objective.
	- Think about building predictive models.

1. How do the steps of the Drivetrain Approach map to a recommendation system?

	- Objective is to drive additional sales by recommending items they would not have purchased otherwise.
	- The lever is the ranking of the recommendations.
	- Data must be collected to generate better recommendations.
	- Build models based on seeing or not seeing a recommendation.

1. Create an image recognition model using data you curate, and deploy it on the web.

	https://nzw2k7fa.gradient.paperspace.com/voila/render/course-v4/Assignments/Chapter_2_Model_deploy.ipynb

	<https://hub.gke.mybinder.org/user/ctiller15-fasta-_age_classifier-c9uz22jn/voila/render/Chapter_2_Model_deploy.ipynb?token=UoFTcvuJQTOMDuEwVdUleg>

1. What is `DataLoaders`?

	- Dataloaders is a class that stores whatever `DataLoader` objects you pass to it. Makes them available as train and valid.

1. What four things do we need to tell fastai to create `DataLoaders`?

	- What kinds of data we're working with.
	- How to get the list of items.
	- How to label these items.
	- How to create the validation set.

1. What does the `splitter` parameter to `DataBlock` do?

	It splits out a certain chunk of data into the validation set.

1. How do we ensure a random split always gives the same validation set?

	If you use the `seed` parameter, you can ensure the same starting point for "random" numbers each time.

1. What letters are often used to signify the independent and dependent variables?

	independent: x
	dependent: y

1. What's the difference between the crop, pad, and squish resize approaches? When might you choose one over the others?

	- Crop can lose important details. I.E. In recognizing an animal we can accidentally crop out facial features that would make it easy to identify.
	- Squishing and stretching runs the risk of making everything into unrealistic shapes.
	- Padding the images can lead to a lot of wasted space. That's just wasted computation.

1. What is data augmentation? Why is it needed?

	- Data augmentation is creating random variations such that they appear different but don't actually change the meaning. So for example if I rotate an image, warp its perspective, change the contrast, etc.

1. What is the difference between `item_tfms` and `batch_tfms`?

	`item_tfms` is to run on every individual item.
	`batch_tfms` allows us to apply augmentations to an entire batch using the GPU, saving us time.

1. What is a confusion matrix?

	The confusion matrix is a visualization for what mistakes the model is making.
	The rows of a confusion matrix represent the actual values, while the columns represent what it was predicted as. The goal is to have the offset items zeroed and only the diagonals populated.

1. What does `export` save?

	By default it saves a file called `export.pkl`, this is your model generated via training.

1. What is it called when we use a model for getting predictions, instead of training?

	Using a model for inference.

1. What are IPython widgets?

	IPython widgets are GUI components that bring together JavaScript and Python functionality in a web browser. They can be created and used within a Jupyter notebook.

1. When might you want to use CPU for deployment? When might GPU be better?

	For most projects it would be better to use a CPU. GPU's are only really useful when they need to do lots of identical work in parallel. If you have a very high-volume site then maybe it could be useful, however the complexities make it a hard sell.

1. What are the downsides of deploying your app to a server, instead of to a client (or edge) device such as a phone or PC?

	You're required to communicate to a server, necessitating a network connection. Because of this there would be a bit of latency each time the model is called. It is also harder to scale your own server than to just be dependent on users bringing their own compute resources.

1. What are three examples of problems that could occur when rolling out a bear warning system in practice?

	- Handling nighttime images.
	- Low res camera images.
	- Recognizing bears from strange positions.

1. What is "out-of-domain data"?

	Data in production that is very different than what is seen during training.

1. What is "domain shift"?

	Where the type of data we experience over time changes. As an example customer habits may change over time such that the original model is no longer relevant.

1. What are the three steps in the deployment process?

	- Manually process the data.
	- Limited scope deployment.
	- Gradual expansion.
