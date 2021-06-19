# PROJECT EXECUTION

## Description Of The Project Coding And Implementation


### A.Libraries And Packages Required In This Project





### Step 1 :

Firstly, we will import the following modules in our coding : 


![Step 1](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/modules.JPG)


- cv2           = to use OpenCV to process the image
- easygui       = it will allows us to select an image from system
- numpy as np   = to save image and processed it as numbers
- imageio       = to read image stored in specific path
- sys           = to run functions and anything else defined within the module using the module name
- matplotlin    = for visualization and image plotting
- os            = to read and save image 
- tkinter as tk = for tk interface




### Step 2 :

![Step 2](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/1.JPG)

We create the main window with label(title of the project) on top of the window. 
**windows.resizable(False,False)** method is used to create a fixed size for main window.






### Step 3 :

![Step 3](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%203.JPG)

In this step, we will build the button for upload image and label for image name to be converted. This step will opens the file box, it will pop-up so we can choose an image from our device and it will pop-up everytime we run the code. Function  fileopenbox() is the method in easyGUI module which return the path of the chosen image as a string to process it later.





### Step 4 :

![Step 4](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%204.JPG)

covert(UploadImage) are function to read the chosen image. We will convert the image into a numpy array. imread is a method in cv2 which is used to store the image in the form of numbers and it can help us to perform the operations for this project. **OriginalPicture=cv2.cvtColor(OriginalPicture, cv2.COLOR_BGR2RGB)** command is for the image to be convert from bgr > rbg to save the image correctly after being converted into codes.

Then we add command if to check if the picture is uploaded or not. Before the process start, we will resize the uploaded image first so it can display on a similar scale on main window.





### Step 5 :

![Step 5](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%205.JPG)

Here our first step of the process, we will convert the image into grayscale image by BGR2GRAY. This will returns the image in grayscale. A grayscale image will be store as GrayScalePic.

![Figure 1](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%205.2.JPG)
               **Figure 1**

After each transformation, we will resize the resultant image using resize() method in cv2 and display the image using **plot.imshow()** method. This method is done so we will get more clear insights into every single transformation during the whole process like **Figure 1**.





### Step 6 :

![Step 6](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%206.JPG)

This transformation is to smoothen an image and apply a blur effect. This is done using medianBlur() function in method cv2. During this transformation process, the center pixel is assigned a mean value of all the pixels. In turn, creating a blur effect. 





### Step7 :

![Step 7](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%207.JPG)

In this step, we will retrieve the image edges and highlight them. This step is done by adaptiveThreshold function or technique in method cv2. The threshold value is the mean of the neighborhood pixel values area minus the constant C. Constant C is subtracted from the mean or weighted sum of the neighborhood pixels. Thresh_binary is the type pf threshold applied.

![Figure 2](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%207.2.JPG)
**Figure 2**

**Figure 2** shows example of using adaptiveThreshold() function in step 7.





### Step 8 :

![Step 8](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%208.JPG)


We use bilateralFilter() function to remove the noise in the image. It can be taken as smoothening of an image to an extent.

This step is a step where we beautify the image similar with AI effect in cameras of modern device.





### Step 9 :

![Step 9](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%209.JPG)


In this step, it will be done using MASKING. We perform bitwise_and on the image. Images are just number and that's how we mask the edged image on our cartoonify image. This finally will convert original image into cartoonify image!





### Step 10 :

![Step 10](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%2010.JPG)

To plot all images for each transformation in this process, we will make a list of all the images first. The list will be named **images** and contains all the images that has been resized after each transformation. Then, we create axes like sublplots in a plot and siplay one-one image in each blocks on the axis using imshow() function that we used during the transformations.


![Step 10.2](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%2010.2.JPG)
**Figure 3**

**Figure 3** shows of how subplots works after the process.






### Step 11 :

![Step 11](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%2011.JPG)


Above code makes save buttons after the process of transform an image into cartoon is done. For save button, we can choose either we want to save the cartoonified image only or the sketch image only but we can also save both image if we want!  

![Step 11.2](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/11.2.JPG)
**Figure 4**

**Figure 4** shows the save buttons on main window.





### Step 12 :

![Step 12.1](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/12.JPG)
Step 12.1

![Step 12.2](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%20122.JPG)
Step 12.2



In step 12, we will display the original image, the cartoonified image and the skecthed image on main window with label on top of each image.
So that, we can see the preview of before(original image) and after(sketched & cartonified image) the process of transformation.


![Step 12.3](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%2012.2.JPG)
**Figure 5**

**Figure 5** shows the preview of the images and the label on top of the images.




### Step 13 :

![Step 13](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%2014.JPG)


Step 13 is the iea to save the resultant image. To save the image, we take the original image's location. 
**os.path.dirname()** method will be use to save the resultant image in the same file as original image.
**os.path.splitext(UploadImage)[1]** is used to extract the extension of the file from the path.


**newName = simpledialog.askstring("", "", parent=windows)** method will display a new window for us to enter new name if we want to save the resultant image.
**path1 = os.path.join(path, newName+extension)** method will save the resultant image with the name that we just enter just now.



![Step 13.2](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%2014.2.JPG)
**Figure 6**

**Figure 6** shows the window that will poo-up right after we click the save image button, then we will enter new name for the image that we want to save.




### Step 14 :

![Step 14](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%2015.JPG)

This step is to make the upload button in the main window like **Figure 7** below.

![Figure 7](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%2015.2.JPG)
**Figure 7**




### Step 15 :

![Step 15](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Step%2016.JPG)

This is the last step for this process. In this step we create the main function to build the tkinter window.


### B. Project Result

![Start](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Start.JPG)
**Figure 8**


**Figure 8** shows the main window before we upload image.


![Final](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/Step/Finall.JPG)
**Figure 9**


**Figure 9** shows the final main window after the process cartonify image is finish.




**Next :** [Project Closing](https://github.com/AfzaAdaw/Artificial-Intelligence-Project/blob/main/Documentation/E-ProjectClosing.md)
