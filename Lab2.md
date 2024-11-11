# Phân tích hệ thống Payroll System

## 1. Phân tích các ca sử dụng trong Payroll System

### 1.1 Run Payroll
- **Mô tả**: Tự động chạy quy trình trả lương cho nhân viên vào mỗi thứ Sáu và ngày làm việc cuối cùng của tháng.
- **Các lớp phân tích**: `PayrollSystem`, `Employee`, `Paycheck`, `BankSystem`.
- **Các hành vi chính**:
  - Lấy danh sách nhân viên cần được trả lương.
  - Tính toán số tiền lương dựa trên thông tin thời gian làm việc và các khoản khấu trừ.
  - Gửi giao dịch ngân hàng nếu chọn hình thức chuyển khoản.

### 1.2 Select Payment Method
- **Mô tả**: Nhân viên có thể chọn phương thức thanh toán (nhận trực tiếp, qua bưu điện hoặc chuyển khoản).
- **Các lớp phân tích**: `Employee`, `PaymentMethod`.
- **Các hành vi chính**:
  - Lấy yêu cầu từ nhân viên và xác nhận phương thức thanh toán đã chọn.

### 1.3 Maintain Employee Information
- **Mô tả**: Payroll Administrator quản lý thông tin nhân viên như thêm mới, chỉnh sửa và xóa.
- **Các lớp phân tích**: `PayrollAdministrator`, `Employee`.
- **Các hành vi chính**:
  - Thêm, cập nhật hoặc xóa thông tin nhân viên từ hệ thống.

### 1.4 Maintain Purchase Order
- **Mô tả**: Nhân viên có hoa hồng ghi nhận và quản lý đơn hàng của họ để nhận tiền hoa hồng.
- **Các lớp phân tích**: `CommissionedEmployee`, `PurchaseOrder`.
- **Các hành vi chính**:
  - Tạo, chỉnh sửa, và xóa đơn hàng cho nhân viên.

### 1.5 Login
- **Mô tả**: Người dùng đăng nhập vào hệ thống.
- **Các lớp phân tích**: `LoginForm`, `SecurityAccess`.
- **Các hành vi chính**:
  - Kiểm tra tên người dùng và mật khẩu.

## 2. Mã Java mô phỏng ca sử dụng Maintain Timecard

```java
import java.util.HashMap;
import java.util.Map;

class Employee {
    private String id;
    private String name;
    private Map<String, Timecard> timecards;

    public Employee(String id, String name) {
        this.id = id;
        this.name = name;
        this.timecards = new HashMap<>();
    }

    public String getId() {
        return id;
    }

    public void submitTimecard(Timecard timecard) {
        timecards.put(timecard.getPeriod(), timecard);
        System.out.println("Timecard submitted for period: " + timecard.getPeriod());
    }

    public Timecard getTimecard(String period) {
        return timecards.get(period);
    }
}

class Timecard {
    private String period;
    private Map<String, Integer> hoursWorked;

    public Timecard(String period) {
        this.period = period;
        this.hoursWorked = new HashMap<>();
    }

    public String getPeriod() {
        return period;
    }

    public void addHours(String date, int hours) {
        hoursWorked.put(date, hours);
        System.out.println("Added " + hours + " hours for date: " + date);
    }

    public Map<String, Integer> getHoursWorked() {
        return hoursWorked;
    }

    public void submit() {
        System.out.println("Timecard for period " + period + " is submitted.");
    }
}

public class PayrollSystem {
    public static void main(String[] args) {
        Employee employee = new Employee("001", "Trin");

        // Tạo Timecard cho một tuần
        Timecard timecard = new Timecard("2024-W45");
        timecard.addHours("2024-11-04", 8);
        timecard.addHours("2024-11-05", 7);
        timecard.addHours("2024-11-06", 8);
        timecard.addHours("2024-11-07", 6);
        timecard.addHours("2024-11-08", 8);

        // Gửi Timecard
        employee.submitTimecard(timecard);

        // Truy xuất và xem lại Timecard đã gửi
        Timecard submittedTimecard = employee.getTimecard("2024-W45");
        System.out.println("Submitted Timecard for period: " + submittedTimecard.getPeriod());
        submittedTimecard.submit();
    }
}
