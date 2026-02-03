
# Dense 3D Scene Reconstruction

This project is about reconstruction of a dense 3d scene and obtaining 3d point cloud that is ”hole‑free” from distoreded images and depths and calibration data.

Our Flow: Load Data > Undistort RGB > Depth to Metric Conversion > Back-projection to 3D > World Transformation > PLY Export.


• Input Data:

1. 9 RGB Images: Captured with lens distortion.
2. 9 Depth Images: Already undistorted, scaled to 8-bit grayscale(Z-depth divided by max depth, 
multiplied by 255).
3. Calibration Data: Camera intrinsic parameters and distortion coefficients (k_1, k_2, p_1, p_2, 
k_3).
4. Pose Data: 8 transformations representing the camera movement between successive frames.

• Output: 

1. A single, 3d point cloud unified .ply that is "hole-free".


