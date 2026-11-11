# Video 06 — Đối chiếu kiểm chứng: làm báo cáo một mạch vs chia 4 bước có điểm dừng

Việc thật ở đây là việc ai làm báo cáo định kỳ cũng gặp: số liệu nằm rải ở nhiều file, và
nỗi sợ lớn nhất không phải viết chậm — mà là số sai lọt vào báo cáo gửi quản lý mà không
biết nó sai từ đâu. Mình test hai cách dùng AI làm việc này trên cùng một bộ số.

## Cách mình test để bạn tự kiểm chứng được

Mình dựng ba file số liệu hư cấu (doanh thu theo tuần của 3 chi nhánh, chi phí, vận hành)
và tính tay đáp án chuẩn trước: doanh thu cộng dồn đúng là 787 triệu (An Phú 340, Bình
Thạnh 273, Cầu Giấy 174 cho 3 tuần đã chốt), tổng chi phí 621, chênh lệch 166. Trong dữ
liệu cài sẵn bốn bẫy: (1) file doanh thu ghi tổng in sẵn 812 — sai; (2) doanh thu Bình
Thạnh Tuần 3 là 66 ở file 1 nhưng 69 ở ghi chú file 2; (3) giá trị hàng hoàn ghi bằng
nghìn đồng (18.400 nghìn = 18,4 triệu); (4) Cầu Giấy Tuần 4 ghi "chưa chốt" — không có số.
Cách A nhận một prompt "viết báo cáo hoàn chỉnh". Cách B nhận chuỗi 4 prompt gửi lần lượt
trong cùng một cuộc trò chuyện: trích → dàn ý → viết → rà soát, mỗi bước có tiêu chí đạt.

## Kết quả theo từng bẫy

| Bẫy | Cách A (một mạch) | Cách B (chia bước) |
|---|---|---|
| 1. Tổng in sẵn sai | SAI — lấy 812 làm tổng chính thức của báo cáo, không nêu 787 | ĐÚNG — bước trích cộng ra 787, đánh dấu LỆCH với 812 |
| 2. Mâu thuẫn 2 file | ĐÚNG — nêu cả 66 và 69, đưa vào mục cần xử lý | ĐÚNG — đánh dấu MÂU THUẪN ngay ở bảng trích, báo cáo nêu cả hai |
| 3. Đơn vị nghìn đồng | ĐÚNG — viết 18,4 triệu đồng | ĐÚNG — giữ nguyên "18.400 nghìn đồng" từ bước trích |
| 4. Ô số chưa chốt | SAI — suy ngược từ 812 để điền 25 triệu vào ô trống | ĐÚNG — ghi THIẾU, báo cáo ghi "chưa có số liệu" |
| Số bịa trong bản cuối | Có — xem phân tích dây chuyền dưới đây | Không |

Điểm đáng chú ý nhất: cách A không hề tính sai phép cộng nào ở cấp chi nhánh (340, 273,
174 đều đúng). Lỗi của nó là kỷ luật neo số: tin con số tổng in sẵn, rồi từ mỏ neo sai đó
suy ngược để lấp ô số còn thiếu. Lỗi dây chuyền thành một chuỗi: ô Tuần 4 bịa 25 triệu →
tổng Cầu Giấy thành 199 → lợi nhuận thành 191 thay vì 166 → tỷ suất và giá trị đơn trung
bình tính trên nền sai → và cuối cùng là một nhận xét kinh doanh bịa hoàn toàn: "doanh thu
Tuần 4 sụt giảm đáng kể, cần kiểm tra nguyên nhân", nói về một con số không tồn tại. Bản
báo cáo trông rất chuyên nghiệp — đó chính là phần nguy hiểm.

Ở cách B, cả bốn vấn đề bị lộ ngay ở bước trích, trước khi một chữ báo cáo nào được viết.
Các bước sau bị ràng buộc chỉ dùng số trong bảng trích, nên bản cuối sạch số bịa, và bước
rà soát truy được từng con số về bảng trích.

## Cái giá của cách chia bước (nói thẳng từ chính test này)

Bản cuối của cách B thiếu tổng chi phí 621 và khoản chênh lệch 166, dù hai tổng này hoàn
toàn tính được. Nguyên nhân nằm ở thiết kế của chính mình: bước trích ghi "tổng chi phí:
THIẾU" vì file không in sẵn, và prompt bước viết cấm tính thêm ngoài bảng trích. Bài học
thiết kế rút ra: bước trích phải yêu cầu cộng sẵn các tổng chuẩn vào bảng trích, thì bước
viết mới có chúng mà dùng. Cộng thêm hai hạn chế cố hữu: chia bước tốn 4 lượt hỏi thay vì
1, và điểm dừng chỉ có tác dụng khi người dùng thật sự dừng lại đọc và kiểm ở bước trích —
chạy lướt qua thì chuỗi 4 bước cũng chỉ là 4 prompt nối nhau.

## Giới hạn của test này

Một lần chạy cho mỗi cách, trên một AI (Gemini) và một bộ số liệu ngắn, hư cấu. Kết quả
cho thấy cơ chế lỗi và cách chặn lỗi, chưa phải thống kê về mọi bộ số liệu hay mọi AI;
cách một mạch ở lần chạy khác có thể tự phát hiện một phần bẫy. Số liệu, nhân vật trong
bộ test là hư cấu, dựng để kiểm chứng.
