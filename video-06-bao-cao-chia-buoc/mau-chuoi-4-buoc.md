# Mẫu chuỗi 4 prompt có điểm dừng (nguyên văn) + checklist tiêu chí đạt

Bốn prompt này gửi lần lượt trong CÙNG một cuộc trò chuyện, chờ AI trả lời xong mới
gửi bước tiếp theo. Tư tưởng thiết kế: bước đầu tiên luôn là trích số liệu chứ không
phải viết, và mỗi bước có tiêu chí đạt riêng để lỗi bị chặn ở đúng bước sinh ra nó.

Checklist kiểm nhanh ở từng điểm dừng (30 giây mỗi bước):
- Sau bước TRÍCH: chọn 3 con số bất kỳ, đối chiếu với file gốc; có đánh dấu nào cho
  số lệch, số mâu thuẫn, số thiếu không?
- Sau bước DÀN Ý: dàn ý có phủ hết các nhóm số liệu không; mục thiếu số có ghi để trống không?
- Sau bước VIẾT: còn con số nào trong bản viết không truy được về bảng trích không?
- Sau bước RÀ SOÁT: AI có liệt kê được từng số đã đối chiếu không, hay chỉ nói chung chung?

Bài học rút ra từ chính test này: bước TRÍCH nên yêu cầu cộng sẵn các tổng chuẩn
(tổng chi phí, chênh lệch doanh thu − chi phí) vào bảng trích, nếu không bước viết
sẽ thiếu các số tổng hợp đó vì bị cấm tính thêm.


## Bước 1 — TRÍCH (tiêu chí đạt: mọi con số đều có nguồn file; mâu thuẫn và số thiếu phải lộ ra)
Bước 1 — TRÍCH SỐ LIỆU. Chưa viết báo cáo. Hãy liệt kê mọi con số trong 3 file dưới đây thành bảng theo 3 nhóm: Doanh thu / Chi phí / Vận hành. Mỗi con số ghi rõ lấy từ file nào. Cộng dồn các số theo tuần thành số tháng cho từng chi nhánh và ghi con số cộng dồn của bạn bên cạnh mọi con số tổng in sẵn trong file (nếu lệch nhau, đánh dấu LỆCH). Nếu hai file ghi khác nhau cho cùng một chỉ tiêu, liệt kê CẢ HAI và đánh dấu MÂU THUẪN. Chỉ tiêu nào chưa có số thì ghi THIẾU, không tự điền.

=== FILE 1: doanh-thu-thang-10.txt ===
DOANH THU THÁNG 10/2026 — SHOP SAO MAI (đơn vị: triệu đồng)

Chi nhánh An Phú: Tuần 1: 82 · Tuần 2: 79 · Tuần 3: 88 · Tuần 4: 91
Chi nhánh Bình Thạnh: Tuần 1: 64 · Tuần 2: 70 · Tuần 3: 66 · Tuần 4: 73
Chi nhánh Cầu Giấy: Tuần 1: 55 · Tuần 2: 58 · Tuần 3: 61 · Tuần 4: chưa chốt

Tổng doanh thu tháng toàn hệ thống: 812 triệu đồng.

=== FILE 2: chi-phi-thang-10.txt ===
CHI PHÍ THÁNG 10/2026 — SHOP SAO MAI (đơn vị: triệu đồng)

Nhập hàng: 402
Nhân sự: 118
Mặt bằng: 66
Điện nước: 14
Marketing: 21

Ghi chú đối chiếu: doanh thu Chi nhánh Bình Thạnh Tuần 3 theo sổ kho là 69 triệu đồng.

=== FILE 3: van-hanh-thang-10.txt ===
SỐ LIỆU VẬN HÀNH THÁNG 10/2026 — SHOP SAO MAI

Tổng số đơn hàng: 4.218 đơn
Số đơn hoàn: 96 đơn
Giá trị hàng hoàn: 18.400 nghìn đồng
Khách hàng mới trong tháng: 612
Tỷ lệ khách quay lại: 38%

## Bước 2 — DÀN Ý (tiêu chí đạt: phủ hết 3 nhóm số liệu; mục thiếu số phải ghi sẽ để trống)
Bước 2 — DÀN Ý. Dựa vào bảng trích ở bước 1, lập dàn ý báo cáo tháng (chỉ dàn ý, chưa viết): các mục chính, mỗi mục ghi sẽ dùng những con số nào từ bảng trích. Mục nào bị THIẾU số hoặc đang MÂU THUẪN thì ghi rõ trong dàn ý là "để trống, chờ chốt" hoặc "nêu cả hai số".

## Bước 3 — VIẾT (tiêu chí đạt: chỉ dùng số trong bảng trích; không số mới)
Bước 3 — VIẾT BÁO CÁO. Viết báo cáo tháng hoàn chỉnh theo dàn ý bước 2, chỉ dùng các con số đã có trong bảng trích bước 1. Chỗ MÂU THUẪN: nêu cả hai con số và ghi chưa chốt. Chỗ THIẾU: ghi "chưa có số liệu". Không tính thêm, không ước lượng thêm bất kỳ con số nào ngoài những phép tính đã có trong bảng trích.

## Bước 4 — RÀ SOÁT (tiêu chí đạt: mọi con số trong bản cuối truy được về bảng trích)
Bước 4 — RÀ SOÁT. Đối chiếu bản báo cáo vừa viết với bảng trích ở bước 1: liệt kê mọi con số trong báo cáo không khớp bảng trích hoặc không rõ nguồn, sửa lại các chỗ đó, rồi đưa ra BẢN BÁO CÁO CUỐI CÙNG hoàn chỉnh sau rà soát.
