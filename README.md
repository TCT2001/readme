# INT3405_20-tinyPython & Sentiment Analysis Problem
## Overview
Đối với bài toán phân tích và đánh giá tính tích cực hay tiêu cực của các bình luận trên trang web https://www.foody.vn, hai mô hình học máy được sử dụng khảo sát là LSTM (Long Short Term Memory networks) và Phobert. Nhìn chung, để áp dụng hai mô hình đều phải trải qua các bước chính như sau:
* Tiền xử lý
* Chuẩn hóa vector
* Phân tích ngữ nghĩa

## Introduction
### Partner
* Vũ Minh Tuyến - UET
* Vũ Trọng Thanh - UET
* Phạm Đăng Nguyên - UET
* Dương Văn Tân - UET
* Nguyễn Phúc Vinh - UET

### Methods Used
* LSTM model
* Phobert model
* Data crawling

### Technologies
* Python

### Main python libraries
* pandas
* keras
* tensorflow
* pyvi
* sklearn
* numpy
* seaborn
* transformer

## About Dataset
* Additional dataset (Crawl thêm ~400.000 data): [LINK](https://drive.google.com/file/d/1XUJGqCAzAXYdZwn1TdO12p0ID_gKhinQ/view?usp=sharing)
* Original dataset (Có sẵn từ cuộc thi):
    * Train dataset: ~9.000 data
    * Test dataset: ~5.103 data

## Code & Model

### Requirement
* Sử dụng Kaggle or tương đương
* Should have GPU acceleration while training
* Link file requirements.txt: [LINK](https://drive.google.com/file/d/1ilaaBDZHcszpUk3tsi9z5RuLpnw0m7J3/view?usp=sharing)

### Using Kaggle

**Note**: Link model LSTM và Phobert: [LINK](https://drive.google.com/drive/folders/1llutGFyZ7ORSLjVUFaDNUIu1c9P2zClF?usp=sharing)

* Bước 1: Tạo mới notebook
* Step 2: Trong notebook, chọn import notebook và import file notebook đối với từng model [LINK](https://drive.google.com/drive/folders/1llutGFyZ7ORSLjVUFaDNUIu1c9P2zClF?usp=sharing)
* Step 3: Vào notebook thay đường dẫn file train ở dòng
```python
input_file1 = 'path/of/more/data.csv' # file crawl them
input_file2 = '/kaggle/input/int3405-sentiment-analysis-problem/full_train.csv' # file train tren Kaggle
```
***Note***: trong trường hợp không muốn sử dụng file được crawl thêm, tạo ra file csv rỗng rồi chỉnh đường dẫn và set giá trị vào biến input_file1
* Step 4: Kiểm tra notebook đã chạy python và GPU chưa.
    * Đối với Phobert dùng TPU tăng tốc độ train lên gấp khoảng 4 lần so với dùng GPU
* Step 5: Nhận nút Run All để chạy toàn bộ notebook
    * Model train xong sẽ lưu vào đường dẫn /kaggle/working
    * File submission.csv cũng được tạo ra sau khi dùng model ở trên để đánh label cho tập test và được lưu vào đường dẫn /kaggle/working