# UC-07 - Chấp nhận hoặc từ chối chuyến

**Tổng số test case:** 8

**Phạm vi kiểm thử:** Positive (2), Negative (2), Boundary (1), Empty (1), Error (2).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC-UC07-001 | UC07 - Phản hồi yêu cầu chuyến | [Positive] Tài xế sẵn sàng chấp nhận chuyến | TX001 ở trạng thái sẵn sàng và nhận yêu cầu TRIP001 | 1. Mở thông báo chuyến<br>2. Chọn Chấp nhận | DriverId: TX001<br>TripId: TRIP001<br>Decision: ACCEPT | Ghi nhận chấp nhận; phân công TX001; thông báo cho khách hàng | High |
| TC-UC07-002 | UC07 - Phản hồi yêu cầu chuyến | [Positive] Tài xế từ chối và hệ thống tìm tài xế khác | TX001 nhận yêu cầu TRIP001 | 1. Mở yêu cầu<br>2. Chọn Từ chối<br>3. Theo dõi quá trình ghép tiếp | DriverId: TX001<br>TripId: TRIP001<br>Decision: REJECT | Ghi nhận từ chối; khách hàng không phải đặt lại; hệ thống tiếp tục tìm tài xế | High |
| TC-UC07-003 | UC07 - Phản hồi yêu cầu chuyến | [Negative] Tài xế không sẵn sàng chấp nhận chuyến | TX001 có Available=false | 1. Gửi ACCEPT cho TRIP001 | DriverId: TX001<br>TripId: TRIP001<br>Decision: ACCEPT | Từ chối phản hồi vì tài xế không đủ điều kiện nhận chuyến | High |
| TC-UC07-004 | UC07 - Phản hồi yêu cầu chuyến | [Negative] Tài xế phản hồi yêu cầu được gửi cho tài xế khác | TRIP001 đang chờ phản hồi của TX002 | 1. TX001 gửi ACCEPT cho TRIP001 | DriverId: TX001<br>TripId: TRIP001 | Từ chối do không đúng tài xế; không thay đổi phân công | High |
| TC-UC07-005 | UC07 - Phản hồi yêu cầu chuyến | [Boundary] Phản hồi đúng thời điểm hết hạn | Thời gian phản hồi đã được xác nhận theo TBD-03 | 1. Gửi ACCEPT đúng mốc hết hạn<br>2. Kiểm tra kết quả | Response time = thời hạn cấu hình | Xử lý nhất quán theo quy tắc biên đã cấu hình; không vừa nhận vừa chuyển cho tài xế khác | Medium |
| TC-UC07-006 | UC07 - Phản hồi yêu cầu chuyến | [Empty] Request không có decision | TX001 đang được mời nhận TRIP001 | 1. Gửi request phản hồi nhưng bỏ decision | DriverId: TX001<br>TripId: TRIP001<br>Decision: empty | Trả lỗi validation; chuyến vẫn ở trạng thái chờ hoặc tiếp tục theo quy tắc thời gian | High |
| TC-UC07-007 | UC07 - Phản hồi yêu cầu chuyến | [Error] Hai phản hồi được gửi đồng thời | TRIP001 đang chờ phản hồi; có request cạnh tranh | 1. Gửi ACCEPT và REJECT gần như đồng thời<br>2. Kiểm tra trạng thái cuối | TripId: TRIP001<br>Concurrent decisions: ACCEPT/REJECT | Chỉ một phản hồi hợp lệ được ghi nhận; trạng thái chuyến không mâu thuẫn | High |
| TC-UC07-008 | UC07 - Phản hồi yêu cầu chuyến | [Error] Dịch vụ ghi nhận phản hồi không hoạt động | TX001 nhận TRIP001; dịch vụ bị gián đoạn | 1. Chọn ACCEPT<br>2. Quan sát phản hồi hệ thống | DriverId: TX001<br>TripId: TRIP001 | Thông báo phản hồi chưa được ghi nhận; không hiển thị đã nhận chuyến khi dữ liệu chưa lưu | High |
