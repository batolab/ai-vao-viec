# Đối chiếu kiểm chứng — Video 07: cùng một bảng số, hai cách hỏi, hai AI

Bài kiểm chứng tại gia: một bảng doanh thu 2 tháng của shop hư cấu, đáp án chuẩn đã tính
tay trước (toàn bộ mức giảm −60 triệu truy về đúng 3 nguyên nhân có số trong bảng — xem
`bang-so-lieu-va-dap-an.md`). Mỗi AI được hỏi bằng 2 prompt: kiểu brainstorm ("càng sáng
tạo, càng bất ngờ càng tốt") và kiểu phân tích (khung phân tích + chỉ dùng số trong bảng
+ tách mục "chưa đủ dữ kiện"). Cách chấm: đếm nguyên nhân truy được /3, số khẳng định
không truy được về dữ kiện, số con số bịa.

## Kết quả đo được

| Lượt | Nguyên nhân đúng /3 | Lớp suy đoán sinh thêm | Số bịa |
|---|---|---|---|
| ChatGPT — brainstorm | 3/3 | 30 giả thuyết, để RIÊNG một mục "kho ý tưởng", tự gắn nhãn "chưa được chứng minh" | 0 |
| ChatGPT — phân tích | 3/3 | 0 — có mục "chưa đủ dữ kiện" liệt kê đúng những thứ bảng không có | 0 |
| Gemini — brainstorm | 3/3 | 12 "giả thuyết táo bạo" lồng trong mạch phân tích, kèm bảng xếp hạng "khả năng xảy ra" và gán mức tiền 5–10 triệu cho một phỏng đoán; cộng 2 con số suy diễn (chia mức giảm của sản phẩm hết hàng thành "~23 triệu vì hết hàng, ~22 triệu bốc hơi" từ giả định bán đều theo ngày) | 2 số suy diễn + 1 khoảng ước lượng |
| Gemini — phân tích | 3/3 | 0 — mục "chưa đủ dữ kiện" đúng phạm vi | 0 (có 1 lỗi gõ trong câu văn: "từ 3 triệu" thay cho 30 — bảng số vẫn đúng) |

## Đọc kết quả này thế nào cho đúng

- Prompt brainstorm KHÔNG làm hai AI mất dấu sự thật: cả hai đều tìm đủ 3 nguyên nhân ở
  mọi cách hỏi. Cái nó sinh ra là một LỚP GIẢI THÍCH không căn cứ bao quanh sự thật.
- Mức độ rủi ro khác nhau theo cách lớp đó được trình bày: để riêng một mục có gắn nhãn
  (ChatGPT) thì người đọc còn phân biệt được; lồng vào mạch phân tích, xếp hạng độ tin
  cậy và gán tiền cho phỏng đoán (Gemini) thì ranh giới thật — đoán biến mất.
- Prompt phân tích cho kết quả sạch ở CẢ HAI AI: đúng 3 nguyên nhân kèm con số, phần
  không biết được khai rõ là không biết.
- Giới hạn của bài test: một bảng số, một lần chạy cho mỗi tổ hợp. Kết quả cho thấy xu
  hướng của cách hỏi, không phải bảng xếp hạng hai AI — đổi bảng số hoặc chạy lại,
  con số giả thuyết cụ thể (30, 12) sẽ khác; điều ổn định là prompt phân tích luôn cho
  ra bản trả lời truy ngược được về dữ kiện.
