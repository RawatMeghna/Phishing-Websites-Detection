# Phishing Websites Detection
Build a model to find out if a website is Legitimate/Suspicious/Malicious using different machine learning algorithms and choosing the correct fit for the prediction.

The input data is already preprocessed and hence the attributes are coded into following format for application of different ML models.
 	SFH's type is nominal, range is ('1', '-1', '0')
 	popUpWidnow's type is nominal, range is ('-1', '0', '1')
 	SSLfinal_State's type is nominal, range is ('1', '-1', '0')
 	Request_URL's type is nominal, range is ('-1', '0', '1')
 	URL_of_Anchor's type is nominal, range is ('-1', '0', '1')
 	web_traffic's type is nominal, range is ('1', '0', '-1')
 	URL_Length's type is nominal, range is ('1', '-1', '0')
 	age_of_domain's type is nominal, range is ('1', '-1')
 	having_IP_Address's type is nominal, range is ('0', '1')
 	Result's type is nominal, range is ('0', '1', '-1'))

    The  data coding is as follows:
    "1"  - Legitimate Website
    "0"  - Suspicious
    "-1" - Malicious Website


**Approach for Building the model**
   - We leave the 'having_IP_Address' attribute as there is not much variation in the data while creating predictors.
   - We Experiment with different machine learning models like KNN, Random Forest, SVM, Logistic Regression to find out the best fit for the prediction
     - The result was as such :  
       <img src="https://github.com/RawatMeghna/Phishing-Websites-Detection/blob/main/res.PNG" width="250" height="250" />  
     -  Applied GridsearchCV to loop through predefined hyperparameters and fit our estimator (model) on our training set. So, in the end, we can select the best parameters from the listed hyperparameters.
   - The model is ready to predict whether or not it is a phishing website using the url of that website as its input.

 We can further deploy our model in any desired deployment platform.

