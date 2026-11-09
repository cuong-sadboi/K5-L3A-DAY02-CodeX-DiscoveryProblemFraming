# Báo cáo cá nhân — 03427_NguyenVuKhanh

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Vũ Khanh
- MSSV: 2A202603427
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm:CodeX
- Link repo nhóm:https://github.com/cuong-sadboi/K5-L3A-DAY02-CodeX-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 |Tốn thời gian|Khi vừa code xong môt bài tập lớn, tôi muốn công cụ tự động đọc thư mục code để tạo sẵn file readme.md và tóm tắt các hàm chính để nộp bài mà không cần phải gõ tài liệu từ đầu|Cá nhân tôi, giảng viên, bạn cùng nhóm|Mất 1-2 tiếng để gõ cấu trúc code, file hướng dẫn mỗi khi hoàn thành|
| 2 |Lặp lại|Khi tải code về máy hoặc chuyển sang làm bài tập môn khác, tôi muốn một công cụ tự động kiểm tra thiếu thư viện nào và cài sẵn và tạo file cấu hình mẫu .env để bấm chạy được ngay|Cá nhân tôi và các bạn trong nhóm|Mất 15-20 phút mỗi lần pull code mới về dò lỗi|
| 3 |Pain từ người khác|Khi bạn trong nhóm đẩy code lên Git, tôi muốn nhận được một bản tóm tắt ngắn gọn về những thay đổi mà hành viên trong nhóm đã sửa và nó có ảnh hưởng gì đến các feature của tôi không|Cá nhân tôi và thành viên nhóm|Tin nhắn commit trên GitHub chỉ ghi đơn giản (update, fix bug) khiến người khác không biết sửa gì|
| 4 |Tốn thời gian|Khi chọn thử nghiệm code với các tham số khác nhau, tôi muốn tự động gom các kết quả in ra màn hình thành một bảng so sánh gọn gàng để tiện sử dụng để so sánh hoặc được vào slide, báo cáo|Cá nhân tôi|Mất 20-30 phút để lướt lại màn hình console, copy số liệu vào note|
| 5 |Cần đọc, tổng hợp nhiều thông tin|Khi chuẩn bị đi xin intern hoặc tìm việc làm, tôi muốn AI đọc trực tiếp các dự án tôi đã làm trong local và viết thành mục trong cv để cập nhật cv mà tôi không cần tự mình tổng hợp|Cá nhân tôi|Các dự án làm rất kỹ nhưng đã lâu rồi không xem lại nên việc viết vào cv khá khăn, có thể thiếu sót các thông tin|
| 6 | | | | |
| 7 | | | | |
| 8 | | | | |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 |Tự động tạo file README.md và tóm tắt báo cáo từ thư mục code|Dễ đưa vào thực thi, đầu vào là các repo bài tập có sẵn|Đối với các project có quá nhiều file hoặc thư mục lồng với nhau phức tạp , nếu đưa vào prompt có thể bị tràn giới hạn từ hoặc tốn nhiều token|
| 2 |Tóm tắt thay đổi khi người trong nhóm đẩy code mới lên Git|Giải quyết nỗi đau làm đồ án nhóm |AI có thể chỉ nhìn vào mỗi đoạn code thay đổi nên có khả năng cảnh bào nhầm nếu không năm được luồng của cả hệ thống|
| 3 |Đọc dự án trong máy để viết mục kinh nghiệm dự án trong cv để khớp jd|Giá trị sử dụng cao cho những người tìm việc làm|Khó đánh giá tự động câu chữ viết ra đã tốt và thuyết phục được nhà tuyển dụng không|

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi vừa code xong môt bài tập lớn, tôi muốn công cụ tự động đọc thư mục code để tạo sẵn file readme.md và tóm tắt các hàm chính để nộp bài mà không cần phải gõ tài liệu từ đầu |
| Actor | Sinh viên, coder |
| Thời điểm / bối cảnh | Khi code chạy được nhưng kho lưu trữ vẫn trống, chưa có hướng dẫn cài đặt hay mô tả cấu trúc |
| Quy trình hiện tại (3–7 bước) | Bước 1: Mở lại từng thư mục để xem cấu trúc dự án.<br>Bước 2: Kiểm tra các thư viện đã dùng để ghi lại requirements.txt<br>Bước 3: Mở các file code chính để nhớ lại luồng chạy, tham số đầu vào và tên các hàm quan trọng.<br>Bước 4: Chạy thử lại các lệnh trên Terminal để copy câu lệnh mẫu và kết quả in ra màn hình.<br>Bước 5: Mở file README.md, tự gõ mô tả dự án, kẻ khung cây thư mục và định dạng cú pháp Markdown thủ công.<br>Bước 6: Đọc soát lại, lưu file và git push|
| Bottleneck (bước nào, mất bao nhiêu phút) |Bước 3 và 5 mất 45-60 phút|
| Impact (nếu không giải thì sao) | Gây ra bất đồng bộ trong nhóm các bạn cùng nhóm kéo code về nhưng không hiểu cấu trúc thư mục và cách dùng hàm |
| Success metric (baseline → target) | Thời gian viết tài liệu cho 1 repo giảm từ 60-70 phút xuống còn 5-10 phút, Người khác làm theo REAMDE.md chạy được code ngay lần đầu|
| Phương án không dùng AI | Tạo sẵn template cố định cho README.md, dùng lệnh có sẵn trên máy để xuất nhanh cấu trúc thư mục và danh sách thư viện|
| Giả thuyết về AI (nếu có) | |
| Cảm nhận nhanh | Workflow / Agent |

Quy trình nháp hiện tại:

```text
[1. Code xong dự án] 
       │
       ▼
[2. Mở Code rà soát thủ công từng thư mục & danh sách thư viện] (10-15 phút)
       │
       ▼
[3. Đọc lại các file code chính để nhớ luồng chạy & chức năng từng hàm] (20-25 phút) 
       │
       ▼
[4. Chạy lại lệnh trên Terminal để copy câu lệnh mẫu & kết quả đầu ra] (10 phút)
       │
       ▼
[5. Tự gõ nội dung, vẽ cây thư mục & căn chỉnh Markdown trong README.md] (25-35 phút) 
       │
       ▼
[6. Kiểm tra lại, lưu file và git push lên GitHub] (5 phút)

```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi bạn trong nhóm đẩy code lên Git, tôi muốn nhận được một bản tóm tắt ngắn gọn về những thay đổi mà hành viên trong nhóm đã sửa và nó có ảnh hưởng gì đến các feature của tôi không |
| Actor | Thành viên trong nhóm làm dự án |
| Thời điểm / bối cảnh | Trong giai đoạn chạy nước rút làm đồ án môn học, khi các thành viên liên tục git push code lên nhánh chung vào buổi tối trước ngày báo cáo tiến độ nhưng chỉ ghi lời nhắn commit ngắn như "update", "fix bug". |
| Quy trình hiện tại (3–7 bước) | Bước 1: Kéo (git pull) code mới của bạn cùng nhóm về máy cục bộ.<br>Bước 2: Chạy thử chương trình và phát hiện lỗi đỏ màn hình .<br>Bước 3: Mở lịch sử GitHub hoặc VS Code Git Graph để dò xem ai vừa sửa những file nào.<br>Bước 4: Mở từng file có dấu cộng/trừ để đọc bằng mắt thường xem bạn đã đổi logic gì.<br>Bước 5: Nhắn tin vào nhóm  hỏi lại bạn cho chắc chắn và chờ phản hồi.<br>Bước 6: Tự sửa lại các file code của mình cho khớp với thay đổi của bạn.|
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4,5 mất 30-60 phút |
| Impact (nếu không giải thì sao) | Chậm tiến độ cả nhóm: Mất cả buổi tối chỉ để sửa lỗi ghép nối thay vì code tính năng mới |
| Success metric (baseline → target) |  Thời gian hiểu thay đổi & xử lý lỗi ghép code: Giảm từ 30–60 phút/lần pull → xuống còn dưới 5 phút |
| Phương án không dùng AI | Đặt quy tắc bắt buộc trong nhóm: Ai sửa API/Database phải viết tin nhắn báo vào nhóm chat và ghi commit theo mẫu cố định,dùng tính năng GitHub Branch Protection bắt buộc phải có 1 người đọc duyệt (Review) trước khi gộp code |
| Giả thuyết về AI (nếu có) | |
| Cảm nhận nhanh | Workflow / Agent |

Quy trình nháp hiện tại:

```text
[1. Kéo code mới của bạn về máy (git pull)] 
       │
       ▼
[2. Chạy thử project -> Phát sinh lỗi bất ngờ do lệch biến/API] (5 phút)
       │
       ▼
[3. Mở lịch sử Git tìm xem ai vừa sửa những file nào] (5-10 phút)
       │
       ▼
[4. Đọc dò từng dòng xanh/đỏ trong git diff để tìm nguyên nhân] (15-25 phút) 
       │
       ▼
[5. Nhắn tin hỏi bạn cùng nhóm và chờ trả lời] (15-30 phút)
       ▼
[6. Sửa lại code của mình cho khớp và chạy thử lại] (10-15 phút)

```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi chuẩn bị đi xin intern hoặc tìm việc làm, tôi muốn AI đọc trực tiếp các dự án tôi đã làm trong local và viết thành mục trong cv để cập nhật cv mà tôi không cần tự mình tổng hợp |
| Actor | Người cần chuẩn bị cv để xin việc |
| Thời điểm / bối cảnh | Mùa tuyển dụng; khi tìm thấy một tin tuyển dụng (JD) ưng ý nhưng nhận ra CV hiện tại đang viết quá sơ sài, hoặc phải sửa lại cách mô tả các đồ án ở trường sao cho trúng các từ khóa kỹ thuật mà công ty đó yêu cầu |
| Quy trình hiện tại (3–7 bước) | Bước 1: Đọc bản Mô tả công việc (JD) để gạch chân các kỹ năng và công nghệ công ty yêu cầu.<br>Bước 2: Lục lại các thư mục code bài tập lớn/đồ án cũ trong máy tính hoặc trên GitHub.<br>Bước 3: Mở lại code, file requirements.txt và báo cáo cũ để nhớ xem hồi đó mình dùng thư viện gì, giải quyết bài toán gì và kết quả (độ chính xác, tốc độ) ra sao.<br>Bước 4: Mở file CV , tự viết thành 3–4 câu mô tả theo văn phong chuyên nghiệp.<br>Bước 5: So sánh lại với JD xem đã đủ từ khóa chưa, chỉnh sửa độ dài câu cho vừa trang giấy rồi xuất file PDF.|
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3,4 mất 30-45 phút |
| Impact (nếu không giải thì sao) | Ngại cá nhân hóa CV: Vì sửa mỗi bản CV mất gần cả tiếng đồng hồ nên sinh viên thường dùng 1 bản CV duy nhất rải cho mọi công ty |
| Success metric (baseline → target) | Thời gian điều chỉnh mục Dự án trong CV theo 1 JD mới: Giảm từ 45–60 phút → xuống còn 5–10 phút, độ khớp từ khóa với JD: Đạt trên 80% các kỹ năng thực tế có trong code. |
| Phương án không dùng AI | Tự lập một bảng Excel lưu trữ sẵn thông tin mọi đồ án đã làm (tên môn, thư viện đã dùng, số liệu kết quả, câu mô tả mẫu) ngay sau khi kết thúc mỗi học kỳ để lúc làm CV chỉ việc copy ra. |
| Giả thuyết về AI (nếu có) | Nếu dùng một AI Agent tự động quét repo dự án để lấy đúng danh sách thư viện + số liệu thực nghiệm, sau đó đối chiếu với văn bản JD để gợi ý 3 phương án viết gạch đầu dòng (có bước Human-in-the-Loop để tôi kiểm tra số liệu và chọn câu ưng ý nhất), thì sẽ tạo ra bản CV vừa trúng từ khóa tuyển dụng vừa bám sát 100% những gì tôi đã code. |
| Cảm nhận nhanh | Agent |

Quy trình nháp hiện tại:

```text
[1. Đọc tin tuyển dụng (JD) và lọc ra các từ khóa kỹ năng] (5-10 phút)
       │
       ▼
[2. Lục tìm lại các thư mục đồ án / bài tập lớn phù hợp trong máy] (5 phút)
       │
       ▼
[3. Mở đọc lại code & báo cáo cũ để tìm tên thư viện và số liệu kết quả] (15-20 phút) 
       │
       ▼
[4. Tự nghĩ câu chữ viết thành 3-4 gạch đầu dòng khớp với từ khóa JD] (20-25 phút) 
       │
       ▼
[5. Căn chỉnh lại độ dài trong CV, kiểm tra lỗi và xuất file PDF] (5-10 phút)

```

### Card muốn pitch nhất

- Card số: 1
- Vì sao: Mang tính ứng dụng cao
- Câu hỏi muốn nhóm phản biện: Đã có GitHub Copilot hay ChatGPT hỗ trợ viết tài liệu rồi, vậy công cụ này có điểm gì vượt trội hơn hẳn để sinh viên chịu dùng thay vì copy-paste code lên web hỏi?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|Nguy cơ tràn bộ nhớ (Context Limit) và tốn token: Nếu thiết kế ngây thơ cho AI đọc toàn bộ mọi file trong thư mục dự án, khi gặp các thư mục như node_modules, .venv, .git hoặc file dữ liệu .csv nặng hàng chục MB thì hệ thống sẽ bị treo hoặc hết sạch quota API ngay lập tức|Đồng ý|Thiết kế lại luồng xử lý tách làm 2 bước (Workflow + Agent):
Bước 1 (Rule-based, không dùng AI): Dùng script Python quét cây thư mục và tự động loại bỏ các thư mục rác/môi trường ảo (.venv, __pycache__, .git, file dữ liệu lớn).<br>Bước 2 (Agent): Chỉ gửi cây thư mục gọn nhẹ cho AI xem trước để AI tự chọn đúng 3–5 file cốt lõi (requirements.txt, main.py, config.py) cần đọc nội dung chi tiết.|
| | | |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card |Tôi đem Card #1 của mình (Tự động đọc thư mục code tạo `README.md`) ra pitch trước nhóm | Card của tôi chỉ dừng ở vòng pitch, **không được chọn** làm bài toán chung vì nhóm đánh giá việc viết `README.md` chỉ giải quyết phần ngọn cho sinh viên nộp bài, chưa giải quyết được nỗi đau lớn hơn ở môi trường doanh nghiệp |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | Câu hỏi tôi đã đặt cho Card #1 của bạn Nguyễn Tiến Cường (Setup môi trường dự án cũ / Onboard): "Tại sao các dự án cũ không dùng luôn Docker Compose hoặc VS Code Dev Containers để đóng gói từ đầu, hoặc cài GitHub Copilot CLI để hỏi lỗi cho nhanh?" | Câu hỏi này trở thành tiền đề trực tiếp để nhóm phân công tôi phụ trách Mục 3.3 (Research 3 giải pháp có sẵn) nhằm chứng minh khoảng trống thực tế của các công cụ này trên dự án legacy |
| Nhận phản biện | Câu hỏi tôi nhận được từ bạn Cường và nhóm cho Card tạo `README.md` của tôi: "Có tạo sẵn README đẹp mấy mà thư viện trong project bị xung đột version với máy người cài thì pull về build vẫn crash. Sao không giải quyết thẳng khâu dò lỗi dependency lúc setup?" | Tôi đã sửa góc nhìn: Đồng ý gác lại Card tạo `README.md` của mình và kết hợp ý tưởng số #2 ở CP1 của tôi (kiểm tra thư viện & tạo `.env`) vào bài toán Setup môi trường dự án cũ của bạn Cường |
| Gom cluster / cây OST | Cùng nhóm gom 12 candidate về các cụm và xây dựng nhánh Opportunity xoay quanh nỗi đau: *"Tài liệu lỗi thời khiến cài đặt liên tục bị crash do xung đột thư viện/version, phải chờ Senior pair-debug"* | Giúp nhóm loại bỏ các giải pháp đội lốt opportunity (như "Làm chatbot hỏi đáp onboard") ra khỏi cây OST |
| Chọn candidate problem | Chấm điểm shortlist và bỏ phiếu chọn Card #1 của bạn Nguyễn Tiến Cường: Setup môi trường dự án cũ / Onboard (Actor: Dev mới, Techlead/Senior; Bottleneck: Dò lỗi dependency và nhờ Senior pair-debug mất 270'/360') | Nhóm thống nhất 100% chọn bài của Cường vì có baseline thời gian rõ ràng (360 phút), nỗi đau thực tế cao (lãng phí 4–8 tiếng của Dev mới, gián đoạn 1–2 tiếng của Senior, chậm sprint 1–2 ngày với tần suất 5–6 lần/quý) |
| Kiểm chứng / research | Trực tiếp đảm nhận và viết Mục 3.3 (Research giải pháp có sẵn) trong báo cáo nhóm: Phân tích chuyên sâu 3 công cụ VS Code Dev Containers, Docker Compose + `.env` (No-AI) và GitHub Copilot CLI | Chỉ ra bài học cốt lõi cho nhóm: Container hóa quá nặng để áp vào repo cũ ngay lập tức, còn Copilot CLI thiếu ngữ cảnh file cấu hình dự án và dễ gợi ý lệnh nguy hiểm |
| Quy trình nhóm | Phụ trách thiết lập Mục 4.3 (Bảng Before / After) đối chiếu định lượng trước và sau khi áp dụng Workflow AI vào bài toán của Cường | Chốt bảng chỉ số chuẩn cho cả nhóm: Tổng thời gian giảm từ 360' → 40', thời gian gỡ lỗi dependency giảm từ 270' → 15', số lần làm phiền Senior giảm từ 3 lần → 0 lần, số bước từ 5 → 4 bước |
| Problem Statement | Phụ trách viết Mục 7 (Problem Statement v1 + Tiêu chí đánh giá AI - Eval) dựa trên bài toán của Cường | Chốt Problem Statement v1 và thiết lập 3 tiêu chí Đạt / Không đạt của AI: (1) Chỉ đúng tên thư viện & version xung đột; (2) Không gợi ý lệnh can thiệp file hệ thống; (3) Lệnh phải chạy được và khắc phục dứt điểm lỗi build |
| Mức can thiệp AI | Đề xuất chọn mức Workflow (Rule script kiểm tra `.env` và gom `[Log lỗi + package.json/requirements.txt + OS]` → AI chẩn đoán và đề xuất lệnh sửa → Dev mới kiểm tra và chạy) | Giúp nhóm giải thích rõ vì sao không chọn No-AI/Rule đơn thuần (không tự chẩn đoán được lỗi xung đột thư viện) và không chọn Agent (rủi ro tự chạy lệnh phá hỏng hệ thống) |
| Quyết định | Cùng nhóm đánh giá 4 rủi ro (Value, Usability, Feasibility, Viability) và thống nhất quyết định Go với phạm vi pilot nhỏ | Đưa bộ 3 tiêu chí Eval ở Mục 7 vào làm điều kiện kiểm soát chất lượng và ngưỡng dừng cho pilot của nhóm |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Nhờ AI gợi ý thêm các tình huống gây tốn thời gian và lặp đi lặp lại trong quá trình code đồ án nhóm | Gợi ý nhanh các tình huống thực tế giúp tôi nhớ ra ý #2 (kiểm tra thư viện & tạo `.env`) và ý #4 (gom kết quả chạy thử nghiệm) | Gợi ý một số bài toán quá vĩ mô như "AI tự động quản lý toàn bộ tiến độ dự án và tự fix mọi bug" | Loại bỏ các ý tưởng viển vông, chỉ giữ lại những vấn đề sát sườn có thể đo đếm bằng số phút thực tế |
| CP2 Problem Card | Nhờ AI đóng vai người phản biện khó tính để bắt lỗi 3 Problem Cards cá nhân của tôi (đặc biệt là Card #1 tạo `README.md`) | Chỉ ra rất đúng điểm yếu tràn ngữ cảnh (Context Limit) và tốn token nếu cho AI đọc toàn bộ thư mục chứa cả `node_modules`, `.venv` | Khuyên tôi dùng Agent tự động quét và tự động push thẳng file `README.md` lên nhánh chính mà không cần người duyệt | Tôi tách thành 2 bước (Rule lọc bỏ thư mục rác trước + AI chỉ đọc 3–5 file cốt lõi) và giữ bước sinh viên kiểm tra lại trước khi `git push` |
| CP4 Research | Khi làm Mục 3.3 cho bài toán Setup môi trường dự án cũ của bạn Cường, tôi dùng AI để tổng hợp điểm mạnh/yếu của VS Code Dev Containers, Docker Compose + `.env`** và GitHub Copilot CLI | Liệt kê nhanh tính năng kỹ thuật và đường link tài liệu chính thức của 3 công cụ | Phân tích rất chung chung, không gắn với quy trình 5 bước của nhóm và tưởng rằng Copilot CLI có thể tự đọc toàn bộ repo để bắt lỗi xung đột version | Tôi tự đối chiếu vào đúng từng bước trong Card của Cường (Bước 2–3 mất 75', Bước 4–5 mất 270'), chỉ rõ Copilot CLI thiếu ngữ cảnh đối chiếu `package.json`/`requirements.txt` với OS và dễ xúi chạy lệnh `--force`, `sudo` |
| CP5 Quy trình | Dùng AI hỗ trợ kẻ bảng Mục 4.3 (Before / After) đối chiếu các chỉ số trước và sau khi áp dụng giải pháp | Tạo khung bảng Markdown nhanh và gợi ý thêm chỉ số về số bước thủ công, rủi ro mới phát sinh | Ở bản nháp đầu, AI tự bịa quy trình Trước có 6–7 bước và quên mất chi tiết script kiểm tra biến môi trường `.env` | Tôi đối chiếu lại với sơ đồ quy trình của Cường, sửa chính xác về 5 bước → 4 bước, điền đúng các con số định lượng: Tổng thời gian 360' → 40', gỡ lỗi 270' → 15', làm phiền Senior 3 lần → 0 lần |
| CP5–6 Problem Statement | Nhờ AI nháp khung Mục 7 (Problem Statement v1 và bảng so sánh v0 → v1) cho bài toán Setup môi trường dự án cũ | Gợi ý cách diễn đạt mạch lạc cho các trường Boundary và AI intervention point | Viết thiếu vai trò Tester/Techlead trong bối cảnh dự án outsource/maintain cũ và đưa ra các tiêu chí Eval khá mơ hồ ("AI trả lời hay, chính xác") | Tôi bổ sung đầy đủ Actor (Dev mới, Tester, Techlead), bối cảnh dự án cũ, và viết lại 3 tiêu chí Eval thật cụ thể: chỉ đúng tên thư viện/version lỗi, cấm gợi ý lệnh can thiệp file hệ thống (`sudo`, `rm -rf`), và lệnh phải chạy được ngay |
| CP6 Mức can thiệp / quyết định | Hỏi AI so sánh giữa việc dùng Rule, Workflow và Agent tự động chạy lệnh sửa lỗi trên terminal | Giúp hệ thống hóa lý lẽ vì sao No-AI và Rule không giải quyết được 270 phút debug xung đột thư viện ở Bước 4 & 5 | AI có xu hướng khuyên làm Agent tự động thực thi lệnh cài đặt lại thư viện trên máy của Dev mới cho tiện | Tôi bác bỏ hướng Agent, giữ vững mức Workflow kết hợp Boundary (HITL): AI chỉ phân tích và đề xuất lệnh, Dev mới bắt buộc phải đọc duyệt rồi mới chạy để bảo vệ máy cục bộ |
---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
Khi lắng nghe các bạn trong nhóm CodeX trình bày Top 3 Problem Cards của mình, đặc biệt là Card #1 của bạn Nguyễn Tiến Cường về bài toán "Setup môi trường dự án cũ / Onboard", tôi đã nhận ra sự khác biệt rất lớn giữa một "sự bất tiện cá nhân khi đi học" và một "nỗi đau có tính hệ thống trong thực tế làm việc". Ban đầu, các card của tôi (như tự động viết `README.md` sau khi làm xong bài tập lớn hay viết mục dự án trong CV) chỉ xoay quanh việc tiết kiệm 30–60 phút cho bản thân tôi. Ngược lại, bài toán của Cường chỉ ra một điểm nghẽn dây chuyền: khi tài liệu dự án cũ bị lỗi thời, người mới (Dev mới, Tester) cài đặt liên tục bị crash do xung đột thư viện và version, làm mất tới 270 phút trên tổng số 360 phút chỉ để mò mẫm dò lỗi và phải kéo cả Senior/Techlead vào pair-debug. Nó không chỉ làm lãng phí 4–8 tiếng của nhân sự mới mà còn cắt ngang sự tập trung của Senior mất 1–2 tiếng và làm chậm tiến độ sprint của cả team 1–2 ngày (lặp lại 5–6 lần mỗi quý). Tôi học được rằng một candidate problem xuất sắc phải có Actor rõ ràng ở cả hai phía (người trực tiếp gặp lỗi và người bị ảnh hưởng dây chuyền), có quy trình từng bước cụ thể và đo lường được tác động bằng những con số biết nói.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
Có, nhóm tôi đã vướng vào bẫy "solution-first" ngay lúc mới chốt chọn bài toán Setup môi trường dự án cũ của Cường. Lúc đó, một vài thành viên (trong đó có cả tôi) lập tức nghĩ ngay tới việc: *"Hay là mình làm một con AI Agent tự động đọc repo rồi tự chạy lệnh cài đặt hết từ A đến Z trên terminal cho Dev mới luôn?"* hoặc *"Cứ bắt buộc đóng gói hết vào Docker Dev Containers là xong"*. May mắn là khi bắt tay vào vẽ cây Opportunity Solution Tree (OST) ở CP3 và thực hiện phần Research công cụ ở CP4 (Mục 3.3 do tôi phụ trách), nhóm đã kịp thời nhận ra mình đang đi ngược. Khi phân tích kỹ quy trình 5 bước của Cường, nhóm thấy rằng 90 phút đầu (đọc docs, cài runtime, tạo `.env`) không phải là chỗ gây đau đớn nhất, mà 270 phút chết nằm ở Bước 4 (build bị crash do xung đột thư viện/version giữa code cũ và máy mới) và Bước 5 (phải chờ Senior sang pair-debug). Nếu áp đặt giải pháp Agent tự chạy lệnh trên máy sẽ cực kỳ nguy hiểm vì AI có thể chạy lệnh `sudo` hoặc cài đè làm hỏng hệ điều hành của Dev mới. Nhóm đã gạch bỏ các "solution đội lốt opportunity" khỏi cây OST và quay về bám sát nỗi đau gốc để thiết kế đúng mức can thiệp.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
Tôi đã đổi ý hoàn toàn ở hai thời điểm quan trọng sau khi nhận phản biện. Lần thứ nhất là ở vòng hội tụ nhóm (CP3): ban đầu tôi rất tâm đắc với Card #1 cá nhân của mình là công cụ tự động tạo file `README.md`. Tuy nhiên, khi các bạn trong nhóm phản biện rằng: *"Nếu một dự án cũ mà các gói thư viện trong `package.json` hay `requirements.txt` đã bị deprecated hoặc xung đột với hệ điều hành mới, thì dù AI có viết lại file README.md đẹp đến mấy, người tiếp theo kéo code về chạy lệnh build vẫn bị crash như thường"*, tôi đã hoàn toàn bị thuyết phục. Tôi quyết định rút lại sự ưu tiên cho Card của mình để ủng hộ chọn **Card #1 của bạn Nguyễn Tiến Cường**, đồng thời đem ý tưởng số #2 ở phần Scan của tôi (tự động kiểm tra thư viện và file `.env`) ghép vào làm một bước Rule bổ trợ cho bài toán của Cường. Lần đổi ý thứ hai là khi viết Mục 7: từ chỗ nghĩ chỉ cần đưa đoạn log lỗi cho AI đọc là đủ, sau khi đối chiếu với hạn chế của GitHub Copilot CLI, tôi đã đổi sang thiết kế Workflow bắt buộc phải gom đủ bộ 3 dữ liệu `[Log lỗi khi build fail + file manifest/lockfile + thông tin OS/Runtime]` thì AI mới chẩn đoán chính xác được.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
Khi trực tiếp làm nhiệm vụ Research 3 giải pháp có sẵn ở Mục 3.3 (VS Code Dev Containers, Docker Compose + `.env`, và GitHub Copilot CLI), tôi đã rất bất ngờ trước khoảng trống thực tế của các công cụ nổi tiếng này. Trước khi tìm hiểu sâu, tôi cứ đinh ninh rằng Docker Compose hoặc VS Code Dev Containers là "viên đạn bạc" giải quyết được 100% chuyện lệch môi trường. Nhưng khi đặt vào bối cảnh thực tế của các dự án outsource/maintain cũ mà nhóm đang xét, tôi mới vỡ lẽ: các dự án cũ thường chưa được chuẩn hóa container, hoặc bản thân `Dockerfile` cũ sử dụng các base image và thư viện C/C++ đã ngừng hỗ trợ, thậm chí xung đột với kiến trúc chip mới (như máy Mac M1/M2/M3 của Dev mới). Việc bắt Senior bỏ hàng chục giờ ra viết lại Dev Container cho một dự án cũ là bất khả thi. Bất ngờ thứ hai nằm ở GitHub Copilot CLI: dù rất tiện để giải thích lệnh bash, nhưng vì nó chỉ nhìn thấy câu lệnh đơn lẻ trên terminal mà không tự động đối chiếu với `package.json` hay `requirements.txt` của dự án, nó rất dễ gợi ý các lệnh ép cài đặt (`--force`, `sudo`) làm nát chuỗi dependency. Phát hiện này giúp tôi và nhóm tự tin hẳn vào giá trị của giải pháp Workflow mà nhóm đề xuất.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**
Trải nghiệm trực tiếp viết Mục 7 (Problem Statement v1 và bảng Tiêu chí đánh giá AI) cho tôi thấy điều khó nhất là biến những mong muốn chung chung thành các con số định lượng sắc bén (Success Metric) và ranh giới an toàn không thể xâm phạm (Boundary). Ở bản v0 ban đầu, nhóm chỉ ghi mục tiêu khá rộng là giảm thời gian gỡ lỗi từ 270 phút xuống dưới 30 phút và hạn chế gọi Senior. Nhưng khi nâng cấp lên v1 và khớp với bảng Before/After ở Mục 4.3, tôi phải tính toán thật khớp từng bước trong quy trình để chốt con số khả thi: giảm tổng thời gian từ 360 phút xuống 40 phút (trong đó 25 phút cho các bước cài đặt cơ bản đã có script hỗ trợ và 15 phút cho bước gỡ lỗi cùng AI, giảm từ 270 phút), đồng thời ép số lần làm phiền Senior từ 3 lần về 0 lần. Khó không kém là việc định nghĩa 3 tiêu chí Đạt / Không đạt (Eval) cho đầu ra của AI: viết làm sao để bất kỳ ai trong nhóm nhìn vào câu trả lời của AI cũng chấm điểm giống nhau được—từ việc AI phải chỉ đích danh tên thư viện và version xung đột, tuyệt đối không chứa lệnh can thiệp file hệ thống OS, cho tới việc câu lệnh copy vào terminal phải chạy qua được bước build ngay lần đầu.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Nếu được làm lại quy trình Discovery & Problem Framing này một lần nữa, ngay từ bước CP1 và CP2 cá nhân, tôi sẽ không chỉ bó hẹp góc nhìn ở các bài tập môn học trong trường mà sẽ hỏi chuyện sớm các anh chị đang đi thực tập hoặc đi làm để tìm ra những bài toán có quy mô và tác động lớn như bài toán Onboard dự án cũ của bạn Cường. Thứ hai, trong quá trình làm việc nhóm, tôi sẽ phản biện mạnh mẽ hơn ở hai điểm: (1) Tôi sẽ yêu cầu nhóm kiểm chứng kỹ hơn giả định về việc *"Dev mới có đủ kiến thức nền tảng để hiểu và tự kiểm duyệt (Human-in-the-loop) câu lệnh do AI đề xuất trong vòng 15 phút hay không?"* — vì nếu Dev mới cứ nhắm mắt bấm chạy theo gợi ý của AI thì cơ chế HITL sẽ mất tác dụng; và (2) Tôi sẽ thúc đẩy nhóm làm rõ hơn quy trình cập nhật ngược lại tài liệu `README.md` sau khi Dev mới đã sửa xong lỗi xung đột, để người thứ hai, thứ ba vào dự án sau đó hưởng lợi trực tiếp từ kết quả của người đầu tiên.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.
Bài toán của nhóm CodeX bắt nguồn từ việc các dự án cũ có tài liệu cài đặt lỗi thời khiến Dev mới khi onboard liên tục bị crash lúc build do xung đột thư viện/version, làm lãng phí 4–8 tiếng của Dev mới, gián đoạn 1–2 tiếng của Senior và làm chậm sprint 1–2 ngày (5–6 lần/quý). Trong quy trình hiện tại gồm 5 bước kéo dài 360 phút, điểm nghẽn (bottleneck) lớn nhất nằm ở Bước 4 và Bước 5 khi Dev mới phải tự mò lỗi dependency (180 phút) và gọi Senior sang pair-debug (90 phút), chiếm tới 270 phút. Nhóm đặt ra Success Metric định lượng là giảm tổng thời gian setup từ 360 phút xuống 40 phút, giảm thời gian gỡ lỗi từ 270 phút xuống 15 phút và giảm số lần làm phiền Senior từ 3 lần xuống 0 lần. Để đảm bảo an toàn cho máy cục bộ, nhóm thiết lập Boundary nghiêm ngặt: AI không được tự ý thực thi lệnh trên terminal, không gợi ý lệnh can thiệp file hệ thống (`sudo`, `rm -rf`, `--force`) và mọi lệnh sửa lỗi đều phải do Dev mới kiểm tra trước khi chạy (Human-in-the-loop). Nhóm chọn mức can thiệp là **Workflow** (kết hợp Rule script kiểm tra `.env` và gom log lỗi + file manifest + thông tin OS gửi cho AI phân tích, sau đó gợi ý lệnh sửa đáp ứng 3 tiêu chí Eval) vì No-AI không tự bắt được lỗi xung đột, còn Agent thì quá rủi ro. Từ đó, nhóm đưa ra quyết định **Go** với một pilot nhỏ áp dụng ngay cho đợt onboard tiếp theo và sẵn sàng quay về quy trình cũ nếu tỉ lệ lệnh AI gợi ý chạy thành công không đạt ngưỡng.


---

## 7. Tài liệu tham khảo

-
