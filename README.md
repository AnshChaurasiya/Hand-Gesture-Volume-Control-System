# Hand-Gesture-Volume-Control-System
This program make user to control volume of there system using hand Gesture

The code consists of two files: 'handtrackmod.py' and 'volumecontrol.py'.

'handtrackmod.py' is a module that contains a class 'handDetector' for detecting hand landmarks using the MediaPipe library. The class takes several parameters in its constructor, such as mode, maxHands, modelComplexity, detectionCon, and trackCon, which are used to configure the hand detector. The class provides two methods: 'findHands' and 'findPosition'. The 'findHands' method takes an image as input and returns the image with hand landmarks drawn on it. The 'findPosition' method takes an image and a hand number as input and returns the list of landmark positions for the specified hand.

'volumecontrol.py' is a script that uses the 'handtrackmod' module to control the system volume using hand gestures. The script initializes a video capture object to capture video from the default camera. It then creates an instance of the 'handDetector' class and sets the minimum and maximum volume levels. The script then enters a loop where it continuously captures frames from the camera, detects hand landmarks using the 'handDetector' instance, and calculates the distance between the index finger and thumb tips. If the distance is within a certain range, the script adjusts the system volume accordingly. The script also draws a volume bar on the screen to visualize the current volume level.
