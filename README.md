# LambdaFunction-HelloWorld
![image](https://github.com/shaikshaz/LambdaFunction-HelloWorld/assets/154241222/0f6074d8-d550-4b3f-82cb-a2294ecb9f6e)


SITUATION: To write a lambda function for “Hello World” and to understand what a Lambda function is and what are the dependencies and how it works in backend.

TASK: To create a serverless lambda function and to run code without provisioning or managing servers using python runtime in the environment in response to events and to check the output logs with CloudWatch.

ACTION: There are two ways to create a lambda function :
1.Using AWS lambda console (no dependencies required)
2.Lambda deployment package (when there are external dependencies)-Like uploading all files in with dependencies into the zip folder and then to lambda console.(Ex.S3)

-We need to login in to the lambda console and create a new lambda-sample.
-Select the Runtime: which is the language used to write the lambda function code -python 3.9.
-Permission should be given like to read and write data by attaching the IAM role which has all those permissions with an existing role and can also create a new role depends upon the kind of function we write.
-Here I have given to create a new role which create a basic IAM role to run the lambda function and to create logs in CloudWatch and it gets attached to lambda function .
-Test is to run any sample lambda function and can create an event to run it and when we trigger the lambda it function will pass through the ‘event’ variable.
-Can also give configurations like timeout time etc.
-When ever we trigger a lambda function it goes to the lambda_handler which runs the main function.
-Write data in print (“Hello World”) and run ,we can also pass test events: Print(event),deploy to save changes and can pass anything in Key-value and Test.
import json

def lambda_handler(event, context):
    print(event)
    print("Hello World")

RESULT : The even we passed goes through the lamnda_handler ‘event’ variable and the result is displayed as in Execution Results in function logs printed as “Hello World”.
-In the monitor section we can also see logs through CloudWatch which we gave access for .
-Can also create alarms for logs.
