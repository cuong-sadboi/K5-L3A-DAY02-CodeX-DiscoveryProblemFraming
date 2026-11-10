1. Tổng quan đề tài

Đề tài đề xuất xây dựng một trợ lý AI hỗ trợ người dùng kiểm tra tình trạng máy tính, nhận diện các dấu hiệu bất thường và hiểu nguyên nhân có thể khiến thiết bị hoạt động chậm hoặc không ổn định. Hệ thống cung cấp giải thích và khuyến nghị bảo trì an toàn, giúp người dùng không am hiểu kỹ thuật có cơ sở xử lý hoặc biết khi nào cần hỗ trợ chuyên môn.

2. Problem Statement

Thành phần | Mô tả
Actor | Người dùng máy tính cá nhân/nhân viên văn phòng không có nhiều kiến thức kỹ thuật.

Context |Thiết bị chạy chậm, bộ nhớ gần đầy, CPU/RAM tăng bất thường, xuất hiện lỗi hoặc hoạt động không ổn định.

Current workflow | Người dùng tự tìm kiếm trên Internet, mở Task Manager/Settings, thử nhiều cách hoặc nhờ người có chuyên môn.

Bottleneck | Người dùng khó kết nối nhiều dấu hiệu để xác định nguyên nhân; hướng dẫn trực tuyến thường chung chung và không dựa trên tình trạng cụ thể của thiết bị.

Impact | Mất thời gian tự kiểm tra, xử lý sai cách, phụ thuộc hỗ trợ IT và có nguy cơ ảnh hưởng dữ liệu/cấu hình.

Desired outcome | Nhanh chóng hiểu tình trạng thiết bị, biết nguyên nhân có khả năng và nhận hướng xử lý rõ ràng, an toàn.

3. Người dùng mục tiêu

Người dùng máy tính cá nhân không am hiểu sâu về phần cứng và hệ điều hành.
Nhân viên văn phòng thường xuyên sử dụng máy tính cho công việc.
Nhân sự IT/helpdesk cần công cụ hỗ trợ kiểm tra ban đầu và chuẩn hóa thông tin sự cố.

4. Giải pháp đề xuất

Trợ lý thu thập các chỉ số hệ thống trong phạm vi được cấp quyền, chạy các phép kiểm tra theo quy tắc và sử dụng AI để tổng hợp dấu hiệu, giải thích nguyên nhân có thể, xếp mức độ ưu tiên và đề xuất bước xử lý. Người dùng có thể xem lý do của từng khuyến nghị và tự quyết định có thực hiện hay không.

5. Chức năng chính của MVP

Chức năng | Mô tả | Mức ưu tiên
Kiểm tra tình trạng | Hiển thị CPU, RAM, dung lượng lưu trữ và một số thông tin hệ thống được phép truy cập. | Cao

Phát hiện dấu hiệu bất thườn | Dùng ngưỡng/quy tắc để nhận diện tình trạng tài nguyên cao kéo dài hoặc dung lượng thấp. | Cao

Phân tích và giải thích | AI tổng hợp các dấu hiệu liên quan, đưa ra nguyên nhân có khả năng và giải thích dễ hiểu. | Cao

Đề xuất bảo trì | Đưa ra hướng dẫn từng bước, phân loại theo mức độ rủi ro. | Cao

Theo dõi lịch sử | Lưu lịch sử kiểm tra để người dùng so sánh tình trạng theo thời gian. | Trung bình

Mở rộng đa nền tảng | Hỗ trợ macOS, Android và iOS sau khi đánh giá quyền truy cập và nhu cầu. | Ngoài MVP

6. Vai trò của AI và phần xử lý theo quy tắc

Thành phần | Nhiệm vụ phù hợp 

Rule-based | Kiểm tra các điều kiện rõ ràng như CPU vượt ngưỡng trong một khoảng thời gian, ổ đĩa gần đầy hoặc RAM sử dụng cao.

AI | Kết hợp nhiều dấu hiệu, phân tích ngữ cảnh/lịch sử, diễn giải nguyên nhân có khả năng và cá nhân hóa hướng dẫn.

Người dùng/kỹ thuật viên | Xác minh tình trạng thực tế và quyết định thực hiện các hành động có ảnh hưởng đến thiết bị.

7. Phạm vi và giới hạn

MVP ưu tiên Windows; chưa cam kết hỗ trợ đầy đủ mọi máy tính và điện thoại.
Không cam kết khắc phục mọi nguyên nhân gây chậm, đặc biệt là lỗi phần cứng.
Không tự nhận diện mọi loại mã độc thay thế phần mềm bảo mật chuyên dụng.
Không tự động xóa tệp, gỡ ứng dụng, tắt tiến trình hoặc thay đổi cấu hình quan trọng.
Kết quả AI là gợi ý dựa trên dữ liệu quan sát được, không phải kết luận kỹ thuật tuyệt đối.

8. An toàn, quyền riêng tư và kiểm soát
Chỉ thu thập dữ liệu cần thiết và thông báo rõ mục đích cho người dùng.
Ưu tiên xử lý cục bộ đối với dữ liệu hệ thống nhạy cảm nếu kiến trúc cho phép.
Ẩn hoặc loại bỏ thông tin cá nhân trước khi gửi dữ liệu đến dịch vụ AI bên ngoài.
Yêu cầu xác nhận trước mọi thao tác có khả năng ảnh hưởng đến dữ liệu hoặc cấu hình.
Ghi nhận khuyến nghị và hành động đã được người dùng chấp thuận để hỗ trợ truy vết.

9. Chỉ số đánh giá thành công

KPI | Ý nghĩa / cách đo

Độ chính xác chẩn đoán | Tỷ lệ nguyên nhân gợi ý phù hợp với kết quả được xác minh.

Tỷ lệ cảnh báo sai | Tỷ lệ cảnh báo bất thường trong các trường hợp thiết bị không có vấn đề tương ứng.

Thời gian kiểm tra ban đầu | Thời gian từ lúc bắt đầu quét đến khi có báo cáo tình trạng.

Tỷ lệ khuyến nghị hữu ích | Tỷ lệ khuyến nghị được người dùng hoặc kỹ thuật viên đánh giá là phù hợp.

Tỷ lệ xử lý thành công | Tỷ lệ tình huống được giải quyết sau khi làm theo hướng dẫn.

Mức độ an toàn | Số hành động rủi ro được thực hiện khi chưa có xác nhận; mục tiêu là 0.

Các ngưỡng KPI cụ thể cần được xác định sau khi có dữ liệu thử nghiệm ban đầu; không nên đặt mục tiêu phần trăm khi chưa có bộ kiểm thử đại diện.

10. Kế hoạch triển khai sơ bộ

Giai đoạn 1 – Xác thực vấn đề: phỏng vấn/khảo sát người dùng, thu thập các tình huống máy chậm và lỗi thường gặp.
Giai đoạn 2 – Xây dựng MVP: phát triển module thu thập chỉ số, kiểm tra Rule-based và giao diện báo cáo.
Giai đoạn 3 – Tích hợp AI: xây dựng phần tổng hợp dấu hiệu, giải thích nguyên nhân và sinh hướng dẫn có kiểm soát.
Giai đoạn 4 – Kiểm thử: chạy trên nhiều cấu hình Windows, đo KPI, đánh giá cảnh báo sai và kiểm tra an toàn.
Giai đoạn 5 – Hoàn thiện: điều chỉnh mô hình, quy tắc, trải nghiệm người dùng và xem xét mở rộng nền tảng.

11. Kết luận

Đề tài có tiềm năng nếu tập trung vào khoảng trống giữa dữ liệu kỹ thuật khó hiểu và khả năng tự xử lý hạn chế của người dùng phổ thông. Giá trị cốt lõi không nằm ở việc dọn dẹp hay tăng tốc máy một cách chung chung, mà ở khả năng hỗ trợ chẩn đoán, giải thích và đưa ra khuyến nghị phù hợp, có kiểm soát. Tính khả thi và nhu cầu thị trường vẫn cần được xác thực qua khảo sát và thử nghiệm MVP.