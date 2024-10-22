# Lab1
## 1.Phân tích kiến trúc
Hệ thống Payroll được xây dựng dựa trên kiến trúc client-server với desktop interface dành cho người dùng cuối và server backend để xử lý dữ liệu.<br> <br>
-Các thành phần chính: <br>
Giao diện người dùng (UI): Giao diện desktop cho phép nhân viên và quản trị viên nhập dữ liệu (thẻ chấm công, đơn đặt hàng) và tạo các báo cáo.<br>
Business Logic Layer: Xử lý logic nghiệp vụ như tính lương, xác nhận thời gian làm việc và quản lý đơn hàng.<br>
Database Layer: Hệ thống sử dụng cơ sở dữ liệu DB2 cho các dự án và thông tin liên quan đến lương.<br>
Legacy Interface: Tương tác với các hệ thống cơ sở dữ liệu cũ (Project Management Database).<br>
Security Layer: Cung cấp bảo mật thông qua kiểm soát truy cập theo user và quyền hành.<br> <br>
Lí do lựa chọn kiến trúc:
-Phân lớp rõ ràng: Giúp dễ dàng bảo trì và mở rộng trong tương lai.<br>
-Tương tác với hệ thống kế thừa: Hệ thống vẫn phải sử dụng cơ sở dữ liệu dự án hiện có để giảm chi phí và tránh gián đoạn hoạt động.


# ![](https://www.planttext.com/api/plantuml/png/P93D2G9138NlKqKgi0HnPHKyY89QG8X1H-T7CbbX4IlpO4csu8pWxehNbxpllUJrU4wIecZZdKbd6q1YOgDM7SCQMudEmQPDoXugeQDL9cs4ZRaWdV70i5l0pG2GmvHWQpqJoduUnNTYndWE-j7klN7Q91iups_3pHAuORbQuZ_gMY9bGvGXfaR5YkWNDFCN5rlckbhrS8cdN7w98TjAeU7m6r6q3Cz7ZKRZhgBfkXQrJpHcmc5VNlS6003__mC0) 

