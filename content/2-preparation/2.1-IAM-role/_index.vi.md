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

![IAM](/images/1/1.1.png)

---

### 2. Trong giao diện IAM Dashboard

- Chọn **Roles**
- Nhấn **Create role**

![IAM](/images/1/1.2.png?width=90pc)

---

### 3. Trong phần **Create role**, tại mục **Select trusted entity**

- Chọn **AWS Service**
- Dưới phần _Service or use case_, chọn **Lambda**
- Nhấn **Next**

![IAM](/images/1/1.3.png?width=90pc)

---

### 4. Trong phần **Add Permission**

- Tìm và chọn **AmazonS3FullAccess**

![AmazonS3FullAccess](/images/1/1.4.png?width=90pc)

- Tìm và chọn thêm **AWSLambdaServiceRole**
- Nhấn **Next**

![AWSlambdaServiceRole](/images/1/1.5.png?width=90pc)

---

### 5. Trong phần **Name, review and create**

- Đặt tên cho vai trò là `AWSlambdaServiceRoleDefault`

![AWSlambdaServiceRole](/images/1/1.6.png?width=90pc)

- Kiểm tra lại phần thông tin về **Select trusted entity** và **Add Permission**

![AWSlambdaServiceRole](/images/1/1.7.png?width=90pc)

- Nhấn **Create role**

![AWSlambdaServiceRole](/images/1/1.8.png?width=90pc)

---

### 6. Giao diện tạo vai trò thành công sẽ xuất hiện
