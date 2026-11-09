# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: CodeX
- Candidate problem nhóm chọn (1 câu): Khi tiếp nhận một dự án outsource/maintain cũ (hoặc onboard thành viên mới) mà tài liệu cài đặt đã lỗi thời, Developer và Techlead lãng phí 4–8 tiếng để gỡ lỗi crash do xung đột thư viện/version; nhóm chọn bài toán chuẩn hóa môi trường bằng Docker (No-AI) kết hợp AI Workflow phân tích log lỗi build để giảm thời gian setup xuống dưới 30 phút.
- Quyết định cuối (Go / Not Yet / No-Go): (Chưa quyết định)

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Nguyễn Tiến Cường | 2A202603425 | Nhóm trưởng | cuong-sadboi |
| 2 | Nguyễn Trần Anh Khôi | 2A202603422 | Thành viên | khoinguyentran1111 |
| 3 | | | | |
| 4 | | | | |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | | | Cluster, cây OST, bảng chấm điểm |
| CP4 — Kiểm chứng | | | Assumption map, snapshot hoặc survey |
| CP4 — Research | | | Bảng research có link |
| CP5 — Quy trình trước/sau | | | Quy trình + bảng before/after |
| CP5 — Problem Statement v0 | | | Problem Statement v0 |
| CP6 — Mức can thiệp + Problem Statement v1 | | | Ma trận, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định | | | 4 rủi ro + Go/Not Yet/No-Go |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### NguyenTienCuong-2A202603425

**Phần việc phụ trách:**

- Nhóm trưởng điều phối nhóm CodeX, tham gia pitch và phản biện tại CP3.
- (Sẽ cập nhật các task cụ thể sau khi nhóm chốt phân công CP4 - CP6).

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Hoàn thành báo cáo cá nhân CP1 (10 problem) và CP2 (3 Problem Card + quy trình nháp).
- Chuẩn bị sẵn Card #1 để pitch với nhóm.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/individual/2A202603425_NguyenTienCuong.md`.
- Lịch sử commit trên branch cá nhân / repo từ tài khoản `cuong-sadboi`.

**Điều mình học được từ phần nhóm:**

- (Sẽ điền sau khi hoàn thành phần làm việc nhóm ở CP7).

### NguyenTranAnhKhoi-2A202603422

**Phần việc phụ trách:**

- Phụ trách kiểm chứng người dùng tại CP4: phỏng vấn nhanh một Developer ở nhóm khác về trải nghiệm setup dự án cũ, lỗi thực tế, thời gian xử lý và cách khắc phục.
- Phụ trách chi tiết hóa quy trình setup dự án hiện tại tại CP5, xác định các bước gây tốn thời gian và bottleneck chính.
- Tham gia phân tích câu hỏi Google PAIR tại CP6, xác định mức độ can thiệp phù hợp của AI (Augment/Automate) và đánh giá rủi ro False Positive/False Negative.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Chuẩn bị kịch bản phỏng vấn, tập trung vào trải nghiệm thực tế khi Developer setup dự án cũ.
- Xây dựng mẫu Interview Snapshot để ghi nhận vấn đề, thời gian xử lý, cách giải quyết và câu nói đáng nhớ của người được phỏng vấn.
- Xây dựng bảng Current Workflow gồm 5 bước setup dự án, với tổng thời gian 360 phút.
- Phân tích bottleneck tại bước Build crash lỗi dependency và bước nhờ Techlead hỗ trợ, chiếm tổng cộng 270 phút (75% quy trình).
- Phân tích định hướng Augment thay vì Automate và rủi ro False Positive/False Negative theo Google PAIR.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/individual/2A202603422_NguyenTranAnhKhoi.md`.
- Lịch sử commit trên branch cá nhân / repo từ tài khoản `khoinguyentran1111`.

**Điều mình học được từ phần nhóm:**

- Biết cách kiểm chứng một vấn đề bằng trải nghiệm thực tế thay vì chỉ dựa vào giả định.
- Hiểu cách phân tích quy trình để xác định bottleneck và lựa chọn mức độ can thiệp AI phù hợp.
- Nhận ra AI nên hỗ trợ Developer ra quyết định, không nên tự ý thay đổi dự án khi chưa được kiểm tra.

### HoVaTen-MSSV

**Phần việc phụ trách:**

-

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

-

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

-

**Điều mình học được từ phần nhóm:**

-
