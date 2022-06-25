# fastai

- What is ML?

Machine learning is a discipline where we define a program not by writing it entirely ourselves, but by learning from data. Deep learning is a specialty within machine learning that uses neural networks with multiple layers. Image classification is a representative example (also known as image recognition). We start with labeled data; that is, a set of images where we have assigned a label to each image indicating what it represents. Our goal is to produce a program, called a model, which, given a new image, will make an accurate prediction regarding what that new image represents.

Every model starts with a choice of architecture, a general template for how that kind of model works internally. The process of training (or fitting) the model is the process of finding a set of parameter values (or weights) that specialize that general architecture into a model that works well for our particular kind of data. In order to define how well a model does on a single prediction, we need to define a loss function, which determines how we score a prediction as good or bad.

To make the training process go faster, we might start with a pretrained model—a model that has already been trained on someone else's data. We can then adapt it to our data by training it a bit more on our data, a process called fine-tuning.

When we train a model, a key concern is to ensure that our model generalizes—that is, that it learns general lessons from our data which also apply to new items it will encounter, so that it can make good predictions on those items. The risk is that if we train our model badly, instead of learning general lessons it effectively memorizes what it has already seen, and then it will make poor predictions about new images. Such a failure is called overfitting. In order to avoid this, we always divide our data into two parts, the training set and the validation set. We train the model by showing it only the training set and then we evaluate how well the model is doing by seeing how well it performs on items from the validation set. In this way, we check if the lessons the model learns from the training set are lessons that generalize to the validation set. In order for a person to assess how well the model is doing on the validation set overall, we define a metric. During the training process, when the model has seen every item in the training set, we call that an epoch.

All these concepts apply to machine learning in general. That is, they apply to all sorts of schemes for defining a model by training it with data. What makes deep learning distinctive is a particular class of architectures: the architectures based on neural networks. In particular, tasks like image classification rely heavily on convolutional neural networks, which we will discuss shortly.

- Nitty-Gritty: Where do we start, model building wise?

Remember to make a baseline model (mean) before attempting to build something more advanced (multi-layered-perceptron/layered-MLP: ResNet, LTST, GPT, etc.)! Example: in MNIST, the baseline would be a model that is trained to recognise the average of pixels in a training set.

- A positive sum game: What is a predictive model in the Deep Learning world which is viable investment wise, and ethically?

```
- User must opt into the data extraction happily: this means they should benefit from the data analytics that they are producting data for. The economy should be a two way non-extractive system. Or at the very least, mutually extractive. 

- The data flow should be continuous. This means that the source of the data should have a long-term investment in the program that collects the data; be that emotionally, fincancially, socially or otherwise. The source and the anaytic models should communicate effectively. The data should feed into the model, the model should provide value, the source should be compensated, and then provide more data happily knowing that they will benefit from the process as it continues.

- In order to cut out the advertising agents and avoid further collapse of civilisation, the data should be hidden. The problem here is that: how can a user trust that the computer is providing the correct work on their data? The future of this process will likely involve ZKP, where we can verify that a calculation is done fairly without any trust or revealing the data itself. This allows for a truly tustless and anonymous economic system where real work is rewarded and malicious actors are destroyed.
```

Where does the magic happen, computationally? Well, we batch data correctly into the `DataLoaders` class for GPU acceleration. NOTE-TO-SELF: explore here!

> ALL CONTENT IN THIS REPO IS FOR EDUCATIONAL PURPOSES ONLY

> ALL IMAGE SOURCES FOR IMAGES IN [/Psilocybe](/Psilocybe/) ARE FILED UNDER [/SOURCES.json](/SOURCES.json)
