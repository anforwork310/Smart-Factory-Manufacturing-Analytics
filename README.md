# Smart-Factory-Manufacturing-Analytics
The project helps to track the following indicators: Machine performance, Energy costs, Product defect rates, Production and productivity, Total maintenance &amp; energy costs by month/quarter.

## I. Introduction
### 1. Introduction to Dataset
This dataset provides a comprehensive analytical view of a Smart Factory specializing in the manufacturing of Automation Equipment. The data is structured across four key performance areas: Manufacturing Analytics (Overview), Machine Performance, Energy Management, and Product Quality.

The primary objective of this data compilation is to enable data-driven decision-making related to operational efficiency, maintenance strategies, energy consumption optimization, and quality control.

### 2. Data Model
<img width="1093" height="867" alt="image" src="https://github.com/user-attachments/assets/963220a0-d775-437d-91bf-2452d589253b" />

### 3. Business Question
1. Which specific machines or machine types (e.g., CNC, Sensor Module) pose the highest operational risk?

We seek to identify machines with the lowest MTBF (Mean Time Between Failure) and highest MTTR (Mean Time To Repair) to prioritize Preventive Maintenance actions.

2. What is the total energy cost trend, and how is the cost distributed across energy sources?

This helps determine if the factory is becoming more or less efficient over time and which energy source (e.g., Electricity, Compressed Air) represents the largest financial commitment.

3. Which defect categories and product specifications are the primary drivers of quality loss (Pareto Principle)?

We need to focus on the top 2-3 Product_Total_Defect by Category to achieve the maximum reduction in the overall defect rate.

## II. Design Thinking Method
Here are the five steps of design thinking:
### Step 1: Empathize
<img width="2114" height="870" alt="image" src="https://github.com/user-attachments/assets/904f2bab-7b00-4f13-8b5f-28993dcc72e0" />

### Step 2: Define
<img width="513" height="619" alt="image" src="https://github.com/user-attachments/assets/230c1757-c1e0-48ac-96d8-e02d1e75d509" />

### Step 3: Ideate
<img width="1738" height="571" alt="image" src="https://github.com/user-attachments/assets/128ecf21-7588-45d1-a0a2-07eaf1f80ea8" />

### Step 4: Prototype

### Step 5: Review

## III. Visualization
### 1. Overview
<img width="2045" height="1161" alt="image" src="https://github.com/user-attachments/assets/f4282fcb-f00c-4273-9759-18d4473a38d3" />

### 2. Machine Performance
<img width="2049" height="1162" alt="image" src="https://github.com/user-attachments/assets/38cc321b-7cf9-4008-a3b1-6304c4a3cbcc" />

### 3. Energy Management
<img width="2046" height="1162" alt="image" src="https://github.com/user-attachments/assets/13212963-1283-4946-bf7f-bf42e9cea488" />

### 4. Product Quality
<img width="2054" height="1155" alt="image" src="https://github.com/user-attachments/assets/57e15cdf-6e19-4404-8bd9-8f8c268ab457" />

## IV. Recommendation & Insights
### 1. Overview 
- Tính Sẵn sàng Máy móc Ổn định: Tỷ lệ sẵn sàng máy (96.60%) và tỷ lệ năng suất (97.29%) được giữ vững qua các năm và quý, cho thấy quy trình bảo trì tổng thể đang hoạt động tốt.

  => Cảnh báo Sớm Giảm Sút: Mặc dù ổn định, cần giám sát chặt chẽ Qúy có sự sụt giảm (ví dụ: Q3/2023 có Machine Availability thấp 96.47%). Điều tra xem vấn đề này có phải là sự cố tạm thời hay dấu hiệu của một vấn đề bảo trì lớn hơn.

- Tăng trưởng & Chi phí được Kiểm soát: Tổng giờ vận hành (+25.66%), Sản lượng (+25.83%), và Chi phí năng lượng (+25.51%) đều tăng trưởng mạnh mẽ và gần như tương đương. Điều này cho thấy sự mở rộng sản xuất mà không làm tăng chi phí vận hành/đơn vị một cách bất thường.

  => Duy trì Tốc độ Tăng trưởng: Tiếp tục theo dõi chặt chẽ mối quan hệ giữa Energy Total Cost và Product Total Output. Nếu chi phí tăng nhanh hơn sản lượng, cần xem xét lại hiệu suất máy hoặc giá năng lượng.

- Hiệu quả Năng lượng Kém: Biểu đồ phân tán giữa chi phí năng lượng và sản lượng cho thấy tương quan nghịch (đường xu hướng đi xuống). Các máy có tổng chi phí năng lượng cao lại có xu hướng sản xuất sản lượng thấp.

  => Phân tích Máy Kém Hiệu quả: Lọc ra các máy nằm ở góc dưới bên phải của biểu đồ phân tán (chi phí cao, sản lượng thấp) và tiến hành kiểm toán năng lượng chuyên sâu để xác định nguyên nhân (ví dụ: rò rỉ khí nén, máy hoạt động không tải).

### 2. Machine Performance
- MTTR Rất Cao: Chỉ số MTTR (Thời gian Trung bình Sửa chữa) hiện tại là 16.13 phút, trong khi MTBF (Thời gian Trung bình giữa các Lần Hỏng) là 13.99 giờ. MTTR cao (16.13 phút) cho thấy tốc độ phản ứng và khắc phục sự cố còn chậm sau khi máy hỏng.

  => Tối ưu hóa Quy trình Sửa chữa: Tập trung vào việc giảm MTTR bằng cách: 1. Đảm bảo tồn kho phụ tùng quan trọng. 2. Đào tạo kỹ thuật viên chuyên sâu hơn. 3. Áp dụng quy trình chuẩn hóa (SOP) cho các lỗi thường gặp.

- Thiết bị Cảm biến và CNC rủi ro cao: Các loại máy Sensor Module và CNC Machine đang có thời gian dừng máy (Hours Downtime) cao nhất (lần lượt là 906 và 904 giờ).

  => Ưu tiên Bảo trì Dự phòng: Lập tức thiết lập chương trình Bảo trì Dự phòng (Preventive Maintenance) dựa trên điều kiện hoạt động cho các máy Sensor Module và CNC, tập trung vào các máy có MTBF thấp nhất trong hai loại này.
  
- Fanuc và Mitsubishi có MTBF tốt: Dựa trên biểu đồ % Performance by Manufacturer (dù cần thêm MTBF/MTTR chi tiết), Fanuc và Mitsubishi (37.27% & 34.79%) có vẻ có hiệu suất tốt hơn Siemens (32.60%).

  => Đánh giá Nhà cung cấp: Dùng dữ liệu chi tiết để đưa ra quyết định mua sắm hoặc hợp đồng bảo trì. Yêu cầu Siemens cải thiện chất lượng/độ tin cậy của máy móc.


### 3. Energy Management
- Biến động Chi phí Năng lượng: Biểu đồ xu hướng cho thấy chi phí năng lượng tổng thể có sự biến động đáng kể theo quý, với các đỉnh chi phí vào Quý 1 hàng năm (khoảng 170M - 179M) và đáy chi phí vào Quý 2/Quý 4 (khoảng 147M - 162M).

  => Lập Kế hoạch Chi phí theo Mùa vụ: Phân tích nguyên nhân của các đỉnh chi phí (ví dụ: nhu cầu sưởi ấm/làm mát, tăng sản xuất đầu năm). Có thể đặt mục tiêu tiết kiệm năng lượng linh hoạt theo quý thay vì mục tiêu cố định.

- HMI Panel và PLC kém hiệu quả về chi phí/sản lượng: HMI Panel (4.6K) và PLC (4.0K) vẫn là các loại máy có chi phí năng lượng/đơn vị sản phẩm cao nhất theo Category.

  => Điều tra về Mức độ Sử dụng (Utilization): Kiểm tra xem HMI Panel và PLC có hoạt động liên tục (Standby Mode) với chi phí điện năng nhất định mà không tạo ra sản phẩm không. Đây có thể là vấn đề về quản lý tải (Load Management).

### 4. Product Quality
- CNC và Sensor là nguồn lỗi chính: CNC Machine (1.6M) và Sensor Module (1.5M) là hai loại máy tạo ra số lượng sản phẩm lỗi cao nhất.

  => Đánh giá Chất lượng Máy: Phối hợp nhóm Kỹ thuật và Vận hành để kiểm tra tính ổn định/độ chính xác của máy CNC và Sensor Module. Lỗi thường xuyên ở CNC có thể do sai lệch cơ học, ở Sensor Module có thể do sai số hiệu chuẩn.

- Phân bổ Tỷ lệ Lỗi Đồng đều giữa các Operator: Biểu đồ tròn cho thấy tỷ lệ lỗi % Product_Defect_Rate của 4 Operator là rất sát nhau, dao động từ 2.69% đến 2.74%. Điều này cho thấy nguyên nhân lỗi không nằm ở sự khác biệt về kỹ năng vận hành cá nhân, mà là do yếu tố hệ thống (Máy móc, Quy trình, Thiết kế Sản phẩm).

  => Chuyển trọng tâm Phân tích: Ngừng tập trung vào đào tạo Operator để giảm lỗi. Thay vào đó, tập trung 80% nỗ lực vào việc khắc phục lỗi từ các nguồn chính: Máy móc (CNC/Sensor Module) và Loại Lỗi (Robot Module/Servo Motor).

- Lỗi Robot Module và Servo Motor cần ưu tiên: Robot Module (38K) và Servo Motor (29K) là các loại lỗi có số lượng tuyệt đối cao nhất.

  => Phân tích Nguyên nhân Cốt lõi (Root Cause Analysis - RCA): Lập tức tiến hành RCA cho lỗi Robot Module. Đây có thể là lỗi vật liệu, quy trình lắp ráp, hoặc lỗi trong quá trình kiểm tra chất lượng.


















