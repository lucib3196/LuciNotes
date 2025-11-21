---
{"dg-publish":true,"permalink":"/02-notes/ar-uco-markers/","tags":["notes/atomic","project"]}
---

Link: [[02Notes/Computer Vision\|Computer Vision]] - [[02Notes/Python\|Python]] - [[02Notes/OpenCV\|OpenCV]] - [[02Notes/Machine Learning\|Machine Learning]] - [[02Notes/Robotics\|Robotics]] - [[02Notes/QKD Resources\|QKD Resources]]

**ArUco Markers**: They stand for Augmented Reality University of Cordoba

ArUco Markers are used for computer vision applications such as camera calibration, pose estimation and augmented reality. They are constructed via grids which contain a unique binary pattern which allows it to be detected by computer vision algorithms.  In terms of ARuco 0 is black while white is 1. [^4]
They are defined by dictionaries size and marker size
- **Dictionary**: A collection of markers where size refers to the collection of them
- **Marker Size**: The marker size followed by the number of bits
**Example**
Dict_6x6_250: 6x6 is the grid size, while the 250 is how many bits. 
![Pasted image 20250205115315.png|aruco marker](/img/user/Attachments/Pasted%20image%2020250205115315.png)
**Benefits**: 
- **Robust detection:** The black border and binary pattern allow the markers a robust to various lighting conditions and partial occlusions
- **Pose estimation:** The four corners provide enough correspondence to estimate the camera pose
- **Error detection and correction:** Binary patter allows for error detection and correction


![Untitledvideo-MadewithClipchamp-ezgif.com-video-to-gif-converter.gif|ArUco Tracking Basic](/img/user/Attachments/Untitledvideo-MadewithClipchamp-ezgif.com-video-to-gif-converter.gif)


---
# Related
- [[02Notes/Camera Calibration\|Camera Calibration]] 
----
# Source
- https://youtube.com/shorts/MZPZ565-ux8?si=0ihgA8D2GQNx3aSX
-  [Detecting ArUco markers with OpenCV and Python - GeeksforGeeks](https://www.geeksforgeeks.org/detecting-aruco-markers-with-opencv-and-python-1/#)


