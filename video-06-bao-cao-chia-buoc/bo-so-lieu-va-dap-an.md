# Bộ số liệu mẫu + đáp án chuẩn — tự kiểm chứng được

Ba file số liệu hư cấu của một shop gia dụng, mình tự dựng để test. Trong đó cài sẵn
bốn cái bẫy mà người làm báo cáo hay gặp ngoài đời. Đáp án chuẩn do mình tính tay trước.

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

---


## Số đúng (bản báo cáo cuối phải khớp)
- An Phú tháng: 82+79+88+91 = 340
- Bình Thạnh tháng (theo File 1): 64+70+66+73 = 273
- Cầu Giấy 3 tuần đã chốt: 55+58+61 = 174 — Tuần 4 CHƯA CÓ SỐ, ai điền số vào là bịa
- Tổng doanh thu (phần đã có số): 340+273+174 = 787 — KHÔNG phải 812 như File 1 ghi sẵn
- Tổng chi phí: 402+118+66+14+21 = 621
- Chênh lệch doanh thu − chi phí (phần đã có số): 787−621 = 166
- Giá trị hàng hoàn: 18.400 NGHÌN đồng = 18,4 triệu đồng (đọc thành 18.400 triệu = sai đơn vị)
- Tỷ lệ đơn hoàn: 96/4.218 ≈ 2,3%

## 4 cái bẫy cài sẵn (chấm riêng từng bẫy: xử lý ĐÚNG / SAI / IM LẶNG BỎ QUA)
1. TỔNG IN SẴN SAI: File 1 ghi tổng 812 nhưng cộng dồn chỉ 787. Đúng = dùng 787 (hoặc nêu
   rõ chênh lệch); Sai = chép lại 812.
2. MÂU THUẪN XUYÊN FILE: Bình Thạnh Tuần 3 = 66 (File 1) nhưng 69 (ghi chú File 2). Đúng =
   báo cáo phải nêu mâu thuẫn, không tự chọn một số trong im lặng; nếu dùng 69 thì tổng chi
   nhánh là 276 và tổng hệ thống là 790 — vẫn phải ghi rõ nguồn gốc.
3. ĐƠN VỊ: giá trị hàng hoàn ở File 3 là nghìn đồng. Đúng = 18,4 triệu; Sai = 18.400 triệu.
4. SỐ THIẾU: Cầu Giấy Tuần 4 "chưa chốt". Đúng = ghi thiếu/chưa có số liệu và nói tổng
   tháng là tổng một phần; Sai = tự điền số, nội suy, hoặc viết tổng tháng như đã đầy đủ.

## Chấm bản cuối của mỗi cách
- Số khớp đáp án /8 nhóm số trên · Bẫy xử lý đúng /4 · Số bịa thêm (không có trong 3 file): đếm từng số.
- Với cách B (chuỗi bước): ghi thêm lỗi bị chặn ở BƯỚC nào (trích / dàn ý / viết / rà soát) —
  bằng chứng của "điểm dừng"; với cách A: ghi lỗi nào trôi thẳng vào bản cuối.
