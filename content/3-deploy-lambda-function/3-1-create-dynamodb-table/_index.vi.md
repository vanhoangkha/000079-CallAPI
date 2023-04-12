---
title : "Tạo bảng trong DynamoDB"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---
1. Mở bảng điều khiển [DynamoDB](https://ap-southeast-1.console.aws.amazon.com/dynamodbv2/home?region=ap-southeast-1#dashboard) 
2. Ấn nút **Create table**

![DynamoDBConsole](/images/3-deploy-lambda-function/3-1-create-dynamodb-table-1.png?featherlight=false&width=90pc)

3. Nhập tên cho bảng: **Books**
- Nhập parition key: `id`
- Nhập sort key: `rv_id` (review id), kiểu **Number**

![CreateTable](/images/3-deploy-lambda-function/3-1-create-dynamodb-table-2.png?featherlight=false&width=90pc)

4. Kéo xuống phần **Table settings**, chọn **Customize settings**
- Sau đó, chọn **On-demand**
- Ấn nút **Create local Index**

![CreateTable](/images/3-deploy-lambda-function/3-1-create-dynamodb-table-3.png?featherlight=false&width=90pc)

5. Nhập sort key: **name**
- Ấn nút **Create index**

![CreateTable](/images/3-deploy-lambda-function/3-1-create-dynamodb-table-4.png?featherlight=false&width=90pc)

6. Kéo xuống cuối trang, ấn nút **Create table**

![CreateTable](/images/3-deploy-lambda-function/3-1-create-dynamodb-table-5.png?featherlight=false&width=90pc)

Vậy là bạn đã tạo xong bảng **Books** với Local secondary index là **name-index**

7. Để thêm dữ liệu cho bảng, bạn có thể tải tệp dưới đây:

{{%attachments title="Data" pattern=".*\.(json)$"/%}}

8. Mở tệp, sau đó thay toàn bộ **`<AWS-REGION>`** bằng vùng mà bạn tạo S3 bucket **book-image-resize-store**, ví dụ: **ap-southeast-2**

9. Chạy câu lệnh sau tại thư mục mà bạn lưu tệp dynamoDB.json
```
aws dynamodb batch-write-item --request-items file://dynamoDB.json
```

![BooksData](/images/5-test-api-by-postman/5-test-api-by-postman-6.png?featherlight=false&width=90pc)