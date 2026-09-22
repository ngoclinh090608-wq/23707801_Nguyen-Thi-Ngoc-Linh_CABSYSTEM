# UC-12 - Quản lý vận hành

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC12-001 | UC12 - Quản lý dữ liệu vận hành | [Positive] Nhân viên vận hành xem và cập nhật dữ liệu được phép | NV001 đã đăng nhập và có quyền vận hành | 1. Mở giao diện quản trị<br>2. Chọn khách hàng/tài xế/phương tiện/chuyến<br>3. Xem hoặc cập nhật dữ liệu được phép | OperatorId: NV001 | Thao tác thành công và được lưu vết | High |
| TC-UC12-002 | UC12 - Theo dõi hoạt động | [Positive] Xem chuyến đang diễn ra và trạng thái tài xế | NV001 có quyền; có dữ liệu hoạt động | 1. Mở Active Trips<br>2. Mở Driver Status | OperatorId: NV001 | Trả đúng danh sách chuyến đang diễn ra và trạng thái tài xế hiện tại | High |
| TC-UC12-003 | UC12 - Truy cập quản trị | [Negative] Khách hàng truy cập giao diện vận hành | KH001 đã đăng nhập với vai trò Customer | 1. Gọi chức năng quản trị | Actor role: Customer | Từ chối với lỗi phân quyền; không trả dữ liệu vận hành | High |
| TC-UC12-004 | UC12 - Thao tác nhạy cảm | [Negative] Nhân viên không có quyền thực hiện thao tác nhạy cảm | NV002 đăng nhập nhưng thiếu quyền tương ứng | 1. Thực hiện thao tác quản trị nhạy cảm | OperatorId: NV002 | Từ chối thao tác; dữ liệu không đổi; lưu vết lần truy cập bị từ chối | High |
| TC-UC12-005 | UC12 - Xem chuyến đang diễn ra | [Boundary] Không có chuyến đang diễn ra | NV001 có quyền; số chuyến active = 0 | 1. Mở Active Trips | Active trip count: 0 | Trả danh sách rỗng hợp lệ; giao diện không báo lỗi | Medium |
| TC-UC12-006 | UC12 - Quản lý dữ liệu | [Empty] Request cập nhật không có mã đối tượng | NV001 có quyền | 1. Gửi cập nhật nhưng bỏ userId/driverId/vehicleId/tripId | ResourceId: empty | Trả lỗi validation; không cập nhật hàng loạt ngoài ý muốn | High |
| TC-UC12-007 | UC12 - Giao diện vận hành | [Error] Một dịch vụ phụ thuộc bị lỗi | NV001 có quyền; dịch vụ thanh toán hoặc thông báo bị gián đoạn | 1. Mở các chức năng quản trị<br>2. Truy cập chức năng còn hoạt động | Dependency: Payment/Notification unavailable | Hiển thị rõ phần bị lỗi; các chức năng vận hành độc lập vẫn sử dụng được | High |
| TC-UC12-008 | UC12 - Thao tác nhạy cảm | [Error] Không thể ghi nhật ký hệ thống | NV001 thực hiện thao tác cần audit; dịch vụ nhật ký lỗi | 1. Gửi thao tác quản trị nhạy cảm<br>2. Kiểm tra kết quả | Audit service: unavailable | Không để thao tác nhạy cảm hoàn tất mà không được kiểm soát; trả lỗi hoặc cơ chế bảo đảm audit phù hợp | High |
