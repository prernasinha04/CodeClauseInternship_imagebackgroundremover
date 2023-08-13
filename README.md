# CodeClauseInternship_imagebackgroundremover
Project: OpenCV Face Detection

Description:
In this project, I'm using the OpenCV library in Python to build a face detection application using your computer's webcam. The application captures video from the webcam, detects faces in the video frames, and marks the detected faces with rectangles.

Steps:

Setup:

Import the necessary libraries, including cv2 for OpenCV and numpy for array operations.
Load Haar Cascade Classifier:

Create a CascadeClassifier object using the pre-trained Haar Cascade classifier XML file (haarcascade_frontalface_default.xml).
Open Webcam:

Use the cv2.VideoCapture function to open the default camera (camera index 0).
Face Detection Loop:

Enter a loop to continuously capture video frames from the webcam.
Frame Processing:

Convert each video frame to grayscale using cv2.cvtColor.
Face Detection:

Use the detectMultiScale method of the cascade classifier to detect faces in the grayscale frame.
This function returns a list of rectangles representing the detected faces.
Rectangle Drawing:

Loop through the detected face rectangles and draw rectangles around them using cv2.rectangle.
Display Result:

Display the video frame with the detected faces using cv2.imshow.
Loop Control:

Wait for a key press using cv2.waitKey. If the key is 'q', exit the loop.
Cleanup:

Release the webcam using cap.release() and close all OpenCV windows using cv2.destroyAllWindows().
Outcome:
As I run the code, your webcam will start capturing video frames. The code will detect faces in each frame using the Haar Cascade classifier and draw rectangles around the detected faces. The processed frames with rectangles will be displayed in a window. Pressing the 'q' key will exit the application.
