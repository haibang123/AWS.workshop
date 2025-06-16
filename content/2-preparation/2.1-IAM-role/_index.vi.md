+++
title = "Tạo Vai Trò IAM"
weight = 1
chapter = false
pre = "<b>2.1. </b>"
+++

## Tạo Vai Trò IAM

Trong bước này, bạn sẽ truy cập vào giao diện IAM Console và tạo một vai trò dành cho dịch vụ Lambda. Vai trò này sẽ cho phép AWS Lambda truy cập dữ liệu từ S3 và thực hiện các thao tác cần thiết.

---

### 1. Truy cập [AWS Management Console](https://aws.amazon.com/console/)

- Tìm kiếm từ khóa **IAM**
- Chọn **IAM** để mở trang **IAM Dashboard**


   ![ConnectPrivate](../../../images/1/1.1.png)

   
### 2. Trong giao diện IAM Dashboard

- Chọn **Roles**
- Nhấn **Create role**


   ![ConnectPrivate](../../../images/1/1.2.png)


### 3. Trong phần **Create role**, tại mục **Select trusted entity**

- Chọn **AWS Service**
- Dưới phần _Service or use case_, chọn **Lambda**
- Nhấn **Next**


   ![ConnectPrivate](../../../images/1/1.3.png)

### 4. Trong phần **Add Permission**

- Tìm và chọn **AmazonS3FullAccess**


   ![ConnectPrivate](../../../images/1/1.4.png)

- Tìm và chọn thêm **AWSLambdaServiceRole**
- Nhấn **Next**


   ![ConnectPrivate](../../../images/1/1.5.png)

---

### 5. Trong phần **Name, review and create**

- Đặt tên cho vai trò là `AWSlambdaServiceRoleDefault`


   ![ConnectPrivate](../../../images/1/1.6.png)

- Kiểm tra lại phần thông tin về **Select trusted entity** và **Add Permission**


   ![ConnectPrivate](../../../images/1/1.7.png)

- Nhấn **Create role**


   ![ConnectPrivate](../../../images/1/1.8.png)

---

### 6. Giao diện tạo vai trò thành công sẽ xuất hiện
