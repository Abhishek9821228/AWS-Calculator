# End-to-End Webaplication

## Overview
The Web application we are deploying on AWS is a Math calculator. It uses the services AWS Amplify, AWS Lambda, AWS API Gateway, DynamoDB, IAM. The User gives the input to the calculator and the application return the result.


## Architecture

The application architecture uses AWS Lambda, Amazon API Gateway, Amazon DynamoDB, and AWS Amplify Console. Amplify Console provides continuous deployment and hosting of the static web resources including HTML, CSS, JavaScript, and image files which are loaded in the user's browser. JavaScript executed in the browser sends and receives data from a public backend API built using Lambda and API Gateway. Finally, DynamoDB provides a persistence layer where data can be stored by the API's Lambda function.

AWS services used

- Amplify
- Lambda
- API Gateway
- DynamoDB
- IAM

![artitecture](https://github.com/Abhishek9821228/AWS-Calculator/assets/135989734/3a661877-c375-4074-965d-11b14ef73a2a)


# Step 1 - Hosting a static Website using AWS amplify

In this step, I used AWS to deploy the website without Git and Codecommit.

    1. create a Website frontend part.
    2. Deploy it on AWS Amplify.
    3. The website will be shown once deployed.


In this step we completed the website hosting using Amplify.

![1](https://github.com/Abhishek9821228/AWS-Calculator/assets/135989734/2c902b37-7637-4da6-a79c-5f6eaf9e5a9b)


# Step 2 - Now Create a AWS Lambda function.

In this step, I created Lambda function which will be getting invoked by users once they submit there calculation values. When user click on the submit then the API will invoke the Lambda and A alert messag will go to user with result.

    1. Create a lambda fucntion.
    2. Write function for it to calculate the result.
    3. Test the function.


![2](https://github.com/Abhishek9821228/AWS-Calculator/assets/135989734/100fa2de-f7fb-4b48-b957-03e4765bce14)

![lambda](https://github.com/Abhishek9821228/AWS-Calculator/assets/135989734/35e2c649-825b-4450-a357-4ba2db1c36fa)


# Step 3 - Create DynamoDb and connect Lambda and DynamoDB by giving lambda the permission from IAM console.

In this step, I use AWS Lambda and Amazon DynamoDB to build a backend process for handling requests for web application. 

    1. Create a DynamoDB table, Make a partition key name "ID".
    2. Save the ARN of the table, because it will be used later to add it with lambda.
    3. Now create a role for the lambda fucntion. Becuase the role define what other service the lambda function is allowed to interact with.
    4. Give AWSLambdaBasicExecutionRole  policy to role and also add DynamoDB Full access policy to this role.
    5. Now create a lambda function that gets trigged when a API call is made from frontend.


![3](https://github.com/Abhishek9821228/AWS-Calculator/assets/135989734/93e9fe44-3d60-4530-bfc9-9cda97ecd1e5)


![dynamo](https://github.com/Abhishek9821228/AWS-Calculator/assets/135989734/529d2d89-2b74-45dc-9ccd-91fcc7576d49)


![larole](https://github.com/Abhishek9821228/AWS-Calculator/assets/135989734/b76171f7-6f9e-4e8d-9c20-4bf07786615d)




# Step 4 - Creating API Gateway.

In this step, I use Amazon API Gateway to expose the Lambda function I built in the previous module as a RESTful API. This API will be accessible on the public Internet. 

    1. Create a new RESTful API.
    2. Create a post method.
    3. Now create a resource and a post method.
    4. Select Lambda Function for the Integration type.
    5. Now reploy the API.
    6. Now a url will be genrated which will be the url to invoke the lambda function.
    7. Its done and a serverless web Application has been created.



![3](https://github.com/Abhishek9821228/AWS-Calculator/assets/135989734/93e9fe44-3d60-4530-bfc9-9cda97ecd1e5)

![image](https://github.com/Abhishek9821228/AWS-Calculator/assets/135989734/5b7cc589-28e8-4a00-8552-c724478ab45b)

# Step 5 - Integrating API Gateway with frontend.

In this step, we will create a API call function in frontend using JavaScript so that the when user click on calculate button the the lambda function can get invoked using API.

    1. Create a Call API fucntion.
    2. Use the API that get generate from API Gateway creation.
    
![5](https://github.com/Abhishek9821228/AWS-Calculator/assets/135989734/720976e5-0722-411b-83cc-40d63d637c9c)

Now the full web application is completed. 



## conclusion

We create a web application using AWS Amplify, AWS Lambda, AWS API Gateway, DynamoDB, IAM and connect them together. We gets hand on experince on various AWS services and sucessfullt completed the project.
