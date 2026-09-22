# UC-02 - Đặt xe

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC02-001 | UC02 - Tạo yêu cầu đặt xe | [Positive] Đặt xe với điểm đón, điểm đến và loại xe hợp lệ | Khách hàng đã đăng nhập | 1. Mở chức năng Đặt xe<br>2. Nhập điểm đón<br>3. Nhập điểm đến<br>4. Chọn loại xe<br>5. Gửi yêu cầu | Pickup: 10 Nguyễn Huệ<br>Destination: 100 Lê Lợi<br>VehicleType: CAR | Tạo chuyến thành công; thông báo yêu cầu đã được tiếp nhận; bắt đầu tìm tài xế | High |
| TC-UC02-002 | UC02 - Tạo yêu cầu đặt xe | [Positive] Đặt xe bằng một loại phương tiện được hỗ trợ khác | Khách hàng đã đăng nhập; loại xe được cấu hình hoạt động | 1. Nhập điểm đón và điểm đến hợp lệ<br>2. Chọn loại xe được hỗ trợ<br>3. Gửi yêu cầu | Pickup: A<br>Destination: B<br>VehicleType: BIKE | Yêu cầu được tạo đúng loại xe đã chọn | Medium |
| TC-UC02-003 | UC02 - Tạo yêu cầu đặt xe | [Negative] Người chưa xác thực gửi yêu cầu đặt xe | Người dùng chưa đăng nhập | 1. Gửi yêu cầu tạo chuyến | Pickup: A<br>Destination: B<br>VehicleType: CAR | Hệ thống yêu cầu xác thực; không tạo chuyến | High |
| TC-UC02-004 | UC02 - Tạo yêu cầu đặt xe | [Negative] Điểm đón và điểm đến giống nhau | Khách hàng đã đăng nhập | 1. Nhập cùng một địa điểm cho điểm đón và điểm đến<br>2. Gửi yêu cầu | Pickup: 10 Nguyễn Huệ<br>Destination: 10 Nguyễn Huệ | Từ chối yêu cầu không hợp lệ; yêu cầu khách hàng chọn điểm đến khác | Medium |
| TC-UC02-005 | UC02 - Tạo yêu cầu đặt xe | [Boundary] Điểm đón nằm đúng ranh giới khu vực phục vụ | Khu vực phục vụ đã được cấu hình | 1. Chọn điểm đón đúng trên ranh giới hợp lệ<br>2. Nhập điểm đến hợp lệ<br>3. Gửi yêu cầu | Pickup: điểm đúng ranh giới phục vụ | Xử lý đúng quy tắc ranh giới; chấp nhận nếu điểm thuộc khu vực phục vụ | Medium |
| TC-UC02-006 | UC02 - Tạo yêu cầu đặt xe | [Empty] Bỏ trống điểm đón hoặc điểm đến | Khách hàng đã đăng nhập | 1. Để trống một trường vị trí bắt buộc<br>2. Chọn loại xe<br>3. Gửi yêu cầu | Pickup: empty<br>Destination: B<br>VehicleType: CAR | Không tạo chuyến; hiển thị lỗi yêu cầu nhập đủ điểm đón và điểm đến | High |
| TC-UC02-007 | UC02 - Tạo yêu cầu đặt xe | [Error] Dịch vụ bản đồ không xác định được địa điểm | Khách hàng đã đăng nhập; dịch vụ bản đồ bị lỗi | 1. Nhập địa điểm<br>2. Gửi yêu cầu đặt xe | Pickup: địa chỉ hợp lệ<br>Destination: địa chỉ hợp lệ | Thông báo không thể xác định vị trí; không tạo chuyến với tọa độ sai; cho phép thử lại | High |
| TC-UC02-008 | UC02 - Tạo yêu cầu đặt xe | [Error] Lỗi lưu dữ liệu khi tạo chuyến | Khách hàng đã đăng nhập; dịch vụ lưu chuyến bị gián đoạn | 1. Nhập dữ liệu hợp lệ<br>2. Gửi yêu cầu | Pickup: A<br>Destination: B<br>VehicleType: CAR | Thông báo tạo chuyến thất bại; không lưu bản ghi chuyến dở dang hoặc trùng lặp | High |
