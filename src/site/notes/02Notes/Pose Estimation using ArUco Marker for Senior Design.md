---
{"dg-publish":true,"permalink":"/02-notes/pose-estimation-using-ar-uco-marker-for-senior-design/","tags":["notes/atomic","project","publish"]}
---

Link: [[02Notes/Transformation Matrices\|Transformation Matrices]] - [[02Notes/QKD Resources\|QKD Resources]] - [[02Notes/Pose Estimation\|Pose Estimation]] - [[02Notes/ArUco Markers\|ArUco Markers]]


![Pasted image 20250228183522.png](/img/user/Attachments/Pasted%20image%2020250228183522.png)

A **preliminary ArUco-based tracking system** was developed to enable object detection, pose estimation, and alignment control. 

Scripts were created to generate ArUco markers for identification and tracking, allowing us to determine the marker's orientation and position relative to the camera frame. 

By extracting translational and rotational vectors, we can compute the angle between the marker and the camera using functions like `atan(x, z)`, which is particularly useful for calculating yaw. 

This approach is the primary reason for calibrating the camera, as accurate pose estimation depends on precise intrinsic parameters. 

Furthermore, once we establish the transformation matrix from the marker, we do not need to continuously track it. If we know the position of a reference point in a given frame, we can perform a coordinate transformation, leveraging the known pose of the marker. 

This is crucial for our goal of aligning a laser with a mirror, as it enables precise adjustments without requiring constant marker detection.

---
# Related
- [[02Notes/How Camera Calibration was used for the senior design project\|How Camera Calibration was used for the senior design project]]
- [[02Notes/ArUco Markers\|ArUco Markers]]
----
# Source
- [PRECISION LANDING | with OPENCV and ARUCO Markers | Part 1]([https://www.youtube.com/watch?v=wlT_0fhGrGg] )