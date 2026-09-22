# UC-04 - Xem lịch sử chuyến và số tiền phải trả

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC04-001 | UC04 - Xem lịch sử chuyến | [Positive] Xem danh sách các chuyến của khách hàng | Khách hàng KH001 đã đăng nhập và có lịch sử chuyến | 1. Mở Lịch sử chuyến<br>2. Tải danh sách chuyến | UserId: KH001 | Trả đúng các chuyến thuộc KH001, gồm trạng thái và thông tin liên quan | High |
| TC-UC04-002 | UC04 - Xem số tiền phải trả | [Positive] Xem số tiền của chuyến đã hoàn thành | TRIP001 thuộc KH001 và đã hoàn thành | 1. Mở lịch sử<br>2. Chọn TRIP001<br>3. Xem số tiền phải trả | TripId: TRIP001 | Hiển thị đúng số tiền đã xác định cho TRIP001 | High |
| TC-UC04-003 | UC04 - Xem lịch sử chuyến | [Negative] Khách hàng truy vấn lịch sử của người khác | KH001 đã đăng nhập; KH002 tồn tại | 1. Gửi request lịch sử với userId KH002 bằng quyền KH001 | Actor: KH001<br>Target userId: KH002 | Từ chối truy cập; không trả lịch sử của KH002 | High |
| TC-UC04-004 | UC04 - Xem số tiền phải trả | [Negative] Yêu cầu tiền cước khi chuyến chưa hoàn thành | TRIP003 đang di chuyển | 1. Gọi chức năng lấy tiền cước của TRIP003 | TripId: TRIP003 | Thông báo tiền cước chưa khả dụng; không trả số tiền tạm như số tiền cuối cùng | High |
| TC-UC04-005 | UC04 - Xem lịch sử chuyến | [Boundary] Khách hàng chưa có chuyến nào | KH_NEW đã đăng nhập và có 0 chuyến | 1. Mở Lịch sử chuyến | UserId: KH_NEW | Trả danh sách rỗng hợp lệ; không báo lỗi hệ thống | Medium |
| TC-UC04-006 | UC04 - Xem lịch sử chuyến | [Empty] Request bỏ trống userId | API lịch sử đang hoạt động | 1. Gửi request lịch sử không có userId | UserId: empty | Trả lỗi validation; không trả dữ liệu của người dùng khác | High |
| TC-UC04-007 | UC04 - Xem lịch sử chuyến | [Error] Dịch vụ lịch sử hoặc cơ sở dữ liệu không phản hồi | Khách hàng đã đăng nhập | 1. Mở lịch sử khi dịch vụ dữ liệu bị gián đoạn | UserId: KH001 | Hiển thị lỗi tải lịch sử; không trả danh sách thiếu nhưng gắn nhãn là đầy đủ | High |
| TC-UC04-008 | UC04 - Xem số tiền phải trả | [Error] Dịch vụ tính cước không trả kết quả cho chuyến hoàn thành | TRIP001 đã hoàn thành | 1. Mở TRIP001<br>2. Yêu cầu số tiền phải trả | TripId: TRIP001 | Thông báo chưa thể lấy tiền cước; không hiển thị 0 như số tiền hợp lệ; cho phép thử lại | High |
