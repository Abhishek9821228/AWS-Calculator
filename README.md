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

![App Screenshot](https://d1.awsstatic.com/diagrams/Serverless_Architecture.d930970c77b382db6e0395198aacccd8a27fefb7.png)

# Step 1 - Hosting a static Website using AWS amplify

In this step, I used AWS to deploy the website without Git and Codecommit.

    1. create a Website frontend part.
    2. Deploy it on AWS Amplify.
    3. The website will be shown once deployed.


In this step we completed the website hosting using Amplify.

![App Screenshot](https://d1.awsstatic.com/diagrams/Amplify_Wild_Rydes.1760839c5336d01cd6ac6eabb5d2ad8a37c3304a.png)


# Step 2 - Now Create a AWS Lambda function.

In this step, I created Lambda function which will be getting invoked by users once they submit there calculation values. When user click on the submit then the API will invoke the Lambda and A alert messag will go to user with result.

    1. Create a lambda fucntion.
    2. Write function for it to calculate the result.
    3. Test the function.


![App Screenshot](https://d1.awsstatic.com/Test%20Images/Kate%20Test%20Images/Serverless_Web_App_LP_assets-03.1403870f0fabeb6a11d3e4116092aa6b19b6a924.png)


# Step 3 - Create DynamoDb and connect Lambda and DynamoDB by giving lambda the permission from IAM console.

In this step, I use AWS Lambda and Amazon DynamoDB to build a backend process for handling requests for web application. 

    1. Create a DynamoDB table, Make a partition key name "ID".
    2. Save the ARN of the table, because it will be used later to add it with lambda.
    3. Now create a role for the lambda fucntion. Becuase the role define what other service the lambda function is allowed to interact with.
    4. Give AWSLambdaBasicExecutionRole  policy to role and also add DynamoDB Full access policy to this role.
    5. Now create a lambda function that gets trigged when a API call is made from frontend.


![App Screenshot](https://d1.awsstatic.com/Test%20Images/Kate%20Test%20Images/Serverless_Web_App_LP_assets_04.76030d61413ff43bd6aa75fbd16e02ad23aec67a.png)


# Step 4 - Creating API Gateway.

In this step, I use Amazon API Gateway to expose the Lambda function I built in the previous module as a RESTful API. This API will be accessible on the public Internet. 

    1. Create a new RESTful API.
    2. Create a post method.
    3. Now create a resource and a post method.
    4. Select Lambda Function for the Integration type.
    5. Now reploy the API.
    6. Now a url will be genrated which will be the url to invoke the lambda function.
    7. Its done and a serverless web Application has been created.



![App Screenshot](https://d1.awsstatic.com/Test%20Images/Kate%20Test%20Images/Serverless_Web_App_LP_assets_05.d1ecdfaab160d7dc00ddbc9e0245fa34b8d8f26b.png)

# Step 4 - Integrating API Gateway with frontend.

In this step, we will create a API call function in frontend using JavaScript so that the when user click on calculate button the the lambda function can get invoked using API.

    1. Create a Call API fucntion.
    2. Use the API that get generate from API Gateway creation.


Now the full web application is completed. 

## conclusion

We create a web application using AWS Amplify, AWS Lambda, AWS API Gateway, DynamoDB, IAM and connect them together. We gets hand on experince on various AWS services and sucessfullt completed the project.
