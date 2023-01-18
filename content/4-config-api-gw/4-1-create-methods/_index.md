---
title : "Create methods"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---
#### Create list API
1. Click **Actions**, then select **Create method**

![CreateListAPI](/images/4-config-api-gw/4-config-api-gw-8.png?featherlight=false&width=90pc)

2. Select **GET** method

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-9.png?featherlight=false&width=90pc)

3. Click to "check" icon

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-10.png?featherlight=false&width=90pc)

4. Select **Lambda Function** for **Integration type**
- Check to **Use Lambda Proxy integration**
- Enter Lambda function name to be integrated: **books_list**
- Click **Save**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-11.png?featherlight=false&width=90pc)

5. Click **OK**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-12.png?featherlight=false&width=90pc)

#### Create write API
1. Click **Actions**, then select **Create method**

![CreateListAPI](/images/4-config-api-gw/4-config-api-gw-13.png?featherlight=false&width=90pc)

2. Select **POST** method
- Click to "check" icon

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-14.png?featherlight=false&width=90pc)

3. Select **Lambda Function** for **Integration type**
- Check to **Use Lambda Proxy integration**
- Enter Lambda function name to be integrated: **book_create**
- Click **Save**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-15.png?featherlight=false&width=90pc)

4. Click **OK**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-16.png?featherlight=false&width=90pc)

#### Create delete API

1. Click **Actions**, then select **Create Resource**

![CreateListAPI](/images/4-config-api-gw/4-config-api-gw-17.png?featherlight=false&width=90pc)

2. Enter **id** for **Resource name** pattern
- Enter **{id}** for **Resource path** pattern
- Click **Create Resource**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-18.png?featherlight=false&width=90pc)

3. Click **Actions**, then select **Create method**

![CreateListAPI](/images/4-config-api-gw/4-config-api-gw-19.png?featherlight=false&width=90pc)

4. Select method **DELETE**
- Click to "check" icon

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-20.png?featherlight=false&width=90pc)

5. Select **Lambda Function** for **Integration type**
- Check to **Use Lambda Proxy integration**
- Enter Lambda function name to be integrated: **book_delete**
- Click **Save**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-21.png?featherlight=false&width=90pc)

6. Click **OK**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-22.png?featherlight=false&width=90pc)

So, we have created the APIs that interact with Lambda functions.