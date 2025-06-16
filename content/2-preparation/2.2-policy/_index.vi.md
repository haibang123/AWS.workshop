+++
title = "Chính Sách IAM"
weight = 2
chapter = false
pre = "<b>2.2. </b>"
+++

## Tạo Chính Sách IAM

Trong bước tiếp theo, chúng ta sẽ tạo một chính sách (policy) để cấp quyền cần thiết cho Lambda và các dịch vụ khác.

---

### 1. Trong giao diện **IAM**

- Chọn mục **Policies**
- Nhấn **Create policy**

![Policy](/images/1/1.9.png)

---

### 2. Trong phần **Create policy**, mục **Specify permission**

- Chọn tab **JSON**
- Dán đoạn mã sau vào phần **Policy Editor**, thay thế `AccountID` bằng mã tài khoản AWS thực tế của bạn.
- Nhấn **Next**

![Policy](/images/1/1.10.png)

---

### 3. Trong phần **Review and create**

- Đặt tên chính sách là: `AWSGlueServicePolicy`

![Policy](/images/1/1.11.png)

- Xem lại cấu hình và nhấn **Create policy**

![Policy](/images/1/1.12.png)

---

### 4. Sau khi tạo thành công chính sách

![Policy](/images/1/1.13.png)
