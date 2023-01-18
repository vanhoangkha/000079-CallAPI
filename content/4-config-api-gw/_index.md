---
title : "Config API Gateway"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 4. </b> "
---
Next, we'll set up the API Gateway to interact with the Lambda functions created in the previous section:
1. Open [API Gateway console](https://ap-southeast-2.console.aws.amazon.com/apigateway/main/apis?region=ap-southeast-2)

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-1.png?featherlight=false&width=90pc)

2. Scroll down and click **Build** of **REST API** pattern

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-2.png?featherlight=false&width=90pc)

3. Click **OK**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-3.png?featherlight=false&width=90pc)

4. Select **REST** for **Protocol**
- Select **New API** to create a new API
- Enter REST API name, such as: **fcj-serverless-api**
- Click **Create API**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-4.png?featherlight=false&width=90pc)

5. Click on the API just created

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-5.png?featherlight=false&width=90pc)

6. Click **Actions**, then select **Create resource**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-6.png?featherlight=false&width=90pc)

7. Enter resource name, such as: **books**
- Then click **Create Resource**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-7.png?featherlight=false&width=90pc)

So we have created a new REST API and resource for it. Next, we will create methods to interact with Lambda functions and set them:
1. [Create methods](4-1-create-methods/)
2. [Setting and enable CORS](4-2-setting-and-cors/)

