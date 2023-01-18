---
title : "Setting and enable CORS"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---
In this section, we will add binary file support settings and enable CORS for the APIs
1. Select **Settings** on the left menu.
- Click **Add Binary Media Type**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-23.png?featherlight=false&width=90pc)

2. Enter **multipart/form-data**
- Click **Save Changes**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-24.png?featherlight=false&width=90pc)

3. After the setting is done, back to **Resource** on the left menu.
- Select **/books** resource
- Click **Actions**
- Select **Enable CORS**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-25.png?featherlight=false&width=90pc)

4. Click **Enable CORS and replace existing CORS headers**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-26.png?featherlight=false&width=90pc)

5. Click **Yes, replace existing values**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-27.png?featherlight=false&width=90pc)

- Enable CORS for successful GET and POST methods

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-28.png?featherlight=false&width=90pc)

6. Select **books/{id}** resource
- Click **Actions**
- Select **Enable CORS**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-29.png?featherlight=false&width=90pc)

7. Click **Enable CORS and replace existing CORS headers**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-30.png?featherlight=false&width=90pc)

8. Click **Yes, replace existing values**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-31.png?featherlight=false&width=90pc)

- Enable CORS for successful DELETE method

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-32.png?featherlight=false&width=90pc)

9. To front-end can use APIs, we need deploy APIs.
- Select **/** resource
- Click **Actions**
- Select **Deploy API**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-33.png?featherlight=false&width=90pc)

10. Select **New stage**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-34.png?featherlight=false&width=90pc)

11. Enter stage name, such as: **staging**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-35.png?featherlight=false&width=90pc)

12. Take note URL to call API

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-36.png?featherlight=false&width=90pc)

- URL of list and write API:

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-37.png?featherlight=false&width=90pc)

- URL of delete API:

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-38.png?featherlight=false&width=90pc)