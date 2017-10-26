# Lambda + DynamoDB
This is an example of creating, deploying and invoking of AWS Lambda Functions which connect to a DynamoDB and get exposed through an AWS API Gateway in order to read and write data from and to the DynamoDB which is also supported for offline mode.


## Prerequisites

* You have made you AWS access and secret key available through a provided method, like storing them in the ~/.aws/credentials file or export them into environment variables
* You need to install Node.js  with a minimum version of 6.5.0 
* Then you need to install the serverless CLI with `sudo npm install -g serverless`
* `npm install`
* `serverless dynamodb install`


## Start locally

* **NOTE**: You need to have a Java Runtime installed for DynamoDB to work locally
* `serverless offline start `


## Deploy

* `serverless deploy -v`


## Test

* Write: `curl -H "Content-Type: application/json" -X POST -d '{"text":"blablabalbla"}' <url>`
* Read: `curl <url>`
* If you run it locally the url is: http://localhost:3000/todos


## Undeploy

* `serverless remove`
