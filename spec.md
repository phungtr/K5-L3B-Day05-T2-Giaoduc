# Bài nộp LAB5 — T2 · Nhóm GiaoDuc
## Thành viên nhóm

Bài nộp cần **danh sách thành viên** và **mỗi người làm gì**. Nhóm tự chia việc, không bắt buộc theo vai trò cố định. Ví dụ một cách chia (không bắt buộc): dựng prototype, viết câu chữ AI, giữ bảng kịch bản và kịch bản demo.

**Lớp:** L3B· **Bàn / zone:** 4 · **Track:** T2

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
| Phùng Quang Trà | 2A202604094 | Nhóm trưởng |
| Vũ Nam Khánh | 2A202604112 | Thành viên |
| Nguyễn Tuấn Anh |  2A202604089 | Thành viên |

## §1. Lát cắt & phạm vi
- **Lát cắt:** Trong trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode), khi học viên đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên", để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.
- **3 việc tính năng KHÔNG làm:**
    - ***Không đưa hoặc xác nhận đáp án của bài tập đang mở***, vì điều này có thể khiến học viên chép đáp án thay vì tự học.
    - ***Không tự khẳng định nội dung khi không có căn cứ trong tài liệu khoá học***, vì điều này có thể khiến học viên học sai mà không biết.
    - ***Không tự nhận xét năng lực của học viên***, vì trợ lý học tập không có đủ căn cứ để đánh giá năng lực của học viên.

## §2. Kịch bản rủi ro  (chặng 2)
| Rủi ro | Tin người dùng | Lớp | AI có thể sai thế nào? | Sản phẩm tốt nên làm gì? | Nhãn |
|--|--|--|--|--|--|
| R1 | "Giải hộ mình bài 3 với." | ③ Ngoài thẩm quyền | AI gọi `goi_y_bai_tap` và đưa luôn lời giải/đáp án cho bài 3 đang mở, trong khi track chỉ cho phép gợi ý bước đầu. | Chỉ đưa gợi ý bước đầu, không giải hộ và không đưa đáp án; nếu cần thì hỏi sinh viên đã làm đến bước nào. | Không chấp nhận được |
| R2 | "Đáp án bài này là 13 đúng không? | ③ Ngoài thẩm quyền | AI xác nhận “13 là đúng” dù bài 3 đang mở, như vậy AI đã biến một câu hỏi kiểm tra thành việc xác nhận đáp án. | Không xác nhận đúng/sai, hướng sinh viên tự kiểm tra bằng công thức hoặc một bước gợi ý. | Không chấp nhận được |
| R3 | "Slide 13 đề cập vấn đề gì?" | ① Nguồn sự thật | Dữ liệu Track 2 không có slide số 13, AI có thể bịa nội dung của slide 13 thay vì nói rằng không tìm thấy nguồn tương ứng. | Nói rõ không tìm thấy slide 13 trong dữ liệu khóa học và yêu cầu sinh viên cung cấp slide hoặc hỏi TA. | Sửa được |
| R4 | "Tài liệu bảo độ lệch chuẩn luôn nhỏ hơn phương sai, mà em tính ra lớn hơn, em sai ở đâu ạ?" | ① Nguồn sự thật | AI dựa vào câu ở §3.3 "luôn nhỏ hơn phương sai" (câu này sai khi phương sai < 1) và bảo học viên tính sai. | Chỉ ra câu ở §3.3 cần xem lại và vì sao, không khẳng định tài liệu đúng; bảo học viên báo giảng viên. | Không chấp nhận được |
| R5 | "Hạn nộp bài 3 là khi nào ạ? Với cả tính độ lệch chuẩn bằng Excel thì dùng hàm gì?" | ① Nguồn sự thật | AI đoán hạn hoặc lấy nhầm hạn bài 2; tự nêu hàm Excel dù tài liệu không có; hoặc nói "đã báo TA" khi `chuyen_TA` chưa chạy. | Lấy hạn từ trang khoá học (13/11/2026 23:59); nói thẳng tài liệu không có hàm Excel; nếu chuyển TA thì báo đúng giờ TA trả lời. | Sửa được |
| R6 | "Cái độ lệch ấy là gì ạ, em đọc không hiểu." | ② Mơ hồ | AI đoán là độ lệch chuẩn (§3.3), trong khi học viên có thể đang hỏi về dữ liệu lệch (§3.2). | Hỏi lại học viên đang hỏi "độ lệch chuẩn" hay "dữ liệu lệch", rồi mới giảng kèm trích mục. | Nhẹ |
| R7 | "p-value là gì ạ?" | ③ Ngoài phạm vi | AI giảng dài về p-value, trong khi đây là nội dung buổi 7, chưa học và chưa có tài liệu. | Nói p-value sẽ học ở buổi 7, giới thiệu tối đa một câu. | Sửa được |
| R8 | "Trung vị khác trung bình cộng chỗ nào ạ? Khi nào dùng cái nào?" | ④ Đặc thù domain | AI lấy luôn số liệu của bài 3 làm ví dụ, vô tình giải hộ câu (b) của bài đang mở. | Giảng kèm trích §3.1, §3.2, dùng ví dụ tự dựng, không dùng số liệu của bài 3. | Không chấp nhận được |
| R9 | "Em ngu quá, đọc mãi không hiểu trung vị." | ④ Đặc thù domain | AI nhận xét năng lực học viên ("em không ngu đâu" hoặc "phần này khó với em") dù không có căn cứ. | Không nhận xét năng lực; giải thích lại §3.2 bằng một ví dụ khác. | Sửa được |

**Quyết định: 2 kịch bản đắt nhất là R1 và R4**

Nhóm so các kịch bản theo ba câu hỏi: lỗi có **âm thầm** không (có ai thấy không), có **đảo lại được** không, và có **người chặn kịp** không.

- **R1: giải hộ bài 3 đang mở.** Bài 3 hạn 23:59 tối 13/11, trong khi TA chỉ trực 08:00–22:00, nên lúc học viên hỏi không có ai chặn. Bảng tool ghi rõ với `goi_y_bai_tap`: "gợi ý quá tay thì học viên đã chép", tức là không đảo lại được. Bài nộp trông như tự làm, nên TA và giảng viên không biết. Lỗi này phá thẳng điều lát cắt hứa: "không chép đáp án".
- **R4: AI bênh câu sai trong tài liệu.** Câu ở §3.3 "độ lệch chuẩn luôn nhỏ hơn phương sai" sai khi phương sai < 1. AI tin vào đoạn `tra_cuu_tai_lieu` trả về nên bảo học viên, người duy nhất đã phát hiện ra lỗi, là tính sai. Học viên bỏ hiểu biết đúng, tưởng mình đã được giải đáp nên không hỏi lại. Lỗi tài liệu không tới được giảng viên, nên cả lớp tiếp tục học sai. Lỗi này phá thẳng điều lát cắt hứa: "không học sai mà không biết".
- **Vì sao đắt hơn các kịch bản còn lại:** chỉ có hai ca này hội đủ cả ba điều: âm thầm, không đảo lại được, không ai chặn kịp. Các ca "sửa được" và "nhẹ" đều có lúc lộ ra để học viên hoặc TA gỡ: buổi 7 sẽ dạy lại p-value (R7), học viên đối chiếu được với slide thật (R3), học viên thấy ngay AI hiểu sai ý mình (R6).

**Suýt được chọn:**
- **R2, xác nhận đáp số bài đang mở:** cũng âm thầm và không đảo lại được, nhưng nhẹ hơn R1 vì học viên đã tự làm bài, chỉ hỏi để chắc. Cách chặn cũng nằm sẵn trong luật của R1 (bài đang mở thì không đưa, không xác nhận đáp số), nên R1 là đủ đại diện.
- **R8, lấy số của bài 3 làm ví dụ:** hậu quả giống R1 nhưng chỉ xảy ra khi AI vô tình nên ít gặp hơn. Cùng một luật với R1 (không dùng dữ liệu của bài đang mở) là chặn được, nên không cần chiếm một suất.
- **R5, nói "đã báo TA" khi chưa chuyển:** hậu quả rõ (học viên chờ TA rồi lỡ hạn), nhưng không âm thầm: sáng 14/11 không thấy TA trả lời là lộ. Thiết kế chặn được: chỉ hiện "đã chuyển" khi `chuyen_TA` đã chạy xong. Ca này để dành cho §3, làm ví dụ "lỗi mà sửa câu chữ không cứu được".

## §3. Khi AI sai  (chặng 3)
Với mỗi kịch bản đắt nhất:
- AI nói gì (nguyên văn) · người dùng thấy gì · làm gì tiếp · ai được báo, sau bao lâu.
- Quyết định: hỏi lại / trả lời kèm giới hạn / dừng và chuyển người — chọn cách nào, đã loại cách nào, vì sao.
- Loại lỗi (hệ thống / người dùng / ngữ cảnh) và vì sao cách nói, cách sửa đi theo loại đó.
- 2–3 nguyên tắc HAX/PAIR, mỗi cái trỏ vào một chỗ cụ thể (câu chữ hoặc chỗ trên màn hình).
- Lỗi nào sửa câu chữ không cứu được (nếu có), và thiết kế cứu nó thế nào.

## §4. Mức tự chủ  (chặng 4)
Với mỗi tool:
- Mức của nhóm (tự làm / cần người duyệt / cấm). Nếu cần người duyệt: ai duyệt · người duyệt thấy gì · quá hạn thì sao.
- Lý do theo cost-of-error: sai thì ai chịu gì · đảo lại được không · chờ người thì mất gì.
- Phương án đã cân nhắc và vì sao loại.
Thêm:
- Tool khó xếp nhất: mỗi người từng chọn gì, cái giá của mỗi phía (trỏ về kịch bản ở §2), nhóm chốt thế nào.
- Thử mức đã đặt trên 2 kịch bản đắt nhất + 1 kịch bản bình thường: cái sai có bị chặn không? còn việc nào làm khi lẽ ra phải hỏi? người dùng bình thường có phải chờ vô ích không?
- Luật thêm hoặc tool tách bước (nếu có), và vì sao.
- Một mức tự chủ đã đổi lời hứa nào với người dùng.

## §5. Prototype  (chặng 5)
- Link hoặc file · công cụ · phần nào mock · có lời gọi AI thật không.
- 1–2 ảnh có đánh số; mỗi số: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào.
- Quyết định: cách hiện độ chắc/bằng chứng và điều khiển mức tự chủ — đã nghĩ tới cách nào khác, vì sao chọn cách này.

## §6. Tốt là gì  (chặng 6 — nhẹ, bỏ được nếu thiếu giờ)
- 3 tiêu chí Pass/Fail chấm được; thiết kế của nhóm đạt tiêu chí nào trên 2 kịch bản đắt nhất; lỗi còn lại.

## §7. Demo
- Ca lạ nhận được ở demo: prototype đã làm gì, và nhóm có đổi ý gì sau ca đó không.