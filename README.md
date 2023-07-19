
# Gender Detection Using CNN, Keras, OpenCv

This code is an implementation of a gender detection model using a Convolutional Neural Network (CNN) with Keras and TensorFlow. Here's a brief overview of the code:

1. Load images from the dataset directory and convert them into arrays. Images are resized to (96, 96) dimensions and normalized to values between 0 and 1.
2. Labels are assigned to the images based on the parent folder (either "man" or "woman"), and they are one-hot encoded.
3. The dataset is split into training and testing sets.
4. Data augmentation is applied to the training set using `ImageDataGenerator` to create additional training samples through rotation, width/height shifting, shearing, zooming, and horizontal flipping.
5. The CNN model is defined with convolutional layers, activation functions, batch normalization, max-pooling, and dropout layers.
6. The model is compiled with Adam optimizer, binary cross-entropy loss (since we have two classes: "man" and "woman"), and accuracy as a metric.
7. The model is trained using the augmented training data and evaluated on the test set.
8. The trained model is saved to a file named 'gender_detection.h5'.
9. Training and validation loss/accuracy are plotted and saved to 'plot.png'.

The `build` function defines the architecture of the CNN model. It uses Conv2D layers with ReLU activation, BatchNormalization, MaxPooling2D, and Dropout layers to prevent overfitting. The output layer uses the sigmoid activation function since this is a binary classification problem (man or woman).

Make sure to have the dataset correctly structured with separate folders for "man" and "woman" images. You can adjust the parameters such as `epochs`, `batch_size`, and data augmentation settings to further optimize the model's performance.

If you have any specific questions or need further assistance, feel free to ask!





![Screenshot (9)](https://user-images.githubusercontent.com/108931665/201774882-a34542c0-9874-4688-8266-2797872e4f84.png)
![Screenshot (7)](https://user-images.githubusercontent.com/108931665/201774925-db3b7ea1-ce78-41ed-964a-131ba4e35926.png)
![Screenshot (6)](https://user-images.githubusercontent.com/108931665/201774932-77d5d4ca-fcab-40e2-b25e-1191e41b5735.png)
