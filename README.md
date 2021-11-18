# MNIST-digit-classifier-from-scratch
A feedforward deep neural network built from scratch to classify handwritten digits from the MNIST dataset

This is a simple feedforward neural network that can be initialised with a flexible number of layers, and layer size.
The purpose of this project was to learn the fundamentals of deep learning, gaining an understanding of the computations taking place.
I'm aware a similar, if not better, model could be trained with a few lines of code using Keras and TensorFlow, but that approach obscures the underlying computation.

A lot of the code for this project is messy, with debugging steps still included. I wanted to leave these in as it is a reminder of the process I went through when creating the model. I have tried to indicate the redundant blocks where possible.

To load a pretrained model, run the pickel block that imports the saved parameters.

The inspiration for the project came whilst completing Deeplearning.AI's course on Neural Networks and Deeplearing. In the course it showed how to create a similar model for binary classification. I then applied what I learnt to MNIST dataset. This was ultimately successful, however I'm aware it could be significantly improved by using a different cost function. The current cost function is mean square error. This works ok for binary classification, but for classifying 10 digits using one-hot encoding it fall short. The learning algorithm immediately biases the output neurons to near zero. This is a very quick way of reducting the cost, but causes long plateaus getting stuck on a cost of roughly 0.9. However, with enough training iterations and tuning of the hyperparameters, this plateau can be overcome and the model starts to learn quickly again. An accuracy of about 97% can be achieved using this approach. Using catagorical cross entropy as a cost function would improve training speeds, and likely overall performance. Another way to improve performance could be to add convolution layers.
