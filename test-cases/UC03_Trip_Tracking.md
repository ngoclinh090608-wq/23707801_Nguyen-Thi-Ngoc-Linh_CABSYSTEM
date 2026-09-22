# UC-03 - Theo dõi chuyến đi

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC03-001 | UC03 - Theo dõi quá trình tìm tài xế | [Positive] Hiển thị trạng thái từ đang tìm đến tài xế đã nhận | Khách hàng đã tạo yêu cầu đặt xe | 1. Mở chi tiết chuyến<br>2. Theo dõi khi hệ thống tìm tài xế<br>3. Chờ tài xế chấp nhận | TripId: TRIP001 | Hiển thị lần lượt trạng thái đang tìm tài xế và tài xế đã nhận chuyến | High |
| TC-UC03-002 | UC03 - Theo dõi tài xế | [Positive] Xem vị trí tài xế và thời gian dự kiến đến | TRIP001 đã được phân công tài xế | 1. Mở chi tiết TRIP001<br>2. Quan sát vị trí tài xế và ETA | TripId: TRIP001 | Hiển thị vị trí cập nhật của tài xế và thời gian dự kiến đến | High |
| TC-UC03-003 | UC03 - Xem chi tiết chuyến | [Negative] Khách hàng xem chuyến của người khác | KH001 đã đăng nhập; TRIP002 thuộc KH002 | 1. Truy cập TRIP002 bằng tài khoản KH001 | Actor: KH001<br>TripId: TRIP002 | Từ chối truy cập; không lộ vị trí hoặc thông tin chuyến của KH002 | High |
| TC-UC03-004 | UC03 - Xem chi tiết chuyến | [Negative] Theo dõi tripId không tồn tại | Khách hàng đã đăng nhập | 1. Gửi yêu cầu xem chuyến với tripId không tồn tại | TripId: TRIP_UNKNOWN | Trả thông báo không tìm thấy chuyến; không hiển thị dữ liệu giả | Medium |
| TC-UC03-005 | UC03 - Theo dõi thời gian đến | [Boundary] ETA giảm về đúng 0 khi tài xế tới điểm đón | Tài xế đang tiếp cận điểm đón | 1. Theo dõi ETA đến thời điểm tài xế cập nhật đã đến | TripId: TRIP001<br>ETA: 0 phút | Hiển thị tài xế đã đến điểm đón; không hiển thị ETA âm | Medium |
| TC-UC03-006 | UC03 - Xem chi tiết chuyến | [Empty] Request không có tripId | Khách hàng đã đăng nhập | 1. Gửi yêu cầu theo dõi nhưng bỏ tripId | TripId: empty | Trả lỗi validation; không truy vấn toàn bộ chuyến | High |
| TC-UC03-007 | UC03 - Theo dõi vị trí | [Error] Luồng cập nhật vị trí bị gián đoạn | TRIP001 đang diễn ra; dịch vụ vị trí mất kết nối | 1. Mở màn hình theo dõi<br>2. Ngắt luồng vị trí | TripId: TRIP001 | Thông báo vị trí tạm thời chưa cập nhật; không hiển thị vị trí giả; trạng thái chuyến không bị đổi | High |
| TC-UC03-008 | UC03 - Theo dõi trạng thái | [Error] Dịch vụ trạng thái chuyến trả lỗi | TRIP001 đang diễn ra | 1. Mở chi tiết chuyến khi dịch vụ trạng thái lỗi | TripId: TRIP001 | Hiển thị lỗi tải trạng thái; không tự đánh dấu chuyến hoàn thành; cho phép tải lại | High |
