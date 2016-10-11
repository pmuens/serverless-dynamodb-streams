# Serverless DynamoDB streams

Serverless service to showcase DynamoDB stream support.

## Installation

Make sure that you use Serverless v1.

1. Run `serverless install --url https://github.com/pmuens/serverless-dynamodb-streams` to install the service in your current working directory
2. Next up cd into the service with `cd serverless-dynamodb-streams`
3. Run `npm install`
4. Create a new DynamoDB table called `users` with a primary partition key called `id` and enable stream support for this table
5. Update the stream ARN property in the `serverless.yml` file with the stream ARN of your `users` table
6. Deploy with `serverless deploy`

## How to use

1. Run `serverless invoke --function updateProfile --path event.json` to simulate a profile update process
2. Run `serverless logs --function logger` to see the which data has changed in the `users` table

## AWS services used

- Lambda
- DynamoDB
