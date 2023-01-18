---
title : "Cài đặt và kích hoạt CORS"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---
Trong phần này chúng ta sẽ thêm cài đặt hỗ trợ binary file và kích hoạt CORS cho API
1. Chọn **Settings** ở menu phía bên trái
- Ấn vào **Add Binary Media Type**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-23.png?featherlight=false&width=90pc)

2. Nhập **multipart/form-data**
- Ấn nút **Save Changes**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-24.png?featherlight=false&width=90pc)

3. Sau khi cài đặt xong, quay lại **Resource** ở menu bên trái.
- Chọn **/books** resource
- Ấn nút **Actions**
- Chọn **Enable CORS**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-25.png?featherlight=false&width=90pc)

4. Ấn nút **Enable CORS and replace existing CORS headers**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-26.png?featherlight=false&width=90pc)

5. Ấn nút **Yes, replace existing values**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-27.png?featherlight=false&width=90pc)

- Kích hoạt CORS cho method GET và POST thành công

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-28.png?featherlight=false&width=90pc)

6. Chọn **books/{id}** resource
- Ấn nút **Actions**
- Chọn **Enable CORS**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-29.png?featherlight=false&width=90pc)

7. Ấn nút **Enable CORS and replace existing CORS headers**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-30.png?featherlight=false&width=90pc)

8. Ấn nút **Yes, replace existing values**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-31.png?featherlight=false&width=90pc)

- Kích hoạt CORS cho method DELETE thành công

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-32.png?featherlight=false&width=90pc)

9. Để front-end có thể sử dụng API, chúng ta cần deploy chúng.
- Chọn **/** resource
- Ấn nút **Actions**
- Chọn **Deploy API**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-33.png?featherlight=false&width=90pc)

10. Chọn **New stage**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-34.png?featherlight=false&width=90pc)

11. Nhập tên cho stage, ví dụ: **staging**

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-35.png?featherlight=false&width=90pc)

12. Ghi lại URL để gọi API

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-36.png?featherlight=false&width=90pc)

- URL của API đọc và ghi:

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-37.png?featherlight=false&width=90pc)

- URL của API xoá:

![CreateRestAPI](/images/4-config-api-gw/4-config-api-gw-38.png?featherlight=false&width=90pc)