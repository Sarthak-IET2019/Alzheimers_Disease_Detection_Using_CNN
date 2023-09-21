# Installation Steps

Steps : 
1. Install virtual environment by running the command on your local : "pip install virtualenv"
2. cd to your cloned repository and create a venv by running  : "python -m venv env"
3. activate the environment as : ".\env\Scripts\activate"
4. The repository contains requirements.txt file for installing all necessary packages. Run the command "pip install -r requirements.txt"
5. Run the command "python main.py" to run the server in the dev environment






**Machine Learning Model for Alzheimer's Image Classification**

**Overview:**

Our machine learning model is designed for the classification of Alzheimer's disease images into one of four categories: "NonDemented," "VeryMildDemented," "MildDemented," and "ModerateDemented." To achieve this, we've built a Convolutional Neural Network (CNN) model, which is well-suited for image classification tasks.

**Key Components:**

1. **Convolutional Layers:** Our CNN architecture includes multiple convolutional layers. Convolutional layers are responsible for automatically extracting relevant features from the input images. These layers play a critical role in understanding the spatial patterns in the images.

2. **Dropout Layers:** To prevent overfitting, we've incorporated dropout layers into our model. Dropout layers temporarily deactivate a fraction of neurons during training, which encourages the network to learn more robust and generalizable features.

3. **Dense Layers:** After the convolutional layers, we employ dense (fully connected) layers to further process the learned features. These layers enable the network to make high-level decisions based on the extracted features.

4. **Flatten Layer:** Before passing data to the dense layers, we use a flatten layer to convert the 2D feature maps from the convolutional layers into a 1D vector. This flattening step is necessary to connect the convolutional part of the network to the fully connected part.

5. **Image Augmentation:** To enhance the model's ability to generalize from the available data, we have applied image augmentation techniques to our training and test datasets. Image augmentation introduces variations in the training images, such as rotations, translations, and flips. This helps the model become more robust to different orientations and positions of the images.

6. **Optimizer:** We've employed the Adam optimizer during training. The Adam optimizer is known for its efficiency in updating the network's weights and converging to a solution in a wide range of tasks. It adapts the learning rates for each parameter individually, which can lead to faster convergence.

7. **Loss Function:** For the training process, we use the cross-entropy loss function. Cross-entropy loss is commonly used in multi-class classification problems like ours. It measures the dissimilarity between the predicted class probabilities and the true class labels.

**Performance Evaluation:**

To assess the model's performance, we employ various evaluation metrics, including accuracy, precision, recall, and the Area Under the Curve (AUC) of the Receiver Operating Characteristic (ROC) curve. These metrics provide insights into the model's ability to correctly classify Alzheimer's disease images.

