# Sign_language_Detection_Walkthrough

This set of Notebooks provides a complete set of code to be able to train and leverage your own custom object detection model using the Tensorflow Object Detection API.

# Steps

**Step 1.**
Clone this repository:

**Step 2.**
Create a new virtual environment

```ruby 
python -m venv tfod
```

**Step 3.**
Activate your virtual environment
```ruby 
.\tfod\Scripts\activate # Windows
```
  
**Step 4.**
Install dependencies and add a virtual environment to the Python Kernel
```
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=tfod
```
**Step 5.**

Collect images using the Notebook 1. Image Collection.ipynb - ensure you change the kernel to the virtual environment as shown below 
![image](https://github.com/MadhaB3/Sign_language_Detection_Walkthrough/assets/106802789/98b38d44-ab59-4305-b53c-17065252bdd3)


**Step 6.**

Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders. \Folder_Name\Tensorflow\workspace\images\train \Folder_Name\Tensorflow\workspace\images\test

**Step 7.**

Begin training process by opening 2. Training and Detection.ipynb, this notebook will walk you through installing Tensorflow Object Detection, making detections, saving and exporting your model.

**Step 8.**

During this process, the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has been installed successfully at Step 8 with the last line stating OK. 
![image](https://github.com/MadhaB3/Sign_language_Detection_Walkthrough/assets/106802789/58da085a-42dc-4a50-bc51-c4c2f806265f)


**Step 9.**

Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics.

**Step 10.**

You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g. cd Tensorlfow/workspace/models/my_ssd_mobnet/eval and open Tensorboard with the following command tensorboard --logdir=. Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.

