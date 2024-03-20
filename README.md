# Mini Project - eldahl - EMNIST Convolutional model
## Repository Link
[https://github.com/eldahl/ML-Mini-Project](https://github.com/eldahl/ML-Mini-Project)
## Problem statement
For the exam in Machine Learning (F2024) a small machine learning solution based on a self-chosen dataset should be developed. 
### Requirements
- The project can be individual, or in a group of up to 3 people.
- The project either be a regression task, or a classification task.
- The project should include:
	- Loading and preparation of data
	- Selection, training and fine-tuning of a model
	- Evaluation of the model
- One of the following model architectures are to be chosen:
	- Multilayer Perceptron
	- Convolutional Neural Network
	- Random Forest
	- Gradient Boosted Decision Trees (incl. Histogram-Based Gradient Boosting)

## Project case
This project is done individually, by eldahl, and is a classification task using a Convolutional Neural Network. The task is to categorize grayscale images with a size of 28x28, as one of 47 unique characters.
### Dataset
The chosen dataset is the EMNIST dataset ([https://www.nist.gov/itl/products-and-services/emnist-dataset](https://www.nist.gov/itl/products-and-services/emnist-dataset)), specifically a subset of it titled 'EMNIST Balanced'. The dataset features 131,600 images of characters of either, the English Latin alphabet in lowercase or uppercase, excluding characters that easily might be misinterpreted as another character, or digits 1 through 9. This results in 47 unique classes of handwritten characters.
### Model architecture
The model is fairly simple in its composition: 
First an input layer, taking the 28x28x1 grayscale image. Then 1-4 convolutional layers, with a kernel size of 2x2, 4x4, or 6x6, and a stride of (1, 1). Next, the convolutional outputs are flattened, in a flatten layer, after which it is feed into a hidden layer with 32-512 neurons. Lastly, an the hidden layer feeds into the output layer, which has a size of 47 neurons. This corresponds to the amount of unique classes in the dataset.
