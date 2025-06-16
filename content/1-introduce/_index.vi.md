+++
title = "Giới thiệu"
date = 2020
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

# Xây dựng ứng dụng Chuyển văn bản thành giọng nói không máy chủ với Amazon Polly

#### Giới thiệu về Amazon Polly

**Amazon Polly là một dịch vụ chuyển văn bản thành giọng nói (TTS)** của Amazon, sử dụng công nghệ học sâu tiên tiến để tổng hợp giọng nói giống như con người. Polly hỗ trợ hàng chục giọng đọc chân thực bằng hơn 20 ngôn ngữ khác nhau, giúp các nhà phát triển tạo ra các ứng dụng hỗ trợ giọng nói cho người dùng toàn cầu.

Polly giải quyết các thách thức phổ biến trong hệ thống TTS như:

- Xử lý các từ có cách viết giống nhau nhưng cách phát âm khác nhau (ví dụ: "live" trong các ngữ cảnh khác nhau),
- Chuẩn hóa văn bản (ví dụ: viết tắt như “St.” thành “Street” hoặc “Saint”),
- Chuyển đổi văn bản sang phiên âm trong các ngôn ngữ phức tạp như tiếng Anh (ví dụ: "tough", "though", "through"),
- Xử lý từ nước ngoài, tên riêng, và tiếng lóng (ví dụ: "déjà vu", "ASAP").

Amazon Polly cung cấp thời gian phản hồi nhanh và ổn định, phù hợp với các ứng dụng tương tác thời gian thực. Bạn có thể lưu trữ hoặc phát lại các tệp âm thanh ngoại tuyến mà không phải trả thêm phí.

Cách sử dụng rất đơn giản: chỉ cần gửi văn bản đến API của Amazon Polly, và nó sẽ trả về luồng âm thanh (ví dụ: định dạng MP3) mà ứng dụng của bạn có thể phát hoặc lưu lại.

Trong hội thảo này, bạn sẽ xây dựng một ứng dụng không máy chủ đơn giản sử dụng Amazon Polly để chuyển đổi văn bản đa ngôn ngữ thành giọng nói, có thể phát trực tiếp trên trình duyệt. Ứng dụng này có thể được dùng để đọc công thức nấu ăn, tin tức, sách hoặc bất kỳ nội dung nào mà không cần chạm tay.

#### Lợi ích của Amazon Polly

- Tạo bảng Amazon DynamoDB để lưu trữ dữ liệu
- Tạo API RESTful bằng Amazon API Gateway
- Tạo các hàm AWS Lambda được kích hoạt qua API Gateway
- Kết nối các hàm Lambda với Amazon SNS (Simple Notification Service)
- Sử dụng Amazon Polly để chuyển văn bản thành giọng nói với nhiều ngôn ngữ và giọng đọc khác nhau

#### Thách thức khi sử dụng Amazon Polly

- **Chuẩn hóa văn bản**: Cần xử lý trước với viết tắt và chữ số.
- **Từ đồng dạng và ngữ cảnh**: Cùng cách viết nhưng khác cách đọc (ví dụ: "live").
- **Từ nước ngoài và tên riêng**: Có thể phát âm sai (ví dụ: "François").
- **Hạn chế về ngôn ngữ và giọng đọc**: Không phải mọi tính năng đều hỗ trợ mọi ngôn ngữ.
- **Độ trễ với văn bản dài**: Có thể chậm với văn bản dài hoặc nhiều yêu cầu cùng lúc.
- **Chi phí sử dụng**: Tần suất sử dụng cao có thể gây tốn kém.
- **Bảo mật API**: Không nên để lộ khóa API trong frontend.
- **Giọng đọc chưa thật sự tự nhiên**: Thiếu cảm xúc giống người thật.

#### Kiến trúc hội thảo

##### Tổng quan kiến trúc

Sơ đồ bên dưới minh họa kiến trúc hệ thống Amazon Polly mà chúng ta sẽ triển khai trong hội thảo:

![Workshop](../../images/Diagramworkshop.png)

##### Mô tả kiến trúc

- **Tương tác người dùng**:
  - Người dùng truy cập một website tĩnh được lưu trữ trên Amazon S3.
  - Họ sử dụng form (ví dụ: gửi bài viết hoặc xem bài viết), dữ liệu được gửi qua Amazon API Gateway.

- **API Gateway kích hoạt hàm Lambda**:
  - Nếu là yêu cầu tạo bài viết mới → API Gateway gọi hàm Lambda "New Post".
  - Nếu là yêu cầu lấy bài viết → gọi hàm Lambda "Get Post".

- **Lambda truy cập DynamoDB**:
  - Cả hai hàm Lambda đều tương tác với Amazon DynamoDB để lưu trữ dữ liệu bài viết.

- **Hàm "New Post" kích hoạt thông báo SNS**:
  - Sau khi tạo bài viết mới, hàm Lambda "New Post" gửi thông báo đến dịch vụ Amazon SNS.

- **SNS kích hoạt hàm Lambda khác**:
  - Hàm Lambda "Convert to Audio" được SNS gọi để xử lý chuyển đổi văn bản thành giọng nói.

- **Lambda gọi Amazon Polly**:
  - Hàm này dùng Polly để chuyển văn bản thành âm thanh.

- **Lưu trữ tệp âm thanh**:
  - Polly trả về tệp MP3, được lưu trữ trên Amazon S3 (để phục vụ phát audio).

##### Mục tiêu hội thảo

- Hiểu các thành phần của hệ thống chuyển văn bản thành giọng nói sử dụng Amazon Polly.
- Triển khai một hệ thống đơn giản với Polly và các dịch vụ AWS (S3, Lambda, API Gateway, DynamoDB, v.v.).
- Tích hợp công cụ web và lưu trữ để tạo và phát file âm thanh từ văn bản người dùng nhập.

{{% notice info %}}
Phòng lab này được thực hiện tại khu vực Singapore (ap-southeast-1).
{{% /notice %}}
