+++
title = "Tạo Bài Viết Mới & Chuyển Văn Bản Thành Âm Thanh"
date = 2020
weight = 1
chapter = false
pre = "<b>4.1. </b>"
+++

## Tạo Lambda Crawler

1. Tìm kiếm và chọn **AWS Lambda**

   ![lambda](/images/4/4.1/4.1.png?width=90pc)

2. Trong giao diện **AWS Lambda**

- Chọn **Author from scratch** (Tạo từ đầu)
- Nhập **tên hàm**
- Chọn ngôn ngữ **Python**
  ![lambda](/images/4/4.1/4.2.png?width=90pc)

3.
  - Chọn **Use an existing role** (Sử dụng role có sẵn)
  - Chọn **Lab-lambda-Role**
  - Nhấn **Create function** (Tạo hàm)

  ![lambda](/images/4/4.1/4.3.png?width=90pc)

  - Nhấn **Add a data source** (Thêm nguồn dữ liệu)

  ![lambda](/images/4/4.1/4.4.png?width=90pc)

  - Chọn **Data source lambda**
  - Nhấn **Browse lambda**
  - Chọn **đường dẫn Lambda** (như hình minh họa)
  - Nhấn **Deploy**
  - Nhấn **Add environment variables** (Thêm biến môi trường)

  ![lambda](/images/4/4.1/4.5.png?width=90pc)

  - Nhấn **Add**  
    ![lambda](/images/4/4.1/4.6.png?width=90pc)

  - Nhấn **Save**

  - Chọn tab **Configuration**, sau đó chọn **Edit**

    ![lambda](/images/4/4.1/4.7.png?width=90pc)

- Thiết lập **thời gian chạy**

    ![lambda](/images/4/4.1/4.8.png?width=90pc)

- Tạo một **sự kiện (event)**

![lambda](/images/4/4.1/4.9.png?width=90pc)

- Nhấn **Test**

![lambda](/images/4/4.1/4.10.png?width=90pc)

---

4.  
- Chọn **Author from scratch**
- Nhập **tên hàm**
- Chọn ngôn ngữ **Python**

![lambda](/images/4/4.1/4.11.png?width=90pc)

- Chọn **Create function**

![lambda](/images/4/4.1/4.12.png?width=90pc)

- Nhấn **Add a data source**

  - Chọn **Data source lambda**
  - Nhấn **Browse lambda**
  - Chọn **đường dẫn Lambda** như hình
  - Nhấn **Deploy**

![lambda](/images/4/4.1/4.13.png?width=90pc)

- Nhấn **Add environment variables**

![lambda](/images/4/4.1/4.14.png?width=90pc)

- Chọn **Configuration** > **Edit**

![lambda](/images/4/4.1/4.15.png?width=90pc)

- Thiết lập **thời gian**

![lambda](/images/4/4.1/4.16.png?width=90pc)

- Thêm **Trigger** (Trình kích hoạt)

![lambda](/images/4/4.1/4.17.png?width=90pc)

- Nhấn **Add**

![lambda](/images/4/4.1/4.18.png?width=90pc)

---

8. Chọn **Explore items** (Khám phá các mục)

![lambda](/images/4/4.1/4.19.png?width=90pc)

8. Chọn **posts**

![lambda](/images/4/4.1/4.20.png?width=90pc)

8. Chọn **MP3**

![lambda](/images/4/4.1/4.21.png?width=90pc)

8. Nhấn **Test**
