+++
title = "Dịch vụ Web RESTful"
date = 2020
weight = 1
chapter = false
pre = "<b>5.1. </b>"
+++

## Dịch vụ Web RESTful

1. Tìm kiếm và chọn **AWS API**

   ![Lambda](/images/5/5.7.png?width=90pc)

2. 

- Chọn **New API**
- Nhập tên **API**
  
  ![Lambda](/images/5/5.8.png?width=90pc)

3. Thêm **Mô tả (Description)**

- Chọn **IPv4** 

  - Nhấn **Create API** (Tạo API)

  ![Lambda](/images/5/5.9.png?width=90pc)

---

- Nhấn **Create method** (Tạo phương thức)

- Chọn **Phương thức GET**
- Nhấn vào **Lambda function**
- Chọn hàm **Postreader**
- Nhấn **Create method** (Tạo phương thức)

  ![Lambda](/images/5/5.12.png?width=90pc)

---

- Trong bước **API**

  - Chọn **Enable CORS** (Bật CORS – chia sẻ tài nguyên giữa các miền)

    ![Lambda](/images/5/5.13.png?width=90pc)

---

- Trong phần **Gateway Responses**

  - Nhấn **Default 4XX**
  - Nhấn **Default 5XX**

- Trong phần **Access-Control-Allow-Methods**

  - Chọn **GET**
  - Chọn **POST**
  - Nhấn **Save** (Lưu)

  ![Lambda](/images/5/5.14.png?width=90pc)

---

- Nhấn vào **Integration Request**
- Chọn **Edit** (Chỉnh sửa)

  ![Lambda](/images/5/5.111.png?width=90pc)

- Trong bước **Mapping templates**

  - Chọn **application/json**

    ![Lambda](/images/5/5.16.png?width=90pc)

---

- Trong phần **Template body**

  - Thêm **data source**
  - Chọn **Save**

    ![Lambda](/images/5/5.17.png?width=90pc)

---

- Trong bước **API Gateway**

  - Nhấn **Deploy API** (Triển khai API)

  ![Lambda](/images/5/5.18.png?width=90pc)

  - Chọn **New Stage**
  - Nhập tên giai đoạn là **Dev**
  - Nhấn **Deploy**

  ![Lambda](/images/5/5.19.png?width=90pc)

---

- Hoàn tất triển khai

  ![Lambda](/images/5/5.20.png?width=90pc)
