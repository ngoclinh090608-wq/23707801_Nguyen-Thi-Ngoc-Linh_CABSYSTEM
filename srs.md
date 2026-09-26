
## 1. Stakeholder List & Roles (Danh sách & Vai trò Bên liên quan)

| STT | Tên Stakeholder | Vai trò |
|---|---|---|
| 1 | Ban lãnh đạo / Ban giám đốc | Mong muốn xây dựng nền tảng CAB mới có khả năng phục vụ số lượng lớn khách hàng và tài xế, có thể phát triển thêm tính năng trong tương lai. Kỳ vọng hệ thống hỗ trợ ít nhất ba nhóm người dùng chính gồm khách hàng, tài xế và nhân viên vận hành. Mong muốn có báo cáo về số lượng chuyến, doanh thu, tỷ lệ chuyến hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế |
| 2 | Khách hàng | Đăng ký tài khoản, đăng nhập, cập nhật thông tin cá nhân. Nhập điểm đón và điểm đến, lựa chọn loại xe, gửi yêu cầu đặt xe và theo dõi chuyến đi. Muốn biết hệ thống đang tìm tài xế, tài xế nào đã nhận chuyến, thời gian dự kiến tài xế đến và trạng thái hiện tại của chuyến đi. Thanh toán bằng tiền mặt hoặc phương thức thanh toán điện tử. Xem lịch sử chuyến đi, số tiền phải trả và đánh giá tài xế sau khi hoàn thành chuyến. |
| 3 | Tài xế | Đăng ký hoặc được nhân viên vận hành tạo tài khoản. Cập nhật hồ sơ, thông tin phương tiện và trạng thái hoạt động; chuyển sang trạng thái sẵn sàng nhận chuyến khi đang làm việc. Nhận thông báo, chấp nhận hoặc từ chối chuyến. Cập nhật trạng thái: đã đến điểm đón, đã đón khách, đang di chuyển và hoàn thành chuyến. |
| 4 | Nhân viên vận hành | Sử dụng giao diện quản trị để quản lý khách hàng, tài xế, phương tiện và chuyến đi. Tạo tài khoản cho tài xế. Xem các chuyến đang diễn ra, kiểm tra trạng thái tài xế, hỗ trợ xử lý các trường hợp chuyến bị lỗi và tra cứu lịch sử giao dịch. Một số chức năng quản trị được phân quyền để nhân viên thông thường không thể thực hiện các thao tác nhạy cảm. |
| 5 | Nhà cung cấp thanh toán bên ngoài | Doanh nghiệp muốn tích hợp với nhà cung cấp thanh toán bên ngoài, nhưng không muốn thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán được lưu trực tiếp trong hệ thống CAB. |
| 6 | Business Analyst | Làm rõ với các bên liên quan về cách tính cước, tiêu chí ưu tiên tài xế, thời gian tài xế phải phản hồi, chính sách hủy chuyến, cách xử lý khi mất kết nối mạng và thời gian lưu trữ dữ liệu. Xác định phạm vi, tác nhân, quy trình nghiệp vụ, yêu cầu chức năng, yêu cầu phi chức năng, quy tắc nghiệp vụ, các trường hợp ngoại lệ và những điểm còn chưa rõ cần xác nhận với khách hàng. |
| 7 | Nhóm phát triển | Xây dựng giải pháp sau khi Business Analyst làm rõ các vấn đề chưa chốt. |

## 2. Stakeholder Matrix (Ma trận Bên liên quan)

| STT | Stakeholder | Ảnh hưởng (Influence) | Quan tâm (Interest) | Nhóm | Căn cứ trong đề |
|---|---|---|---|---|---|
| 1 | Ban lãnh đạo / Ban giám đốc | Cao | Cao | Key Decision Makers | "Ban lãnh đạo mong muốn xây dựng một nền tảng CAB mới…"; "Ban giám đốc kỳ vọng hệ thống mới hỗ trợ ít nhất ba nhóm người dùng chính"; "Ban lãnh đạo cũng mong muốn có báo cáo về số lượng chuyến, doanh thu…" |
| 2 | Khách hàng | Thấp | Cao | Engaged Supporters | Sử dụng trực tiếp hệ thống để đặt xe, theo dõi chuyến, thanh toán; "khách hàng muốn biết hệ thống đang tìm tài xế, tài xế nào đã nhận chuyến…"; không tham gia quyết định yêu cầu |
| 3 | Tài xế | Thấp | Cao | Engaged Supporters | Sử dụng trực tiếp hệ thống để nhận thông báo, chấp nhận hoặc từ chối chuyến, cập nhật trạng thái chuyến; không tham gia quyết định yêu cầu |
| 4 | Nhân viên vận hành | Thấp | Cao | Engaged Supporters | Sử dụng giao diện quản trị để quản lý khách hàng, tài xế, phương tiện, chuyến đi; "bộ phận vận hành gặp khó khăn khi muốn mở rộng hệ thống"; nhân viên thông thường không thể thực hiện thao tác nhạy cảm |
| 5 | Business Analyst | Thấp | Cao | Engaged Supporters | "Khách hàng mong muốn Business Analyst làm rõ các vấn đề này với các bên liên quan", tức BA làm rõ, không phải người chốt yêu cầu; chịu trách nhiệm xác định phạm vi, tác nhân, quy trình, yêu cầu… |
| 6 | Nhóm phát triển | Thấp | Cao | Engaged Supporters | Xây dựng giải pháp sau khi Business Analyst làm rõ các vấn đề chưa chốt; không tham gia quyết định yêu cầu |
| 7 | Nhà cung cấp thanh toán bên ngoài | Cao | Thấp | Potential Influencers | "Doanh nghiệp muốn tích hợp với một nhà cung cấp thanh toán bên ngoài"; thanh toán điện tử phụ thuộc vào nhà cung cấp; "không muốn một lỗi xảy ra ở chức năng thanh toán… làm cho toàn bộ hệ thống đặt xe ngừng hoạt động"; đề không nêu mong muốn nào của nhà cung cấp đối với dự án |

> **Minimal Impact Stakeholders:** không có stakeholder nào trong đề thuộc nhóm này.

### Sơ đồ Stakeholder Matrix

```mermaid
quadrantChart
    title Stakeholder Analysis Matrix - Hệ thống CAB
    x-axis Low Influence --> High Influence
    y-axis Low Interest --> High Interest
    quadrant-1 Key Decision Makers
    quadrant-2 Engaged Supporters
    quadrant-3 Minimal Impact Stakeholders
    quadrant-4 Potential Influencers
    "Ban lãnh đạo / Ban giám đốc": [0.80, 0.88]
    "Khách hàng": [0.12, 0.92]
    "Tài xế": [0.28, 0.80]
    "Nhân viên vận hành": [0.16, 0.68]
    "Business Analyst": [0.40, 0.90]
    "Nhóm phát triển": [0.36, 0.58]
    "Nhà cung cấp thanh toán bên ngoài": [0.75, 0.25]
```
## 3. Business Goals (Mục tiêu kinh doanh/ nghiệp vụ)

| Mã BR | Mục tiêu nghiệp vụ | Nguồn | Căn cứ trong đề |
|---|---|---|---|
| BR-01 | Tự động hóa việc tìm và phân công tài xế, ưu tiên tài xế phù hợp và gần khách hàng. | Công ty ABC | "việc phân công tài xế chủ yếu được thực hiện thủ công"; "Doanh nghiệp mong muốn hệ thống ưu tiên tài xế phù hợp và gần khách hàng" |
| BR-02 | Giúp khách hàng theo dõi được trạng thái chuyến đi và nhận thông báo trong suốt quá trình đặt xe. | Công ty ABC | "khách hàng khó theo dõi trạng thái chuyến đi"; "khách hàng muốn biết hệ thống đang tìm tài xế, tài xế nào đã nhận chuyến, thời gian dự kiến tài xế đến và trạng thái hiện tại của chuyến đi"; "Thông báo là một thành phần quan trọng" |
| BR-03 | Quản lý tập trung thông tin thanh toán và tính cước. | Công ty ABC | "thông tin thanh toán chưa được quản lý tập trung"; "Hệ thống cũng phải hỗ trợ thanh toán và tính cước" |
| BR-04 | Phục vụ số lượng lớn khách hàng và tài xế, mở rộng được khi tải tăng. | Ban lãnh đạo, Công ty ABC | "bộ phận vận hành gặp khó khăn khi muốn mở rộng hệ thống"; "Ban lãnh đạo mong muốn xây dựng một nền tảng CAB mới có khả năng phục vụ số lượng lớn khách hàng và tài xế"; "Các thành phần của hệ thống cần có khả năng mở rộng độc lập khi tải tăng" |
| BR-05 | Xây dựng nền tảng phát triển lâu dài, bổ sung được tính năng mới mà không phải xây dựng lại toàn bộ ứng dụng. | Ban lãnh đạo, Công ty ABC | "có thể phát triển thêm các tính năng trong tương lai"; "bổ sung các loại dịch vụ mới, thêm phương thức thanh toán, thêm nhà cung cấp thông báo hoặc thay đổi một số thành phần kỹ thuật mà không phải xây dựng lại toàn bộ ứng dụng"; "muốn một nền tảng CAB có thể phát triển lâu dài" |
| BR-06 | Hỗ trợ ba nhóm người dùng chính: khách hàng, tài xế và nhân viên vận hành. | Ban giám đốc | "Ban giám đốc kỳ vọng hệ thống mới hỗ trợ ít nhất ba nhóm người dùng chính gồm khách hàng, tài xế và nhân viên vận hành" |
| BR-07 | Đáp ứng trọn vẹn quy trình từ khi khách hàng tạo yêu cầu đến khi đánh giá sau chuyến. | Công ty ABC | "Hệ thống cần đáp ứng tốt quy trình từ khi khách hàng tạo yêu cầu, tìm và phân công tài xế, thực hiện chuyến, tính cước, thanh toán, thông báo đến đánh giá sau chuyến" |
| BR-08 | Cung cấp đủ dữ liệu và báo cáo để theo dõi hoạt động kinh doanh. | Ban lãnh đạo, Công ty ABC | "Ban lãnh đạo cũng mong muốn có báo cáo về số lượng chuyến, doanh thu, tỷ lệ chuyến hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế"; "có đủ dữ liệu để theo dõi hoạt động" |
| BR-09 | Giúp các bộ phận trong doanh nghiệp phối hợp thông qua hệ thống. | Công ty ABC | "Các bộ phận trong doanh nghiệp phải có thể phối hợp thông qua hệ thống" |
| BR-10 | Duy trì dịch vụ đặt xe ổn định, kể cả vào thời điểm nhu cầu tăng cao. | Công ty ABC | "Hệ thống phải hoạt động ổn định vào các thời điểm nhu cầu tăng cao"; "Doanh nghiệp không muốn một lỗi xảy ra ở chức năng thanh toán hoặc thông báo làm cho toàn bộ hệ thống đặt xe ngừng hoạt động" |
| BR-11 | Bảo vệ dữ liệu cá nhân, phương tiện, vị trí và giao dịch; kiểm soát được các thao tác quan trọng. | Công ty ABC | "Thông tin cá nhân, thông tin phương tiện, dữ liệu vị trí và dữ liệu giao dịch phải được bảo vệ"; "không muốn thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán được lưu trực tiếp trong hệ thống CAB"; "Doanh nghiệp cần lưu vết các thao tác quan trọng để phục vụ kiểm tra khi có sự cố" |

## 4. Minimum Viable Product (MVP) Modules

| STT | Module | Chức năng chính |
|---|---|---|
| 1 | Quản lý tài khoản khách hàng | Đăng ký tài khoản, đăng nhập, cập nhật thông tin cá nhân. Khách hàng phải được xác thực trước khi sử dụng các chức năng yêu cầu tài khoản. *(BR-06, BR-11)* |
| 2 | Quản lý tài xế và phương tiện | Tài xế đăng ký hoặc được nhân viên vận hành tạo tài khoản; cập nhật hồ sơ, thông tin phương tiện và trạng thái hoạt động; chuyển sang trạng thái sẵn sàng nhận chuyến khi đang làm việc. Lưu thông tin vị trí của tài xế để hỗ trợ việc tìm tài xế gần khách hàng và cải thiện khả năng dự kiến thời gian đến. Tài xế phải được xác thực trước khi sử dụng các chức năng yêu cầu tài khoản. *(BR-01, BR-06, BR-11)* |
| 3 | Đặt xe | Nhập điểm đón và điểm đến, lựa chọn loại xe, gửi yêu cầu đặt xe. *(BR-07)* |
| 4 | Tìm và phân công tài xế | Xác định các tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và một số tiêu chí vận hành khác; ưu tiên tài xế phù hợp và gần khách hàng. Khi có yêu cầu phù hợp, tài xế nhận được thông báo và có thể chấp nhận hoặc từ chối chuyến. Nếu tài xế được đề xuất không phản hồi hoặc từ chối, hệ thống tiếp tục tìm tài xế khác mà không yêu cầu khách hàng tạo lại yêu cầu. Không tìm được tài xế thì khách hàng phải được thông báo rõ ràng. *(BR-01)* |
| 5 | Thực hiện và theo dõi chuyến đi | Tài xế cập nhật trạng thái: đã đến điểm đón, đã đón khách, đang di chuyển và hoàn thành chuyến. Khách hàng theo dõi chuyến đi: hệ thống đang tìm tài xế, tài xế nào đã nhận chuyến, thời gian dự kiến tài xế đến và trạng thái hiện tại của chuyến đi. Khách hàng xem lịch sử chuyến đi và số tiền phải trả. *(BR-02, BR-07)* |
| 6 | Tính cước và thanh toán | Sau khi chuyến đi hoàn thành, xác định số tiền khách hàng phải trả dựa trên loại dịch vụ và thông tin chuyến đi. Khách hàng thanh toán bằng tiền mặt hoặc phương thức thanh toán điện tử. Tích hợp với nhà cung cấp thanh toán bên ngoài; thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán không được lưu trực tiếp trong hệ thống CAB. Giao dịch thanh toán điện tử thất bại thì thông báo cho khách hàng và cho phép xử lý lại theo chính sách của doanh nghiệp. *(BR-03, BR-07, BR-11)* |
| 7 | Thông báo | Thông báo cho khách hàng khi yêu cầu đặt xe được tiếp nhận, khi có tài xế nhận chuyến, khi tài xế đến điểm đón, khi chuyến hoàn thành và khi thanh toán có kết quả. Thông báo cho tài xế về các chuyến mới hoặc những thay đổi liên quan đến chuyến đang thực hiện. *(BR-02, BR-07)* |
| 8 | Đánh giá tài xế | Khách hàng đánh giá tài xế sau khi hoàn thành chuyến. *(BR-07)* |
| 9 | Quản trị vận hành | Giao diện quản trị để quản lý khách hàng, tài xế, phương tiện và chuyến đi. Xem các chuyến đang diễn ra, kiểm tra trạng thái tài xế, hỗ trợ xử lý các trường hợp chuyến bị lỗi và tra cứu lịch sử giao dịch. Một số chức năng quản trị được phân quyền để nhân viên thông thường không thể thực hiện các thao tác nhạy cảm. *(BR-06, BR-11)* |
| 10 | Báo cáo | Báo cáo về số lượng chuyến, doanh thu, tỷ lệ chuyến hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế. *(BR-08)* |

> **Ngoài phạm vi MVP (đề ghi "trong tương lai"):** bổ sung các loại dịch vụ mới, thêm phương thức thanh toán, thêm nhà cung cấp thông báo, mở rộng thêm các kênh thông báo, thay đổi một số thành phần kỹ thuật. *(BR-05)*

## 4. Minimum Viable Product (MVP) Modules

| STT | Module | Chức năng chính |
|---|---|---|
| 1 | Quản lý tài khoản khách hàng | Đăng ký tài khoản, đăng nhập, cập nhật thông tin cá nhân. Khách hàng phải được xác thực trước khi sử dụng các chức năng yêu cầu tài khoản. *(BR-06, BR-11)* |
| 2 | Quản lý tài xế và phương tiện | Tài xế đăng ký hoặc được nhân viên vận hành tạo tài khoản; cập nhật hồ sơ, thông tin phương tiện và trạng thái hoạt động; chuyển sang trạng thái sẵn sàng nhận chuyến khi đang làm việc. Lưu thông tin vị trí của tài xế để hỗ trợ việc tìm tài xế gần khách hàng và cải thiện khả năng dự kiến thời gian đến. Tài xế phải được xác thực trước khi sử dụng các chức năng yêu cầu tài khoản. *(BR-01, BR-06, BR-11)* |
| 3 | Đặt xe và chuyến đi | **Đặt xe:** nhập điểm đón và điểm đến, lựa chọn loại xe, gửi yêu cầu đặt xe. **Tìm và phân công tài xế:** xác định các tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và một số tiêu chí vận hành khác; ưu tiên tài xế phù hợp và gần khách hàng; khi có yêu cầu phù hợp, tài xế nhận được thông báo và có thể chấp nhận hoặc từ chối chuyến; nếu tài xế được đề xuất không phản hồi hoặc từ chối, hệ thống tiếp tục tìm tài xế khác mà không yêu cầu khách hàng tạo lại yêu cầu; không tìm được tài xế thì khách hàng phải được thông báo rõ ràng. **Thực hiện và theo dõi chuyến đi:** tài xế cập nhật trạng thái đã đến điểm đón, đã đón khách, đang di chuyển và hoàn thành chuyến; khách hàng theo dõi hệ thống đang tìm tài xế, tài xế nào đã nhận chuyến, thời gian dự kiến tài xế đến và trạng thái hiện tại của chuyến đi; xem lịch sử chuyến đi và số tiền phải trả. **Đánh giá:** khách hàng đánh giá tài xế sau khi hoàn thành chuyến. *(BR-01, BR-02, BR-07)* |
| 4 | Tính cước và thanh toán | Sau khi chuyến đi hoàn thành, xác định số tiền khách hàng phải trả dựa trên loại dịch vụ và thông tin chuyến đi. Khách hàng thanh toán bằng tiền mặt hoặc phương thức thanh toán điện tử. Tích hợp với nhà cung cấp thanh toán bên ngoài; thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán không được lưu trực tiếp trong hệ thống CAB. Giao dịch thanh toán điện tử thất bại thì thông báo cho khách hàng và cho phép xử lý lại theo chính sách của doanh nghiệp. *(BR-03, BR-07, BR-11)* |
| 5 | Thông báo | Thông báo cho khách hàng khi yêu cầu đặt xe được tiếp nhận, khi có tài xế nhận chuyến, khi tài xế đến điểm đón, khi chuyến hoàn thành và khi thanh toán có kết quả. Thông báo cho tài xế về các chuyến mới hoặc những thay đổi liên quan đến chuyến đang thực hiện. *(BR-02, BR-07)* |
| 6 | Quản trị vận hành và báo cáo | **Quản trị:** giao diện quản trị để quản lý khách hàng, tài xế, phương tiện và chuyến đi; xem các chuyến đang diễn ra, kiểm tra trạng thái tài xế, hỗ trợ xử lý các trường hợp chuyến bị lỗi và tra cứu lịch sử giao dịch; một số chức năng quản trị được phân quyền để nhân viên thông thường không thể thực hiện các thao tác nhạy cảm. **Báo cáo:** báo cáo về số lượng chuyến, doanh thu, tỷ lệ chuyến hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế. *(BR-06, BR-08, BR-11)* |

> **Ngoài phạm vi MVP (đề ghi "trong tương lai"):** bổ sung các loại dịch vụ mới, thêm phương thức thanh toán, thêm nhà cung cấp thông báo, mở rộng thêm các kênh thông báo, thay đổi một số thành phần kỹ thuật. *(BR-05)*
