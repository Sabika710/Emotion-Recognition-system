🎭 Real-Time Human Emotion Detection using CNN

This project detects human emotions in real-time using a webcam feed. It utilizes a Convolutional Neural Network (CNN) trained on facial expression data to classify emotions such as happy, sad, angry, surprised, neutral, disgust, and fear.

🧠 Project Overview

This project uses a deep learning model built with Keras and OpenCV to recognize human emotions from facial expressions.
It captures live video input, detects faces using Haar cascades, and classifies the emotion on each detected face.

📂 Repository Contents
File	Description
realtimedetection.py	Main Python script for running real-time emotion detection using webcam input.
emotiondetector.json	Saved model architecture in JSON format.
emotiondetector.h5	Model weights file (not included here, should be placed in the same directory).
README.md	Project documentation (this file).
⚙️ How It Works

The model (emotiondetector.json + emotiondetector.h5) is loaded using Keras.

The webcam feed is accessed using OpenCV (cv2.VideoCapture(0)).

Faces are detected using the pre-trained Haar Cascade Classifier.

Each detected face is resized to 48×48 pixels and passed through the CNN model.

The predicted emotion label is displayed on the live video stream.

🧩 Detected Emotions

The model can classify faces into seven categories:

Label	Emotion
0	Angry 😠
1	Disgust 🤢
2	Fear 😨
3	Happy 😀
4	Neutral 😐
5	Sad 😢
6	Surprise 😲
🛠️ Installation & Setup
1. Clone the Repository
git clone https://github.com/<your-username>/human-emotion-detection.git
cd human-emotion-detection

2. Install Dependencies

Make sure you have Python 3.8+ installed, then run:

pip install tensorflow keras opencv-python numpy

3. Add Model Weights

Download or place your emotiondetector.h5 file in the same directory as:

realtimedetection.py
emotiondetector.json
emotiondetector.h5

4. Run the Program
python realtimedetection.py

🖥️ Example Output

When you run the script, your webcam feed will open and detected faces will be annotated with the predicted emotion label.

🧪 Model Details

Framework: TensorFlow / Keras

Architecture: CNN with multiple Conv2D, MaxPooling, Dropout, and Dense layers

Input Size: 48 × 48 grayscale images

Loss Function: Categorical Crossentropy

Optimizer: Adam

Dataset: FER2013 (Facial Expression Recognition)

🚀 Future Improvements

Improve accuracy with larger datasets

Add GUI using Flask or Tkinter

Support multi-face detection with separate emotion overlays

Deploy as a web app using Flask or Streamlit
