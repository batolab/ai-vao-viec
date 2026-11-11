# Tổng hợp test 11/11-06 — Gemini 3.6 Flash, 11/11/2026

Đáp án chuẩn 6 điểm (2 quyết định đủ số · 3 việc có người + hạn · không nâng ý chưa quyết,
không bịa). Bản nháp yếu cài sẵn 5 lỗi (mất số 15 triệu/mốc tháng 12 · hạ "ngừng bán"
thành "xem xét" · mất người phụ trách + hạn · nâng Hải Phòng thành quyết định · câu bịa
"mọi người đều đồng ý").

## Cách A — sửa OUTPUT trong 1 chat bằng phản hồi mơ hồ ("hay hơn đi" ×3)
- Lượt 1: 6/6. Gemini sửa sạch cả 5 lỗi của bản nháp ngay từ đầu (tự tuyên bố "đã chỉnh
  sửa triệt để các điểm thiếu chính xác ở bản nháp cũ").
- Lượt 2: nội dung vẫn 6/6 NHƯNG sinh lỗi mới — ngày họp bị lật thành "11/10/2026"
  (biên bản: sáng 10/11/2026). Thêm lời kêu gọi cuối bản không có trong biên bản.
- Lượt 3: 6/6 cả hai phương án nó tự đề xuất; phình định dạng (emoji, phong cách chat),
  dài gần gấp đôi.
- Lượt 4: 6/6 nội dung gốc, NHƯNG tự thêm cột "Trạng thái: ⏳ Đang triển khai" cho cả 3
  việc — trạng thái tiến độ không hề có trong biên bản. Thêm nhãn lạ "Quảng cáo sàn
  Commerce".
→ Chấm: đạt chuẩn nội dung nhưng TRÔI KHÔNG KIỂM SOÁT: 1 lỗi ngày thật ở vòng 2, chi
  tiết bịa ở vòng 4, không tiêu chí dừng, không để lại tài sản tái sử dụng.

## Cách B — sửa PROMPT bằng phản hồi 4 ý, chạy mới mỗi vòng
- V1 (prompt 1 câu): 6/6. V2 (+ cấu trúc 3 mục, bảng việc): 6/6. V3 (+ vai trò, quy tắc
  chép nguyên văn số, cấm thêm thông tin, tự rà soát): 6/6 — trạng thái "chưa quyết"
  được ghi rõ nhất; mục tự rà soát không hiện trong đầu ra (nội dung vẫn đúng).
→ Cùng đích, nhưng mỗi vòng thay đổi có lý do ghi lại được; prompt V3 là tài sản dùng
  lại cho mọi cuộc họp sau.

## Kết luận trung thực
Với biên bản ngắn, rõ, Gemini hiện đã chính xác ngay từ prompt đơn giản nhất — vòng lặp
KHÔNG "cứu" được nội dung sai trong test này vì không có nội dung sai để cứu. Khác biệt
đo được nằm ở: (1) cách mơ hồ tự sinh lỗi mới khi bị giục "hay hơn" vô định (lật ngày,
thêm cột trạng thái bịa) — rủi ro tăng theo số vòng; (2) cách sửa prompt để lại prompt
thắng + nhật ký lý do, dùng lại được; cách sửa output để lại một bản văn dùng một lần.
Giới hạn: 1 biên bản, 1 AI; biên bản dài/mâu thuẫn có thể cho chênh lệch lớn hơn — chưa test.
