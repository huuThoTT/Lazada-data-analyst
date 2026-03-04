# Crawling Lazada Data and Applying Machine Learning for Analysis.


## Mục lục
- Giới thiệu
- Dữ liệu
- Quy trình thực hiện
- Cấu trúc thư mục
- Cách chạy project
- Thành viên nhóm

## Giới thiệu
Mục tiêu đồ án là nhằm giúp hiểu được quá trình thu thập dữ liệu, đọc và hiểu dữ liệu, tiền xử lý dữ liệu (bao gồm: chọn feature, loại bỏ missing, duplicate, ...). Và áp dụng các mô hình học máy để phân tích các dữ liệu thu được áp dụng vào các câu hỏi thực tế.

## Dữ liệu
Dữ liệu bạn có thể tự thu thập bằng code hoặc sử dụng data do nhóm đã thu thập:
- **Nguồn:** Data của nhóm thu thập trước được zip trong thư mục raw. Giải nén và để data tại vị trí /raw/product_details.csv và tạo thư mục processed bên trong thư mục data.
- **Kích thước:** Dữ liệu gồm 1987 dòng. Bao gồm các sản phẩm thuộc nhiều danh mục khác nhau.
- **Tiền xử lý:** xử lý giá trị thiếu, chuẩn hóa dữ liệu, tách tập train/test (70/30).

## Quy trình thực hiện
1. **Data Collection:** Thu thập dữ liệu từ trang Lazada.
2. **Data Cleaning:** loại bỏ giá trị thiếu và ngoại lệ.
3. **Exploratory Data Analysis (EDA):** dùng seaborn và matplotlib để trực quan hóa.
4. **Feature Engineering:** chọn lọc biến có tương quan cao.
5. **Modeling:** huấn luyện các mô hình Linear Regression, Random Forest, XGBoost,...
6. **Evaluation:** so sánh MAE, RMSE, R² giữa các mô hình.

## Cấu trúc thư mục
```text
DATASCIENCEPROJECT/
├─ data/
│   ├─ processed/       # Chứa các dữ liệu đã qua xử lý
│   └─ raw/             # Dữ liệu gốc
│
├─ src/
│   └─ process/
│       ├─ data/
│       │   ├─ eda.ipynb
│       │   └─ splitdata.ipynb
│       │
│       ├─ data_crawling/
│       │   └─ crawler.ipynb
│       │
│       ├─ preprocessing/
│       │   ├─ normalization.ipynb
│       │   └─ preprocessing.ipynb
│       │
│       └─ questions/
│           ├─ question1.ipynb
│           ├─ question2.ipynb
│           ├─ question3.ipynb
│           ├─ question4.ipynb
│           └─ question5.ipynb
│
├─ .gitignore
├─ requirements.txt
└─ README.md\
```
## Cách chạy project
1. Clone repository:
   ```bash
   git clone https://github.com/s2yuuki2s/DataScienceProject.git
   cd DataScienceProject

2. Cài đặt môi trường:
pip install -r requirements.txt

3. Thu thập dữ liệu (nếu cần):
Bạn có thể thu thập thêm dữ liệu cần thiết cho bài làm của mình. Cụ thể:
- Tại file /src/process/data_crawling/crawler.ipynb, ở phần *Get product link on the page.* thay đổi keyword bằng sản phầm bạn muốn thu thập thêm.
- Tiến hành chạy các cell trong file /src/process/data_crawling/crawler.ipynb.

## Nhóm thực hiện
- **Thành viên nhóm:** Lương Quốc Dũng, Bùi Công Mậu, Thái Hữu Thọ
- **Mục đích:** Bài tập môn *Introduction to Data Science*







