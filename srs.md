# ĐẶC TẢ YÊU CẦU PHẦN MỀM - HỆ THỐNG CAB

## 1. STAKEHOLDERS

| STT | Bên liên quan | Vai trò |
|:---:|---|---|
| 1 | **Ban lãnh đạo** | Định hướng phát triển hệ thống, theo dõi hiệu quả hoạt động và sử dụng các báo cáo để hỗ trợ ra quyết định. |
| 2 | **Khách hàng** | Đăng ký, đăng nhập, cập nhật thông tin cá nhân, đặt xe, theo dõi chuyến đi, thanh toán, xem lịch sử chuyến và đánh giá tài xế. |
| 3 | **Tài xế** | Quản lý hồ sơ, phương tiện và trạng thái hoạt động; nhận hoặc từ chối chuyến; cập nhật vị trí và trạng thái chuyến đi. |
| 4 | **Nhân viên vận hành** | Quản lý khách hàng, tài xế, phương tiện và chuyến đi; theo dõi chuyến đang diễn ra, hỗ trợ xử lý sự cố và tra cứu lịch sử giao dịch. |
| 5 | **Nhà cung cấp thanh toán bên ngoài** | Xử lý các giao dịch thanh toán điện tử được tích hợp với hệ thống CAB. |
| 6 | **Chuyên viên phân tích nghiệp vụ (BA)** | Xác định phạm vi, quy trình nghiệp vụ, yêu cầu, quy tắc nghiệp vụ, trường hợp ngoại lệ và làm rõ các vấn đề chưa được xác định. |
| 7 | **Nhóm phát triển** | Xây dựng giải pháp dựa trên các yêu cầu đã được làm rõ và xác nhận. |

---

## 2. STAKEHOLDER MATRIX

```mermaid
quadrantChart
    title Ma trận Quyền lực - Mức độ quan tâm của hệ thống CAB
    x-axis Mức độ quan tâm thấp --> Mức độ quan tâm cao
    y-axis Quyền lực thấp --> Quyền lực cao

    quadrant-1 Quản lý chặt chẽ
    quadrant-2 Duy trì sự hài lòng
    quadrant-3 Theo dõi
    quadrant-4 Cập nhật thông tin

    Ban lãnh đạo: [0.90, 0.92]
    Chuyên viên BA: [0.68, 0.84]
    Nhân viên vận hành: [0.88, 0.72]
    Nhóm phát triển: [0.66, 0.67]
    Nhà cung cấp thanh toán: [0.35, 0.64]
    Tài xế: [0.72, 0.38]
    Khách hàng: [0.90, 0.27]
```

| Nhóm | Bên liên quan |
|---|---|
| **Quản lý chặt chẽ** | Ban lãnh đạo, Nhân viên vận hành, Chuyên viên BA, Nhóm phát triển |
| **Duy trì sự hài lòng** | Nhà cung cấp thanh toán bên ngoài |
| **Cập nhật thông tin** | Khách hàng, Tài xế |
| **Theo dõi** | Không xác định thêm bên liên quan cụ thể |

---

## 3. BUSINESS GOALS

- **BG-01:** Tự động hóa quy trình đặt xe và phân công tài xế, giảm việc phân công tài xế thủ công.
- **BG-02:** Nâng cao khả năng theo dõi chuyến đi của khách hàng từ khi gửi yêu cầu đến khi hoàn thành chuyến.
- **BG-03:** Quản lý tập trung chuyến đi, tính cước, thanh toán và lịch sử giao dịch.
- **BG-04:** Nâng cao hiệu quả quản lý hoạt động của khách hàng, tài xế, phương tiện và chuyến đi.
- **BG-05:** Cung cấp dữ liệu và báo cáo phục vụ việc theo dõi hoạt động và hỗ trợ ban lãnh đạo ra quyết định.
- **BG-06:** Xây dựng nền tảng CAB có khả năng mở rộng, hoạt động ổn định, bảo mật và linh hoạt để phát triển thêm chức năng trong tương lai.

---

## 4. MVP MODULES

| STT | Module | Chức năng chính |
|:---:|---|---|
| 1 | **Quản lý tài khoản và xác thực** | Đăng ký, đăng nhập, cập nhật thông tin cá nhân và xác thực người dùng. |
| 2 | **Quản lý tài xế và phương tiện** | Quản lý hồ sơ tài xế, thông tin phương tiện và trạng thái hoạt động. |
| 3 | **Đặt xe** | Nhập điểm đón, điểm đến, lựa chọn loại xe và gửi yêu cầu đặt xe. |
| 4 | **Tìm kiếm và phân công tài xế** | Tìm tài xế phù hợp, gửi yêu cầu nhận chuyến và tiếp tục tìm tài xế khác khi tài xế từ chối hoặc không phản hồi. |
| 5 | **Quản lý chuyến đi và vị trí** | Theo dõi trạng thái chuyến đi, cập nhật vị trí tài xế, hỗ trợ dự kiến thời gian đến, lưu lịch sử chuyến và hỗ trợ đánh giá tài xế sau chuyến. |
| 6 | **Tính cước và thanh toán** | Tính số tiền phải trả và hỗ trợ thanh toán bằng tiền mặt hoặc thanh toán điện tử. |
| 7 | **Thông báo** | Gửi thông báo về yêu cầu đặt xe, tài xế nhận chuyến, tài xế đến điểm đón, hoàn thành chuyến và kết quả thanh toán. |
| 8 | **Quản lý vận hành và báo cáo** | Quản lý khách hàng, tài xế, phương tiện, chuyến đi; hỗ trợ xử lý sự cố, tra cứu giao dịch và cung cấp báo cáo. |

---

## 5. BUSINESS REQUIREMENTS

| Mã | Yêu cầu nghiệp vụ |
|:---:|---|
| **BR-01** | Hệ thống phải hỗ trợ khách hàng đăng ký, đăng nhập, cập nhật thông tin, đặt xe, theo dõi chuyến, xem lịch sử, số tiền phải trả và đánh giá tài xế sau chuyến. |
| **BR-02** | Hệ thống phải hỗ trợ tài xế quản lý hồ sơ, phương tiện, trạng thái hoạt động, nhận hoặc từ chối chuyến, cập nhật vị trí và trạng thái chuyến đi. |
| **BR-03** | Hệ thống phải tự động tìm tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí vận hành; ưu tiên tài xế phù hợp và gần khách hàng. Nếu tài xế không phản hồi hoặc từ chối, hệ thống phải tiếp tục tìm tài xế khác mà không yêu cầu khách hàng tạo lại yêu cầu. Nếu không tìm được tài xế, hệ thống phải thông báo rõ ràng cho khách hàng. |
| **BR-04** | Sau khi chuyến hoàn thành, hệ thống phải tính cước và hỗ trợ thanh toán bằng tiền mặt hoặc thanh toán điện tử thông qua nhà cung cấp bên ngoài. Hệ thống không được lưu trực tiếp thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán. Nếu thanh toán điện tử thất bại, hệ thống phải thông báo cho khách hàng và cho phép xử lý lại theo chính sách của doanh nghiệp. |
| **BR-05** | Hệ thống phải thông báo cho khách hàng khi yêu cầu đặt xe được tiếp nhận, khi có tài xế nhận chuyến, khi tài xế đến điểm đón, khi chuyến hoàn thành và khi có kết quả thanh toán; đồng thời thông báo cho tài xế về chuyến mới hoặc các thay đổi liên quan đến chuyến đang thực hiện. |
| **BR-06** | Hệ thống phải cung cấp giao diện cho nhân viên vận hành để quản lý khách hàng, tài xế, phương tiện, chuyến đi, hỗ trợ xử lý sự cố và tra cứu lịch sử giao dịch. |
| **BR-07** | Hệ thống phải cung cấp báo cáo về số lượng chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế. |
| **BR-08** | Hệ thống phải đảm bảo xác thực, phân quyền, bảo vệ dữ liệu, lưu vết thao tác, khả năng mở rộng và hạn chế ảnh hưởng toàn hệ thống khi thanh toán hoặc thông báo gặp lỗi. |

### Các vấn đề cần làm rõ

- Cách tính cước.
- Tiêu chí ưu tiên tài xế.
- Thời gian tài xế phải phản hồi.
- Chính sách hủy chuyến.
- Cách xử lý khi mất kết nối mạng.
- Thời gian lưu trữ dữ liệu.

---

## 6. BUSINESS PROCESS MODELING

### 6.1. Quy trình đặt xe và thực hiện chuyến

**Business Requirements liên quan:** BR-01, BR-02, BR-03, BR-05.

```mermaid
flowchart TD
    A[Khách hàng đăng nhập] --> B[Nhập điểm đón và điểm đến]
    B --> C[Chọn loại xe]
    C --> D[Gửi yêu cầu đặt xe]

    D --> E[Hệ thống tiếp nhận yêu cầu]
    E --> F[Thông báo đã tiếp nhận yêu cầu]
    F --> G[Hệ thống tìm tài xế phù hợp]

    G --> H{Có tài xế phù hợp?}

    H -- Không --> I[Thông báo không tìm được tài xế]
    I --> Z[Kết thúc yêu cầu]

    H -- Có --> J[Gửi yêu cầu nhận chuyến cho tài xế]
    J --> K{Tài xế chấp nhận?}

    K -- Không hoặc không phản hồi --> G
    K -- Có --> L[Phân công tài xế]

    L --> M[Thông báo tài xế đã nhận chuyến]
    M --> N[Tài xế di chuyển đến điểm đón]
    N --> O[Cập nhật đã đến điểm đón]
    O --> P[Thông báo tài xế đã đến]

    P --> Q[Đón khách]
    Q --> R[Cập nhật trạng thái đang di chuyển]
    R --> S[Thực hiện chuyến đi]
    S --> T[Hoàn thành chuyến]
```

### 6.2. Quy trình tính cước và thanh toán

**Business Requirements liên quan:** BR-04, BR-05.

```mermaid
flowchart TD
    A[Chuyến đi hoàn thành] --> B[Hệ thống tính cước]
    B --> C[Hiển thị số tiền phải trả]

    C --> D{Phương thức thanh toán}

    D -- Tiền mặt --> E[Ghi nhận thanh toán tiền mặt]

    D -- Điện tử --> F[Gửi yêu cầu đến nhà cung cấp thanh toán]
    F --> G{Thanh toán thành công?}

    G -- Không --> H[Thông báo thanh toán thất bại]
    H --> I[Cho phép xử lý lại theo chính sách]

    G -- Có --> J[Ghi nhận thanh toán thành công]

    E --> K[Lưu thông tin chuyến và giao dịch]
    J --> K

    K --> L[Lưu lịch sử chuyến]
    L --> M[Khách hàng đánh giá tài xế]
    M --> N[Kết thúc]
```

### 6.3. Quy trình quản lý vận hành và báo cáo

**Business Requirements liên quan:** BR-06, BR-07.

```mermaid
flowchart TD
    A[Nhân viên vận hành đăng nhập] --> B[Truy cập giao diện quản trị]

    B --> C{Chọn chức năng}

    C --> D[Quản lý khách hàng]
    C --> E[Quản lý tài xế và phương tiện]
    C --> F[Xem chuyến đang diễn ra]
    C --> G[Kiểm tra trạng thái tài xế]
    C --> H[Hỗ trợ xử lý chuyến bị lỗi]
    C --> I[Tra cứu lịch sử giao dịch]

    D --> J[Dữ liệu hoạt động]
    E --> J
    F --> J
    G --> J
    H --> J
    I --> J

    J --> K[Tổng hợp báo cáo]

    K --> L[Số lượng chuyến]
    K --> M[Doanh thu]
    K --> N[Tỷ lệ hoàn thành]
    K --> O[Tỷ lệ hủy]
    K --> P[Hiệu quả hoạt động của tài xế]
```

### 6.4. Yêu cầu áp dụng xuyên suốt

**BR-08** được áp dụng cho toàn bộ hệ thống:

- Xác thực khách hàng và tài xế.
- Kiểm soát quyền đối với các thao tác quản trị.
- Bảo vệ thông tin cá nhân, phương tiện, vị trí và giao dịch.
- Lưu vết các thao tác quan trọng.
- Đảm bảo khả năng mở rộng khi tải tăng.
- Lỗi ở chức năng thanh toán hoặc thông báo không được làm toàn bộ hệ thống đặt xe ngừng hoạt động.

## 7. FUNCTIONAL REQUIREMENTS

| Mã | Yêu cầu chức năng |
|:---:|---|
| **FR-01** | Hệ thống cho phép khách hàng đăng ký tài khoản, đăng nhập và cập nhật thông tin cá nhân. |
| **FR-02** | Hệ thống cho phép khách hàng nhập điểm đón, điểm đến, lựa chọn loại xe và gửi yêu cầu đặt xe. |
| **FR-03** | Hệ thống cho phép khách hàng theo dõi quá trình tìm tài xế, thông tin tài xế nhận chuyến, thời gian dự kiến tài xế đến và trạng thái hiện tại của chuyến đi. |
| **FR-04** | Hệ thống cho phép khách hàng xem lịch sử chuyến đi, số tiền phải trả và đánh giá tài xế sau khi chuyến hoàn thành. |
| **FR-05** | Hệ thống cho phép tài xế đăng ký tài khoản hoặc cho phép nhân viên vận hành tạo tài khoản tài xế; tài xế có thể cập nhật hồ sơ, thông tin phương tiện và trạng thái hoạt động. |
| **FR-06** | Hệ thống cho phép tài xế chuyển sang trạng thái sẵn sàng nhận chuyến, nhận thông báo chuyến mới và chấp nhận hoặc từ chối chuyến. |
| **FR-07** | Hệ thống cho phép tài xế cập nhật trạng thái chuyến gồm: đã đến điểm đón, đã đón khách, đang di chuyển và hoàn thành chuyến. |
| **FR-08** | Hệ thống lưu vị trí tài xế và sử dụng vị trí, trạng thái sẵn sàng cùng các tiêu chí vận hành để tìm tài xế phù hợp và gần khách hàng. |
| **FR-09** | Nếu tài xế được đề xuất từ chối hoặc không phản hồi, hệ thống tự động tiếp tục tìm tài xế khác mà không yêu cầu khách hàng tạo lại yêu cầu; nếu không tìm được tài xế, hệ thống thông báo cho khách hàng. |
| **FR-10** | Sau khi chuyến hoàn thành, hệ thống tính số tiền phải trả dựa trên loại dịch vụ và thông tin chuyến đi; hỗ trợ thanh toán bằng tiền mặt hoặc thanh toán điện tử thông qua nhà cung cấp thanh toán bên ngoài. |
| **FR-11** | Nếu thanh toán điện tử thất bại, hệ thống thông báo cho khách hàng và cho phép xử lý lại theo chính sách của doanh nghiệp. |
| **FR-12** | Hệ thống gửi thông báo cho khách hàng khi yêu cầu đặt xe được tiếp nhận, có tài xế nhận chuyến, tài xế đến điểm đón, chuyến hoàn thành và có kết quả thanh toán; đồng thời gửi thông báo chuyến mới hoặc thay đổi chuyến cho tài xế. |
| **FR-13** | Hệ thống cung cấp giao diện quản trị cho nhân viên vận hành để quản lý khách hàng, tài xế, phương tiện và chuyến đi; xem chuyến đang diễn ra, kiểm tra trạng thái tài xế, hỗ trợ xử lý chuyến bị lỗi và tra cứu lịch sử giao dịch. |
| **FR-14** | Hệ thống kiểm soát quyền truy cập đối với các chức năng quản trị để nhân viên không có quyền không thể thực hiện các thao tác nhạy cảm. |
| **FR-15** | Hệ thống cung cấp báo cáo về số lượng chuyến, doanh thu, tỷ lệ chuyến hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế. |

## 8. BUSINESS RULES

| Mã | Quy tắc nghiệp vụ |
|:---:|---|
| **RULE-01** | Khách hàng và tài xế phải được xác thực trước khi sử dụng các chức năng yêu cầu tài khoản. |
| **RULE-02** | Tài xế chỉ được xem xét để nhận chuyến khi có trạng thái sẵn sàng và đáp ứng các tiêu chí vận hành của hệ thống. |
| **RULE-03** | Khi tìm tài xế, hệ thống ưu tiên tài xế phù hợp và gần khách hàng. |
| **RULE-04** | Nếu tài xế được đề xuất từ chối hoặc không phản hồi, hệ thống phải tiếp tục tìm tài xế khác mà không yêu cầu khách hàng tạo lại yêu cầu đặt xe. |
| **RULE-05** | Nếu không tìm được tài xế phù hợp, hệ thống phải thông báo rõ ràng cho khách hàng. |
| **RULE-06** | Trong quá trình thực hiện chuyến, tài xế phải cập nhật trạng thái chuyến gồm: đã đến điểm đón, đã đón khách, đang di chuyển và hoàn thành chuyến. |
| **RULE-07** | Cước chuyến đi được xác định sau khi chuyến hoàn thành, dựa trên loại dịch vụ và thông tin chuyến đi. |
| **RULE-08** | Khách hàng có thể thanh toán bằng tiền mặt hoặc thanh toán điện tử. |
| **RULE-09** | Thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán không được lưu trực tiếp trong hệ thống CAB. |
| **RULE-10** | Nếu thanh toán điện tử thất bại, hệ thống phải thông báo cho khách hàng và cho phép xử lý lại theo chính sách của doanh nghiệp. |
| **RULE-11** | Các thao tác quản trị nhạy cảm chỉ được thực hiện bởi người dùng có quyền phù hợp. |
| **RULE-12** | Các thao tác quan trọng trong hệ thống phải được lưu vết để phục vụ kiểm tra khi xảy ra sự cố. |

## 9. NON-FUNCTIONAL REQUIREMENTS

| Mã | Nhóm yêu cầu | Yêu cầu phi chức năng |
|:---:|---|---|
| **NFR-01** | **Hiệu năng và ổn định** | Hệ thống phải hoạt động ổn định trong các thời điểm nhu cầu đặt xe tăng cao. |
| **NFR-02** | **Khả năng mở rộng** | Các thành phần của hệ thống phải có khả năng mở rộng độc lập khi tải tăng để phục vụ số lượng lớn khách hàng và tài xế. |
| **NFR-03** | **Khả năng chịu lỗi** | Lỗi xảy ra ở chức năng thanh toán hoặc thông báo không được làm toàn bộ hệ thống đặt xe ngừng hoạt động. |
| **NFR-04** | **Khả năng triển khai** | Các chức năng mới phải có khả năng được triển khai từng phần và hạn chế ảnh hưởng đến các chức năng đang hoạt động. |
| **NFR-05** | **Bảo mật và phân quyền** | Khách hàng và tài xế phải được xác thực trước khi sử dụng các chức năng yêu cầu tài khoản; các thao tác quản trị phải được kiểm soát quyền truy cập. |
| **NFR-06** | **Bảo vệ dữ liệu** | Thông tin cá nhân, thông tin phương tiện, dữ liệu vị trí và dữ liệu giao dịch phải được bảo vệ; thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán không được lưu trực tiếp trong hệ thống CAB. |
| **NFR-07** | **Khả năng kiểm tra và truy vết** | Hệ thống phải lưu vết các thao tác quan trọng để phục vụ kiểm tra khi xảy ra sự cố. |
| **NFR-08** | **Khả năng mở rộng chức năng** | Kiến trúc hệ thống phải đủ linh hoạt để có thể bổ sung loại dịch vụ mới, phương thức thanh toán mới, nhà cung cấp thông báo hoặc thay đổi một số thành phần kỹ thuật mà không phải xây dựng lại toàn bộ ứng dụng. |

## 10. ENTITY MODEL

### 10.1. Các thực thể chính

| STT | Thực thể | Mô tả |
|:---:|---|---|
| 1 | **Tài khoản** | Lưu thông tin tài khoản, vai trò, trạng thái phục vụ xác thực và phân quyền. |
| 2 | **Khách hàng** | Lưu thông tin cá nhân của khách hàng sử dụng dịch vụ đặt xe. |
| 3 | **Tài xế** | Lưu hồ sơ tài xế và trạng thái hoạt động. |
| 4 | **Nhân viên vận hành** | Lưu thông tin nhân viên sử dụng giao diện quản trị và quyền truy cập. |
| 5 | **Phương tiện** | Lưu thông tin phương tiện của tài xế. |
| 6 | **Chuyến đi** | Lưu yêu cầu đặt xe, điểm đón, điểm đến, loại xe/dịch vụ, tài xế được phân công, trạng thái chuyến và số tiền phải trả. |
| 7 | **Vị trí tài xế** | Lưu thông tin vị trí của tài xế phục vụ tìm tài xế gần khách hàng và dự kiến thời gian đến. |
| 8 | **Thanh toán** | Lưu phương thức, số tiền và kết quả thanh toán của chuyến đi. |
| 9 | **Thông báo** | Lưu các thông báo gửi đến khách hàng hoặc tài xế trong quá trình thực hiện chuyến. |
| 10 | **Đánh giá** | Lưu đánh giá của khách hàng dành cho tài xế sau khi chuyến hoàn thành. |
| 11 | **Nhật ký hệ thống** | Lưu vết các thao tác quan trọng để phục vụ kiểm tra khi xảy ra sự cố. |

### 10.2. Mô hình quan hệ thực thể

```mermaid
erDiagram

    TAI_KHOAN ||--o| KHACH_HANG : "thuộc"
    TAI_KHOAN ||--o| TAI_XE : "thuộc"
    TAI_KHOAN ||--o| NHAN_VIEN_VAN_HANH : "thuộc"

    TAI_XE ||--o{ PHUONG_TIEN : "có"
    TAI_XE ||--o{ VI_TRI_TAI_XE : "cập nhật"

    KHACH_HANG ||--o{ CHUYEN_DI : "đặt"
    TAI_XE o|--o{ CHUYEN_DI : "thực hiện"

    CHUYEN_DI ||--o{ THANH_TOAN : "phát sinh"
    CHUYEN_DI ||--o{ THONG_BAO : "phát sinh"
    CHUYEN_DI ||--o| DANH_GIA : "được đánh giá"

    KHACH_HANG ||--o{ DANH_GIA : "thực hiện"
    TAI_XE ||--o{ DANH_GIA : "nhận"

    TAI_KHOAN ||--o{ THONG_BAO : "nhận"
    TAI_KHOAN ||--o{ NHAT_KY_HE_THONG : "thực hiện"

    TAI_KHOAN {
        int account_id PK
        string username
        string password_hash
        string role
        string status
    }

    KHACH_HANG {
        int customer_id PK
        int account_id FK
        string thong_tin_ca_nhan
    }

    TAI_XE {
        int driver_id PK
        int account_id FK
        string thong_tin_ho_so
        string trang_thai_hoat_dong
    }

    NHAN_VIEN_VAN_HANH {
        int staff_id PK
        int account_id FK
        string quyen_truy_cap
    }

    PHUONG_TIEN {
        int vehicle_id PK
        int driver_id FK
        string thong_tin_phuong_tien
    }

    CHUYEN_DI {
        int trip_id PK
        int customer_id FK
        int driver_id FK
        string diem_don
        string diem_den
        string loai_xe
        string loai_dich_vu
        string trang_thai
        string thoi_gian_du_kien_den
        decimal so_tien_phai_tra
    }

    VI_TRI_TAI_XE {
        int location_id PK
        int driver_id FK
        decimal latitude
        decimal longitude
        datetime thoi_gian_cap_nhat
    }

    THANH_TOAN {
        int payment_id PK
        int trip_id FK
        string phuong_thuc
        decimal so_tien
        string trang_thai
    }

    THONG_BAO {
        int notification_id PK
        int account_id FK
        int trip_id FK
        string loai_thong_bao
        string noi_dung
        datetime thoi_gian_gui
    }

    DANH_GIA {
        int rating_id PK
        int trip_id FK
        int customer_id FK
        int driver_id FK
        int diem_danh_gia
    }

    NHAT_KY_HE_THONG {
        int log_id PK
        int account_id FK
        string thao_tac
        datetime thoi_gian
    }
