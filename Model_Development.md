# Model Development
![Model Development Image](https://github.com/johnyhuang/Google-Play-Store-Rating/blob/master/Images/Model_Development_Image.png)

For reference to all the phases and steps explained in this documentation, [click here.](https://github.com/johnyhuang/Google-Play-Store-Rating/blob/master/Google%20Play%20Store.ipynb) 

## Data Acquisition Phase
This project uses the ‘googleplaystore.csv’ file obtained from Kaggle. The entire dataset contains all the relevant data with all types of unfiltered and uncleansed features of random Google Playstore applications. The following are the features contained in the dataset:
* App
* Category
* Rating
* Reviews
* Size
* Installs
* Type
* Price
* Content Rating
* Genres
* Last Updated
* Current Version
* Android Version
You can find all the raw data [here.](https://github.com/johnyhuang/Google-Play-Store-Rating/tree/master/Data)

## Data Cleansing
Data Cleansing phase includes removing all rows with missing data, transforming the sizes into a uniformed format, transforming the types into a binary format, relabeling Content Rating for easier handling, dropping features that most likely don’t affect Rating prediction, and transforming Price into a float value. 

## Feature Selection
After selecting all the necessary features to contribute to our predictions models, the dataframe looks something like this:
## Feature Encoding
Since models doesn't accept string data types, we need to convert our string data types into an acceptable format. There are 3 features which we are encoding in this section which are ‘Category, "content_rating" and Genres’. These features are categorical data and to convert them into numerical data there are several methods such as Label Encoding and One Hot Encoding.
We use **One Hot Encoding** over Label Encoding for our features because with Label Encoding the machine learning algorithm may "misinterpret" the numerical value of the encoded data so that one is more significant than the other, even though it may not be the case.
One Hot Encoding separates each unique data in our feature into a separate column. If the data corresponds to that column, then its value is one, otherwise it is 0.
For ‘Genres’ because there are several data with multiple genres such as ‘Art & Design; Pretend Play’ we encode it so that both Art & Design and Pretend Play has the value 1. 

## Train-Test-Validation Split
Here, we split the data into training, testing and validation data with a ratio of 3/5, 1/5 and 1/5. The training data is used to build the model; the testing data is then used to predict the result by running the test data through the model. The validation data is used to find the margin of error that could be possible between our predicted data and the real data.  

## Model Training
This is where we run the training data through the three model algorithms mentioned before, to get the models for each individual algorithm. So, for our X-Axis, we have our features which are ‘Category, Size, Type, Price, content_rating, and Genres’, and for our Y-Axis, we have ‘Rating’. We run all these features through our machine-learning algorithms. 

## Model Testing
After getting the model from Model Training, we test the model from training to predict the Rating given our test data.

## Model Evaluation
We compare the result from the Rating prediction to our real data – which is the validation data, for the purpose of finding the margin of errors (Mean Absolute Error, Mean Square Error, and R2 Score), to observe the accuracy and quality from the measurements of the margin of errors. This will then be plotted into a graph for visual reference.

## Save Model
The model will then be saved using Pickle, so we don’t have to re-run the data processing again. If we re-run the data processing, it could potentially result in a different model altogether.


