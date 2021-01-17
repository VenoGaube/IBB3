# How to run the script  

##### Prerequisites

1. Download the dataset and pickle file from:

https://drive.google.com/drive/folders/1xah475_2zcMYdvg-wAEhJPRYO-uKMgfb?usp=sharing

2. Put the dataset wherever you want (remember it's location)
3. Put the pickle file named "my_classifier.pkl" into the IBB3/facenet/models folder (beside the 20170512-110547.pb file).  
  
##### As the interpreter we use Python 3.6.8, because it's compatible with the version of FaceNet and it's connected to the requirements.txt files.  
    
1.  git clone https://github.com/VenoGaube/IBB3.git  
2.  cd IBB3  
3.  pip install -r requirements.txt  
4.  python UserInterface.py  

##### Instructions for the use of the program:

After executing the command "python UserInterface.py" you will get presented by the explore files Tkinter Window.

![alt text](docs/1.%20Korak.PNG)

Pick the supplied database of images from the RHCP folder (Click RHCP so that it pops-up in the Folder: "X" input field and click "Select Folder"). It contains 40 different images, ranging from 1 face per image to multiple.


The program will then process all the images inside of the RHCP folder and display the following messages inside the Terminal.

![alt text](docs/2.%20Korak.PNG)

After creating the networks and loading the parameters it will start finding the faces within the provided images.
When it is done it will display the number of "face images".

![alt text](docs/3.%20Korak.PNG)

It will process the data and cluster the data using Chinese Whispers. When it is done clustering it will display all the images with the 
bounding boxes containing their clustered face ID. 

Here you can just press Enter or any other key to go through all the images with their assigned
cluster ID bounding boxes.

![alt text](docs/4.%20Korak.PNG)

After going through the unsupervised learning part we begin our supervised part, where the
user helps the program learn and provides it with a learning data set.

First the program displays a menu where the user can check all the created clusters with their assigned face images.
Here press the "Brose Files" button to be redirected to the menu where the clustered images are stored.
![alt text](docs/5.%20Korak.PNG)
![alt text](docs/6.%20Korak.PNG)

Go through the images and if one cluster is full of images that aren't faces or are faces of random people throw that folder away, by just selecting it and pressing "Delete".
It is really important that you delete the unneeded or false face detection folders, since the next step
will display 8 random images from each of these folders for the user to assign on their own. Mostly with this database the useful folders are 0, 1, 3 and 4. 

![alt text](docs/7.%20Korak.PNG)

Then just press the "X" or Cancel and in the Menu press "Exit".

![alt text](docs/5.%20Korak.PNG)

The program will display one image from the folder and an accompanying Input text box.
It is really important that you mark the same faces with the same name, otherwise too many
folders will be created and the program will receive wrong learning data.
In this case I've marked each of 4 different faces with the letters 'A', 'B', 'C' and 'D'.
Lower or upper case doesn't matter since the program turns all strings into upper case.


![alt text](docs/9.%20Korak.PNG)
![alt text](docs/9.%20KorakB.PNG)
![alt text](docs/9.%20KorakC.PNG)
![alt text](docs/9.%20KorakD.PNG)

After going through all the images and assigning all the faces a "name" the program
will learn from the marked images and do it's own prediction on the remaining data, displaying
the final result when finished.

![alt text](docs/10.%20Korak.PNG)
![alt text](docs/10.%20Korak2.PNG)