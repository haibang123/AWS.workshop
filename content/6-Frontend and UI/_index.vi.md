+++
title = "Giao Diện Người Dùng (Frontend / UI)"
date = 2020
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

## Giao Diện Người Dùng (Frontend / UI)

**Giao diện không máy chủ (Serverless Interface)**  
Trong bước này, bạn sẽ xây dựng một giao diện web tĩnh cho phép người dùng:

- Gửi bài viết văn bản với giọng đọc được chọn từ Amazon Polly
- Xem danh sách các bài viết
- Nghe file âm thanh được tạo từ mỗi bài viết

Frontend này sẽ được lưu trữ trên Amazon S3 và tương tác với các hàm Lambda phía backend thông qua API Gateway.

---

## Tạo Giao Diện Không Máy Chủ (Serverless UI)

Bước này bao gồm việc tải lên một ứng dụng HTML + JavaScript đơn giản lên bucket S3 và cấu hình để kết nối với các API đã triển khai.

🧰 **Chức năng của giao diện:**
- Gửi yêu cầu POST để tạo bài viết mới
- Gửi yêu cầu định kỳ đến API để lấy chi tiết bài viết
- Hiển thị nội dung văn bản gốc và file âm thanh MP3 để người dùng nghe
- Cho phép lựa chọn ngôn ngữ và giọng đọc từ Amazon Polly

🧪 **Yêu cầu:**
- Bucket S3 cần được cấu hình để **lưu trữ trang web tĩnh**
- API Gateway cần được **bật CORS**
- Cập nhật file JavaScript với các đường dẫn **API thực tế**

---

### Các bước triển khai:

- Tìm kiếm và chọn dịch vụ **S3**
- Chọn **Create Bucket (Tạo Bucket)**

  ![ConnectPrivate](../../images/6/6.0.png)

- Chọn kiểu **General purpose (Mục đích chung)**
- Đặt tên cho Bucket
- Nhấn **Create Bucket (Tạo Bucket)**

  ![ConnectPrivate](../../images/5/5.21.png)

- Nhấn **Add files (Thêm tệp)** để tải các file frontend lên

  ![ConnectPrivate](../../images/6/6.0.png)

---

- Trong bước **Buckets**, chọn **Bucket policy**
- Nhấn **Next (Tiếp tục)**

  ![ConnectPrivate](../../images/6/6.0.png)

---

- Trong bước **Bucket policy**
  - Thêm chính sách truy cập dữ liệu (data source)
  - Nhấn **Save changes (Lưu thay đổi)**

  ![ConnectPrivate](../../images/6/6.0.png)

---

- Trong bước **Block public access (Chặn truy cập công khai)**
  - Chọn **Delete all (Xóa tất cả)**
  - Nhấn **Confirm (Xác nhận)**

   ![ConnectPrivate](../../images/6/6.0.png)

---

- Nhấn vào **Link (Liên kết)** để tạo URL truy cập giao diện

  ![ConnectPrivate](../../images/6/6.0.png)

---

- Trong bước **Link**
  - Thêm **nội dung (content)**
  - Sao chép **ID**
  - Thêm **thông tin cần thiết**
  - Nhấn **Hoàn tất**

  ![ConnectPrivate](../../images/6/6.0.png)
