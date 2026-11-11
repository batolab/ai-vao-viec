# Mẫu phản hồi 4 ý + mẫu nhật ký vòng lặp sửa prompt

Nguyên tắc: khi đầu ra chưa đạt, đừng sửa đầu ra — hãy sửa PROMPT, và ghi mỗi lần sửa
bằng đúng 4 ý sau. Sau 3–4 vòng mà không tiến triển, đổi cách tiếp cận thay vì lặp tiếp.

## Mẫu phản hồi 4 ý (điền sau mỗi vòng chạy)

- GIỮ GÌ: phần nào của prompt hiện tại đang cho kết quả đúng, không đụng vào.
  (Ví dụ: "Cấu trúc 3 mục Quyết định / Việc được giao / Đang bàn — giữ nguyên.")
- SỬA GÌ: điểm yếu cụ thể vừa nhìn thấy ở đầu ra, nêu bằng chứng.
  (Ví dụ: "Việc được giao đang gộp chung một đoạn văn, mất hạn chót của từng việc.")
- SỬA THÀNH GÌ: câu chữ mới sẽ thay vào prompt — viết sẵn để dán.
  (Ví dụ: "Thêm câu: 'Mục Việc được giao trình bày dạng bảng 3 cột: Việc | Người phụ trách | Hạn.'")
- DỰA VÀO ĐÂU: dòng/dữ kiện nào trong tài liệu gốc làm căn cứ cho thay đổi này.
  (Ví dụ: "Biên bản ghi rõ hạn riêng cho từng người ở mục 3.")

## Cách chạy một vòng lặp

1. Chạy prompt hiện tại trên đầu vào gốc (mở cuộc trò chuyện MỚI mỗi vòng để không lẫn ngữ cảnh).
2. Chấm đầu ra theo một bảng tiêu chí cố định (đáp án chuẩn của riêng việc đó).
3. Viết phản hồi 4 ý → sửa prompt → lưu cả prompt mới lẫn dòng nhật ký.
4. Dừng khi đạt tiêu chí, hoặc sau 3–4 vòng không tiến triển thì đổi cách tiếp cận.

## Mẫu nhật ký vòng lặp

| Vòng | Thay đổi trong prompt (theo phản hồi 4 ý) | Điểm chấm vòng này | Ghi chú |
|---|---|---|---|
| 1 | Prompt ban đầu: "Tóm tắt biên bản thành bản tóm tắt gửi cả nhóm" | 6/6 | Đạt nội dung; việc được giao còn dạng đoạn văn |
| 2 | Thêm cấu trúc 3 mục + bảng Việc/Người/Hạn cho mục việc | 6/6 | Trình bày tra cứu nhanh hơn |
| 3 | Thêm vai trò người ghi biên bản + quy tắc chép nguyên văn số + cấm thêm thông tin ngoài biên bản + bước tự rà soát | 6/6 | Bản thắng — lưu làm prompt chuẩn cho các cuộc họp sau |

(Bảng trên là nhật ký thật của bài test trong video: điểm không tăng vì bản đầu đã đạt —
giá trị của các vòng sau nằm ở độ chặt của quy tắc và tính tái sử dụng, không phải ở điểm số.)
