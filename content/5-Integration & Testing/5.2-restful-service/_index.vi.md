+++
title = "Dịch vụ Web RESTful"
date = 2020
weight = 1
chapter = false
pre = "<b>5.1. </b>"
+++

## Dịch vụ Web RESTful

1. Tìm kiếm và chọn **AWS API**

  ![ConnectPrivate](../../../images/5/5.7.png)

2. 

- Chọn **New API**
- Nhập tên **API**
  
  ![ConnectPrivate](../../../images/5/5.8.png)


3. Thêm **Mô tả (Description)**

- Chọn **IPv4** 

  - Nhấn **Create API** (Tạo API)

  ![ConnectPrivate](../../../images/5/5.9.png)


---

- Nhấn **Create method** (Tạo phương thức)

  ![ConnectPrivate](../../../images/5/5.10.png)


- Chọn **Phương thức GET**
- Nhấn vào **Lambda function**
- Chọn hàm **Postreader**
- Nhấn **Create method** (Tạo phương thức)

  ![ConnectPrivate](../../../images/5/5.12.png)


---

- Trong bước **API**

  - Chọn **Enable CORS** (Bật CORS – chia sẻ tài nguyên giữa các miền)

  ![ConnectPrivate](../../../images/5/5.13.png)


---

- Trong phần **Gateway Responses**

  - Nhấn **Default 4XX**
  - Nhấn **Default 5XX**

- Trong phần **Access-Control-Allow-Methods**

  - Chọn **GET**
  - Chọn **POST**
  - Nhấn **Save** (Lưu)

  ![ConnectPrivate](../../../images/5/5.14.png)


---

- Nhấn vào **Integration Request**
- Chọn **Edit** (Chỉnh sửa)

  ![ConnectPrivate](../../../images/5/5.15.png)


- Trong bước **Mapping templates**

  - Chọn **application/json**

  ![ConnectPrivate](../../../images/5/5.16.png)


---

- Trong phần **Template body**

  - Thêm **data source**
  - Chọn **Save**

  ![ConnectPrivate](../../../images/5/5.17.png)


---

- Trong bước **API Gateway**

  - Nhấn **Deploy API** (Triển khai API)

  ![ConnectPrivate](../../../images/5/5.18.png)


  - Chọn **New Stage**
  - Nhập tên giai đoạn là **Dev**
  - Nhấn **Deploy**

  ![ConnectPrivate](../../../images/5/5.19.png)


---

- Hoàn tất triển khai

  ![ConnectPrivate](../../../images/5/5.20.png)

