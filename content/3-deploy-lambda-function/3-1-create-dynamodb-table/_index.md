---
title : "Create DynamoDB table"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---
1. Open [DynamoDB console](https://ap-southeast-1.console.aws.amazon.com/dynamodbv2/home?region=ap-southeast-1#dashboard) 
2. Click **Create table**

![DynamoDBConsole](/images/3-deploy-lambda-function/3-1-create-dynamodb-table-1.png?featherlight=false&width=90pc)

3. Enter table name: **Books**
- Enter parition key: `id`
- Enter sort key: `rv_id` (review id), type is **Number**

![CreateTable](/images/3-deploy-lambda-function/3-1-create-dynamodb-table-2.png?featherlight=false&width=90pc)

4. Scroll down to **Table settings** pattern, select **Customize settings**
- Then, select **On-demand**
- Click **Create local Index**

![CreateTable](/images/3-deploy-lambda-function/3-1-create-dynamodb-table-3.png?featherlight=false&width=90pc)

5. Enter sort key: **name**
- Click **Create index**

![CreateTable](/images/3-deploy-lambda-function/3-1-create-dynamodb-table-4.png?featherlight=false&width=90pc)

6. Scroll down to the bottom, click **Create table**

![CreateTable](/images/3-deploy-lambda-function/3-1-create-dynamodb-table-5.png?featherlight=false&width=90pc)

So we have created the **Books** table with the Local secondary index of **name-index**

7. To add data to the table, you can download the file below:

{{%attachments title="Data" pattern=".*\.(json)$"/%}}

8. Open this file, replace all **`<AWS-REGION>`** with the region where you created the S3 **book-image-resize-store** bucket, for example: **ap-southeast-2**

9. Run the following command in the directory where you save the dynamoDB.json
```
aws dynamodb batch-write-item --request-items file://dynamoDB.json
```

![BooksData](/images/5-test-api-by-postman/5-test-api-by-postman-6.png?featherlight=false&width=90pc)