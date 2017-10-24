# Lambda + DynamoDB
This is an example of creating, deploying and invoking of AWS Lambda Functions which connect to a DynamoDB and get exposed through an AWS API Gateway in order to read and write data from and to the DynamoDB


## Prerequisites

* You have made you AWS access and secret key available through a provided method, like storing them in the ~/.aws/credentials file or export them into environment variables
* You need to install Node.js  with a minimum version of 6.5.0 
* Then you need to install the serverless CLI with `sudo npm install -g serverless`
* `npm install`


## Deploy

* `serverless deploy -v`


## Test

* Write: `curl -H "Content-Type: application/json" -X POST -d '{"text":"blablabalbla"}' <url>`
* Read: `curl https://3z0atjqhu5.execute-api.eu-west-1.amazonaws.com/dev/todos`


## Undeploy

* `serverless remove`

## Known Problems

* redeploy will throw an error, because table already exists. Right now I have no better solution that go to the AWS console UI and delete the table manually.