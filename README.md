### Create DynamoDB POJO for Book

### Introduction

You have recently opened a bookstore and want to keep track of all the books in the store. Each book has a unique asin,
a title, author, and a year that it was published. This is currently represented through the DynamoDB table
`DynamoDbAnnotationsLoadSave-Books`.

### Deploy the `DynamoDbAnnotationsLoadSave-Books` table

The `DynamoDbAnnotationsLoadSave-Books` table has already been [designed and implemented 
in CloudFormation](../../../../../../../../../cloudformation/BooksTable.yaml)
but it has not yet been deployed. Your first task will be to deploy the `DynamoDbAnnotationsLoadSave-Books` table to your 
AWS account and see that it is working.
 
1. Create the tables we'll be using for this activity by running these aws CLI commands from your Snippets package root:
   ```none
   aws cloudformation create-stack --region us-west-2 --stack-name dynamodbannotationsloadsave-bookstable01 --template-body file://BooksTable.yaml --capabilities CAPABILITY_IAM
   ```
1. Make sure the `aws cloudformation` command runs without error.
1. Log into your AWS account and verify that the table exists and has
   sample data.
  * You can check the status of your new CloudFormation stack at 
    https://us-west-2.console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks, which will include
    links to the resources the template defined.
 
**GOAL:** `DynamoDbAnnotationsLoadSave-Books` table is created in your AWS Account.

### Implement the `Book` class

Implement a POJO (Plain Old Java Object) class for a `Book` based on the `DynamoDbAnnotationsLoadSave-Books` DynamoDB
table. The `Book` class is currently empty, so add in the necessary fields and getters and setters. Once you have your
POJO set up, insert the appropriate DynamoDB annotations so that an item from the `DynamoDbAnnotationsLoadSave-Books`
table could be mapped to your Java class `Book`.

The `DynamoDbAnnotationsLoadSave-Books` table can be found in your AWS Console. Use the table to help you annotate
the `Book` class properly.

You can run the `dynamodb-annotations-prework` RDE workflow to verify you have implemented `Book` properly.

**You have completed this pre-work when:**
* You have implemented the `Book` class with fields matching the attributes you see in the
  `DynamoDbAnnotationsLoadSave-Books` table in DynamoDB.
* You have added the correct DynamoDB annotations to the `Book` class.
* You have committed and pushed your code.
* You have answered the Canvas quiz with a link to your commit on code browser.


