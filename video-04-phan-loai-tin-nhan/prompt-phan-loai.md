# Prompt phân loại tin nhắn — nguyên văn mình đã dùng

Đây là prompt nguyên văn mình dán vào Gemini trong Video 04. Bạn thay danh sách tin nhắn
ở cuối bằng tin nhắn của shop mình, giữ nguyên phần danh mục và quy tắc. Mẫu danh mục
tách riêng ở mau-danh-muc-5-nhom.md để bạn tiện sửa cho khớp việc của mình.

---

Bạn là trợ lý của một shop online bán đồ điện gia dụng. Hãy phân loại 20 tin nhắn khách dưới đây vào đúng MỘT nhóm trong danh mục cố định sau:

- HOI_GIA: hỏi giá sản phẩm, phí ship, khuyến mãi/mã giảm — chưa chốt mua.
- DAT_HANG: chốt mua, hỏi cách đặt, xác nhận đơn, đổi địa chỉ giao, hỏi còn hàng để mua.
- KHIEU_NAI: phàn nàn về sản phẩm/dịch vụ/giao hàng đã xảy ra, đòi bảo hành, đổi trả, hoàn tiền.
- GOP_Y: khen, đề xuất cải tiến/mở rộng — không phàn nàn về một sự cố cụ thể đã xảy ra với chính họ.
- KHAC: không thuộc 4 nhóm trên.

Quy tắc bắt buộc:
1. Mỗi tin nhắn chỉ đúng 1 nhóm, chỉ được chọn trong 5 nhóm trên, không tự thêm nhóm mới.
2. Tin có 2 ý thì chọn nhóm của ý cần shop xử lý trước.
3. Trả lời bằng bảng 3 cột: STT | Nhóm | Lý do ngắn (tối đa 12 từ).
4. Sau bảng, thêm đúng 1 dòng tổng hợp: số lượng tin theo từng nhóm.

Danh sách tin nhắn:
[dán danh sách tin nhắn của bạn vào đây, đánh số từ 1]
