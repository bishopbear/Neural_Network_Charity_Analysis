# Neural_Network_Charity_Analysis
Overview of the analysis: 
Our client, Alphabet Soup, is a philanthropic organziation dedicated to helping organziations that protect the environment, improve people's well-being, and unify the world. Alphabet Soup has raised and donated over 10 billion dollars over the past 20 years. This money has been used to invest in life-saving technologies and organize reforestation groups around the world. We are in charge of data collection and analysis for the entire organization. Ultimately we are tring to help analyze the impact of each donation and vet potential recipients. This helps ensure that the foundations money is being used effectively. Our job is to predict which organzations are worth donating to and which are too high risk. We are creating a mathematical data driven solution that can do this accurately.

We will design and train a deep learning neural network that will evaluate all types of input data and hopefully produce a clear decision making result.

Results: Using bulleted lists and images to support your answers, address the following questions.

Data Preprocessing
Our target variable is the column "IS_SUCCESSFUL"

Our feature data is as follows:

APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT
   

We have identified three pieces of data that we will not consider and will drop. 

Those are:

EIN, NAME, SPECIAL_CONSIDERATION




Compiling, Training, and Evaluating the Model

First attempt:
![first attempt](https://user-images.githubusercontent.com/58608736/153778176-07ada407-6f73-42eb-b2de-0bde5c31a077.PNG)
![fa result](https://user-images.githubusercontent.com/58608736/153778205-82c0394e-d3e7-496f-8229-1771ebcf258c.PNG)

2 hidden layers

10 and 5 nodes

100 epochs

relu and sigmoid activation

This is a decent first attempt. We used these model characteristics because they had been successful on other datasets.


Second attempt:
![fa test 2](https://user-images.githubusercontent.com/58608736/153778495-70e2cc56-98f9-4398-88b6-9348213f66b0.PNG)
![fa result 2](https://user-images.githubusercontent.com/58608736/153778500-92e33f24-ecef-472e-a33f-10736118e5eb.PNG)


2 hidden layers

increase node amount to 100 and 50

100 epochs

relu and sigmoid activation

No real positive change here. In fact, our loss increased, which is not ideal.

Third attempt:
![ta test relu](https://user-images.githubusercontent.com/58608736/153780471-bba1c9a7-2a48-4777-af95-a5c50316927f.PNG)
![ta result](https://user-images.githubusercontent.com/58608736/153780479-5437eb5f-571b-46ec-81a6-4ea3680453e5.PNG)


3 hidden layers

increase node amount to 1000, 500 and 300

increase epoch to 200 from 100

only relu activation

We can see that things got much worse by only using relu.

Fourth attempt:
![fa test](https://user-images.githubusercontent.com/58608736/153780545-7785af4f-67c4-4ef9-a789-99c51b562497.PNG)
![la result](https://user-images.githubusercontent.com/58608736/153780670-ac245bce-a2ee-40fb-b825-0fb4362c9be7.PNG)


3 hidden layers

nodes set at 1000, 500 and 300

epoch set at 200

relu and sigmoid activation


Summary:
Currently our test is not meeting our success threshold of at least 75%. We have tried different variations of the model to no avail. At this point we need to go back to the data and take a look again at our features and possibly bin some of the features or drop some of the features. We recommend this because we have soon almost no improvement after several variations of our neural network setup.
