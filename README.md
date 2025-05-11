Dựa trên nội dung từ file PDF bạn đã cung cấp, dưới đây là một bản mẫu `README.md` phù hợp để mô tả dự án của bạn:

---

# Vietnamese News Text Classification using Machine Learning & Deep Learning

## Giới thiệu

Dự án này xây dựng một hệ thống phân loại văn bản tiếng Việt (tin tức) dựa trên **machine learning** và **deep learning**. Dữ liệu được xử lý từ tập tin `data.csv` chứa tiêu đề, nội dung và danh mục tin tức. Mục tiêu chính là xây dựng mô hình có khả năng phân loại chính xác các bài viết theo 13 chủ đề như: công nghệ, thể thao, giáo dục, pháp luật...

---

## Công nghệ & Thư viện sử dụng

* Python
* Pandas, NumPy, Matplotlib
* Scikit-learn (KNN, Naive Bayes, SVM, TF-IDF, CountVectorizer)
* TensorFlow / Keras (Sequential, Embedding, Dense, Dropout, Tokenizer)
* NLTK, Underthesea (xử lý tiếng Việt)
* BeautifulSoup, Requests (thu thập dữ liệu nếu cần)
* tqdm (hiển thị tiến trình xử lý)

---

## Cấu trúc thư mục

```bash
.
├── dataset/
│   ├── data.csv               # Dữ liệu thô
│   └── clean_data.csv         # Dữ liệu đã tiền xử lý
└── Language_Model.ipynb       # Code chính của chương trình
```

---

## Các bước thực hiện

### 1. Thu thập & Tiền xử lý dữ liệu

* Xóa ký tự đặc biệt, chữ số
* Chuyển chữ thường
* Tách từ tiếng Việt bằng `underthesea.word_tokenize`
* Lưu dữ liệu đã xử lý vào `clean_data.csv`

### 2. Khám phá dữ liệu

* Thống kê số lượng bài theo từng danh mục
* Biểu đồ phân phối số từ trên mỗi bài viết
* Xác định bài viết dài nhất/ngắn nhất

### 3. Vector hóa văn bản

* Sử dụng `TF-IDF` hoặc `CountVectorizer` để biến đổi dữ liệu văn bản thành vector đặc trưng

### 4. Huấn luyện mô hình

* So sánh nhiều mô hình:

  * **K-Nearest Neighbors (KNN)**
  * **Naive Bayes (MultinomialNB)**
  * **Support Vector Machine (SVM)**
  * **Neural Network (Keras Sequential Model)**

### 5. Đánh giá mô hình

* Báo cáo độ chính xác, precision, recall, F1-score với `classification_report`

---

## Kết quả

* Số lượng danh mục: 13
* Số mẫu: 51999 dòng dữ liệu
* Độ dài bài viết dài nhất: 5728 từ

---

## 📌 Ghi chú

* Dữ liệu chứa nhiều lỗi OCR (ví dụ: `điể9u_khiể7n`, `cô9ng_nghệ`) cần xử lý kỹ hơn nếu muốn cải thiện chất lượng mô hình.
* Dự án có thể mở rộng để dùng **transformers** như BERT cho tiếng Việt trong các nghiên cứu tiếp theo.

---

## Tác giả

* **Tên:** Lý Nguyễn Quốc Trung
* **Mục tiêu học tập:** Ứng dụng NLP và học máy để xử lý tiếng Việt trong thực tế

---

