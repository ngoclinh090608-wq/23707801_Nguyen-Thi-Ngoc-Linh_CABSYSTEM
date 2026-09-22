# UC-09 - Tìm và phân công tài xế

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC09-001 | UC09 - Tìm tài xế | [Positive] Ưu tiên tài xế phù hợp và gần khách hàng | TRIP001 đang chờ; TX001 và TX002 đều sẵn sàng | 1. Khởi chạy ghép tài xế<br>2. So sánh kết quả với vị trí và tiêu chí vận hành | TripId: TRIP001<br>TX001 gần hơn TX002 | Chọn tài xế phù hợp, sẵn sàng và được ưu tiên theo quy tắc vận hành | High |
| TC-UC09-002 | UC09 - Tìm lại tài xế | [Positive] Tiếp tục tìm khi tài xế đầu tiên từ chối | TX001 và TX002 phù hợp; TX001 được mời trước | 1. TX001 từ chối<br>2. Theo dõi hệ thống tiếp tục tìm | TripId: TRIP001 | Hệ thống gửi yêu cầu cho TX002; khách hàng không phải tạo lại chuyến | High |
| TC-UC09-003 | UC09 - Tìm tài xế | [Negative] Không có tài xế phù hợp | Không có tài xế sẵn sàng trong phạm vi/tiêu chí | 1. Khởi chạy ghép tài xế | TripId: TRIP001 | Không phân công; thông báo rõ ràng cho khách hàng | High |
| TC-UC09-004 | UC09 - Tìm tài xế | [Negative] Tài xế bận vẫn xuất hiện trong danh sách ứng viên | TX_BUSY có Available=false hoặc đang có chuyến | 1. Khởi chạy ghép<br>2. Kiểm tra danh sách ứng viên | DriverId: TX_BUSY | Loại TX_BUSY khỏi kết quả; không gửi yêu cầu chuyến | High |
| TC-UC09-005 | UC09 - Xếp hạng tài xế | [Boundary] Hai tài xế có khoảng cách bằng nhau | TX001 và TX002 đều hợp lệ và cách khách hàng bằng nhau | 1. Khởi chạy ghép<br>2. Quan sát tiêu chí phân xử | Distance TX001 = Distance TX002<br>Available: true | Áp dụng tiêu chí ưu tiên tiếp theo theo đúng thứ tự đã cấu hình; kết quả xác định được | Medium |
| TC-UC09-006 | UC09 - Tìm tài xế | [Empty] Chuyến không có vị trí đón | TRIP001 tồn tại nhưng pickup bị thiếu | 1. Gọi chức năng match cho TRIP001 | TripId: TRIP001<br>Pickup: empty | Từ chối ghép do thiếu dữ liệu vị trí; không gửi yêu cầu cho tài xế | High |
| TC-UC09-007 | UC09 - Tìm tài xế | [Error] Quá trình tìm tài xế bị timeout | Có tài xế tiềm năng nhưng dịch vụ ghép bị gián đoạn | 1. Khởi chạy ghép<br>2. Chờ đến khi timeout | TripId: TRIP001 | Thông báo trạng thái phù hợp; không yêu cầu khách đặt lại; không tạo phân công nửa chừng | High |
| TC-UC09-008 | UC09 - Phân công tài xế | [Error] Hai tiến trình cùng phân công cho một chuyến | TRIP001 đang chờ và hai tiến trình ghép chạy đồng thời | 1. Thực hiện hai yêu cầu match đồng thời<br>2. Kiểm tra chuyến | TripId: TRIP001 | Chỉ một tài xế được phân công; dữ liệu và thông báo không bị trùng | High |
