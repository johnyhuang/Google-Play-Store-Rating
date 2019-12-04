# Google Playstore Rating Prediction

## Background
In this current generation, IT has become more and more prominent than it used to be before. More and more people are turning toward learning IT, more so in developing mobile applications to contribute to the outward public. Hence, mobile developers would find it very useful if they could predict how their application might turn out, in terms of user ratings from the Google Playstore, even before the launching of their own application. This is where we come in; we have solution. Based on our prediction models, we are able to figure this out for anxious mobile developers. They would just need to input the **type of their application (Free or Paid)**, **the price of their application (If Paid)**, **the genre of their application (Art & Design, Creativity, etc.)**, **Content Rating (Everyone, Teen, etc.)**, **size of their application (in bytes)** through our input dashboard.

## Getting Started
### Pre-requisites
Make sure you already have the following pre-requisites before trying to run your specified features through our input dashboard.
* Python3
* pip
* Jupyter Notebook
### Running Instructions
Follow these instructions below, step-by-step:
#### 1. Cloning/Downloading the Repository
##### Option 1: Cloning
Run the following command in your terminal to clone this repository:
```
$ git clone <https://github.com/johnyhuang/Google-Play-Store-Rating>
```
##### Option 2: Downloading
* Go to <https://github.com/johnyhuang/Google-Play-Store-Rating>
* Download the repository

#### 2. Installing the Requirements
Inside the ‘Google-Play-Store-Rating’ directory, run the following command in your terminal:
```python
pip install pandas
pip install numpy 
pip install pickle
pip install seaborn
pip install sklearn
pip install math
pip install matplotlib
```

#### 3. Running the Application
First of all, you need to make sure you're in the parent directory of the Google Play Store Rating App. Then, run the following command in your terminal to start the app:
`$ python UAS_Frontech.py`
You should see something like this in the terminal:
```
Running on http://127.0.0.1:8050/
Debugger PIN: 828-302-482
 * Serving Flask app "UAS_FronTech" (lazy loading)
 * Environment: production
   WARNING: Do not use the development server in a production environment.
   Use a production WSGI server instead.
 * Debug mode: on
```
When it appears, open your browser and go to ‘http://127.0.0.1:8050’ to access the application.

## Home Screen
The home screen will look like this:

![Web App Image](https://github.com/johnyhuang/Google-Play-Store-Rating/blob/master/Images/Web_App_Image.png)

The following will roughly define the individual functions of the input on our Dash.
### Content Rating Input
Content Rating will be comprised of a dropdown box with all the relevant options that represent content rating.
### Size of App in bytes
Size of App in bytes will have a maximum cap of 100MB. User will input the number accordingly following the estimated size of their application.
### Free of Paid
A dropdown box consisting of the options: ‘Free’ or ‘Paid’.
### Price
The price will be assumed in US dollars.
### Genre
A dropdown box consisting of all the relevant genres found in the Google Playstore.
### Category
A dropdown box consisting of all the relevant categories found in the Google Playstore.
### Predicted Range
This will show the output of the predicted Rating, based on the features input by the user, which will be processed by the three model algorithms: ‘Linear Regression’, ‘Decision Tree’, and ‘Support Vector Regression’.


## Model Development

![Model Development Image](https://github.com/johnyhuang/Google-Play-Store-Rating/blob/master/Images/Model_Development_Image.png) 

The entire process of developing the models that we use can be represented through the diagram as shown above. The models used in this project are ‘Linear Regression’, ‘Support-Vector Machine’ and ‘Decision Tree’ models. The raw code from acquiring the data, cleansing it, all the way to model evaluation can be accessed through the ‘Data’ sub-directory in this repository. If you’d like to understand more about the model development, you can check the documentation [here.](https://github.com/johnyhuang/Google-Play-Store-Rating/blob/master/Model_Development.md)

## Front-end Development

![Front End Image](https://github.com/johnyhuang/Google-Play-Store-Rating/blob/master/Images/Front_End_Image.png)

Front-end is developed using [Dash](https://github.com/johnyhuang/Google-Play-Store-Rating/blob/master/UAS_FronTech.py). There are a few components in the Dash, responsible for creating the UI shown on the image above.
* Dash Core Components
* Dash Html Components
* Dash Dependencies
#### Dash Core Components (dash_core_components)
Is responsible for the inputs such as the dropdown pane found in our dash UI. Dash Core Components can also allow Python to create a web application.
#### Dash Html Components (dash_html_components)
Is responsible for being able to write HTML syntaxes in Python.
#### Dash Dependencies (dash.dependencies)
Is responsible for handling back end processes by processing the inputs and outputs throughout the entire UI.


## Production
Once everything is done, the application is ready for usage.

### Authors
* Johny Huang
* Nicholas Chen
* Eugene Sebastian



