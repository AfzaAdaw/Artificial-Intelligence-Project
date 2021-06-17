# PROJECT EXECUTION

## Description Of The Project Coding And Implementation


### A.Libraries And Packages Required In This Project

**Step 1 :**

Firstly, we will import the following modules in our coding : 


![Step 1](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/modules.JPG)


- cv2           = to use OpenCV to process the image
- easygui       = it will allows us to select an image from system
- numpy as np   = to save image and processed it as numbers
- imageio       = to read image stored in specific path
- sys           = to run functions and anything else defined within the module using the module name
- matplotlin    = for visualization and image plotting
- os            = to read and save image 
- tkinter as tk = for tk interface


**Step 2 :**

![Step 2](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/gui%20screen.JPG)

We create the main window with label(title of the project) on top of the window.


**Step 3 :**

![Step 3](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step%203.JPG)

In this step, we will build the button for upload image and label for image name to be converted. This step will opens the file box, it will pop-up so we can choose an image from our device and it will pop-up everytime we run the code. Function  fileopenbox() is the method in easyGUI module which return the path of the chosen image as a string to process it later.

**Step 4 :**

![Step 4](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step%204.JPG)

covert(UploadImage) are function to read the chosen image. We will convert the image into a numpy array. imread is a method in cv2 which is used to store the image in the form of numbers and it can help us to perform the operations for this project. **OriginalPicture=cv2.cvtColor(OriginalPicture, cv2.COLOR_BGR2RGB)** command is for the image to be convert from bgr > rbg to save the image correctly after being converted into codes.
