## Câu 1
### Context Diagram BankSystem
![Context Diagram](https://www.planttext.com/api/plantuml/png/h5FBJiCm4BpxArOzjOXMS8sYYXOGgeHGrPuuEiwsMFKZiZT0U7mP1pw9Ny1kcZPj94vSR6TtPdQyw_nyVLzvuevAhHZp6saAxhW6eRZt4o8div9m9gnPoZU4Ymu6tXd0b8lDsjdIvDTMMPUclinyvGar5Cw-LkCntClr4zrPbQDPsFmHbR8lx9EnMcJEAsULkhQ6ueuEqbJK7u4RIu0hpGxL7qIYD8HknGN2RChDPbcNIzDzl27cM5WlgSy3NJoXs2JGdCuXe6sa9n3NcLbPfpb9QmO7SqVotPlzJv467KgW8KcDyf3hq5TA8BTbfZ162bxTSC84uXe3g0jbAyJPJGBBC3ApZfRMI9CjjpzeiMDuNWl4-4uYHc_tAZ6nqpbgGijvrwOGiTP3gJDqBHl3y2me7Bk9B2W-S8sddjj2BITrTj5MwsIdEydZ2tGVL--o1yFXUBktNq_IpD73TXWUdYLdRKHaf1-ZqVPmn9IXVQX3KpmxmTULHgEptc7AXqf_e4zxda3fqJDsXIQF_-il0000__y30000)
### Giải thích 
<ul>
  <li>PayrollController: Chịu trách nhiệm thực hiện use case "Run Payroll". Lớp này sẽ điều phối các bước xử lý, bao gồm tính toán tiền lương và gửi yêu cầu gửi tiền đến hệ thống ngân hàng.</li>
  <li>IBankSystem: Định nghĩa phương thức deposit để gửi tiền vào tài khoản ngân hàng.</li>
  <li>BankSystem: Chịu trách nhiệm nhận yêu cầu gửi tiền từ hệ thống tính lương và thực hiện các bước cần thiết để gửi tiền vào tài khoản ngân hàng.</li>
  <li>Paycheck: Đối tượng chính được truyền giữa hệ thống tính lương và hệ thống ngân hàng.</li>
  <li>BankInformation: Được sử dụng bởi lớp BankSystem để thực hiện giao dịch gửi tiền.</li>
</ul>

### Context Diagram PrintService
![Context Diagram](https://www.planttext.com/api/plantuml/png/h5FBJiCm4BpxArOzjOXMS8sYgkKXL0cXYfmukl6IMdNio7OAuV5b7FWaVW7RQTEaGOW3byJUdPdTdKs-FZvdnb9jormGOZPS5bJJ7591ZPbRg_cgjBX8bKpu2y9P3mEl1E22ffjCgrAoIoMKZcDJhanbBEPGQFLSJQTmoxErlL62eRnNx065K4_adP1QP4ahhOH8QawBxvY-042gaLfqk7IDwMQ8UI5KXHZ1zUuqYc2VzRfSMjIFD4LOBBMx9AYttDtYkCaqseK7DDB5xd3GEuKVohMQx-htP_-NAlkGgu3IShiN7eEakQCaRbSo2m7Ac4PZMZ603EsTmmr7nz5v3Mubsbi9dVLBqjmjsqR0LBaI649ke2kteGZyin4FEA_T84DyMODz8i2xNg9s5HbwFxlk3HcrTDzdyARxuGpE1p0UJyExk_Qe5Z0G1ZAmvPHq4PuJlqqcuN34vSvxp9q7XlGuTRt9v6Hmy2i2ZQv7tEBlX6QdVo0C6cyYC2YPgIS2RmaXCnVnl_0t0000__y30000)
### Giải thích 
<ul>
  <li>PayrollSystem: Chịu trách nhiệm tạo ra phiếu lương cho mỗi employee thông qua phương thức createPaycheck.</li>
  <li>IPrintService: Định nghĩa phương thức printPaycheck để in phiếu lương</li>
  <li>PrintService: Nhận yêu cầu in phiếu lương từ PayrollSystem và điều khiển máy in để thực hiện in ấn.</li>
  <li>Employee: Được sử dụng để tạo phiếu lương và có thể được in trên phiếu lương.</li>
  <li>Paycheck: Đối tượng chính được truyền giữa các lớp trong hệ thống để thực hiện in ấn.</li>
</ul>

### Context Diagram PrintService
![Context Diagram](https://www.planttext.com/api/plantuml/png/n5JDRjD04BxxAKQvD46aWgiLHOMqAf4eAXG9SLol9ywIzMxONPUOdnC7pZro8-ACQAzOY4DGtYDFm2kmwxyuJHk94nTxPpq_t_VDUFvalmwq8SeaCVSyFM5YIXI9WNAYzGDZ50iIWqCgnHbxYt1lomVUUG0F2Pr4IYOY74WkLQ-daq2dsc0CKoLdQRyFZraqDiUIXoYUoV0bSYxVU1yyRmzEIQeavp2GmhW3AfYjic_05p_1oCKN0S4g-mnSHepQuu-l8WA-l5pEHUGL4CeCZGIz7YqCMza119M8qglTSRQ5HL7hvon6IbIesnXFkKmHXuS-d5dQ8heBT4nKX4-IE43bmw1XTKheIhv2Qk24219XZCB08J4a81hTjrbQ0IpyrcwrrqrIvO0ZDCs2D-3hR48gWyfIGp6IxHtuVMWu5cIE6P4GibNsILZc4iRs1CO-BwpWhnCdVDwJS9LTmM8kF2OCgX6X2CDT16kt_qNjTd2j-otelUzsTn7mWLby-PrsCWqMSvhBSbMyFeATCwlGXbpbh9NjhwRCYc6pC5CrkHiIWxuR6NJMM2PAlv1gWg4FeKm2db_VJhNKvT4whjsf8otnelfHAUzMzMtTtQqWCJRjAKaTznCqOsbndJRD4i1HdSZLBqFh-XiHrq50Y9oTeqgh_EleFNYQ457e6jcn_4w0Ekr_NrYD6PZbvIgpky3R_ljTMxlTldtlxzzfhGNmgzyUDKpBhJEIogiThWNMVVD18PLsJO2f5aOUkAjqQ_TGARH4yTmYAVeB8c-fzkgYpLJ_b8cvkVSEK8HkgVy5003__mC0)
### Giải thích 
<ul>
  <li>PayrollController: Chịu trách nhiệm chính trong việc xử lý bảng lương (runPayroll) và xử lý các thao tác đến truy xuất employee</li>
  <li>Employee: Được sử dụng trong quá trình tính lương và có thể được liên kết với các bản ghi thời gian làm việc.</li>
  <li>PaymentMethod: Chứa thông tin về phương thức thanh toán.</li>
  <li>Timecard: Đại diện cho một thẻ chấm công</li>
  <li>ProjectManagementDatabase: Đóng vai trò như một boundary truy cập vào cơ sở dữ liệu quản lý dự án.</li>
  <li>IProjectManagementDatabase: Định nghĩa các phương thức để truy xuất thông tin từ cơ sở dữ liệu quản lý dự án.</li>
</ul>

## Câu 2 Analysis class to design element map
| Analysis Class                  | Design Element                                          |
|---------------------------------|---------------------------------------------------------|
| ProjectManagementDatabase       | ProjectManagementDatabase                               |
| EmployeeController              | EmployeeController, ValidationController                |
| Employee                        | EmployeeEntity                                          |
| SelectFunctionForm              | SelectFunctionForm                                      |
| CreateForm                      | CreatePurchaseOrderForm                                 |
| UpdateForm                      | UpdatePurchaseOrderForm                                 |
| SelectFunctionController        | SelectFunctionController                                |
| CreateController                | CreateController, ValidateController                    |
| UpdateController                | UpdateController, ValidateController                    |
| DeleteController                | DeleteController                                        |
| PurchaseOrder                   | PurchaseOrderEntity                                     |
| LoginForm                       | LoginForm                                               |
| LoginController                 | LoginController, ValidateController                     |
| User                            | EmployeeEntity, AdminEntity                             |
| AdministrativeReportForm        | AdministrativeReportForm                                |
| AdministrativeReportController  | AdministrativeReportController                          |
| Report                          | ReportEntity                                            |
| AddEmployeeForm                 | AddEmployeeForm                                         |
| UpdateEmployeeForm              | UpdateEmployeeForm                                      |
| AddEmployeeController           | AddEmployeeController, ValidateController               |
| UpdateEmployeeController        | UpdateEmployeeController, ValidateController            |
| DeleteEmployeeController        | DeleteEmployeeController                                |
| PayrollUI                       | PayrollUIComponent                                      |
| PayrollController               | PayrollController                                       |
| Printer                         | PrinterEntity                                           |
| BankSystem                      | BankSystemEntity                                        |
| Timecard                        | TimecardEntity                                          |
| TimecardForm                    | TimecardForm                                            |
| TimecardController              | TimecardController, ValidateController                  |

## Câu 3 Design element to owning package map
| Design Element                     | "Owning" Package                               |
|------------------------------------|------------------------------------------------|
| ProjectManagementDatabase          | Data Access::Project Management                |
| EmployeeController                 | Applications::Employee Management              |
| EmployeeEntity                     | Data Access::Employee Management               |
| SelectFunctionForm                 | Applications::User Interface                   |
| CreatePurchaseOrderForm            | Applications::Purchase Order Management        |
| UpdatePurchaseOrderForm            | Applications::Purchase Order Management        |
| SelectFunctionController           | Applications::User Interface                   |
| CreatePurchaseOrderController      | Applications::Purchase Order Management        |
| UpdatePurchaseOrderController      | Applications::Purchase Order Management        |
| DeletePurchaseOrderController      | Applications::Purchase Order Management        |
| PurchaseOrderEntity                | Data Access::Procurement                       |
| LoginForm                          | Middleware::Security::GUI Framework            |
| LoginController                    | Middleware::Security::Authentication           |
| AdminEntity                        | Security::User Management                      |
| AdministrativeReportForm           | Applications::Reporting                        |
| AdministrativeReportController     | Applications::Reporting                        |
| ReportEntity                       | Data Access::Reports                           |
| AddEmployeeForm                    | Applications::Employee Management              |
| UpdateEmployeeForm                 | Applications::Employee Management              |
| AddEmployeeController              | Applications::Employee Management              |
| UpdateEmployeeController           | Applications::Employee Management              |
| DeleteEmployeeController           | Applications::Employee Management              |
| PayrollUIComponent                 | Middleware::User Interface Components          |
| PayrollController                  | Applications::Payroll                          |
| PrinterEntity                      | Peripheral::Printer Devices                    |
| BankSystemEntity                   | Business::Banking                              |
| TimecardEntity                     | Data Access::Employee Activities               |
| TimecardForm                       | Applications::Employee Activities              |
| TimecardController                 | Applications::Employee Activities              |

## Câu 4 Architectural layers and their dependencies
![Architectural layers and their dependencies](https://www.planttext.com/api/plantuml/png/T991JiCm44NtFiN86rQz04Ae9M9NfAhb0iOP9LOSsvfnMaM8ax7WI5o1kBHA6gVUUF7_pFT_yk_tpvgZejYrLd1Z791d528etQWAGMv2i4QhQBo3hUgH97mA68wsYXbsgYTlRU5TJ3VIH7itBMf5vQBusWRhUyG3qj5e55-Jp9UEZSF1T14N8tVazU3nT2iLDUhckZH_oqBSatmpPMdnf6YMjEbYZIvUwkTBjxwgZAjouT1pnBQmNZSfwG7sQCyxk3Q1uGFZ2T61JJnPP0nXjNhEQi8Zo8wHfSYvdWTc5KV_3FLr-vJKQCvYatiHH9fHev269xtlTWZaZwP4XZYyLufRXlUAM5yn-83qJr4AiKPNfZ_x1m00__y30000)
