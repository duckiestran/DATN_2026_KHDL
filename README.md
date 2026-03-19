# Tổng quan dự án

Dự án phát hiện gian lận này được xây dựng để phát hiện các giao dịch gian lận trong hệ thống tài chính bằng cách sử dụng các thuật toán học máy. Mục tiêu của dự án là sử dụng dữ liệu từ các giao dịch và thông tin của người dùng để phát hiện các mẫu giao dịch đáng ngờ.

# Thông tin về tập dữ liệu

Dữ liệu được sử dụng trong dự án này bao gồm các tệp sau:
- **train_identity.csv**: Tập dữ liệu chứa thông tin danh tính của người dùng.
- **train_transaction.csv**: Tập dữ liệu chứa thông tin giao dịch.
- **test_identity.csv**: Tập dữ liệu dùng để kiểm tra mô hình với thông tin danh tính.
- **test_transaction.csv**: Tập dữ liệu dùng để kiểm tra mô hình với thông tin giao dịch.

Các tệp này được lưu trữ trên Google Drive và có thể tải xuống để sử dụng trong dự án.

# Hướng dẫn cài đặt

1. Clone repository: `git clone <repository-url>`
2. Cài đặt các thư viện yêu cầu:
   ```bash
   pip install -r requirements.txt
   ```

# Hướng dẫn sử dụng

Để sử dụng ứng dụng, bạn có thể chạy lệnh sau:
```bash
python main.py
```

# Tính năng

- Phát hiện giao dịch gian lận.
- Phân tích các thông tin về người dùng và giao dịch.
- Xuất báo cáo và kết quả phân tích.

# Kiến trúc mô hình

Dự án sử dụng các thuật toán học máy như Random Forest, XGBoost để xây dựng mô hình phát hiện gian lận. Mô hình được huấn luyện trên tập dữ liệu đào tạo và sau đó được kiểm tra trên tập dữ liệu kiểm tra.

# Khắc phục sự cố

- **Lỗi không tìm thấy tập tin**: Đảm bảo rằng tất cả các tệp dữ liệu đã được tải xuống và nằm trong cùng thư mục với mã nguồn.
- **Lỗi về thư viện**: Đảm bảo rằng bạn đã cài đặt tất cả các thư viện được liệt kê trong `requirements.txt`.