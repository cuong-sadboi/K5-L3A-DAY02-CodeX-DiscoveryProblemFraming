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
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | |
| Nhận phản biện | Câu hỏi tôi nhận được: | Tôi đã sửa gì: |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Gợi ý thêm các góc nhìn vấn đề quanh quy trình phát triển phần mềm | Mở rộng thêm các khía cạnh tốn thời gian như release notes, standup log, phân tích log lỗi 500 | Gợi ý các giải pháp viển vông ("AI tự fix bug", "chatbot nói chuyện với khách") và không có số liệu đo lường thật | Loại bỏ các ý không khả thi, tự viết lại Job Story và gắn số liệu thời gian/tần suất thật từ các dự án đã làm |
| CP2 Problem Card | Đóng vai PM hoài nghi để phản biện và chỉ ra lỗ hổng trong Problem Card | Chỉ ra điểm yếu về việc metric thời gian quá lạc quan và rủi ro bảo mật nếu để AI tự chạy lệnh shell | Gợi ý giải pháp AI Agent phức tạp tự sửa code, xem nhẹ vai trò của Docker/Rule | Giữ vững quan điểm No AI (Docker) là nền tảng, AI chỉ hỗ trợ phân tích log lỗi xung đột; bổ sung boundary con người duyệt lệnh |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
