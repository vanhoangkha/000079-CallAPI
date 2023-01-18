---
title : "Kiểm tra API với Postman"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 5. </b> "
---
Trong bước này, chúng ta sẽ kiểm tra hoạt động của các API bằng công cụ [Postman](https://www.postman.com/downloads/)
#### Kiểm tra API đọc
1. Ấn vào dấu **+** để thêm 1 tab mới
- Chọn **GET** method
- Nhập URL của API đọc đã ghi lại từ bước trước
- Ấn nút **Send**

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-1.png?featherlight=false&width=90pc)

2. Kết quả trả về là toàn bộ dữ liệu của bảng **Books** đã qua xử lý

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-2.png?featherlight=false&width=90pc)

#### Kiểm tra API ghi
1. Tương tự tạo một tab mới
- Chọn **POST** method
- Nhập URL của API ghi đã ghi lại từ bước trước
- Trong mục **Body**, chọn **raw**
- Sao chép đoạn dưới đây:
```
{
    "id": "5",
    "rv_id": 0,
    "name": "Learning DevOps",
    "author": "Mikeal Krief",
    "price": "14.95",
    "category": "IT",
    "description": "The complete guide to accelerate collaboration with Jenkins, Kubernetes, Terraform and Azure DevOps",
    "image": "https://book-image-resize-store.s3.<AWS-REGION>.amazonaws.com/LearningDevOps.jpeg"
}
```
- Thay **<AWS-REGION>** bằng vùng mà bạn tạo S3 bucket **book-image-resize-store**, ví dụ: **ap-southeast-2**

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-4.png?featherlight=false&width=90pc)

2. Chuyển sang mục **Headers**
- Thêm KEY là **Content-Type**, VALUE là **application/json**
- Ấn nút **Send**

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-5.png?featherlight=false&width=90pc)

3. Đợi một chút, xem kết quả trả về

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-6.png?featherlight=false&width=90pc)

4. Mở bảng **Books** trong bảng điều khiển của DynamoDB kiểm tra dữ liệu
- Trước khi gọi API ghi

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-3.png?featherlight=false&width=90pc)

- Sau khi gọi API ghi

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-7.png?featherlight=false&width=90pc)

#### Kiểm tra API xoá
Vì Lambda function xoá khi thực hiện sẽ xoá ảnh được tải lên bởi người dùng, nên chúng ta tải thủ công ảnh lên S3 bucket để API có thể chạy đúng.
1. Mở bảng điều khiển của [Amazon S3](https://s3.console.aws.amazon.com/s3/buckets?region=ap-southeast-2&region=ap-southeast-2)
2. Ấn vào bucket **book-image-store** 

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-8.png?featherlight=false&width=90pc)

3. Ấn nút **Upload**

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-9.png?featherlight=false&width=90pc)

4. Ấn nút **Add files**

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-10.png?featherlight=false&width=90pc)

5. Tải ảnh sau về máy của bạn và chọn nó để tải lên bucket

{{%attachments title="Image" pattern=".*\.(jpeg)$"/%}}
6. Ấn nút **Upload**

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-11.png?featherlight=false&width=90pc)

7. Sau khi tải xong, chuyển sang bucket **book-image-resize-store** kiểm tra. Đây là kết quả chạy của reszie_image Lambda funtion

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-12.png?featherlight=false&width=90pc)

8. Trở lại với Postman, thêm một tab mới để thực hiện API xoá
- Chọn **GET** method
- Nhập URL của API xoá dữ liệu đã ghi lại từ bước trước, thay **/{id}** bằng **/5**
- Ấn nút **Send**

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-13.png?featherlight=false&width=90pc)

9. Kiểm tra kết quả trả về:

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-14.png?featherlight=false&width=90pc)

10. Mở bảng **Books** trong bảng điều khiển của DynamoDB kiểm tra dữ liệu

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-15.png?featherlight=false&width=90pc)

11. Mở bucket **book-image-resize-store** kiểm tra kết quả. Ảnh **LearningDevOps.jpeg** đã xoá.

![TestListAPI](/images/5-test-api-by-postman/5-test-api-by-postman-16.png?featherlight=false&width=90pc)



