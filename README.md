# 🔍 Đề tài Phát hiện gian lận trong giao dịch tài chính - DATN_2026_KHDL

## 📋 Tổng Quan Dự Án

Dự án này phát triển và tối ưu hóa **Mô hình phát hiện gian lận trong giao dịch tài chính** sử dụng các thuật toán **Machine Learning** nâng cao. Mục tiêu là xây dựng mô hình có khả năng phân loại các giao dịch điện tử thành hai loại: **gian lận** hoặc **hợp lệ**.

### ✨ Các Tính Năng Chính
- ✅ Xử lý dữ liệu lớn với tối ưu hóa bộ nhớ
- ✅ Tạo đặc trưng (Feature Engineering) từ dữ liệu giao dịch
- ✅ Cân bằng dữ liệu (Handling Imbalanced Data)
- ✅ Huấn luyện mô hình LightGBM với Stratified K-Fold Cross-Validation
- ✅ Đánh giá mô hình với các metrics: ROC-AUC, Precision, Recall, F1-Score
- ✅ Trực quan hóa kết quả (Visualization)

---

## 📊 Thông Tin Tập Dữ Liệu

### 🔗 Nguồn Dữ Liệu
Dữ liệu được tải từ **Google Drive**:
https://drive.google.com/drive/folders/1Bs_pbIss6wQd4fGxwsghNA993S1qrzg_?usp=sharing

Code

### 📁 Các File Dữ Liệu
├── train_identity.csv # Thông tin danh tính giao dịch (Tập huấn luyện) ├── train_transaction.csv # Thông tin giao dịch (Tập huấn luyện) ├── test_identity.csv # Thông tin danh tính giao dịch (Tập kiểm tra) └── test_transaction.csv # Thông tin giao dịch (Tập kiểm tra)

Code

### 📈 Mô Tả Dữ Liệu

| File | Dòng | Cột | Mô Tả |
|------|------|------|-------|
| `train_identity.csv` | 144,233 | 41 | Dữ liệu danh tính và thiết bị của người dùng |
| `train_transaction.csv` | 590,540 | 394 | Dữ liệu giao dịch (bao gồm nhãn `isFraud`) |
| `test_identity.csv` | 141,907 | 41 | Dữ liệu danh tính kiểm tra |
| `test_transaction.csv` | 506,691 | 393 | Dữ liệu giao dịch kiểm tra |

### 🎯 Biến Mục Tiêu
- **isFraud**: 0 = Giao dịch hợp lệ, 1 = Giao dịch gian lận
- **Tỷ Lệ Mất Cân Bằng**: ~96.5% hợp lệ vs ~3.5% gian lận

### 🏷️ Phân Loại Đặc Trưng
- **Đặc Trưng C (14)**: Đặc trưng đếm - số lần giao dịch/sử dụng
- **Đặc Trưng D (15)**: Đặc trưng chênh lệch thời gian
- **Đặc Trưng M (9)**: Đặc trưng so khớp (matching)
- **Đặc Trưng V (339)**: Đặc trưng từ Vesta (đặc trưng độc quyền)
- **Đặc Trưng id (38)**: Đặc trưng danh tính và thiết bị

---

## 🛠️ Hướng Dẫn Cài Đặt & Thiết Lập

### 📋 Yêu Cầu
- Python 3.8 trở lên
- pip hoặc conda

1️⃣ Clone Repository
```bash
git clone https://github.com/duckiestran/DATN_2026_KHDL.git
cd DATN_2026_KHDL
```
2️⃣ Tạo Môi Trường Ảo (Tùy Chọn)
```bash
# Với venv
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

# Hoặc với conda
conda create -n fraud-detection python=3.8
conda activate fraud-detection
```
3️⃣ Cài Đặt Các Thư Viện Phụ Thuộc
```bash
pip install -r requirements.txt
```
4️⃣ Tải Dữ Liệu
Truy cập Google Drive
Tải 4 file CSV xuống
Tạo thư mục data/ và đặt các file vào đó
📁 Cấu Trúc Dự Án
```Code
DATN_2026_KHDL/
├── README.md                      # Tài liệu dự án
├── requirements.txt               # Danh sách thư viện Python
├── fraud_detection-2.ipynb        # Notebook chính
├── data/                          # Thư mục tập dữ liệu
└── outputs/                       # Kết quả & biểu đồ trực quan
```
🚀 Hướng Dẫn Sử Dụng
```bash
# Sử dụng Jupyter Notebook
jupyter notebook fraud_detection-2.ipynb
```
````markdown
## 🎯 Các Metrics Hiệu Suất

| Metrics   | Mô Tả                              |
|-----------|-----------------------------------|
| ROC-AUC   | Diện tích dưới đường cong ROC     |
| Precision | Tỷ lệ dự đoán gian lận đúng       |
| Recall    | Tỷ lệ phát hiện được gian lận     |
| F1-Score  | Trung bình điều hòa của Precision và Recall |

---

## 📦 Các Thư Viện Cần Thiết

```
numpy>=1.19.0
pandas>=1.1.0
matplotlib>=3.3.0
seaborn>=0.11.0
scikit-learn>=0.23.0
lightgbm>=3.1.0
scipy>=1.5.0
````

---

## 🐛 Khắc Phục Sự Cố

* Lỗi không tìm thấy module:

  ```bash
  pip install -r requirements.txt
  ```

* Lỗi bộ nhớ:
  Kiểm tra RAM khả dụng trước khi chạy

* Không tìm thấy dữ liệu:
  Đảm bảo file CSV nằm trong thư mục `data/`

---

## 📚 Tham Khảo

* LightGBM Documentation
* Scikit-learn Documentation
* IEEE Fraud Detection Kaggle


