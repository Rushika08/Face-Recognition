This code is a simple example of using a pre-trained convolutional neural network (CNN) model for image classification in real-time using a webcam. Let's break down the code:

### Importing Libraries:

keras.models: Importing the load_model function from Keras to load a pre-trained model.
cv2: Importing the OpenCV library for image processing and computer vision.
numpy: Importing the NumPy library for numerical operations.

### Disabling Scientific Notation:

Setting NumPy options to suppress scientific notation for better clarity in output.

### Loading the Model:

Using load_model to load a pre-trained Keras model from the file "keras_Model.h5".
compile=False is used to load the model without compiling it.

### Loading Labels:

Opening and reading the labels from the "labels.txt" file into the class_names variable.

### Capturing Video from Webcam:

Initializing the webcam using cv2.VideoCapture(0). The argument can be 0 or 1 based on the default camera of your computer.

### Processing Frames in a Loop:

Running an infinite loop to continuously capture frames from the webcam.
Resizing each frame to (224, 224) pixels.
Displaying the resized frame using cv2.imshow.

### Preparing Image for Prediction:

Converting the image to a NumPy array and reshaping it to match the model's input shape.
Normalizing the image by scaling its values to the range (-1, 1).

### Making Predictions:

Using the pre-trained model to predict the class probabilities for the input image.
Extracting the index of the class with the highest probability using np.argmax.
Retrieving the class name and confidence score based on the index.

### Displaying Prediction and Confidence:

Printing the predicted class and confidence score on the console.

### Handling Keyboard Input:

Listening for keyboard input using cv2.waitKey(1).
If the 'Esc' key (ASCII 27) is pressed, the loop breaks.

### Releasing Resources:

Releasing the camera and closing all OpenCV windows after the loop ends.

### Summary:
This code uses a pre-trained CNN model to classify images from the webcam in real-time. It captures frames, preprocesses them, predicts the class, and displays the results along with confidence scores. The loop continues until the 'Esc' key is pressed.
