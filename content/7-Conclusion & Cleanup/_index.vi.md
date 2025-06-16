+++
title = "Dọn Dẹp Tài Nguyên"
date = 2021-06-08T18:57:03+07:00
weight = 7
chapter = false
pre = "<b>7. </b>"
+++

## Dọn Dẹp Tài Nguyên

Chúng ta sẽ tiến hành dọn dẹp các tài nguyên đã tạo sau khi hoàn thành workshop.

---

#### **Các bước dọn dẹp tài nguyên**:

1. **Xóa bảng DynamoDB tên "Posts"**

  ![ConnectPrivate](../../images/7/7.1.png)
  ![ConnectPrivate](../../images/7/7.2.png)

2. **Xóa bảng DynamoDB "audioposts-161123"**

![clean](../../images/7/delete_dynamodb.png?width=90pc)

3. **Xóa dịch vụ SNS**

  ![ConnectPrivate](../../images/7/7.3.png)

   - **Xóa chủ đề (topic) SNS**

  ![ConnectPrivate](../../images/7/7.4.png)

4. **Xóa hàm Lambda**

   - Chọn **Action**
   - Chọn **Delete**

   ![ConnectPrivate](../../images/7/7.5.png)

   - Chọn **Confirm**

  ![ConnectPrivate](../../images/7/7.6.png)

5. **Xóa API**

   - Chọn **API actions**
   - Chọn **Delete API**

  ![ConnectPrivate](../../images/7/7.7.png)

   - Chọn **Confirm**
   - Nhấn **Delete**

  ![ConnectPrivate](../../images/7/7.8.png)
