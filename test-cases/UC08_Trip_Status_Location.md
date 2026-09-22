# UC-08 - Cập nhật trạng thái chuyến và vị trí

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC08-001 | UC08 - Cập nhật vị trí | [Positive] Tài xế cập nhật vị trí hợp lệ | TX001 đã xác thực và đang hoạt động | 1. Lấy tọa độ hiện tại<br>2. Gửi cập nhật vị trí | DriverId: TX001<br>Location: tọa độ hợp lệ | Lưu vị trí mới và dùng được cho tìm tài xế/ETA | High |
| TC-UC08-002 | UC08 - Cập nhật trạng thái chuyến | [Positive] Cập nhật đúng chuỗi trạng thái | TX001 được phân công TRIP001 | 1. Cập nhật ARRIVED_AT_PICKUP<br>2. Cập nhật PASSENGER_PICKED_UP<br>3. Cập nhật MOVING<br>4. Cập nhật COMPLETED | TripId: TRIP001 | Mỗi trạng thái được lưu đúng thứ tự và khách hàng nhận thông tin liên quan | High |
| TC-UC08-003 | UC08 - Cập nhật trạng thái chuyến | [Negative] Bỏ qua trạng thái bắt buộc | TRIP001 chưa cập nhật đã đón khách | 1. Gửi trực tiếp trạng thái COMPLETED | TripId: TRIP001<br>Status: COMPLETED | Từ chối chuyển trạng thái không hợp lệ; giữ nguyên trạng thái trước | High |
| TC-UC08-004 | UC08 - Cập nhật trạng thái chuyến | [Negative] Tài xế khác cập nhật chuyến không được phân công | TRIP001 thuộc TX001; TX002 đã đăng nhập | 1. TX002 gửi cập nhật trạng thái TRIP001 | Actor: TX002<br>TripId: TRIP001 | Từ chối truy cập; TRIP001 không thay đổi | High |
| TC-UC08-005 | UC08 - Cập nhật vị trí | [Boundary] Tọa độ nằm đúng ranh giới hợp lệ được cấu hình | Cấu trúc và miền tọa độ đã được xác nhận | 1. Gửi tọa độ đúng cận hợp lệ<br>2. Kiểm tra dữ liệu lưu | Location: giá trị đúng biên | Chấp nhận tọa độ đúng biên; từ chối giá trị vượt biên | Medium |
| TC-UC08-006 | UC08 - Cập nhật trạng thái/vị trí | [Empty] Payload không có status hoặc location | TX001 đã xác thực | 1. Gửi request cập nhật với payload rỗng | Payload: {} | Trả lỗi validation; không ghi bản cập nhật rỗng | High |
| TC-UC08-007 | UC08 - Cập nhật trạng thái chuyến | [Error] Cập nhật chuyến đã hoàn thành | TRIP001 đã ở trạng thái COMPLETED | 1. Gửi thêm trạng thái MOVING hoặc COMPLETED | TripId: TRIP001<br>Status: MOVING | Từ chối thay đổi trạng thái cuối; không mở lại chuyến ngoài chính sách | High |
| TC-UC08-008 | UC08 - Cập nhật vị trí | [Error] Mất kết nối khi gửi vị trí | TX001 đang thực hiện chuyến; mạng bị gián đoạn | 1. Gửi vị trí khi mất kết nối<br>2. Kết nối lại và thử lại | Location: tọa độ hợp lệ | Thông báo chưa đồng bộ; không lưu vị trí hỏng; xử lý lại theo chính sách mất kết nối TBD-05 | High |
