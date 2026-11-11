# Đối chiếu kiểm chứng — Video 04 (test thật 11/11/2026)

Người bán online nào cũng ngập tin nhắn khách: hỏi giá, đặt hàng, khiếu nại, góp ý, lẫn cả
spam. Đọc tay từng tin thì hết ngày, mà nhờ AI phân loại thì phải biết nó phân loại có đúng
không. Mình không đoán — mình dựng sẵn một bộ 20 tin nhắn hư cấu với đáp án phân loại chuẩn
chốt trước (xem bo-tin-nhan-va-dap-an.md), trong đó 10 tin là bẫy: mỉa mai, khiếu nại trá
hình, spam dụ AI tự thêm nhóm mới, tin hai ý. Sau đó mình đưa bộ tin nhắn cho Gemini (bản
web) phân loại bằng danh mục 5 nhóm cố định kèm quy tắc (xem mau-danh-muc-5-nhom.md và
prompt-phan-loai.md), rồi chấm từng tin so với đáp án chuẩn.

## Cách chấm

- Đúng nhóm so với đáp án chuẩn = đúng. Sai nhóm = sai, kể cả khi lý do nghe có vẻ hợp lý.
- Đếm riêng hai chỉ số phụ: số tin AI tự thêm nhóm ngoài danh mục, và độ đúng trên 10 tin bẫy.
- Mình chạy hai lượt độc lập (model hiển thị Flash-Lite và 3.6 Flash) — cả hai cho cùng một
  kết quả phân loại, nên bảng dưới đây đại diện cho cả hai lượt.

## Bảng đối chiếu — 20 tin

| STT | Đáp án chuẩn | Gemini xếp | Kết quả |
|---|---|---|---|
| 1 | HOI_GIA | HOI_GIA | Đúng |
| 2 | DAT_HANG | DAT_HANG | Đúng |
| 3 | KHIEU_NAI | KHIEU_NAI | Đúng |
| 4 | GOP_Y | GOP_Y | Đúng |
| 5 | KHAC | KHAC | Đúng |
| 6 | HOI_GIA | HOI_GIA | Đúng |
| 7 | DAT_HANG | DAT_HANG | Đúng |
| 8 | KHIEU_NAI | KHIEU_NAI | Đúng |
| 9 | GOP_Y | GOP_Y | Đúng |
| 10 | KHAC | KHAC | Đúng |
| 11 | KHIEU_NAI | KHIEU_NAI | Đúng |
| 12 | DAT_HANG | DAT_HANG | Đúng |
| 13 | KHIEU_NAI | KHIEU_NAI | Đúng |
| 14 | KHIEU_NAI | GOP_Y | **Sai** |
| 15 | HOI_GIA | HOI_GIA | Đúng |
| 16 | KHAC | KHAC | Đúng |
| 17 | DAT_HANG | DAT_HANG | Đúng |
| 18 | GOP_Y | GOP_Y | Đúng |
| 19 | KHIEU_NAI | KHIEU_NAI | Đúng |
| 20 | KHAC | KHAC | Đúng |

**Tổng kết: đúng 19/20.** Tin rõ ràng 10/10, tin bẫy 9/10. Tự thêm nhóm ngoài danh mục: 0 —
tin spam (tin 16) được xếp vào KHAC đúng quy tắc thay vì bịa ra một nhóm "spam" riêng. Tin
mỉa mai (tin 13) cũng bị bắt đúng là khiếu nại, và tin hai ý (tin 17) được ưu tiên về nhóm
đặt hàng đúng quy tắc xử lý trước.

## Lỗi duy nhất — và vì sao nó quan trọng

Tin 14 viết rất nhẹ nhàng: khách "góp ý" shop kiểm tra khâu đóng gói vì nhận hàng lần nào
cũng móp hộp. Gemini xếp vào GOP_Y — theo đúng giọng bề mặt của câu chữ. Nhưng bản chất của
tin là một khiếu nại về sự cố lặp lại với chính khách đó, đáp án đúng là KHIEU_NAI.

Lỗi này không hề vô hại: một tin khiếu nại bị xếp vào góp ý sẽ được trả lời bằng mẫu cảm ơn
góp ý thay vì được xử lý sự cố — đúng kiểu mất khách thầm lặng. Kết luận rút ra từ test này:
phân loại bằng AI xong, riêng nhóm khiếu nại phải đọc lại bằng mắt trước khi trả lời khách,
và thi thoảng rà cả nhóm góp ý để vớt những tin khiếu nại trá hình bị lọt.

## Giới hạn của test này

- Mới test trên Gemini bản web; chưa đối chiếu với AI khác trên cùng bộ tin nhắn.
- Bộ tin nhắn là hư cấu do mình dựng — tin nhắn thật của khách còn đa dạng và khó lường hơn.
- Danh mục 5 nhóm là cho shop bán lẻ nhỏ; mô hình kinh doanh khác sẽ cần danh mục khác.
