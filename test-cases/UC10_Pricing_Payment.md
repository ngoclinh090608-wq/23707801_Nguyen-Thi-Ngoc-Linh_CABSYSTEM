# UC-10 - Tính cước và thanh toán

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC10-001 | UC10 - Thanh toán tiền mặt | [Positive] Ghi nhận thanh toán tiền mặt sau chuyến | TRIP001 đã hoàn thành và có số tiền phải trả | 1. Chọn CASH<br>2. Xác nhận thanh toán<br>3. Kiểm tra giao dịch | TripId: TRIP001<br>Method: CASH<br>Amount: số tiền đã tính | Ghi nhận giao dịch tiền mặt và lưu lịch sử chuyến | High |
| TC-UC10-002 | UC10 - Thanh toán điện tử | [Positive] Thanh toán điện tử thành công | TRIP001 đã hoàn thành; nhà cung cấp thanh toán hoạt động | 1. Chọn ELECTRONIC<br>2. Gửi thanh toán<br>3. Nhận kết quả thành công | TripId: TRIP001<br>Method: ELECTRONIC<br>Amount: số tiền đã tính | Ghi nhận thành công; không lưu trực tiếp thông tin nhạy cảm của thẻ/tài khoản | High |
| TC-UC10-003 | UC10 - Tính cước | [Negative] Lấy cước khi chuyến chưa hoàn thành | TRIP003 đang di chuyển | 1. Gọi lấy amount due | TripId: TRIP003 | Trả trạng thái xung đột hoặc thông báo cước chưa khả dụng; không tạo thanh toán | High |
| TC-UC10-004 | UC10 - Tạo thanh toán | [Negative] Sử dụng phương thức không được hỗ trợ | TRIP001 đã hoàn thành | 1. Gửi thanh toán với method không hợp lệ | TripId: TRIP001<br>Method: CRYPTO | Từ chối request; không tạo giao dịch | Medium |
| TC-UC10-005 | UC10 - Tính cước | [Boundary] Số tiền đúng tại cận cấu hình của loại dịch vụ | Công thức và mức cận đã được xác nhận theo TBD-01 | 1. Hoàn thành chuyến có dữ liệu tạo ra giá trị đúng cận<br>2. Lấy tiền cước | Amount = cận hợp lệ | Trả đúng số tiền theo công thức; không làm tròn sai hoặc chuyển thành 0 | Medium |
| TC-UC10-006 | UC10 - Tạo thanh toán | [Empty] Bỏ trống tripId hoặc method | API thanh toán đang hoạt động | 1. Gửi request thanh toán thiếu trường bắt buộc | TripId: empty<br>Method: empty | Trả lỗi validation; không tạo giao dịch | High |
| TC-UC10-007 | UC10 - Thanh toán điện tử | [Error] Nhà cung cấp từ chối giao dịch và khách hàng thử lại | Thanh toán PAY001 ở trạng thái thất bại | 1. Gửi thanh toán điện tử<br>2. Nhận thất bại<br>3. Thực hiện Retry | PaymentId: PAY001 | Thông báo thất bại; cho phép xử lý lại theo chính sách; lưu đúng kết quả mỗi lần | High |
| TC-UC10-008 | UC10 - Thanh toán điện tử | [Error] Nhà cung cấp timeout khi đã nhận request | TRIP001 đã hoàn thành; kết nối nhà cung cấp chập chờn | 1. Gửi thanh toán<br>2. Mô phỏng timeout<br>3. Kiểm tra trạng thái và thử lại | TripId: TRIP001 | Không ghi nhận thành công khi chưa xác minh; không thu tiền hai lần; hiển thị trạng thái cần xử lý | High |
