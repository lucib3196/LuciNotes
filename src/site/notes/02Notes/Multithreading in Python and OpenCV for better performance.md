---
{"dg-publish":true,"permalink":"/02-notes/multithreading-in-python-and-open-cv-for-better-performance/","tags":["notes/inbox"]}
---

Link: [[02Notes/QKD Resources\|QKD Resources]] - [[02Notes/Multithreading\|Multithreading]] - [[02Notes/OpenCV\|OpenCV]] - [[02Notes/Python\|Python]] - [[02Notes/Computer Vision\|Computer Vision]]

Video processing is an extensive task, especially for application where we require real time processing such as processing a video stream from a webcam. Specifically IO (Input/Output Operations) where data is transferred between the system (like the program) and external devices or systems. These operations involve communication with hardware or software resources outside the CPU's direction computation. 

In other words, blocking I/O operations (which “block” the execution of later code until the current code executes), like reading or displaying video frames

Multithreading is a programming technique that allows multiple threads to execute concurrently within a single process. This improves performance, responsiveness, and efficiency 


----
# Source
- [Multithreading with OpenCV-Python to improve video processing performance • Najam R. Syed](https://nrsyed.com/2018/07/05/multithreading-with-opencv-python-to-improve-video-processing-performance/)