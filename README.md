# **Hand Gesture Volume Control**
## **Dependencies**
- CoreAudio: Provides access to audio devices and volume control on macOS.<br>
- OpenCV: A computer vision library used for image processing and contour detection.

## **Functionality**
The code provides a hand gesture volume control system using a webcam and the OpenCV library. It allows you to control the volume of a Mac computer by using hand gestures in front of the webcam

## **How It Works**
The code captures frames from the webcam using OpenCV.

**It detects hand gestures by:**
- Selecting a Region of Interest (ROI) within the frame
- Converting the ROI into grayscale
- Applying Gaussian blur to smoothen the image
- Thresholding the image to obtain a binary representation
- Finding contours in the binary image

Once the contours are obtained, the code performs the following steps:

- Selecting the contour with the largest area as the hand contour.
- Finding the convex hull and convexity defects of the hand contour.
- Determining the fingertip points based on the deepest defect.

If fingertip points are successfully detected, the code proceeds with the following actions:

- Drawing lines and circles to highlight the fingertips and the defect.
- Calculating the distance between the fingertips.
- Adjusting the Mac volume based on the calculated distance.
- Displaying the distance between the fingertips on the top-right corner of the image.
- Displaying the current volume percentage on the top-left corner of the image.
- Drawing a rectangle around the ROI on the original image.

The processed frame is then displayed in a window named "Webcam". The code continuously listens for keyboard input to provide additional functionality:

- Pressing 'q' will exit the program.
- Pressing 't' will toggle the display of fingertip detection on and off.

### Instructions

To use the hand gesture volume control system, follow these steps:

1. Ensure that you have a working webcam connected to your computer.
2. Build and run the code.
3. A window named "Webcam" will open, displaying the live feed from the webcam.
4. Position your hand within the defined Region of Interest (ROI) displayed as a green rectangle.
5. Perform hand gestures, and the code will detect your fingertips and adjust the Mac volume accordingly.
6. The distance between your fingertips will be displayed on the top-right corner of the image, while the current volume percentage will be shown on the top-left corner.
7. To exit the program, press the 'q' key.
8. To toggle the display of fingertip detection on and off, press the 't' key.

Note: Make sure that the audio output of your Mac is set to the default device to enable proper volume control.
