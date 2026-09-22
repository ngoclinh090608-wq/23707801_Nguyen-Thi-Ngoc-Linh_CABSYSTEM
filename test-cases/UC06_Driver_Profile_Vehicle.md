# UC-06 - Quản lý hồ sơ, phương tiện và trạng thái hoạt động

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC06-001 | UC06 - Quản lý hồ sơ tài xế | [Positive] Tài xế cập nhật hồ sơ hợp lệ | Tài xế TX001 đã xác thực | 1. Mở Hồ sơ tài xế<br>2. Sửa thông tin hợp lệ<br>3. Nhấn Lưu | DriverId: TX001<br>SĐT mới: 0900000011 | Cập nhật hồ sơ thành công; lưu vết thao tác quan trọng | High |
| TC-UC06-002 | UC06 - Quản lý phương tiện và trạng thái | [Positive] Thêm phương tiện rồi chuyển sang sẵn sàng | TX001 đã xác thực và phương tiện hợp lệ | 1. Thêm thông tin phương tiện<br>2. Lưu phương tiện<br>3. Chuyển trạng thái sang sẵn sàng | DriverId: TX001<br>VehicleId: XE001<br>Available: true | Phương tiện liên kết đúng TX001; trạng thái sẵn sàng được cập nhật | High |
| TC-UC06-003 | UC06 - Quản lý hồ sơ tài xế | [Negative] Khách hàng truy cập chức năng dành cho tài xế | Khách hàng KH001 đã đăng nhập | 1. Gửi yêu cầu cập nhật driverId TX001 | Actor role: Customer<br>DriverId: TX001 | Từ chối do không đúng quyền; hồ sơ tài xế không thay đổi | High |
| TC-UC06-004 | UC06 - Quản lý phương tiện | [Negative] Gắn phương tiện đã thuộc tài xế khác | XE001 đã liên kết TX002 | 1. TX001 gửi yêu cầu liên kết XE001 | DriverId: TX001<br>VehicleId: XE001 | Từ chối liên kết xung đột; giữ nguyên chủ thể hiện tại | Medium |
| TC-UC06-005 | UC06 - Quản lý hồ sơ/phương tiện | [Boundary] Nhập mã hoặc trường văn bản đúng giới hạn tối đa | Quy tắc độ dài đã được cấu hình | 1. Nhập dữ liệu có độ dài đúng giới hạn<br>2. Lưu thay đổi | Độ dài trường = giới hạn tối đa | Chấp nhận dữ liệu đúng biên và không cắt sai nội dung | Medium |
| TC-UC06-006 | UC06 - Quản lý phương tiện | [Empty] Bỏ trống thông tin phương tiện bắt buộc | TX001 đã xác thực | 1. Mở form phương tiện<br>2. Bỏ trống mã hoặc loại phương tiện<br>3. Nhấn Lưu | VehicleId: empty<br>VehicleType: empty | Không tạo phương tiện; hiển thị lỗi validation tương ứng | High |
| TC-UC06-007 | UC06 - Quản lý phương tiện | [Error] Tạo phương tiện có mã bị trùng | XE001 đã tồn tại | 1. Gửi yêu cầu tạo phương tiện XE001 | VehicleId: XE001 | Từ chối tạo trùng; chỉ tồn tại một bản ghi XE001 | High |
| TC-UC06-008 | UC06 - Cập nhật trạng thái hoạt động | [Error] Dịch vụ tài xế bị gián đoạn khi đổi trạng thái | TX001 đang không sẵn sàng | 1. Chuyển Available thành true khi dịch vụ lỗi | DriverId: TX001<br>Available: true | Thông báo cập nhật thất bại; trạng thái cũ được giữ nguyên; cho phép thử lại | High |
