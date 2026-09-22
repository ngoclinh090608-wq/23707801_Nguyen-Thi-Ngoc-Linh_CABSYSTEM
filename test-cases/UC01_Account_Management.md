# UC-01 - Quản lý tài khoản khách hàng

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC01-001 | UC01 - Đăng ký tài khoản | [Positive] Đăng ký bằng thông tin hợp lệ | Khách hàng chưa có tài khoản và đang ở màn hình đăng ký | 1. Mở màn hình đăng ký<br>2. Nhập thông tin hợp lệ<br>3. Nhấn Đăng ký | Username: customer01<br>Password: Cab@123<br>Họ tên: Nguyễn Văn A<br>SĐT: 0900000001 | Tạo tài khoản thành công; thông tin tài khoản được lưu và mật khẩu không xuất hiện trong response | High |
| TC-UC01-002 | UC01 - Đăng nhập và cập nhật hồ sơ | [Positive] Đăng nhập rồi cập nhật thông tin cá nhân | Tài khoản customer01 đã tồn tại và đang hoạt động | 1. Mở Login<br>2. Nhập thông tin đăng nhập hợp lệ<br>3. Đăng nhập<br>4. Mở hồ sơ<br>5. Cập nhật họ tên hoặc số điện thoại<br>6. Nhấn Lưu | Username: customer01<br>Password: Cab@123<br>SĐT mới: 0900000002 | Đăng nhập thành công; hồ sơ được cập nhật và trả về đúng dữ liệu mới | High |
| TC-UC01-003 | UC01 - Đăng nhập | [Negative] Đăng nhập với password không đúng | Tài khoản customer01 tồn tại và đang hoạt động | 1. Mở Login<br>2. Nhập username đúng<br>3. Nhập password sai<br>4. Nhấn Login | Username: customer01<br>Password: Wrong@123 | Đăng nhập thất bại; không tạo phiên hoặc token; hiển thị thông báo phù hợp | High |
| TC-UC01-004 | UC01 - Cập nhật hồ sơ | [Negative] Khách hàng cập nhật hồ sơ của người khác | Khách hàng KH001 đã đăng nhập; hồ sơ KH002 tồn tại | 1. Gửi yêu cầu cập nhật hồ sơ KH002 bằng quyền của KH001 | Actor: KH001<br>Target userId: KH002 | Hệ thống từ chối truy cập; dữ liệu KH002 không thay đổi | High |
| TC-UC01-005 | UC01 - Đăng ký/Cập nhật hồ sơ | [Boundary] Nhập trường văn bản đúng giới hạn tối đa được cấu hình | Quy tắc độ dài dữ liệu đã được cấu hình | 1. Nhập họ tên hoặc thông tin liên hệ có độ dài đúng bằng giới hạn<br>2. Gửi yêu cầu | Độ dài trường = giới hạn tối đa | Hệ thống chấp nhận dữ liệu đúng giới hạn và không tự cắt nội dung | Medium |
| TC-UC01-006 | UC01 - Đăng ký/Đăng nhập | [Empty] Bỏ trống trường bắt buộc | Đang ở màn hình đăng ký hoặc đăng nhập | 1. Để trống username hoặc password<br>2. Nhấn gửi yêu cầu | Username: empty<br>Password: empty | Không tạo tài khoản hoặc phiên đăng nhập; hiển thị lỗi validation tại trường bị thiếu | High |
| TC-UC01-007 | UC01 - Đăng nhập | [Error] Dịch vụ xác thực tạm thời không phản hồi | Tài khoản hợp lệ; dịch vụ xác thực bị gián đoạn | 1. Nhập thông tin hợp lệ<br>2. Nhấn Login khi dịch vụ xác thực không phản hồi | Username: customer01<br>Password: Cab@123 | Hiển thị lỗi hệ thống rõ ràng; không tạo phiên giả; cho phép thử lại an toàn | High |
| TC-UC01-008 | UC01 - Đăng ký tài khoản | [Error] Đăng ký username đã tồn tại | Username customer01 đã được sử dụng | 1. Mở đăng ký<br>2. Nhập username trùng<br>3. Nhập các trường còn lại hợp lệ<br>4. Nhấn Đăng ký | Username: customer01<br>Password: New@123 | Từ chối tạo trùng; chỉ duy trì một tài khoản cho username; trả thông báo phù hợp | High |
