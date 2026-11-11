# Bảng tra nhanh: 4 loại tác vụ — nhận diện trước khi viết prompt

Một câu hỏi sai kiểu sẽ kéo cả câu trả lời đi chệch. Trước khi hỏi AI, hãy xác định việc
của bạn thuộc loại nào trong 4 loại dưới đây — mỗi loại cần một cấu hình prompt khác hẳn:

| Loại việc | Ví dụ | Prompt cần nhấn | Output đạt khi |
|---|---|---|---|
| Phân tích | Đọc bảng số liệu, tìm nguyên nhân doanh thu thay đổi | Khung phân tích rõ ràng; từng bước suy luận theo thứ tự; tách dữ kiện khỏi nhận định; chỉ dùng số có trong dữ kiện | Mọi kết luận đều truy ngược được về một dữ kiện cụ thể; phần không có dữ kiện được ghi là "chưa đủ dữ kiện" |
| Nghiên cứu | Tìm hiểu một chủ đề, so sánh các lựa chọn | Nêu câu hỏi, phạm vi và tiêu chí chọn nguồn TRƯỚC khi yêu cầu trả lời | Trả lời nằm trong phạm vi đã nêu, nguồn đáp ứng tiêu chí đã đặt |
| Soạn thảo | Viết email, viết mô tả sản phẩm, viết thông báo | Nêu đối tượng đọc, giọng văn, cấu trúc và dàn ý trước | Bản thảo đúng đối tượng, đúng giọng, đủ các phần trong dàn ý |
| Brainstorm | Sinh ý tưởng tên sản phẩm, góc nội dung, hướng giải quyết | Yêu cầu SỐ LƯỢNG và ĐA DẠNG; cho phép táo bạo; hoãn đánh giá sang vòng sau | Đủ số lượng, đủ đa dạng — vòng sinh ý tách hẳn khỏi vòng chọn lọc |

Ba điều rút ra từ thực hành:

1. Brainstorm là loại DUY NHẤT được nới ràng buộc. Ba loại còn lại cần ràng buộc chặt
   hơn thường lệ — đặc biệt là phân tích: ở đây, "càng sáng tạo càng tốt" là câu lệnh
   nguy hiểm nhất, vì nó trả tiền cho AI bằng suy đoán.
2. Việc thật thường là việc LAI (ví dụ: nghiên cứu rồi phân tích). Khi đó kết hợp cấu
   hình của hai loại theo từng giai đoạn, thay vì chọn cứng một loại cho cả bài.
3. Tự chấm bằng truy ngược: lấy bất kỳ một kết luận nào trong bản trả lời, hỏi "kết luận
   này dựa trên dữ kiện nào?" — không truy được về dữ kiện gốc thì kết luận đó chưa đạt,
   dù văn phong có chắc nịch đến đâu.
