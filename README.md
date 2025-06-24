# Pose-detector

This project is a posture detection system built using Python, OpenCV, and MediaPipe. It focuses on identifying whether a person in a static image is sitting or standing by analyzing human body landmarks and calculating joint angles.

The core logic utilizes MediaPipe Pose, which provides 33 key landmark points on the human body. From these, the system extracts the coordinates of the shoulders, hips, knees, and ankles. Using trigonometric functions, it computes the angles at the knees and evaluates the vertical positioning of the hips relative to the shoulders.

A person is classified as sitting if:

The leg angles (hip-knee-ankle) are less than a defined threshold (e.g., < 120°), indicating a bent knee.

The hips are lower than the shoulders, based on the y-coordinate values of the landmarks.

Otherwise, the person is classified as standing.

The project also includes a visual output using Matplotlib, showing the original image where the posture has been analyzed. This lightweight tool is useful for applications in fitness monitoring, workplace ergonomics, human activity recognition, and more.