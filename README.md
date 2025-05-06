References:

1. Teachable Machine (https://teachablemachine.withgoogle.com/)

2. PySerial Documentation (https://pyserial.readthedocs.io/en/latest/)

3, TensorFlow Documentation (https://www.tensorflow.org/)

4. Arduino Documentation (https://docs.arduino.cc/)

5. Source Code Documentation (https://github.com/harshitroy2605/2_level_security_arduini-python/tree/master and https://www.youtube.com/watch?v=x1D7QbnZIGU)

 Source code based off Arduino Set-Up Code and Python Serial coding. Free use and modification with expressed written and verbal consent of developers..

Downloads:

Apps:

1. Arduino IDE 2.3.4 Application
2. Python 3.12 fitting your operating system (I have a Windows 11 64-bit with an Intel I5 processor)
3. Visual Studio Code, or use your own compiler

Supports and Imports from PIPy:

1. OpenCV/Keras
2. TensorFlow
3. NumPy
4. OS
5. Face Recognition (all latest as of time of posting)

Hardware: 

Arduino Mega 2560 Kit

Procedures:

Step 1 Creating a Visual Model

1. Log on to Teachable Machine
2. Create Visual Model
3. Create two classes
4. Class 1 can involve a mixture of webcam and file uploads of a man wearing a hat or woman wearing accessories (16 Images)
5. Class 2 can involve bare face and combed hair, without cap or accessories. (16 images).
6 Once classes are created, click train model and preview function.
7. Download model files compatable with OpenCV/Keras and save to project documents. Open in Visual Studio.
8. Copy created TenorFlow program into Visual Studio into created application, and make sure it is compatable with Python and not Java. Upload into started Application and save in project documents.

Step 2 Setting up Aduino Hardware from kit

1. Locate and grab the 4 by 4 digit keypad and grab it.
2. Locate the Blue USB Cable and Arudino Uno Board and grab them
3. Collect 8 colored connector wires from the kit
4. Plug the USB cable into the Arudino Uno and the USB 2.0 jack into your computer
5. Use the 8 wires to connect the Arudino Uno to the Keypad. Connect the end port closest to hashtag into Port 2 on the Arduino, and connect port closest to star into port 9. Connect ports 3-8 on the Arduino to the remaining 6 ports in the Keypad.

Step 3 Setting up Arduino IDE and entering code

1. Access Keypad library and download the appropriate 4 x 4 keypad setup matching arduino hardware keys. It should be keypad.h. This should be found in the example menu under file. Go to keypad, and select "custom keypad".
2. Go to Port menu in tools. Select and connect to the appropriate "COM" port. It should be COM3 in this case.
3. Using any appropriate and researched source code and setup coding from class, begin entering Arduino C++ coding reflecting the dimensions and paramaters of the Arduino Mega 2560 keypad.
4. Save it. I saved mine as KeypadSetipArduinoCode.

Step 4 Entering and modifying Python Serial coding, and then setting up Tensorflow.

1. Enter "serial", "time", "face_recognition", "cv2", "numpy", and "os" as imports
2. Using class and/or researched source code as needed, enter the python code into the Visual Studio compiler. I saved mine as ImportSerial.py.
3. Modify the code in line 8 to reflect the correct port name and baud rate. In this case, it should be "COM3" and "9600"
4. Define the main function in lines 13 and 14 to reflect entering the correct password. print("correct password")
5. Modify line 40 to reflect custom, 3-digit passcode.
6. Snap a photograph with your webcam. Save it as "One.jpg". Enter it into line 50 where it says "load image file".
7. Earlier, a model was created on Teachable Machine named "keras_model.h5". Keras compatible code, saved as TensorFlow.py, should have been generated and saved by Teachable Machine. Open "keras_model.h5", "TensorFlow.py". and "labels.txt" in Visual Studio Code.

Step 5 Test the System

1. Verify your sketch on Arduino, and upload it.
2. Run the ImportSerial.py program with webcam running.
3. Check for bugs, error, and Python-Arduino connection issues.
4. It if runs, without issue, follow the instructions and enter necessary input.

Step 6 Trouble Shooting

1. When I run my application, the Arduino sketch uploads and runs.
2. When I run the ImportSerial.py program, it shows some issues. 1) Import face_recogniton is sometimes recognized and resolved to a variable, and sometimes it cuts out. 2) Keras.models import from TensorFlow.py program is not resolved.
3. I was and am under the impression that the .jpg file was supposed to work in conjunction with the keras.models. Some modification to Face_Recognition starting at line 50 will need to be made.
