# UC-14 - Xem báo cáo hoạt động

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC14-001 | UC14 - Xem báo cáo tổng hợp | [Positive] Xem đầy đủ các chỉ số hoạt động | Người dùng có quyền xem báo cáo; có dữ liệu | 1. Mở Reports<br>2. Chọn khoảng thời gian<br>3. Tải báo cáo | Period: khoảng hợp lệ | Hiển thị số chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả tài xế | High |
| TC-UC14-002 | UC14 - Lọc báo cáo | [Positive] Xem báo cáo theo thời gian hoặc tài xế | Người dùng có quyền; dữ liệu phù hợp tồn tại | 1. Chọn bộ lọc<br>2. Tải báo cáo<br>3. Đối chiếu dữ liệu | Period: hợp lệ<br>DriverId: TX001 | Chỉ số được tính đúng trên tập dữ liệu đã lọc | High |
| TC-UC14-003 | UC14 - Truy cập báo cáo | [Negative] Người dùng không có quyền xem báo cáo | KH001 đăng nhập với vai trò Customer | 1. Gọi Reports | Actor role: Customer | Từ chối truy cập; không trả dữ liệu doanh thu hoặc hiệu quả hoạt động | High |
| TC-UC14-004 | UC14 - Lọc báo cáo | [Negative] Ngày bắt đầu lớn hơn ngày kết thúc | Người dùng có quyền xem báo cáo | 1. Nhập khoảng ngày không hợp lệ<br>2. Tải báo cáo | From: 2026-09-30<br>To: 2026-09-01 | Trả lỗi validation; không tạo báo cáo sai | Medium |
| TC-UC14-005 | UC14 - Tính chỉ số báo cáo | [Boundary] Khoảng thời gian không có chuyến | Người dùng có quyền; số chuyến trong kỳ = 0 | 1. Chọn kỳ không có dữ liệu<br>2. Tải báo cáo | Trip count: 0 | Trả số chuyến và doanh thu bằng 0; tỷ lệ hiển thị 0 hoặc n.a. theo quy ước; không phát sinh lỗi chia cho 0 | Medium |
| TC-UC14-006 | UC14 - Lọc báo cáo | [Empty] Bỏ trống khoảng thời gian bắt buộc | Màn hình báo cáo yêu cầu kỳ báo cáo | 1. Để trống From/To<br>2. Nhấn Tải báo cáo | From: empty<br>To: empty | Hiển thị lỗi yêu cầu nhập kỳ; không chạy truy vấn không giới hạn | High |
| TC-UC14-007 | UC14 - Tổng hợp báo cáo | [Error] Một nguồn dữ liệu đầu vào không khả dụng | Người dùng có quyền; dịch vụ chuyến hoặc thanh toán bị lỗi | 1. Tải báo cáo<br>2. Mô phỏng nguồn dữ liệu lỗi | Dependency: Trip/Payment unavailable | Thông báo báo cáo chưa đầy đủ hoặc không thể tạo; không trình bày số liệu thiếu như số liệu hoàn chỉnh | High |
| TC-UC14-008 | UC14 - Tổng hợp báo cáo | [Error] Truy vấn báo cáo bị timeout | Khối lượng dữ liệu lớn; dịch vụ báo cáo đang hoạt động chậm | 1. Gửi yêu cầu báo cáo<br>2. Chờ đến timeout | Report request: valid | Trả lỗi timeout rõ ràng; không treo giao diện; cho phép người dùng thử lại | High |
