# Tesseract-Animaiton
Tesseract animation using Blender and Python

# Important Info
The "tesseract.blend" file can only be opened with Blender Animation Software and you have to press the play button to see the animation

# Project Summary: Tesseract Animation in Blender

## Introduction to Tesseracts

A tesseract, also known as a 4D hypercube, is a four-dimensional geometric shape. Just as a 3D cube is bounded by square faces, a tesseract is bounded by cubic cells. Each vertex of a tesseract has four coordinates, representing its position in four-dimensional space.

## Projection of a Tesseract

To visualize a tesseract in our three-dimensional world, we project it from 4D to 3D. This is analogous to projecting a 3D cube onto a 2D plane. The projection involves transforming the 4D coordinates of the tesseract into 3D coordinates, allowing us to create a visual representation that can be rendered and animated.

## Code Overview

1. **Importing Libraries:**
    - `bpy`: Blender's Python API for accessing and manipulating 3D objects.
    - `numpy`: A library for numerical operations, used here for matrix and vector calculations.

2. **Animation Parameters:**
    - `axis1` and `axis2`: Axes for rotation.
    - `d`: Perspective distance for projection.
    - `num_frames`: Total number of frames in the animation.
    - `frame_rate`: Frame rate of the animation.
    - `freq` and `rot_dir`: Frequency and direction of rotation.

3. **Retrieving the Tesseract Object:**
    - The active mesh object in Blender, named 'tesseract_fresh', is accessed for manipulation.

4. **Defining Tesseract Vertices:**
    - Vertices of the tesseract are initialized using binary representation to generate all possible combinations of four coordinates.

5. **Projection Matrix:**
    - A function `proj_mat(p)` creates a matrix to project 4D points to 3D. The perspective is controlled by the fourth coordinate.

6. **Rotation Matrix:**
    - A function `rot(a, b, theta)` generates a 4D rotation matrix for rotating points around the specified plane (a-b).

7. **Rotating the Tesseract:**
    - `rot_cube(a, b, theta, points)` applies the rotation matrix to all vertices of the tesseract.

8. **Animating the Tesseract:**
    - The main loop iterates over each frame, rotating the tesseract and projecting its vertices into 3D space.
    - The 3D coordinates are then used to update the mesh vertices in Blender, creating the keyframes for the animation.

In Blender, there were additional components which enabled the creation  and aesthetics of the 3D model of Tesseract. 

This project involves complex mathematical operations for 4D geometry manipulation and demonstrates how Blender's scripting capabilities can be leveraged to create dynamic visualizations of higher-dimensional objects.
