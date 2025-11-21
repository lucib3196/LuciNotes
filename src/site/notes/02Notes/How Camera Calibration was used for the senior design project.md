---
{"dg-publish":true,"permalink":"/02-notes/how-camera-calibration-was-used-for-the-senior-design-project/","tags":["notes/atomic"]}
---

Link: [[02Notes/QKD Resources\|QKD Resources]] - [[02Notes/Camera Calibration\|Camera Calibration]] 

To calibrate a camera, we used OpenCV and a checkerboard to capture multiple images of the checkerboard from different angles. We detected the corners using` cv2.findChessboardCorners()`, refined them with `cv2.cornerSubPix()`, and mapped them to corresponding 3D world coordinates. We then used `cv2.calibrateCamera()` to compute the camera matrix and distortion coefficients. Finally, given an image, we applied `cv2.undistort()` to correct lens distortion. 

Scripts were developed to calibrate the camera, obtaining the camera matrix and distortion coefficients. 

**Note**: When working with a PICamera you need to specify the camera settings at time of calibration. 

For example, if a resolution of 1280x720 is required, images must be captured at that resolution, as the calibration will only be valid for those settings. Changing calibration settings is possible; the scripts are constructed to swap different settings based on the performance we want to achieve. for instance, higher resolution leads to higher quality videos at the cost of frame rate.

![Pasted image 20250106133159.png|Example Calibration Frame](/img/user/Attachments/Pasted%20image%2020250106133159.png)


---
# Related

- [[02Notes/Camera Calibration\|Camera Calibration]]: Overview on how calibration works

----
# Source