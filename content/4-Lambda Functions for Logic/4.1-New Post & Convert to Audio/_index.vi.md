+++
title = "Tạo Bài Viết Mới & Chuyển Văn Bản Thành Âm Thanh"
date = 2020
weight = 1
chapter = false
pre = "<b>4.1. </b>"
+++

## Tạo Lambda Crawler

1. Tìm kiếm và chọn **AWS Lambda**

  ![ConnectPrivate](../../../images/4/4.1/4.1.png)

2. Trong giao diện **AWS Lambda**

- Chọn **Author from scratch** (Tạo từ đầu)
- Nhập **tên hàm**
- Chọn ngôn ngữ **Python**
  ![ConnectPrivate](../../../images/4/4.1/4.2.png)

3.
  - Chọn **Use an existing role** (Sử dụng role có sẵn)
  - Chọn **Lab-lambda-Role**
  - Nhấn **Create function** (Tạo hàm)

  ![ConnectPrivate](../../../images/4/4.1/4.3.png)

  - Nhấn **Add a data source** (Thêm nguồn dữ liệu)

  ![ConnectPrivate](../../../images/4/4.1/4.4.png)

  - Chọn **Data source lambda**
  - Nhấn **Browse lambda**
  - Chọn **đường dẫn Lambda** (như hình minh họa)
  - Nhấn **Deploy**
  - Nhấn **Add environment variables** (Thêm biến môi trường)

  ![ConnectPrivate](../../../images/4/4.1/4.5.png)

  - Nhấn **Add**  
  ![ConnectPrivate](../../../images/4/4.1/4.6.png)

  - Nhấn **Save**

  - Chọn tab **Configuration**, sau đó chọn **Edit**

  ![ConnectPrivate](../../../images/4/4.1/4.7.png)

- Thiết lập **thời gian chạy**

  ![ConnectPrivate](../../../images/4/4.1/4.8.png)

- Tạo một **sự kiện (event)**

  ![ConnectPrivate](../../../images/4/4.1/4.9.png)

- Nhấn **Test**

  ![ConnectPrivate](../../../images/4/4.1/4.10.png)

---

4.  
- Chọn **Author from scratch**
- Nhập **tên hàm**
- Chọn ngôn ngữ **Python**

  ![ConnectPrivate](../../../images/4/4.1/4.11.png)

- Chọn **Create function**

  ![ConnectPrivate](../../../images/4/4.1/4.12.png)

- Nhấn **Add a data source**

  - Chọn **Data source lambda**
  - Nhấn **Browse lambda**
  - Chọn **đường dẫn Lambda** như hình
  - Nhấn **Deploy**

  ![ConnectPrivate](../../../images/4/4.1/4.13.png)

- Nhấn **Add environment variables**

  ![ConnectPrivate](../../../images/4/4.1/4.14.png)

- Chọn **Configuration** > **Edit**

  ![ConnectPrivate](../../../images/4/4.1/4.15.png)

- Thiết lập **thời gian**

  ![ConnectPrivate](../../../images/4/4.1/4.16.png)

- Thêm **Trigger** (Trình kích hoạt)

  ![ConnectPrivate](../../../images/4/4.1/4.17.png)

- Nhấn **Add**

  ![ConnectPrivate](../../../images/4/4.1/4.18.png)

---

8. Chọn **Explore items** (Khám phá các mục)

  ![ConnectPrivate](../../../images/4/4.1/4.19.png)

8. Chọn **posts**

  ![ConnectPrivate](../../../images/4/4.1/4.20.png)

8. Chọn **MP3**

  ![ConnectPrivate](../../../images/4/4.1/4.21.png)

8. Nhấn **Test**
