# Problem
To recognize Facial Expressions from Images or Videos and output the
feeling of expression (e.g., Happiness, Sadness, Neutral).
Pipeline
1. Collect the dataset and preprocess it.
2. The dataset is fed to a Convolutional Neural Network(CNN) to train
the dataset with predictions out of 7 expressions.
3. The trained model is saved in a JSON file.
4. The trained model is then used to predict the expressions from a form
of media in the web interface.
5. OpenCV is used to draw bounding boxes on particular expressions.

# The pipeline of CNN
![image](https://github.com/advit2611/Facial-Expression-Recognition/assets/47061894/4a7a2ca4-3cae-497c-ad46-9b175fdb146e)


This was created with IPython.display package.
Each input has a 48*48 pixel size image of portraits with specific
expressions. 

The model was trained for 15 epochs on my own laptop CPU.
The train and test cases were divided as
- Found 28709 train images belonging to 7 classes.
- Found 7178 test images belonging to 7 classes.
The classes were Angry, Disgust, Fear, Happy, Neutral, Sad, and Surprise.
2
The plots for accuracy and loss are as follows:
The trained model is saved in JSON file with the help of the
tensorflow.keras.model_to_json package.

# Training Graphs
![image](https://github.com/advit2611/Facial-Expression-Recognition/assets/47061894/3353331e-7d78-4662-82f2-25df0bb9beb3)


Use of OpenCV
- The OpenCV package is used to capture video or Live camera with
the help of VideoCapture class.
- The face was detected with Cascade Classifier with
'haarcascade_frontalface_default.xml'
- This is instantiated in the ‘camera.py’ python file being fed to the
‘main.py’ python file.
- The ‘main.py’ file is run to initialize the web framework Flask as the
main app.
- The output is hosted in localhost/5000.

# Results 
![image](https://github.com/advit2611/Facial-Expression-Recognition/assets/47061894/2d6fa28e-1130-4a34-a778-32ccade97304)
