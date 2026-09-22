# UC-13 - Hỗ trợ chuyến lỗi và tra cứu giao dịch

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC13-001 | UC13 - Xử lý chuyến lỗi | [Positive] Xem danh sách chuyến cần hỗ trợ và mở chi tiết | NV001 có quyền vận hành; có chuyến lỗi | 1. Mở Failed Trips<br>2. Chọn một chuyến<br>3. Xem thông tin xử lý | OperatorId: NV001 | Trả đúng các chuyến cần hỗ trợ và chi tiết liên quan | High |
| TC-UC13-002 | UC13 - Tra cứu giao dịch | [Positive] Tra cứu lịch sử giao dịch theo mã | NV001 có quyền; PAY001 tồn tại | 1. Mở Transaction History<br>2. Nhập PAY001<br>3. Tìm kiếm | PaymentId: PAY001 | Hiển thị đúng giao dịch, số tiền, phương thức và kết quả | High |
| TC-UC13-003 | UC13 - Xử lý chuyến lỗi | [Negative] Người không có quyền xem danh sách chuyến lỗi | KH001 đã đăng nhập | 1. Gọi Failed Trips | Actor role: Customer | Từ chối truy cập; không trả dữ liệu nội bộ | High |
| TC-UC13-004 | UC13 - Tra cứu giao dịch | [Negative] Tra cứu mã giao dịch không tồn tại | NV001 có quyền | 1. Tìm kiếm mã không tồn tại | PaymentId: PAY_UNKNOWN | Thông báo không tìm thấy; không trả nhầm giao dịch | Medium |
| TC-UC13-005 | UC13 - Tra cứu giao dịch | [Boundary] Tra cứu tại đúng mốc đầu hoặc cuối khoảng thời gian | NV001 có quyền; bộ lọc thời gian đã được cấu hình | 1. Nhập khoảng thời gian<br>2. Tìm giao dịch đúng tại mốc biên | Transaction time = start/end boundary | Bao gồm bản ghi đúng theo quy tắc biên; không bỏ hoặc tính trùng | Medium |
| TC-UC13-006 | UC13 - Tra cứu giao dịch | [Empty] Bỏ trống toàn bộ tiêu chí bắt buộc | NV001 ở màn hình tra cứu | 1. Để trống mã hoặc bộ lọc bắt buộc<br>2. Nhấn Tìm kiếm | Search criteria: empty | Hiển thị lỗi validation hoặc yêu cầu bổ sung tiêu chí; không truy vấn không giới hạn | High |
| TC-UC13-007 | UC13 - Tra cứu giao dịch | [Error] Dịch vụ giao dịch không phản hồi | NV001 có quyền | 1. Tìm PAY001 khi dịch vụ thanh toán lỗi | PaymentId: PAY001 | Thông báo tra cứu thất bại; không hiển thị dữ liệu cũ như kết quả hiện tại; cho phép thử lại | High |
| TC-UC13-008 | UC13 - Xử lý chuyến lỗi | [Error] Hai nhân viên xử lý cùng một chuyến lỗi | NV001 và NV002 cùng mở TRIP_ERR_01 | 1. Hai nhân viên gửi cập nhật xử lý đồng thời<br>2. Kiểm tra trạng thái và nhật ký | TripId: TRIP_ERR_01 | Chỉ ghi nhận kết quả hợp lệ cuối cùng theo cơ chế đồng bộ; lưu vết cả hai thao tác | High |
