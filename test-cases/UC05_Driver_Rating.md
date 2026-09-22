# UC-05 - Đánh giá tài xế

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC05-001 | UC05 - Gửi đánh giá | [Positive] Khách hàng đánh giá tài xế sau chuyến hoàn thành | TRIP001 thuộc KH001 và đã hoàn thành; chưa có đánh giá | 1. Mở chi tiết TRIP001<br>2. Chọn mức đánh giá hợp lệ<br>3. Nhập nhận xét<br>4. Nhấn Gửi | TripId: TRIP001<br>Rating: giá trị hợp lệ<br>Comment: Tài xế lịch sự | Tạo đánh giá thành công và liên kết đúng khách hàng, chuyến, tài xế | High |
| TC-UC05-002 | UC05 - Xem đánh giá | [Positive] Xem lại đánh giá đã gửi | TRIP001 đã có đánh giá | 1. Mở chi tiết TRIP001<br>2. Xem phần đánh giá | TripId: TRIP001 | Hiển thị đúng mức đánh giá và nhận xét đã lưu | Medium |
| TC-UC05-003 | UC05 - Gửi đánh giá | [Negative] Đánh giá trước khi chuyến hoàn thành | TRIP003 đang di chuyển | 1. Mở TRIP003<br>2. Gửi đánh giá | TripId: TRIP003<br>Rating: giá trị hợp lệ | Từ chối đánh giá vì chuyến chưa hoàn thành | High |
| TC-UC05-004 | UC05 - Gửi đánh giá | [Negative] Gửi đánh giá lần hai cho cùng chuyến | TRIP001 đã có một đánh giá của KH001 | 1. Gửi thêm đánh giá cho TRIP001 | TripId: TRIP001<br>Rating: giá trị hợp lệ khác | Không tạo đánh giá trùng; xử lý theo chính sách cập nhật được xác nhận | Medium |
| TC-UC05-005 | UC05 - Gửi đánh giá | [Boundary] Gửi mức đánh giá tại giá trị thấp nhất và cao nhất được cấu hình | Thang điểm đánh giá đã được cấu hình | 1. Lần lượt gửi giá trị đúng cận dưới và cận trên | Rating: min và max hợp lệ | Chấp nhận cả hai giá trị đúng biên; không chấp nhận giá trị ngoài biên | Medium |
| TC-UC05-006 | UC05 - Gửi đánh giá | [Empty] Bỏ trống mức đánh giá bắt buộc | TRIP001 đã hoàn thành và chưa được đánh giá | 1. Mở form đánh giá<br>2. Để trống mức đánh giá<br>3. Nhấn Gửi | TripId: TRIP001<br>Rating: empty | Không tạo đánh giá; hiển thị lỗi yêu cầu chọn mức đánh giá | High |
| TC-UC05-007 | UC05 - Gửi đánh giá | [Error] tripId không tồn tại hoặc không thuộc khách hàng | Khách hàng đã đăng nhập | 1. Gửi đánh giá với tripId không hợp lệ | TripId: TRIP_UNKNOWN<br>Rating: giá trị hợp lệ | Trả lỗi phù hợp; không tạo bản ghi đánh giá | High |
| TC-UC05-008 | UC05 - Gửi đánh giá | [Error] Dịch vụ lưu đánh giá bị lỗi | TRIP001 hợp lệ và chưa có đánh giá | 1. Gửi đánh giá khi dịch vụ lưu dữ liệu không phản hồi | TripId: TRIP001<br>Rating: giá trị hợp lệ | Thông báo gửi thất bại; không tạo bản ghi một phần hoặc đánh giá trùng khi thử lại | High |
