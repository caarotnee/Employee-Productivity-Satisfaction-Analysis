# 📊 Employee Productivity & Satisfaction Analysis (HR Analytics)

## 📌 Tổng quan dự án
Dự án này đóng vai trò như một chuyên viên HR Analytics nhằm phân tích mối quan hệ giữa năng suất làm việc, mức độ hài lòng và các yếu tố nhân khẩu học của nhân viên. Mục tiêu chính là cung cấp các giải pháp chiến lược giúp cải thiện môi trường làm việc và tối ưu hóa hiệu suất nhân sự.

## 📊 Bộ dữ liệu (Dataset)
Bộ dữ liệu **Employee Productivity and Satisfaction** bao gồm các trường thông tin:
- **Thông tin nhân viên:** Name, Age, Gender, Department, Position.
- **Dữ liệu công việc:** Joining Date, Projects Completed, Productivity (%).
- **Đánh giá sự hài lòng:** Satisfaction Rate, Feedback Score, Salary.

## 🛠 Quy trình thực hiện

### 1. Chuẩn bị & Làm sạch dữ liệu
- **Import:** Kết nối dữ liệu từ file CSV vào Power BI & Python.
- **Cleaning:** - Chuyển đổi định dạng `Joining Date` sang kiểu Ngày tháng (Date).
    - Xử lý các giá trị thiếu (Missing values) trong cột `Salary`.
    - Loại bỏ các bản ghi trùng lặp dựa trên cột `Name`.
- **Feature Engineering:** - `Experience Years`: Tính số năm làm việc từ lúc tham gia công ty đến hiện tại.
    - `Productivity Group`: Phân loại năng suất (Low: <50%, Medium: 50-80%, High: >80%).

### 2. Phân tích dữ liệu & DAX
- **Chỉ số năng suất:** Tính trung bình `Productivity` theo từng phòng ban (`Department`).
- **Phân tích tương quan:** Sử dụng DAX để tìm mối liên hệ giữa `Satisfaction Rate` (Tỷ lệ hài lòng) và `Feedback Score` (Điểm phản hồi).
- **Phân bổ nhân sự:** Phân tích mối quan hệ giữa độ tuổi (`Age`) và số lượng dự án đã hoàn thành (`Projects Completed`).

### 3. Trực quan hóa dữ liệu (Dashboard)
Xây dựng Dashboard tương tác hỗ trợ ra quyết định:
- **Heatmap:** Thể hiện sự tương quan phức hợp giữa Tuổi - Năng suất - Mức lương.
- **Bar Chart:** So sánh tỷ lệ hài lòng giữa các phòng ban.
- **Line Chart:** Theo dõi xu hướng biến động năng suất dựa trên thời điểm gia nhập công ty.
- **Slicers:** Hỗ trợ lọc dữ liệu linh hoạt theo `Position` (Vị trí) và `Gender` (Giới tính).
<img width="1855" height="1026" alt="image" src="https://github.com/user-attachments/assets/37ab9dc6-e850-4c59-8d42-78064d919f87" />


<img width="1886" height="1033" alt="image" src="https://github.com/user-attachments/assets/cfc15556-aeed-4763-acca-0cf1388947e6" />

### 4. Xử lý chuyên sâu với Notebook (Google Colab)
Sử dụng file `.ipynb` để thực hiện:
- Phân tích thống kê mô tả.
- Xử lý dữ liệu quy mô lớn nhanh chóng bằng thư viện Pandas.
- Vẽ các biểu đồ tương quan chuyên sâu bằng Seaborn và Matplotlib.

## 💡 Insights & Đề xuất

### Insights tiêu biểu:
- Xác định các phòng ban đang có mức năng suất thấp để tìm hiểu nguyên nhân gốc rễ.
- Đánh giá mức độ ảnh hưởng của thu nhập (`Salary`) đến sự gắn bó và hài lòng của nhân viên.
- Nhận diện sự khác biệt về năng suất giữa nhóm nhân viên kỳ cựu và nhân viên mới.

### Chiến lược đề xuất:
- **Đào tạo & Phát triển:** Xây dựng lộ trình đào tạo kỹ năng cho nhóm nhân viên trẻ.
- **Chính sách đãi ngộ:** Đề xuất điều chỉnh lương/thưởng cho các vị trí (Position) có mức thu nhập chưa tương xứng nhưng đóng góp năng suất cao.
- **Cải thiện môi trường:** Tập trung vào các phòng ban có điểm Feedback thấp để cải thiện văn hóa doanh nghiệp.

---
**Thực hiện bởi:** Võ Khánh Linh (LinhVK)  
