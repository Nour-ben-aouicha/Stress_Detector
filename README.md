# Stress_Detector 🚀🔍🧘‍♂️
### Real-Time Body Language Detection using MediaPipe and OpenCV

This project offers real-time analysis of body language via a webcam feed, using the MediaPipe and OpenCV libraries. Here's an overview of its functionalities:

#### Functionalities

**Detection and Visualization:**
- Utilizes MediaPipe's Holistic model to identify facial landmarks, hand gestures (both right and left), and body poses from the webcam frames; in this project we mainly targeted stress related gestures and facial expressions.
- Visualizes these detected landmarks on the frame using OpenCV's drawing functions, creating lines and points to represent facial features, hand movements, and body postures.

**Landmark Data Collection:**
- Captures the detected landmarks and exports their coordinates into a CSV file (`coords.csv`), containing data on facial landmarks, pose landmarks, and visibility information.

**Model Creation:**
- Reads the landmark data from the CSV file into a pandas DataFrame.
- Prepares the data for training a machine learning model by splitting it into training and testing sets.

**Model Training and Evaluation:**
- Utilizes multiple machine learning algorithms (Logistic Regression, Ridge Classifier, Random Forest Classifier, Gradient Boosting Classifier) to train models using the collected landmark data.
- Assesses the accuracy of the trained models on the test dataset.

**Model Saving and Real-Time Prediction:**
- Saves the trained Random Forest Classifier model (`body_language.pkl`) using pickle.
- Loads the saved model to make real-time predictions on the detected landmarks from the webcam feed.
- Displays the recognized body language class on the video feed, enhancing visualization by drawing rectangles and text near the left ear area.
