# SQL_SERVER_Practice
## Thông tin sinh viên:
+ **Họ và tên:** Trần Tùng Lâm
+ **Lớp:** K59KMT.K01
+ **Mã số sinh viên:** K235480106039
+ **Trường:** Đại học Kỹ thuật Công Nghiệp Thái Nguyên
---
### 1. Cài đặt _SQL Server 2025 Developer_, cài đặt với 2 kiểu login (Mixed Mode): _Windows Authentication_ và _SQL Server Authentication_ 
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/8ad06243-dfb3-4440-a736-57fe0afa1c81" />

 
### 2+3. Cấu hình _SQL Server_

* Các service đang chạy
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/f14d61a8-5562-4ec7-9f9c-9480f10245ab" />

* Enable TCP/IP
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/7dffd133-ce82-4546-890f-0f93c8a37ba5" />

* Cấu hình chi tiết cho TCP/IP
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/c6f207c8-69a2-4909-89fb-fd261f814bb2" />

* Listen ALL = YES
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/f7c125fd-90fb-4eea-9675-8d2c44fc7cce" />

* IP address + Dynamic Port với cổng `36039`
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/097d4e0f-6f75-466a-b547-1bcd362c5561" />

* Thông báo Mọi thứ đã được lưu lại, restart SQL Server mới có hiệu lực
<img width="1915" height="1038" alt="Screenshot 2026-04-10 194053" src="https://github.com/user-attachments/assets/bd36d9f0-6f4a-4036-98cc-1f30dd91cbeb" />

* Restart SQL Server
<img width="1919" height="1036" alt="Screenshot 2026-04-10 194212" src="https://github.com/user-attachments/assets/0e7552b7-5e04-4f95-97c5-2c99347b1bd8" />

* Kiểm tra cổng `36039` có đang mở bằng lệnh cmd `netstat -ano | findstr LISTENING`
<img width="1919" height="1079" alt="Screenshot 2026-04-10 194503" src="https://github.com/user-attachments/assets/ff029283-5b81-4b53-96ec-4d9535bf0618" />

* Kiểm tra lại bằng tool _CurrPorts v2.61 - Monitoring Opened TCP/IP netwwork ports_
<img width="1919" height="1079" alt="Screenshot 2026-04-10 194717" src="https://github.com/user-attachments/assets/43e4031c-a2e8-4a69-8e02-03bbe25a2dee" />

* SQL Server đang mở cổng `36039`
<img width="1919" height="1079" alt="Screenshot 2026-04-10 194615" src="https://github.com/user-attachments/assets/92cc5572-a1c5-4ba1-af7e-f785c86f02ed" />

### 4. Cài đặt _SQL Server Management Studio 22_

### 5. Đăng nhập vào _SQL Server Management Studio 22_ bằng 2 cách: _Windows Authentication_ và _SQL Server Authentication_

* Kết nối bằng _Windows Authentication_:
<img width="1919" height="1079" alt="Screenshot 2026-04-10 195151" src="https://github.com/user-attachments/assets/6dd44a08-215a-4cc4-933e-eb9a18f14991" />

* Kết nối bằng _SQL Server Authentication_
<img width="1919" height="1079" alt="Screenshot 2026-04-10 195235" src="https://github.com/user-attachments/assets/c8b0b405-7626-4edb-b153-bec8ce7e4161" />

* Kết quả login bằng 2 cách
<img width="1919" height="1035" alt="Screenshot 2026-04-10 195313" src="https://github.com/user-attachments/assets/9bd24b74-9d5c-4fdb-b615-caf82f58d078" />

### 6. Tạo cơ sở dữ liệu mới

+ Database: `DSSV`
<img width="1919" height="1079" alt="Screenshot 2026-04-10 210646" src="https://github.com/user-attachments/assets/6b3e0477-41f0-44ed-8792-09883606bfb6" />

+ Đường dẫn (Path) lưu trữ file dữ liệu `DSSV_Data` và file lưu log `DSSV_Log` : `D:\CSDL\CSDLDATA`
<img width="1919" height="1079" alt="Screenshot 2026-04-10 210826" src="https://github.com/user-attachments/assets/5d058dc4-d3f8-4c24-aca2-52a2c4ad51ca" />

### 7. Tạo bảng dữ liệu với tên `Sinhvien`, có Khóa chính (Primary Key) là trường `masv`
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/05808ea6-0ce4-4abc-831b-2f7fe1cf3eaa" />

### 8. Import dữ liệu từ file mẫu `svtnut.csv`

+ Import dữ liệu
<img width="1919" height="1079" alt="Screenshot 2026-04-10 222223" src="https://github.com/user-attachments/assets/abeb2d2b-00f9-421d-9f0d-445b52d87abf" />

+ Import dữ liệu thành công

### 9. Kiểm tra số dòng của bảng dữ liệu sau khi import

### 10. Thêm dữ liệu cá nhân của sinh viên vào bảng

+ Thêm dữ liệu thành công

+ Kiểm tra dữ liệu sau khi nhập

### 11.  Gõ lệnh để update trường _noisinh_ thành 'Sao Hoả' cho những dòng có _noisinh_ và _diachi_ đều là NULL

### 12. Tạo bảng SaoHoa gồm những sinh viên có nơi sinh ở 'Sao Hoả'

+ Kiểm tra bảng SaoHoa

### 13. Xóa những sinh viên có cùng họ Trần

### 14. Xuất toàn bộ kết quả của các bước 6 -> 13 ra file ``

+ Xuất file `` thành công

### 15. Xóa cơ dở dữ liệu `Quanly_Sinhvien`

+ Kiểm tra path 

### 16. Mở file dữ liệu ``


### 17. Upload file `` lên Github repository của em

