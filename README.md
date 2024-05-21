# Flower-recognition-using-CNN
This project uses Convolutional Neural Networks (CNNs) to identify flower species from images. Trained on a large dataset, the CNN model accurately classifies flowers, handling variations in perspective and lighting.Incorporated with a user-friendly interface using Tkinter.Here user can enter the path of the image and can find about the species of the flower.

## **DEPENDENCIES**
 1.Numpy
 2.Pandas
 3.Tensorflow

## **DATASET**
 https://www.robots.ox.ac.uk/~vgg/data/flowers/102/

## **TOOLS**
 jupyterlab

## **ABOUT DATASET**
There are totally 100 classes and a total of 8051 images.
From those images i've taken 6478 for training and 1573 for testing.

## **TRAINING MODEL**
### **Data Preparation:**
I have used the ImageDataGenerator class for data augmentation and rescaling, splitting the dataset into training and validation sets.
I've loaded the dataset from a directory and applied transformations to enhance the training process.

### **Model architecture**
I've constructed a sequential CNN model with multiple convolutional layers (Conv2D) and max-pooling layers (MaxPooling2D).
The model includes several layers to extract features from the images, followed by a dense layer for classification.
I've  added a softmax activation function in the final layer to classify the images into 100 different flower categories.

### **Model compilation and training**
I've compiled the model using the Adam optimizer and the categorical cross-entropy loss function.
I've trained the model for 30 epochs, tracking the accuracy and loss for both training and validation datasets.

### **Model performance visualization**
I plotted the training and validation accuracy and loss over the epochs to visualize the model’s performance.
These plots help to understand how well the model is learning and generalizing to new data.

### **Model saving**
I saved the trained model to a file named Flower.keras for future use or deployment.

Overall, I created and trained a CNN model, evaluated its performance, saved the model, and visualized ROC curves for a detailed analysis of the classification performance.

## **PREDICTION MODEL**
### **Importing Libraries**

First, I imported the necessary libraries such as tkinter for creating the GUI, PIL (Python Imaging Library) for image processing, numpy for handling numerical operations, and tensorflow.keras for loading the trained model.
I also used cv2 from OpenCV for image preprocessing.

### **Loading the Trained Model**
I loaded a pre-trained CNN model (Flower.keras) which I had previously trained to classify flower images into one of 100 categories.

## **Defining Flower Names**
I defined a list of 100 flower names that correspond to the classes the model can predict. This list is used to map the predicted class ID to the actual flower name.

### **Classify Image Function**
I've created a function, classify_image(), to handle image classification:
   It retrieves the image path from a text entry widget.
   Loads and preprocesses the image, ensuring it's in the correct format and size.
   Predicts the flower class using the loaded model.
   Updates the GUI to display the predicted flower name and the selected image.
   This function streamlines the classification process for a smooth user experience.

### **Creating the Tkinter GUI**
I designed the main window of the application, setting its title. Then, I added a label and an entry widget for the image path input. A button was included to trigger the classify_image() function upon clicking. Additionally, I integrated a label to exhibit the selected image and another to showcase the predicted class name.

### **Running the GUI**
Finally, I started the Tkinter main loop with window.mainloop() to keep the application running and waiting for user interaction.
