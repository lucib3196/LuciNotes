---
{"dg-publish":true,"permalink":"/02-notes/camera-calibration/","tags":["notes/atomic","project"]}
---

Link: [[02Notes/Computer Vision\|Computer Vision]] - [[02Notes/QKD Resources\|QKD Resources]]

![Pasted image 20250205120327.png|camera distortion visualized](/img/user/Attachments/Pasted%20image%2020250205120327.png) [^5]
##### Radial and Tangential Distortion

- **Radial Distortion**: Occurs when straight lines appear curved, with distortion increasing as points move farther from the image center.
  - Radial distortion can be represented as:
    $$
    x_{\text{distorted}} = x(1 + k_1 r^2 + k_2 r^4 + k_3 r^6)
    $$
    $$
    y_{\text{distorted}} = y(1 + k_1 r^2 + k_2 r^4 + k_3 r^6)
    $$
- **Tangential Distortion**: Occurs when the image-taking lens is not perfectly aligned parallel to the image plane.
  - Tangential distortion is given by:
    $$
    x_{\text{distorted}} = x + [2p_1 xy + p_2 (r^2 + 2x^2)]
    $$
    $$
    y_{\text{distorted}} = y + [p_1 (r^2 + 2y^2) + 2p_2 xy]
    $$
- The distortion coefficients that need to be determined are:

    $$
    \text{Distortion coefficients} = (k_1, k_2, p_1, p_2, k_3)
    $$

##### Camera Intrinsic and Extrinsic Parameters

- **Intrinsic Parameters**: These are specific to the camera, such as focal length and optical centers.
  - Focal lengths are denoted as \( $f_x$, $f_y$ \).
  - Optical centers are denoted as \( $c_x$, $c_y$ \).
  - These values can be used to construct a **camera matrix**, which helps correct distortions caused by the camera lens.
    The **camera matrix** is given by:
    $$
    \text{camera matrix} =
    \begin{bmatrix}
    f_x & 0 & c_x \\
    0 & f_y & c_y \\
    0 & 0 & 1
    \end{bmatrix}
    $$

----
# Source
- [https://docs.opencv.org/4.x/dc/dbb/tutorial_py_calibration.html](Documentation on how to perform camera calibration using OpenCV) 