---
title : "Tạo các method"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---
#### Tạo API đọc
1. Ấn nút **Actions**, sau đó chọn **Create method**

![CreateListAPI](/images/4-config-api-gw/4-config-api-gw-8.png?featherlight=false&width=90pc)

2. Chọn method **GET**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-9.png?featherlight=false&width=90pc)

3. Ấn vào biểu tượng "check" như hình

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-10.png?featherlight=false&width=90pc)

4. Chọn **Lambda Function** cho **Integration type**
- Tích vào mục **Use Lambda Proxy integration**
- Nhập tên của Lambda function cần tích hợp: **books_list**
- Ấn nút **Save**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-11.png?featherlight=false&width=90pc)

5. Ấn nút **OK**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-12.png?featherlight=false&width=90pc)

#### Tạo API ghi
1. Ấn nút **Actions**, sau đó chọn **Create method**

![CreateListAPI](/images/4-config-api-gw/4-config-api-gw-13.png?featherlight=false&width=90pc)

2. Chọn method **POST**
- Ấn vào biểu tượng "check" như hình

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-14.png?featherlight=false&width=90pc)

3. Chọn **Lambda Function** cho **Integration type**
- Tích vào mục **Use Lambda Proxy integration**
- Nhập tên của Lambda function cần tích hợp: **book_create**
- Ấn nút **Save**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-15.png?featherlight=false&width=90pc)

4. Ấn nút **OK**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-16.png?featherlight=false&width=90pc)

#### Tạo API xoá

1. Ấn nút **Actions**, sau đó chọn **Create Resource**

![CreateListAPI](/images/4-config-api-gw/4-config-api-gw-17.png?featherlight=false&width=90pc)

2. Nhập **id** cho mục **Resource name**
- Nhập **{id}** cho mục **Resource path**
- Ấn nút **Create Resource**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-18.png?featherlight=false&width=90pc)

3. Ấn nút **Actions**, sau đó chọn **Create method**

![CreateListAPI](/images/4-config-api-gw/4-config-api-gw-19.png?featherlight=false&width=90pc)

4. Chọn method **DELETE**
- Ấn vào biểu tượng "check" như hình

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-20.png?featherlight=false&width=90pc)

5. Chọn **Lambda Function** cho **Integration type**
- Tích vào mục **Use Lambda Proxy integration**
- Nhập tên của Lambda function cần tích hợp: **book_delete**
- Ấn nút **Save**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-21.png?featherlight=false&width=90pc)

6. Ấn nút **OK**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-22.png?featherlight=false&width=90pc)

Vậy là chúng ta đã tạo xong các API tương tác với Lambda function.