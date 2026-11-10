# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: CodeX
- Candidate problem nhóm chọn (1 câu): Khi tiếp nhận một dự án outsource/maintain cũ (hoặc onboard thành viên mới) mà tài liệu cài đặt đã lỗi thời, Developer và Techlead lãng phí 4–8 tiếng để gỡ lỗi crash do xung đột thư viện/version; nhóm chọn bài toán chuẩn hóa môi trường bằng Docker (No-AI) kết hợp AI Workflow phân tích log lỗi build để giảm thời gian setup xuống dưới 30 phút.
- Quyết định cuối (Go / Not Yet / No-Go): Go (Phạm vi nhỏ - Pilot trên Web Node.js/Python)

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Nguyễn Tiến Cường | 2A202603425 | Nhóm trưởng, Kiến trúc giải pháp (System Architect) | cuong-sadboi |
| 2 | Nguyễn Vũ Khanh | 2A202603427 | Thành viên, Research & Đánh giá AI (Eval) | KhnhVux |
| 3 | Nguyễn Trần Anh Khôi | 2A202603422 | Thành viên, Kiểm chứng The Mom Test & Quy trình | khoinguyentran1111 |
| 4 | Nguyễn Quang Vũ | 2A202603407 | Thành viên, Quản trị rủi ro & Thiết kế AI Canvas | NguyenVu8888 |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | Nguyễn Tiến Cường | Cả nhóm | Cluster, cây OST, bảng chấm điểm chọn Card #1 |
| CP4 — Kiểm chứng | Nguyễn Trần Anh Khôi | Nguyễn Tiến Cường | Assumption map, Interview Snapshot The Mom Test |
| CP4 — Research | Nguyễn Vũ Khanh | Nguyễn Quang Vũ | Bảng research Dev Containers, Docker, Copilot CLI |
| CP5 — Quy trình trước/sau | Nguyễn Tiến Cường | Nguyễn Vũ Khanh, Anh Khôi | Sơ đồ quy trình Docker + AI Workflow, bảng before/after |
| CP5 — Problem Statement v0 | Nguyễn Quang Vũ | Nguyễn Tiến Cường | Problem Statement v0 (6 trường, ranh giới Boundary chặt) |
| CP6 — Mức can thiệp + Problem Statement v1 | Nguyễn Tiến Cường | Nguyễn Quang Vũ | Ma trận Mơ hồ x Phức tạp, AI Canvas, Problem Statement v1 |
| CP6 — Quyết định | Nguyễn Vũ Khanh | Cả nhóm | Tiêu chí AI Eval, 4 rủi ro + Quyết định Go và ngưỡng dừng |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### NguyenTienCuong-2A202603425

**Phần việc phụ trách:**

- Nhóm trưởng điều phối nhóm CodeX, chủ trì buổi pitch và phản biện tại CP3.
- Chịu trách nhiệm kiến trúc Quy trình tương lai (Mục 4.2 ở CP5): phân định rạch ròi giữa No-AI (Docker Compose), AI Workflow (phân tích log lỗi build) và Human-in-the-Loop.
- Phụ trách phân tích Ma trận độ mơ hồ × độ phức tạp và lập luận chọn mức can thiệp Workflow (Mục 6.1 & 6.2 ở CP6).
- Hoàn thiện Problem Statement v1, kết luận Quyết định Go phạm vi nhỏ kèm ngưỡng dừng (Mục 8.2 ở CP6).

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Soạn thảo Problem Card #1 đạt điểm cao nhất nhóm (34/35) và được cả nhóm nhất trí chọn làm bài toán chung.
- Thiết kế sơ đồ quy trình tương lai giúp giảm thời gian thao tác gỡ lỗi từ 270 phút xuống dưới 30 phút.
- Phân tích ranh giới can thiệp AI: giữ Docker làm nền tảng No-AI, chỉ can thiệp AI ở bước phân tích log crash; thiết lập boundary cấm AI tự chạy lệnh shell quyền root và cấm đọc source code nghiệp vụ bảo mật.
- Hoàn thiện toàn bộ báo cáo cá nhân CP1 đến CP7 với 7 câu reflection sâu sắc và bản Change Request Log trong `report/assets/change-request-log.md`.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/individual/2A202603425_NguyenTienCuong.md`.
- `report/assets/change-request-log.md`.
- Mục 2, Mục 4.2, Mục 6.1, 6.2, 8.2 trong `report/team/group_report.md`.
- Lịch sử commit trên repo từ tài khoản GitHub `cuong-sadboi`.

**Điều mình học được từ phần nhóm:**

- Học được cách "phanh" tư duy solution-first lại để đào sâu vào nỗi đau thực tế và điểm nghẽn quy trình.
- Hiểu sâu sắc rằng AI không phải là cây đũa thần giải quyết mọi thứ; một giải pháp xuất sắc là biết kết hợp giữa No-AI (Docker chuẩn hóa môi trường) với AI Workflow (chỉ can thiệp vào bước bóc tách log lỗi có độ mơ hồ cao).
- Trải nghiệm thực tế vai trò nhóm trưởng điều phối, phản biện đa chiều và bảo vệ ranh giới an toàn cho hệ thống.

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

### NguyenQuangVu-2A202603407

**Phần việc phụ trách:**

- Thành viên phản biện nhóm CodeX, tham gia pitch và phản biện tại CP3.
- Quản trị rủi ro, Thiết kế AI Canvas & Ranh giới an toàn (Gatekeeper)

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Hoàn thành báo cáo cá nhân CP1 (7 problem) và CP2 (3 Problem Card + quy trình nháp).
- [CP4] Bảng Assumption Map: Lập 4-5 giả định cốt lõi về giá trị, tính khả thi kỹ thuật và mức độ chấp nhận của người dùng; chấm điểm quan trọng vs bằng chứng.
- [CP5] Soạn thảo Problem Statement v0: Điền đủ 6 trường: Actor, Quy trình, Bottleneck, Impact, Success Metric (270' -> 30'), Boundary (AI không tự ý chạy script quyền root). Lưu ý: Không viết từ "AI" vào phần mô tả problem.
- [CP6] Thiết kế AI Canvas rút gọn: Điền 6 ô: Prediction (AI đoán package lỗi & gợi ý lệnh) -> Judgment (Dev duyệt lệnh) -> Action (Dev chạy lệnh) -> Outcome (build pass) -> Input (chỉ lấy log crash + package.json, TUYỆT ĐỐI KHÔNG ĐỌC SOURCE CODE BẢO MẬT) -> Feedback.
- [CP6] Đánh giá 4 rủi ro sản phẩm: Đánh giá Value, Usability, Feasibility, Viability (ở mức an toàn/thấp).

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/individual/2A202603407_NguyenQuangVu.md`.
- Lịch sử commit trên branch cá nhân / repo từ tài khoản `NguyenVu8888`.

**Điều mình học được từ phần nhóm:**

- Biết cách kiểm soát các rủi ro sản phẩm (Value, Usability, Feasibility, Viability) và thiết lập ranh giới an toàn (Boundary & HITL) để bảo vệ hệ thống và mã nguồn.
- Hiểu cách phân công giữa AI và con người thông qua AI Canvas rút gọn, nhận ra AI chỉ nên đề xuất (Prediction), còn con người là người kiểm duyệt (Judgment) và thực thi (Action).

### NguyenVuKhanh-2A202603427

**Phần việc phụ trách:**

- Phụ trách nghiên cứu giải pháp thị trường tại CP4 (Mục 3.3): phân tích 3 công cụ VS Code Dev Containers, Docker Compose + .env (No-AI), và GitHub Copilot CLI.
- Phụ trách xây dựng bảng Before / After tại CP5 (Mục 4.3): đối chiếu định lượng quy trình trước và sau khi áp dụng AI Workflow.
- Phụ trách soạn thảo Problem Statement v1 và 3 tiêu chí đánh giá AI Eval tại CP6 (Mục 7).

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Hoàn thành báo cáo cá nhân CP1 (10 problem) và CP2 (3 Problem Card + quy trình nháp).
- [CP4] Khảo sát chuyên sâu 3 giải pháp thị trường, chỉ ra khoảng trống cốt lõi: Docker ném ra log lỗi dài khi build fail nhưng không chỉ cách sửa, còn Copilot CLI thiếu ngữ cảnh đối chiếu và dễ gợi ý lệnh nguy hiểm (`sudo`, `--force`).
- [CP5] Thiết lập bảng Before / After đối chiếu chuẩn xác: Tổng thời gian 360' → 40', gỡ lỗi dependency 270' → 15', số lần làm phiền Senior 3 lần → 0 lần.
- [CP6] Chốt Problem Statement v1 và thiết lập 3 tiêu chí Eval Đạt / Không đạt của AI (chỉ đúng tên thư viện/version xung đột, an toàn không can thiệp file hệ thống, lệnh phải chạy được ngay).
- Đóng góp các ảnh kết quả survey trong `report/assets/cp4-survey-result-*.png` và sơ đồ quy trình `report/assets/cp5-workflow-future.png`.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/individual/2A202603427_NguyenVuKhanh.md`.
- Mục 3.3, Mục 4.3, Mục 7 trong `report/team/group_report.md`.
- Các file ảnh trong `report/assets/`.
- Lịch sử commit trên branch cá nhân từ tài khoản `KhnhVux`.

**Điều mình học được từ phần nhóm:**

- Nhận thức rõ sự khác biệt giữa "sự bất tiện cá nhân khi đi học" và "nỗi đau có tính hệ thống trong thực tế làm việc".
- Hiểu cách bóc tách bài toán và phân định ranh giới giữa Rule (script gom ngữ cảnh) và AI Workflow, tránh sa đà vào Agent tự chạy lệnh gây rủi ro phá hỏng hệ thống.
