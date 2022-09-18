# Wildfire Detection Project
In this project, we created a U-net deep learning model that takes any satellite imagery and detects the wildfire burning scar. <br/>
The model is trained on Databricks, and the application is deployed on Streamlit. <br/>

### Content of this document
  * [Installation](#Installation)
  * [Inspiration](#Inspiration)
  * [What-it-does](#What-it-does)

### Installation 
Clone this repo and direct to the `./app` folder. <br/>
- **Method :** Run with Python IDE<br/>
Go to the folder`/app` and then in your terminal please type the following code: <br/>
`streamlit run app.py` <br/>
Please make sure you have the dependency installed is the same as listed in the "requirement.txt"


Here is what the application looks like:<br/>
<p align="center">
  <img width="600" height="600" src="https://github.com/yueureka/WildFireDetection/blob/master/Pictures/App2.png">
</p>

After deployed the model, click "browse file" button to add the image you want to predict (we have provided some test images in the 'test_image' folder for you to test), the image needs to be in `"*.PNG"` format, the app will then automatically draw the raw image, burning scar probability picutre and the predicted burning scar mask. <br/>
You may also change the "type of forest" dropdown menu and "image resoltion" to check the burnt area and CO2 emission.  


### Inspiration 
Wildfire has become one of the most devastating disasters that not only causes huge loss to human lives and properties, but also emits enormous CO2 into the environment. The 2018 California Camp fire alone has caused $16.5billion loss and emitted a year’s worth of power pollution. 

Currently, there’re over a thousand of earth observation(EO) satellites that orbiting us, however, only less than 10 of them can monitor wildfire, such as Sentinel and Landsat. These satellites either only track small portion of the land, or require extensive specialties and dedicated preprocessing skills to process, which greatly limit the capability to real time monitor the wildfire across the globe. Therefore, it's important to find a way that may utilize many more of the EO satellite imagery and imporve the effectiveness of wildfire monitoring.

With the increasing development of deep learning technologies, convolutional neural network (CNN) has become one of the most powerful tool in image processing. In this work, we trained a U-net based CNN deep learning model on Databricks, it takes raw imagery from different satellites as the input, and is able to quickly detect the wildfire and monitor the burning scar. 

### What-it-does
This is a user-friendly application. It takes imagery from different satellites resources as input, and then quickly predicts the forest fire probability and segments the burning scar zones.

In addition, given the image resolution and the forest type, it can calculate the total area of the burnt zone of a wildfire, and estimate the total CO2 emission from this fire.

