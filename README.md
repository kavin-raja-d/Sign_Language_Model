# 🎯 Hand Gesture Recognition using MediaPipe and RandomForest

This project is designed to classify hand gestures using a webcam and a pre-trained RandomForest model. The gestures are captured using OpenCV, processed with MediaPipe for landmark detection, and classified with the RandomForest algorithm.

## 📦 Requirements

To run this project, install the following Python libraries:

```bash
pip install opencv-python mediapipe matplotlib scikit-learn numpy
```
## 🎬 How to Run
### Step 1: Data Collection
Collect gesture data for each class using your webcam:

```bash
python collect_dataset.py
```
This script will:
##### Use cv2.VideoCapture(0) to start the webcam.
 ##### Wait for you to press 'Q' to start collecting images.
 ##### Store the captured images in the ./data/ directory.
### Step 2: Train the Model
After collecting the data, train the RandomForest classifier using the collected images:

```bash
python train_classifier.py
```
This will:

 ##### Process the images in the ./data/ folder.
 ##### Extract hand landmarks using MediaPipe.
 ##### Train a RandomForest model to classify the gestures.
 ##### Save the model as model.p for future use.
### Step 3: Real-time Gesture Prediction
Use the trained RandomForest model to predict gestures in real-time:

```bash
python inference_classifier.py
```
This will:

 ##### Start the webcam feed.
 ##### Detect hand landmarks in real-time.
 ##### Predict the gesture and display the results on the webcam feed.
### 🖐 Gesture Classes
The script currently supports 3 classes of hand gestures:

1)Class 0: ✋ Gesture 'A'
2)Class 1: 🖐 Gesture 'B'
3)Class 2: ✌ Gesture 'L'
## 📊 Results
After training, the model can achieve high accuracy depending on the collected dataset. An example result might look like:
```bash
95% of samples were classified correctly!
The trained model is saved in model.p.
```


