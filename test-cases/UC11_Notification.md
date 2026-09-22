# UC-11 - Nhận thông báo

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC11-001 | UC11 - Thông báo đặt xe | [Positive] Khách hàng nhận thông báo yêu cầu được tiếp nhận và tài xế nhận chuyến | KH001 đã đặt TRIP001 | 1. Gửi yêu cầu đặt xe<br>2. Tài xế chấp nhận<br>3. Kiểm tra thông báo của KH001 | TripId: TRIP001 | Khách hàng nhận đúng thông báo ở hai mốc với nội dung liên quan đến TRIP001 | High |
| TC-UC11-002 | UC11 - Thông báo trong và sau chuyến | [Positive] Gửi thông báo tài xế đã đến, chuyến hoàn thành và kết quả thanh toán | TRIP001 đang diễn ra | 1. Cập nhật ARRIVED_AT_PICKUP<br>2. Cập nhật COMPLETED<br>3. Xử lý thanh toán<br>4. Kiểm tra thông báo | TripId: TRIP001 | Gửi đúng thông báo cho khách hàng; tài xế nhận thông báo liên quan | High |
| TC-UC11-003 | UC11 - Xem thông báo | [Negative] Người dùng xem thông báo của tài khoản khác | KH001 đăng nhập; NOTI002 thuộc KH002 | 1. KH001 truy cập NOTI002 | Actor: KH001<br>NotificationId: NOTI002 | Từ chối truy cập; không lộ nội dung của KH002 | High |
| TC-UC11-004 | UC11 - Tạo thông báo | [Negative] Gửi thông báo tài xế đã đến khi trạng thái chưa được cập nhật | TRIP001 chưa ở ARRIVED_AT_PICKUP | 1. Kích hoạt sự kiện thông báo đã đến không hợp lệ | TripId: TRIP001 | Không gửi thông báo sai thời điểm; trạng thái chuyến không đổi | Medium |
| TC-UC11-005 | UC11 - Tạo thông báo | [Boundary] Nội dung có độ dài đúng giới hạn tối đa | Giới hạn nội dung đã được cấu hình | 1. Tạo thông báo có nội dung đúng giới hạn<br>2. Gửi thông báo | Content length = giới hạn tối đa | Chấp nhận và hiển thị đầy đủ nội dung đúng biên | Medium |
| TC-UC11-006 | UC11 - Tạo thông báo | [Empty] Thiếu người nhận hoặc nội dung | Dịch vụ thông báo đang hoạt động | 1. Gửi request thông báo thiếu trường bắt buộc | RecipientId: empty<br>Content: empty | Trả lỗi validation; không tạo thông báo không xác định người nhận | High |
| TC-UC11-007 | UC11 - Gửi thông báo | [Error] Nhà cung cấp thông báo bị gián đoạn | Sự kiện chuyến hợp lệ; nhà cung cấp không hoạt động | 1. Kích hoạt thông báo<br>2. Quan sát luồng đặt xe | TripId: TRIP001 | Ghi nhận lỗi gửi; chức năng đặt xe vẫn hoạt động; cho phép xử lý lại | High |
| TC-UC11-008 | UC11 - Gửi thông báo | [Error] Retry sau timeout tạo nguy cơ gửi trùng | Nhà cung cấp không trả xác nhận cho lần gửi đầu | 1. Gửi thông báo<br>2. Mô phỏng timeout<br>3. Thực hiện retry<br>4. Kiểm tra hộp thông báo | NotificationId: NOTI001 | Không tạo nhiều bản ghi cho cùng một sự kiện hoặc phải đánh dấu rõ trạng thái gửi | Medium |
