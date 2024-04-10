# Gesture_detection-

**Introduction**
This repository contains code for detecting a specific gesture in a video stream. The system processes input video data, detects the desired gesture, overlays text on the video frames where the gesture is detected, and saves the annotated video as an output.

**Setup**
Requirements: Make sure you have Python installed along with the necessary libraries such as OpenCV (cv2) and NumPy (numpy).
Clone Repository: Clone this repository to your local machine.

**Data Processing**

The input data (video frames) are processed using OpenCV, a computer vision library.
The desired gesture representation is loaded, either as an image or a video clip, and converted to grayscale for template matching.

**Model Selection/Development**
The template matching technique is used for gesture detection.
The template matching algorithm (cv2.matchTemplate) compares the template (desired gesture) with the video frames.

**Detection Algorithm**
The algorithm compares the correlation coefficient between the template and each frame.
A threshold is applied to determine whether the gesture is detected.
Bounding boxes are drawn around the detected gestures on the video frames.

**Annotation**
Detected gestures are annotated with "DETECTED" text, accuracy, detection time, CPU usage, and memory usage.
The annotated frames are then saved as an output video.

**Accuracy and Efficiency**
Accuracy: The accuracy of the detection algorithm is measured by the correlation coefficient between the template and the video frames. Higher correlation coefficients indicate a better match between the gesture and the frames.
Efficiency: The efficiency of the algorithm is achieved through real-time processing of video frames. The system monitors CPU and memory usage to optimize performance and resource utilization.

**Usage**
Update the paths for the desired gesture representation and the test video in the provided code.
Run the Python script (gesture_detection.py).
The annotated output video will be saved in the specified location.

**Challenges and Solutions**
Threshold Selection: Choosing an appropriate threshold for template matching can be challenging. It requires experimentation to find the optimal value.
Performance Optimization: Processing video frames in real-time while maintaining accuracy requires efficient code and resource management. Utilizing libraries like Psutil for monitoring CPU and memory usage helps optimize performance.
Handling Various Gestures: Extending the system to detect multiple gestures or complex gestures would require more sophisticated algorithms and potentially a larger dataset for training.

**Contributors**
This code was developed by Pratham Desai.
Contributions and feedback are welcome.

License
This project is licensed under **MIT license**. See the LICENSE file for details.
