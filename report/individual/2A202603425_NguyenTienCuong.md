# Báo cáo cá nhân — 2A202603425_NguyenTienCuong

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên:   Nguyễn Tiến Cường   
- MSSV:     2A202603425
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: CodeX
- Link repo nhóm:    [https://github.com/cuong-sadboi/K5-L3A-DAY02-CodeX-DiscoveryProblemFraming](https://github.com/cuong-sadboi/K5-L3A-DAY02-CodeX-DiscoveryProblemFraming)

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Tốn thời gian | Khi tiếp nhận một dự án outsource/maintain cũ (hoặc thành viên mới join dự án) mà tài liệu setup đã lỗi thời, tôi muốn có một bộ hướng dẫn cài đặt môi trường chuẩn xác và đồng bộ, để đưa code lên chạy được trên máy cục bộ mà không làm gián đoạn thời gian của người khác | Team Dev, Tester, thành viên mới | Tự cài mất 4–8 tiếng (nửa đến 1 ngày làm việc); nhờ người hỗ trợ mất 60–120 phút của cả 2 người; xảy ra mỗi khi có dự án mới hoặc người mới join (5-6 lần/quý) |
| 2 | Pain từ người khác | Khi Tester thực hiện kiểm thử và phát hiện lỗi mà trên máy Dev lại chạy bình thường (lỗi "it works on my machine"), tôi muốn nhanh chóng xác định sự khác biệt về môi trường, cấu hình và dữ liệu giữa hai máy, để thống nhất nguyên nhân gốc rễ và xử lý bug mà không mất thời gian tranh cãi | Team Dev, Tester | Mất 60–180 phút mỗi lần xảy ra bất đồng để đối chiếu log và môi trường giữa 2 máy; xảy ra khoảng 1–2 lần mỗi sprint 2 tuần |
| 3 | Pain từ người khác | Khi phát triển tính năng mà API trên Swagger bị thiếu hoặc không hoạt động đúng tài liệu thiết kế, tôi muốn định vị chính xác đầu mối chịu trách nhiệm của API đó, để xác nhận và thống nhất yêu cầu sửa đổi nhanh nhất mà không phải hỏi vòng qua nhiều cấp quản lý | Frontend Dev, Backend Dev, BA | Mất 30 phút đi hỏi vòng qua BA/Techlead/PM để tìm ra người phụ trách; chờ thêm 30–60 phút để sửa API mới làm tiếp được task; xảy ra 2–3 lần mỗi sprint |
| 4 | Lặp lại | Khi đến kỳ release cuối sprint, tôi muốn tổng hợp nhanh danh sách commit và pull request tương ứng với các task Jira, để lập release note bàn giao cho khách hàng/QC mà không phải copy tay từng link | Dev, Techlead, QC | Mất 45–60 phút vào cuối mỗi sprint 2 tuần để dò lại danh sách commit và điền vào template release note |
| 5 | Lặp lại | Khi bắt đầu buổi họp daily standup hoặc cuối ngày làm việc, tôi muốn có sẵn bản tóm tắt các task/commit đã hoàn thành và blocker phát sinh từ Git và Jira, để cập nhật tiến độ cho lead trong 2 phút mà không phải ngồi lục lại lịch sử | Dev, PM, Scrum Master | Mất 10–15 phút mỗi ngày trước giờ họp standup để xem lại git log và Jira xem hôm qua đã làm những gì |
| 6 | Tốn thời gian | Khi hệ thống trên môi trường kiểm thử (staging) gặp lỗi 500, tôi muốn định vị ngay dòng log và stack trace gây lỗi chính xác kèm bối cảnh liên quan, để khoanh vùng nguyên nhân mà không phải cuộn đọc qua hàng nghìn dòng log rác | Backend Dev, Tester | Mất 30–60 phút mỗi lần tải và đọc file log server dài hàng nghìn dòng; xảy ra 2–4 lần mỗi tuần |
| 7 | Cần đọc, tổng hợp nhiều thông tin | Khi cần tích hợp một thư viện/SDK bên thứ ba vào dự án mà tài liệu có nhiều phiên bản mâu thuẫn nhau, tôi muốn tổng hợp các bước tích hợp cốt lõi và các lỗi thường gặp nhất, để hoàn thành kết nối API mà không phải mò mẫm thử nghiệm nhiều lần | Dev | Mất 3–4 tiếng đọc qua 4–5 bài blog/issues trên GitHub; từng có lần mất cả ngày chỉ vì một lỗi cấu hình nhỏ ở version mới |
| 8 | Cần đọc, tổng hợp nhiều thông tin | Khi nhận tài liệu đặc tả nghiệp vụ (BRD/SRS) dài với nhiều quy tắc nghiệp vụ phụ thuộc chéo, tôi muốn nắm rõ toàn bộ các điều kiện biên và ma trận logic, để viết code xử lý chính xác ngay từ đầu mà không bị sót trường hợp | Dev, BA | Mất 2–3 tiếng đọc và tự vẽ bảng logic; trung bình mỗi tính năng phức tạp có 1–2 lỗi do sót điều kiện biên khi test |
| 9 | Pain từ người khác | Khi tạo Pull Request (PR) lớn gồm nhiều file thay đổi, tôi muốn reviewer nắm được ngữ cảnh và các điểm thay đổi trọng tâm, để nhận được góp ý chất lượng và merge code nhanh chóng mà không bị tắc luồng làm việc | Dev gửi PR, Dev review PR | PR lớn thường bị treo review từ 1–2 ngày; reviewer mất 30–45 phút đọc code mà không hiểu hết ý đồ kiến trúc |
| 10 | Tốn thời gian | Khi dựng xong tính năng mới cần test nhiều kịch bản khác nhau, tôi muốn có bộ dữ liệu mẫu (mock data) đa dạng và đúng chuẩn schema cơ sở dữ liệu, để kiểm thử đầy đủ các case mà không phải tự gõ tay từng dòng dữ liệu | Dev, Tester | Mất 30–60 phút mỗi lần tạo mock data thủ công; thường chỉ test được 2–3 case cơ bản dẫn đến sót bug khi lên staging |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- **Ý AI gợi ý được giữ lại:**
  - Giữ lại các ý #4 (Release note), #5 (Daily standup log), #6 (Phân tích log lỗi 500), #7 (Tổng hợp docs SDK), #8 (Đặc tả nghiệp vụ), #9 (Context cho PR), #10 (Tạo mock data). 
  - *Lý do:* Các ý này đều là nỗi đau có thật trong quy trình phát triển phần mềm hàng ngày của tôi. Tôi đã viết lại theo đúng trải nghiệm thực tế của bản thân và bổ sung số liệu đo lường cụ thể từ các dự án đã tham gia.
- **Ý AI gợi ý bị loại bỏ:**
  - Gợi ý *"Trợ lý AI tự động fix bug khi có exception"*: Bị bỏ vì giải pháp quá viển vông, không khả thi trong môi trường code bảo mật của dự án outsource, thiếu quy trình cụ thể và dễ gây ảo tưởng.
  - Gợi ý *"Chatbot AI tự động giao tiếp và giải thích tiến độ cho khách hàng"*: Bị bỏ vì việc giao tiếp với khách hàng đòi hỏi sự khéo léo ngoại giao và bảo mật thông tin kinh doanh, thuộc thẩm quyền của PM/Account Manager, không thể giao cho AI.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Setup môi trường dự án cũ / onboard người mới (Problem #1) | Nỗi đau lớn nhất (mất 4–8 tiếng), quy trình rõ ràng, bottleneck cụ thể, dễ so sánh giải pháp No AI (Docker) với AI | Có những dự án legacy cấu hình rất phức tạp, liệu AI có hiểu hết ngữ cảnh hệ thống hay chỉ xử lý được các lỗi phổ biến? |
| 2 | Lệch môi trường kiểm thử giữa Dev và Test (Problem #2) | Gây xung đột và mất thời gian đối chiếu giữa 2 team (60–180 phút), tần suất cao trong mỗi sprint | Nguyên nhân lệch môi trường đôi khi nằm ở dữ liệu test chứ không phải cấu hình, việc thu thập đủ thông tin để phân tích có khả thi không |
| 3 | API Swagger lệch tài liệu thiết kế hoặc thiếu đầu mối (Problem #3) | Gây tắc nghẽn công việc của Frontend Dev, tốn thời gian giao tiếp trung gian qua nhiều cấp quản lý | Vấn đề này có thể chỉ cần siết lại quy trình và metadata trên Swagger mà không nhất thiết cần đến công cụ phức tạp |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi tiếp nhận một dự án outsource/maintain cũ (hoặc thành viên mới join dự án) mà tài liệu setup đã lỗi thời, tôi muốn có một bộ hướng dẫn cài đặt môi trường chuẩn xác và đồng bộ, để đưa code lên chạy được trên máy cục bộ mà không làm gián đoạn thời gian của người khác |
| Actor | Developer mới join dự án, Tester, Techlead phụ trách dự án |
| Thời điểm / bối cảnh | Ngày đầu tiên tiếp nhận dự án outsource hoặc onboard thành viên mới vào team |
| Quy trình hiện tại (3–7 bước) | 1. Nhận quyền truy cập repo và đọc README.md cũ (15')<br>2. Tải và cài đặt các runtime, SDK, database theo docs cũ (45')<br>3. Cài đặt dependencies và tạo file cấu hình môi trường .env (30')<br>4. Build và run project, gặp lỗi crash do xung đột thư viện / version (180')<br>5. Nhờ Dev cũ hoặc Techlead sang pair-debug và sửa từng lỗi cấu hình (90') |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4 & 5: Dò lỗi mâu thuẫn dependency và phải gọi Dev cũ hỗ trợ debug trực tiếp (mất tổng cộng 270 phút) |
| Impact (nếu không giải thì sao) | Lãng phí 4–8 tiếng của nhân sự mới; làm gián đoạn 1–2 tiếng của Senior/Techlead; chậm tiến độ kickoff sprint 1–2 ngày |
| Success metric (baseline → target) | Thời gian thao tác và gỡ lỗi cấu hình của người cài từ 270 phút xuống dưới 30 phút; số lần cần người khác can thiệp trực tiếp giảm từ 3–4 lần xuống 0 lần |
| Phương án không dùng AI | Container hóa toàn bộ môi trường bằng Docker (Dockerfile + docker-compose) kèm script tự động kiểm tra biến môi trường .env |
| Giả thuyết về AI (nếu có) | AI phân tích log lỗi khi build fail, đối chiếu package.json / requirements.txt với hệ điều hành để chỉ ra đúng version xung đột và đề xuất lệnh sửa |
| Cảm nhận nhanh | Rule hoặc Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — Tổng thời gian: ~360 phút (6 tiếng)

[1. Đọc docs cũ: 15'] 
  --> [2. Cài runtime/SDK: 45'] 
  --> [3. Cài packages & .env: 30'] 
  --> [4. Build project & gặp lỗi crash: 180'] <--- BOTTLENECK CHÍNH
  --> [5. Nhờ Techlead pair-debug: 90']        <--- BOTTLENECK PHỤ
  --> [6. Code chạy thành công: 0']
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi Tester thực hiện kiểm thử và phát hiện lỗi mà trên máy Dev lại chạy bình thường (lỗi "it works on my machine"), tôi muốn nhanh chóng xác định sự khác biệt về môi trường, cấu hình và dữ liệu giữa hai máy, để thống nhất nguyên nhân gốc rễ và xử lý bug mà không mất thời gian tranh cãi |
| Actor | Developer và Tester trong dự án |
| Thời điểm / bối cảnh | Giai đoạn kiểm thử tính năng cuối sprint trước khi release lên staging |
| Quy trình hiện tại (3–7 bước) | 1. Tester log ticket bug lên Jira kèm mô tả lỗi (10')<br>2. Dev kéo code về máy mình chạy thử, thấy pass và từ chối bug (15')<br>3. Tester và Dev hẹn họp đối chiếu từng bước tái hiện bug (30')<br>4. So sánh thủ công cấu hình môi trường, version database, dữ liệu test giữa 2 máy (60')<br>5. Xác định điểm lệch (thiếu migration, lệch timezone, cache) và sửa cấu hình (25') |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4: So sánh thủ công các thông số môi trường, cấu hình và dữ liệu giữa 2 máy (mất 60 phút) |
| Impact (nếu không giải thì sao) | Mất 140 phút cho mỗi case tranh cãi; gây căng thẳng giữa 2 team; nguy cơ lọt lỗi tiềm ẩn lên môi trường production |
| Success metric (baseline → target) | Thời gian xác định điểm sai lệch giữa 2 môi trường từ 90 phút xuống dưới 10 phút; giảm số buổi họp tranh cãi tay đôi từ 2–3 buổi/sprint xuống 0 |
| Phương án không dùng AI | Chuẩn hóa môi trường test chung bằng Docker runner cố định và chạy test tự động trên CI/CD pipeline giống nhau |
| Giả thuyết về AI (nếu có) | AI nhận log và system dump từ máy Dev và máy Test, tự động highlight các điểm sai lệch về phiên bản package hoặc tham số môi trường |
| Cảm nhận nhanh | Rule |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — Tổng thời gian: ~140 phút

[1. Log bug Jira: 10'] 
  --> [2. Dev test máy mình: 15'] 
  --> [3. Họp đối chiếu tái hiện bug: 30'] 
  --> [4. So sánh cấu hình/data thủ công: 60'] <--- BOTTLENECK CHÍNH
  --> [5. Sửa lệch môi trường: 25']
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi phát triển tính năng mà API trên Swagger bị thiếu hoặc không hoạt động đúng tài liệu thiết kế, tôi muốn định vị chính xác đầu mối chịu trách nhiệm của API đó, để xác nhận và thống nhất yêu cầu sửa đổi nhanh nhất mà không phải hỏi vòng qua nhiều cấp quản lý |
| Actor | Frontend Developer, Backend Developer, BA |
| Thời điểm / bối cảnh | Khi Frontend Dev bắt đầu ghép API vào giao diện người dùng |
| Quy trình hiện tại (3–7 bước) | 1. Frontend Dev đọc tài liệu đặc tả và mở Swagger tìm endpoint (10')<br>2. Endpoint bị thiếu hoặc gọi thử trả về mã lỗi 404/500 (10')<br>3. Nhắn tin hỏi BA xem tài liệu thiết kế có thay đổi không (15')<br>4. BA hỏi tiếp Techlead/PM để xác nhận ai là người viết API đó (20')<br>5. Tìm được Backend Dev phụ trách, trao đổi thống nhất và chờ cập nhật API (35') |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 & 4: Giao tiếp lòng vòng qua BA, Techlead, PM để tìm ra người phụ trách (mất 35 phút) |
| Impact (nếu không giải thì sao) | Frontend Dev bị block task từ 1–2 tiếng; làm gián đoạn 3–4 người vì các chuỗi tin nhắn hỏi đáp; dễ chậm tiến độ bàn giao sprint |
| Success metric (baseline → target) | Thời gian xác định đúng người phụ trách và nguyên nhân lệch API từ 90 phút xuống dưới 15 phút; giảm số người tham gia trao đổi trung gian từ 3 người xuống 0 |
| Phương án không dùng AI | Bổ sung quy định ghi metadata rõ ràng trên Swagger (author, task ID) + checklist kiểm tra API trước khi bàn giao sang Frontend |
| Giả thuyết về AI (nếu có) | AI đối chiếu OpenAPI schema với tài liệu thiết kế và phân tích git blame của repo backend để tự động báo điểm lệch và người phụ trách |
| Cảm nhận nhanh | Rule hoặc Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — Tổng thời gian: ~90 phút

[1. Đọc docs & tìm API: 10'] 
  --> [2. Gọi API lỗi / thiếu: 10'] 
  --> [3. Hỏi BA: 15'] 
  --> [4. BA hỏi Techlead/PM: 20'] <--- BOTTLENECK CHÍNH (Giao tiếp trung gian)
  --> [5. Trao đổi Dev & chờ sửa: 35']
```

### Card muốn pitch nhất

- Card số: Card #1 (Setup môi trường dự án cũ / maintain / onboard thành viên mới)
- Vì sao: Đây là nỗi đau lớn nhất và tốn nhiều thời gian nhất của team (4–8 tiếng), hầu như ai trong ngành phần mềm cũng từng gặp phải. Quy trình có bottleneck rất rõ ràng (lỗi crash do xung đột thư viện), và là bài toán điển hình để so sánh tính hiệu quả giữa No AI (Docker/Script) và AI Workflow.
- Câu hỏi muốn nhóm phản biện: Nếu một dự án outsource quá cũ (legacy code không hỗ trợ Docker chuẩn) thì AI có thể giúp phân tích log lỗi để tự động vá các script cài đặt không, hay chỉ cần một checklist và bộ script thủ công là đủ?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Target metric giảm từ 360 phút xuống 45 phút là quá lạc quan nếu máy yếu download package chậm | Đồng ý | Sửa lại metric: tách riêng thời gian thao tác và gỡ lỗi của người cài (từ 270 phút xuống dưới 30 phút), không tính thời gian tải dữ liệu thụ động của máy tính |
| Đề xuất AI tự động sinh và chạy script cài đặt có nguy cơ bảo mật lớn (chạy lệnh nguy hiểm hoặc quyền admin) | Đồng ý | Thêm boundary rõ ràng: AI chỉ dừng lại ở việc đọc log, giải thích nguyên nhân và gợi ý giải pháp; con người (Dev) là người kiểm tra và bấm chạy |
| Đưa AI vào bài toán này có thể là "dùng dao mổ trâu giết gà" vì Docker đã giải quyết được 80% | Đồng ý một phần | Làm rõ trong card: Docker là giải pháp No AI nền tảng; AI chỉ là Workflow can thiệp ở bước phân tích log khi gặp lỗi xung đột package phức tạp |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Chuẩn bị và trình bày Problem Card #1: "Setup môi trường dự án outsource/maintain cũ (hoặc onboard dev mới) bị lỗi thời tài liệu và xung đột dependency" trong 2 phút; nêu rõ bottleneck tốn 270 phút và đề xuất so sánh Docker vs AI Workflow | Nhóm nhận thấy đây là nỗi đau chung cả 4 thành viên đều từng gặp; ý tưởng được nhóm nhất trí đưa vào shortlist top 3 và chọn làm đề tài chung |
| Phản biện bài của bạn khác | Đặt câu hỏi phản biện cho bài tạo README của Khanh (về tần suất thấp 1-2 lần/kỳ và AI không hiểu nghiệp vụ), bài tóm tắt git diff (về việc AI text không ngăn được bug runtime), và bài theo dõi tiến độ Zalo/LMS của Khôi & Vũ (về rào cản API đóng và giải pháp No-AI có sẵn) | Giúp các thành viên nhận ra rào cản kỹ thuật của các nền tảng đóng (Zalo, LMS) và bẫy "tiện ích sinh viên"; nhóm đồng thuận loại bỏ các ý này để tập trung vào bài toán kỹ thuật |
| Nhận phản biện | Nhận câu hỏi từ Khanh: *"Nếu dự án đã có sẵn Dockerfile thì bài toán này còn tồn tại không?"* và từ Khôi: *"Tại sao Tester không test trên Staging mà test local? Nếu lệch do DB data/migration thì AI có vi phạm bảo mật không?"* | Tôi làm rõ: Dự án outsource cũ thường không có Docker, hoặc base image/dependency cũ bị crash. Đồng thời thừa nhận Card #2 phụ thuộc nhiều vào quy trình CI/CD Staging (No-AI), nên tôi chủ động đề xuất nhóm dồn toàn lực vào Card #1 |
| Gom cluster / cây OST | Cùng nhóm gom 12 candidate thành 4 cụm (A: Môi trường & Triển khai dev/test; B: Hỗ trợ tài liệu & Báo cáo; C: Tiện ích đời sống; D: Quản lý học tập). Gạch bỏ các ý solution đội lốt ("AI tự fix bug", "Bot đọc tin nhắn Zalo") | Xây dựng thành công cây OST với Outcome chung: *"Giảm 70% thời gian chết (downtime) và tắc nghẽn của kỹ sư/thành viên khi tiếp nhận và chuyển giao mã nguồn dự án"* |
| Chọn candidate problem | Chủ trì buổi chấm điểm shortlist 3 candidate theo 7 tiêu chí trong rubric | Candidate #1 đạt điểm cao nhất (34/35 điểm) và được cả nhóm thống nhất 100% làm bài toán chung của nhóm |
| Kiểm chứng / research | Hướng dẫn bạn Khôi chuẩn bị kịch bản phỏng vấn The Mom Test; cùng Vũ rà soát các giả định trong Assumption Map; kiểm tra đối chiếu các link tài liệu kỹ thuật về Docker Compose và VS Code Dev Containers do Khanh tìm | Xác nhận được nỗi đau lớn nhất của dev không phải là cài đặt công cụ mà là bất lực trước log crash xung đột thư viện; phát hiện khoảng trống của Docker là không giải thích được nguyên nhân khi build image fail |
| Quy trình nhóm | Trực tiếp thiết kế và vẽ sơ đồ Quy trình tương lai (Mục 4.2) chuẩn hóa: phân định rõ 3 lớp: Rule (Docker Compose + script check .env) → AI Workflow (phân tích log lỗi khi build fail) → Con người HITL (kỹ sư duyệt và chạy lệnh) | Giúp cả nhóm hình dung trực quan ranh giới giữa Rule và AI, tránh sa đà vào việc dùng AI cho những bước chỉ cần automation script |
| Problem Statement | Cùng bạn Vũ hoàn thiện bản Problem Statement v0 và nâng cấp lên v1; thiết lập Success Metric có baseline và target rõ ràng (270' -> 30'); thiết lập Boundary chặt chẽ (AI không tự ý chạy script quyền root/admin) | Xác định Success Metric có baseline và target rõ ràng (270' -> 30'); thiết lập Boundary chặt chẽ (AI không tự ý chạy script quyền root, không đọc source code nghiệp vụ bảo mật) |
| Mức can thiệp AI | Trực tiếp phân tích bài toán trên ma trận độ phức tạp × độ mơ hồ; lập luận chặt chẽ vì sao chọn Workflow mà không chọn Agent | Thống nhất mức can thiệp là Workflow: Docker chuẩn hóa môi trường (Rule), AI chỉ can thiệp khi có exception/build fail để trích xuất nguyên nhân, đảm bảo tính tất định và an toàn hệ thống |
| Quyết định | Cùng nhóm đánh giá 4 rủi ro sản phẩm (Value, Usability, Feasibility, Viability) và đưa ra quyết định "Go, phạm vi nhỏ" kèm ngưỡng dừng cụ thể | Nhóm thống nhất kết luận Go (Pilot phạm vi nhỏ trên các dự án Node.js/Python) với ngưỡng dừng rõ ràng: Nếu sau 2 tuần pilot mà AI gợi ý sai quá 40% lỗi dependency thì dừng và quay về checklist thủ công |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Gợi ý thêm các góc nhìn vấn đề quanh quy trình phát triển phần mềm | Mở rộng thêm các khía cạnh tốn thời gian như release notes, standup log, phân tích log lỗi 500 | Gợi ý các giải pháp viển vông ("AI tự fix bug", "chatbot nói chuyện với khách") và không có số liệu đo lường thật | Loại bỏ các ý không khả thi, tự viết lại Job Story và gắn số liệu thời gian/tần suất thật từ các dự án đã làm |
| CP2 Problem Card | Đóng vai PM hoài nghi để phản biện và chỉ ra lỗ hổng trong Problem Card | Chỉ ra điểm yếu về việc metric thời gian quá lạc quan và rủi ro bảo mật nếu để AI tự chạy lệnh shell | Gợi ý giải pháp AI Agent phức tạp tự sửa code, xem nhẹ vai trò của Docker/Rule | Giữ vững quan điểm No AI (Docker) là nền tảng, AI chỉ hỗ trợ phân tích log lỗi xung đột; bổ sung boundary con người duyệt lệnh |
| CP4 Research | Tìm kiếm các công cụ và pattern hiện có trên thị trường đã giải quyết bài toán setup môi trường | Gợi ý nhanh các công cụ thực tế như Dev Containers, Docker Compose và GitHub Copilot in the CLI | Đưa một số đường link bài viết không tồn tại (lỗi 404) và phóng đại khả năng tự động fix bug của terminal tools | Tự tay mở từng link tài liệu chính thức của Microsoft, Docker và GitHub để kiểm chứng, chỉ giữ lại các tính năng có thật |
| CP5 Quy trình | Chuyển đổi mô tả các bước quy trình tương lai thành cú pháp sơ đồ Mermaid | Sinh cú pháp Mermaid nhanh, trực quan, phân nhánh điều kiện (nếu build pass vs nếu build fail) rõ ràng | AI tự ý gộp bước "AI phân tích log" và "chạy lệnh sửa" thành một bước tự động hoàn toàn, làm mất bước kiểm duyệt của con người (HITL) | Tách riêng bước AI đề xuất lệnh và bước Kỹ sư kiểm tra an toàn; bổ sung đường rollback (nếu lệnh không sửa được thì quay về hỏi Techlead) |
| CP5–6 Problem Statement | Đóng vai reviewer để soi xem Problem Statement có bị lẫn "solution" vào phần mô tả problem không | Chỉ ra chỗ tôi từng viết "cần một công cụ AI phân tích log" ở mục Problem là bị lỗi solution-first | Gợi ý các metric chung chung, sáo rỗng như "tăng năng suất 50%", "tối ưu hóa quy trình" | Viết lại Problem Statement thuần túy về nỗi đau và điểm nghẽn; giữ nguyên metric đo bằng phút thực tế (270' xuống dưới 30') |
| CP6 Mức can thiệp / quyết định | Thử thách các giả định về việc có nên nâng cấp lên Agent tự động hoàn toàn không | Nêu ra các rủi ro bảo mật tiềm ẩn khi cấp quyền cho AI chạy trong terminal (như vô tình xóa dữ liệu, tải gói mã độc qua npm/pip) | Vẫn thiên vị việc dùng Agent phức tạp để "tự động hóa toàn diện từ A-Z" cho ấn tượng | Kiên quyết giữ mức Workflow, nhấn mạnh nguyên tắc can thiệp tối thiểu (bắt đầu từ No-AI/Docker, chỉ dùng AI ở bước bóc tách log lỗi) |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Khi lắng nghe phần trình bày top 3 problem card của các bạn trong nhóm (Khanh, Khôi, Vũ), bài học lớn nhất tôi rút ra được là: sinh viên công nghệ thông tin chúng tôi rất dễ bị hấp dẫn bởi những vấn đề "tiện ích sinh viên quen thuộc" xung quanh đời sống học tập hàng ngày như nhắc deadline từ LMS, gom tài liệu học tập rải rác trên Zalo/Drive, hay tạo file README khi làm xong bài tập lớn. Những ý tưởng này nghe qua thì có vẻ rất gần gũi, nhưng khi đặt dưới lăng kính phân tích khắt khe của Discovery & Problem Framing, tôi nhận ra chúng bộc lộ 3 điểm yếu rất chí mạng. Thứ nhất, tần suất sử dụng quá thấp: một kỳ học sinh viên chỉ làm 1–2 bài tập lớn hoặc đồ án, một việc cả kỳ chỉ làm một vài lần thì không thể coi là nỗi đau nhức nhối cấp thiết cần xây dựng một giải pháp riêng. Thứ hai, bản chất vấn đề nằm ở thói quen và ý thức kỷ luật của cá nhân/nhóm chứ không phải do thiếu công cụ AI: việc quên deadline hay không tìm thấy tài liệu hoàn toàn có thể giải quyết triệt để trong 5–10 phút bằng các công cụ No-AI miễn phí như Google Calendar hay một folder Google Drive chung. Thứ ba và nguy hiểm nhất là rào cản nền tảng: các ứng dụng như Zalo, Messenger, hệ thống LMS trường học đều là hệ sinh thái đóng kín, chặn API bên ngoài, khiến nhóm hoàn toàn không có khả năng lấy dữ liệu để xây dựng bản thử nghiệm (pilot/PoC). Nhờ lắng nghe các bạn, tôi hiểu rằng một problem thực sự đáng giải quyết phải xuất phát từ một quy trình công việc có thật, có người chịu đau rõ ràng, đo lường được bằng số phút lãng phí cụ thể, và quan trọng là nằm trong tầm kiểm soát công nghệ của nhóm.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Nhóm chúng tôi đã rơi vào cái bẫy "solution-first" ít nhất hai lần rất rõ rệt trong suốt buổi làm việc. Lần thứ nhất xảy ra ngay ở vòng pitch ý tưởng của bạn đề xuất đề tài "Tự động tạo README.md từ code": bạn ấy đã nghĩ ngay đến việc xây dựng một tool dùng mô hình ngôn ngữ lớn (LLM) để quét toàn bộ mã nguồn rồi tự động vẽ bảng biểu, tóm tắt các hàm và xuất ra file Markdown. Tuy nhiên, khi nhóm phản biện bằng câu hỏi: "Thực sự giảng viên chấm điểm cái gì trong README và sinh viên cần README để làm gì?", chúng tôi mới ngỡ ngàng nhận ra rằng điều cốt lõi người chấm cần là hướng dẫn cài đặt môi trường để chạy được code (chạy lệnh gì, biến môi trường `.env` thế nào), chứ không ai cần một bản tóm tắt hàm mà AI đọc chay từ code ra. Lần thứ hai lại xuất hiện ngay trong bài toán Card #1 của chính tôi: ban đầu tôi từng ảo tưởng muốn xây dựng một "Agent AI toàn năng tự động gõ lệnh sửa lỗi build trong terminal". Cả nhóm đã kịp thời "phanh" tôi lại khi phân tích ma trận No-AI vs AI: công nghệ container hóa (Docker) đã ra đời hơn một thập kỷ qua và giải quyết được tới 80% bài toán chuẩn hóa môi trường, vậy tại sao chúng ta lại cố chấp dùng AI để làm việc mà một file Dockerfile hoặc Docker Compose làm tốt hơn, nhanh hơn và tin cậy hơn 100 lần? Nhóm đã xử lý bằng cách bóc tách bài toán thành hai phần rạch ròi: phần hạ tầng cài đặt giao toàn bộ cho Docker (No-AI), còn AI chỉ can thiệp vào đúng một điểm nghẽn duy nhất mà Docker bó tay: đó là đọc và phân tích file log crash dài hàng nghìn dòng để giải thích xung đột dependency khi build thất bại.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Tôi đã có một lần đổi ý mang tính bước ngoặt sau khi bị AI (đóng vai một Product Manager hoài nghi) và các thành viên nhóm phản biện gay gắt về Problem Card #1. Ban đầu, trong bản nháp đầu tiên, tôi đặt ra một chỉ số thành công (Success Metric) cực kỳ lạc quan và có phần ngây thơ: "giảm tổng thời gian cài đặt môi trường từ 360 phút xuống còn 45 phút", đồng thời đề xuất giải pháp cho phép AI tự động sinh ra các dòng lệnh shell và tự động chạy chúng trong terminal của máy tính để khắc phục lỗi. Lời phản biện đã chỉ ra hai lỗ hổng không thể chối cãi: Thứ nhất, tổng thời gian 360 phút bao gồm cả thời gian máy tính tải các package nặng hàng gigabyte từ Internet về máy, việc này phụ thuộc hoàn toàn vào tốc độ đường truyền mạng và phần cứng máy tính, AI không thể nào can thiệp để rút ngắn thời gian tải dữ liệu thụ động này được. Thứ hai, và là rủi ro nghiêm trọng nhất về mặt kỹ thuật, việc cấp quyền cho AI tự ý chạy lệnh shell trong terminal (nhất là các lệnh đòi hỏi quyền root/admin như `sudo`) có thể xóa nhầm dữ liệu quan trọng hoặc làm hỏng cả hệ điều hành nếu AI sinh ảo giác (hallucination). Tôi nhận thấy phản biện này hoàn toàn chính xác và đã lập tức thay đổi quan điểm: tôi sửa lại Success Metric thành "thời gian thao tác và gỡ lỗi của kỹ sư giảm từ 270 phút xuống dưới 30 phút" (tách riêng thời gian máy tải thụ động), đồng thời thiết lập một Ranh giới an toàn (Boundary) bất khả xâm phạm: AI tuyệt đối chỉ được đề xuất câu lệnh dưới dạng văn bản giải thích, quyền kiểm tra và bấm nút thực thi cuối cùng bắt buộc phải thuộc về kỹ sư con người (Human-in-the-Loop).

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Quá trình kiểm chứng thực tế qua phỏng vấn The Mom Test và nghiên cứu thị trường đã mang lại cho tôi hai điều vô cùng bất ngờ. Điều bất ngờ thứ nhất đến từ buổi phỏng vấn một bạn lập trình viên từng làm việc tại công ty gia công phần mềm (outsource): tôi từng nghĩ rằng các lập trình viên ghét nhất là việc phải tải và cài đặt nhiều công cụ lặt vặt (như Node.js, Python, PostgreSQL). Nhưng người được phỏng vấn khẳng định rằng việc cài đặt công cụ chỉ tốn vài cú click chuột và không hề gây ức chế; điều thực sự khiến họ "phát điên" và cảm thấy bất lực nhất chính là khoảnh khắc gõ lệnh `build` hoặc `run` và terminal ném ra một chuỗi thông báo lỗi màu đỏ dài dằng dặc báo xung đột phiên bản thư viện giữa các package cũ từ 3–4 năm trước. Họ mất hàng tiếng đồng hồ chỉ để copy từng dòng stack trace lên Google và StackOverflow nhưng không tìm thấy câu trả lời phù hợp với bối cảnh hệ điều hành của mình. Điều bất ngờ thứ hai đến từ phần nghiên cứu các giải pháp hiện có trên thị trường: tôi nhận ra các công cụ đầu ngành như VS Code Dev Containers hay Docker Compose tuy giải quyết rất tốt khâu đóng gói môi trường nhưng lại để lộ một "khoảng trống chết người": khi file Dockerfile bị lỗi do một package upstream bị thay đổi hoặc một dependency bị xóa khỏi kho lưu trữ, Docker chỉ báo lỗi `non-zero code` và dừng lại mà hoàn toàn không thể giải thích cho người dùng biết phải sửa thế nào. Điều này chứng minh rằng khoảng trống thị trường mà nhóm tôi nhắm tới — dùng AI làm một workflow chuyên bóc tách log lỗi crash và đề xuất phương án vá — là một nhu cầu có thật 100% và cực kỳ cấp thiết.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Điều khó khăn và thử thách nhất đối với tôi khi viết Problem Statement là **buộc bản thân phải từ bỏ thói quen tư duy của một kỹ sư để không lén lút cài cắm giải pháp (solution) vào phần mô tả vấn đề, đồng thời phải định nghĩa được một Ranh giới an toàn (Boundary) thực sự chặt chẽ**. Là dân kỹ thuật, phản xạ tự nhiên của tôi là khi thấy vấn đề liền lập tức nghĩ đến công nghệ: trong bản nháp đầu tiên (v0), tôi liên tục viết những câu như "Developer thiếu một công cụ AI để phân tích log lỗi build" hay "cần xây dựng trợ lý AI tự động sửa dependency". Tôi đã phải xóa đi viết lại rất nhiều lần để đưa câu chữ về đúng bản chất của nỗi đau: mô tả tình huống tiếp nhận dự án cũ, tài liệu lỗi thời, và sự lãng phí 270 phút của cả nhân sự mới lẫn Techlead để gỡ lỗi thủ công. Thách thức lớn thứ hai là việc lượng hóa Success Metric sao cho có thể đo lường và kiểm chứng được bằng số liệu thực tế: việc xác định baseline (270 phút) và target (dưới 30 phút) đòi hỏi phải bóc tách quy trình thành từng bước bấm giờ chi tiết chứ không thể nói chung chung kiểu "giúp tăng năng suất 50%". Cuối cùng, việc viết trường Boundary ép nhóm phải trả lời câu hỏi hóc búa nhất: "AI không được làm gì?". Việc vạch rõ ranh giới cấm AI đọc mã nguồn nghiệp vụ của khách hàng và cấm AI tự chạy lệnh shell chính là chốt chặn quan trọng nhất biến Problem Statement từ một ý tưởng viển vông thành một bài toán khả thi và an toàn để triển khai.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Nếu có cơ hội được làm lại buổi học này từ đầu, tôi sẽ thay đổi trình tự làm việc của nhóm bằng cách **đẩy hoạt động kiểm chứng thực tế (The Mom Test) lên sớm hơn một nhịp, ngay từ giai đoạn hội tụ nhóm ở Checkpoint 3 thay vì chờ đến Checkpoint 4**. Trong buổi thảo luận nhóm, chúng tôi đã tiêu tốn gần 30 phút quý báu chỉ để tranh luận thuần túy dựa trên suy đoán lý thuyết về tính khả thi của các đề tài sinh viên như quản lý deadline hay đọc tin nhắn Zalo. Nếu lúc đó nhóm nhanh chóng phỏng vấn nhanh 1–2 bạn sinh viên ngồi bàn bên cạnh hoặc thử tra cứu chính sách API của Zalo ngay lập tức, chúng tôi sẽ nhận ra sự bế tắc của các ý tưởng đó chỉ trong vòng 5 phút và tiết kiệm được rất nhiều năng lượng tranh cãi. Bên cạnh đó, tôi sẽ phản biện nhóm một cách quyết liệt và mạnh mẽ hơn ở việc **thẳng thừng loại bỏ ngay từ đầu các đề tài thuộc nhóm 'tiện ích sinh viên thiếu động lực sử dụng lâu dài'**. Một số thành viên trong nhóm ban đầu rất tha thiết giữ lại đề tài làm đẹp CV hay quản lý deadline vì cảm thấy gần gũi với bản thân, nhưng lại quên mất rằng trong một môn học về AI Product Engineering, một bài toán tốt phải có quy trình kỹ thuật rõ ràng, có dữ liệu đầu vào ổn định và tạo ra tác động kinh tế đo đếm được. Việc nhân nhượng để thảo luận quá lâu những ý tưởng này đã làm chậm tiến độ chung của cả nhóm.

**6.7. Hiểu bài: Chuỗi liên kết (Problem → Quy trình → Metric → Boundary → Mức can thiệp AI → Quyết định)**

Bài toán của nhóm bắt đầu từ **Problem**: Lập trình viên khi tiếp nhận dự án outsource/maintain cũ (hoặc onboard dev mới) lãng phí 4–8 tiếng để cài đặt môi trường do tài liệu setup lỗi thời và xung đột phiên bản thư viện. Phân tích **Quy trình** hiện tại 5 bước (tổng 360 phút) chỉ ra **Bottleneck** cốt lõi nằm ở bước 4 và 5: dò lỗi crash khi build và phải nhờ Senior/Techlead sang pair-debug trực tiếp (chiếm tới 270 phút). Từ điểm nghẽn này, nhóm xác lập **Success Metric** định lượng rõ ràng: giảm thời gian thao tác và gỡ lỗi của kỹ sư từ 270 phút xuống dưới 30 phút, đồng thời đưa số lần cần Techlead can thiệp thủ công từ 3–4 lần về 0. Để bảo vệ an toàn hệ thống và mã nguồn dự án, nhóm đặt ra **Boundary** nghiêm ngặt: AI tuyệt đối không đọc source code nghiệp vụ (chỉ đọc file log crash và manifest thư viện), không có quyền tự ý thực thi lệnh shell, mọi đề xuất phải do kỹ sư duyệt (Human-in-the-Loop). Dựa trên ma trận độ phức tạp trung bình và độ mơ hồ trung bình, nhóm chọn **Mức can thiệp là Workflow**: dùng Docker Compose (No-AI) để chuẩn hóa hạ tầng và chỉ tích hợp AI ở đúng bước phân tích log lỗi build để trích xuất nguyên nhân và gợi ý câu lệnh vá. Cuối cùng, qua đánh giá 4 khía cạnh rủi ro (Value, Usability, Feasibility, Viability) đều ở mức an toàn, nhóm đưa ra **Quyết định: GO (Pilot phạm vi nhỏ)** cho các dự án Web Node.js/Python, kèm **Ngưỡng dừng** rõ ràng: nếu sau 2 tuần pilot mà AI gợi ý sai quá 40% lỗi dependency thì lập tức dừng lại và quay về checklist thủ công kết hợp Dockerfile mẫu.

---

## 7. Tài liệu tham khảo

1. Teresa Torres (2021), *Continuous Discovery Habits: Discover Products that Create Customer Value and Business Value*, Product Talk LLC.
2. Rob Fitzpatrick (2013), *The Mom Test: How to talk to customers & learn if your business is a good idea when everyone is lying to you*, Founder Centric.
3. Jeff Gothelf & Josh Seiden (2021), *Lean UX: Designing Great Products with Agile Teams* (3rd ed.), O'Reilly Media.
4. Ajay Agrawal, Joshua Gans, Avi Goldfarb (2018), *Prediction Machines: The Simple Economics of Artificial Intelligence*, Harvard Business Review Press.
5. Google PAIR (People + AI Research) (2023), *People + AI Guidebook: Designing human-centered AI products*, https://pair.withgoogle.com/guidebook/.
6. Marty Cagan (2017), *Inspired: How to Create Tech Products Customers Love* (2nd ed.), Silicon Valley Product Group (SVPG), Wiley.
7. Anthropic (2024), *Building Effective Agents*, https://www.anthropic.com/research/building-effective-agents.
8. Docker Documentation (2026), *Overview of Docker Compose and Containerized Development Environments*, https://docs.docker.com/compose/.
9. Visual Studio Code Documentation (2026), *Developing inside a Container using Visual Studio Code Remote Development*, https://code.visualstudio.com/docs/devcontainers/containers.
