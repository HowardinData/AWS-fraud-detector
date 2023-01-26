# For all your Fraud Solutions: Amazon Fraud Detector


One problem with traditional fraud detection techniques is that they often rely on fixed business rules that can be easily evaded by savvy fraudsters. Amazon Fraud Detector is a fully managed service that uses machine learning to automatically identify potentially fraudulent activities online. This service builds on Amazon's 20 years of fraud detection expertise and allows users to quickly and easily build customized fraud detection models with no prior machine learning experience. Amazon Fraud Detector can even detect fraud in real-time, such as new account fraud and loyalty program abuse. With this service, businesses can effectively combat fraud and keep their operations running smoothly


For this project, we trained a model on Amazon Fraud detector and ran it through some test data coming through a custom-built website. 

<h2>How it works</h2>

1.	Upload your training data on to S3
2.	Amazon fraud detector will pull your data set from s3 and run it through their automated machine learning pipeline that has been built specifically for fraud detection
3.	The output from the above process is the customized machine learning model based on the uploaded data set and enriched data that was used through the automated model building process
4.	Take the model at that point, and add it to a detector and combine it with appropriate rules that are most important
5.	Publish the detector and use the Fraud Detector Prediction API to send new events to get scores using custom detection logic

![image](https://media.github.umn.edu/user/24709/files/aa29b5bc-52cc-4e7e-842c-a8c5272c5705)

Amazon Fraud detector takes care of all the heavy lifting like Data Validation, Data Enrichment and transformation (e.g. adding geo location data to IP addresses) and feature engineering based on Amazon’s research and ML experts. 
After picking the best performing model out of a series of models that have been trained, the pipeline outputs a trained model  that can be deployed in the application of your choice

![image](https://media.github.umn.edu/user/24709/files/5a491311-5e52-475c-a845-e6f334b962db)


<h2>Use Cases</h2>
<h3>Identify suspicious online payments</h3>
Reduce online payment fraud by flagging suspicious online payment transactions before processing payments and fulfilling orders.
<h3>Detect new account fraud</h3>
Accurately distinguish between legitimate and high-risk account registrations so you can selectively introduce additional checks—such as phone or email verification.
<h3>Prevent trial and loyalty program abuse</h3>
Spot accounts likely to abuse online services and set appropriate limits on the value of offers to minimize risk.
<h3>Improve account takeover detection</h3>
Easily embed in real-time account login flow to detect accounts that have been compromised while minimizing friction for legitimate users.

<h2>Success Stories</h2>

![image](https://media.github.umn.edu/user/24709/files/6ab90844-bbc6-41cd-a484-6137e09cba8e)


<h2>Creating the Detector</h2>

1.	Sign up for an Amazon Web Services (AWS) account, if you don't already have one.
2.	Go to the Amazon Fraud Detector page on the AWS website and click on the "Get started" button.
3.	Click on Build Model
4.	Create Model
5.	Give the model a name (and an optional description)
6.	Choose the model template
7.	Supply the training data source and location on s3
8.	You can include custom variables to improve the performance of the model further
9.	Specify the labels for Fraud and legitimate transactions
10.	Review the configuration and kick off the model training
11.	Deploy the model 
12.	Click on the Create detector button
13.	Add your model into the detector
14.	Set business rules for your outcome prediction
15.	Review the configuration and published your detector

If you want to connect your local computer to amazon fraud detector, follow the steps in the article to get your credentials: https://towardsdatascience.com/how-to-connect-with-jupyter-server-running-on-aws-ec2-efa309f47c51 <br><br>
After finishing setting credentials, you can connect amazon fraud detector through "import boto3" in your jupyter notebook.







