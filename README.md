# ADEB-GenBot---Advanced-Distress-Emergency-Bot-with-generative-models-using-Deep-learning
ADEB-GenBot is an advanced emergency bot utilizing generative models and deep learning. It analyzes distress signals to provide tailored assistance in real-time, enhancing emergency response.
ADEB-GenBot, an Embedded Hardware device which can detect distress calls using complex hand gestures and help to convey the distress signals in ways such as text messages to family and automatic calls to authorities. Using Inertial Measurement Units (IMU) combined with Deep Learning algorithms served on a MATLAB backend, the bot can detect distress calls with pinpoint accuracy and take action on the same on a real time basis.

Problem Statement

The process of dialing a number and calling someone in an emergency can prove to be time taking. We need FASTER ways of doing so because in such situations, every second is important.
In situations involving criminal acts, for example kidnapping, blackmailing etc, one can be restricted from making a phone call by the offender. We need SUBTLER ways of informing the authorities concerned without bringing it to the knowledge of the offender.


Solution

We built a pipeline based on the state-of-the-art Inertial Measurement Unit using Arduino, MATLAB and Tensorflow to recognise a specific pre-decided hand gesture in the case of an emergency. If such a gesture is detected, a distress alert is automatically sent to the emergency contact of that person to take further action.

Our team integrated Arduino sitting on top of MATLAB computation engine to get live stream accelerometer and gyroscopic data from a BNO055 Inertial Measurement Unit (IMU) attached to a person's wrist and sampling at a frequency of 20 Hz. MATLAB is required to process the 6 dimensional continous data stream from the IMU.
A continuous data link is established between MATLAB and TensorFlow to enable live hand gesture detection using a deep learning model. Given the continuous inflow of data, TensorFlow makes approximately 2 predictions every second using an input vector containing 480 data points.
If a critical/target gesture is detected by TensorFlow, an e-mail is sent on behalf of the person to their listed Emergency Contact notifying them on the distress call with the person's details such as time and location, etc.
