Sign Language Detection using Mediapipe and LSTM
================================================

This project is a **real-time sign language detection** system that uses **Mediapipe** for hand, pose, and face landmark detection and an **LSTM (Long Short-Term Memory) neural network** for recognizing sign language gestures. The system processes webcam input, predicts sign language actions, and visualizes the results in real-time.

Features
--------

*   **Real-time video input** using OpenCV
    
*   **Mediapipe** for detecting hand, face, and pose landmarks
    
*   **LSTM neural network** for classifying sign language gestures from the extracted landmarks
    
*   **Customizable actions** for sign language gestures
    
*   **Live visualization** of the prediction and probabilities of detected gestures
    

Project Structure
-----------------

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   bashCopy code.  ├── action.h5                # Pre-trained model for sign language detection  ├── README.md                # Project documentation  ├── sign_language_detector.py # Main code for real-time gesture detection  └── requirements.txt         # List of required libraries   `

Dependencies
------------

To run this project, you will need the following dependencies:

*   Python 3.x
    
*   OpenCV
    
*   Mediapipe
    
*   TensorFlow
    
*   NumPy
    

You can install the necessary libraries by running:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   bashCopy codepip install -r requirements.txt   `

### requirements.txt

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   bashCopy codeopencv-python  mediapipe  tensorflow  numpy   `

How It Works
------------

1.  **Mediapipe** is used to detect **hand, face, and pose landmarks** from the webcam feed.
    
2.  The **keypoints** from these landmarks are extracted and used as input features for the **LSTM neural network**.
    
3.  The **LSTM model** predicts the sign language gesture based on the last 30 frames of keypoints.
    
4.  The system visualizes the **predicted gesture** and the **probabilities** for all defined actions on the video feed.
    

Code Explanation
----------------

### Model Architecture

The model is a sequential **LSTM neural network** with the following layers:

*   LSTM layers with 64, 128, and 64 units
    
*   Dense layers with 64 and 32 units
    
*   Softmax output layer with 9 classes representing the gestures.
    

### Gesture List

The following sign language gestures are recognized:

*   I
    
*   You
    
*   We
    
*   Are
    
*   Hello
    
*   Thank You
    
*   Sorry
    
*   What
    
*   Eat
    

### Prediction Visualization

The model outputs probabilities for each of the gestures, which are visualized as colored bars on the video feed. The most likely gesture is displayed as text on the screen.
## Results:
![Screenshot 2024-09-27 150230](https://github.com/user-attachments/assets/a653389e-9792-4595-a1e1-bd3ab453ac68)
![Screenshot 2024-09-27 15024](https://github.com/user-attachments/assets/6bf0c6d7-0945-4aa1-a533-9b734b7a6dfe)


Uploading recording.mp4…




Usage
-----

To run the project, execute the following command:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   bashCopy codepython sign_language_detector.py   `

Once the script runs:

*   **Webcam feed** will be displayed with the Mediapipe-detected hand, face, and pose landmarks.
    
*   The **predicted gesture** will appear at the top of the screen.
    
*   Use **'q'** to exit the program.
    

Results
-------

The model demonstrates the following capabilities:

*   **Accurate real-time sign language detection** using LSTM based on Mediapipe landmarks.
    
*   **Smooth visualization** of gesture predictions with a thresholding mechanism to prevent flickering between gestures.
    

Future Work
-----------

*   Incorporate **transformers** for improved sequence modeling and accuracy.
    
*   Add more **sign language gestures** to expand the gesture vocabulary.
    
*   Improve **model training** with more diverse datasets and fine-tuning techniques.
    

References
----------

*   **Mediapipe**: https://google.github.io/mediapipe/
    
*   **OpenCV**: [https://opencv.org/](https://opencv.org/)
    
*   **TensorFlow**: [https://www.tensorflow.org/](https://www.tensorflow.org/)
