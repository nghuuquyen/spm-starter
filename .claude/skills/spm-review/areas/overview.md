# Review: Tổng thể

Dùng trước mỗi vòng feedback hoặc trước khi nộp. Mục tiêu: chọn ra những góp ý **có ích nhất** cho cả repo (tối đa 10 mục "Cần bổ sung"), không phải liệt kê mọi chỗ nhỏ.

## Các bước

1. Chạy các bước của [index.md](index.md) trước. Mục lục sai thì những phần sau có thể bị tìm nhầm chỗ.
2. Với từng hạng mục còn lại (`proposal`, `prd`, `plan`, `github`, `team-charter`, `quality`, `product`, `governance`), mở file hướng dẫn trong thư mục này và kiểm nhanh mục "Chuẩn yêu cầu": phần nào chưa có, phần nào có tiêu đề mà chưa có nội dung. Chưa cần đi sâu từng bước như khi review riêng hạng mục.
3. Chạy [consistency.md](consistency.md) cho 3 tính năng quan trọng nhất, ít nhất 1 tính năng thuộc milestone thực hiện.
4. Kiểm milestone: mỗi milestone có giao phần mềm chạy được để client tự dùng thử không? Milestone thực hiện đã khai báo và có bằng chứng chạy được chưa?
5. Kiểm `Mô phỏng`: client, feedback, báo cáo, CR mô phỏng đã ghi rõ chưa?

## Chọn góp ý

Dùng thứ tự ưu tiên chung trong `SKILL.md`. Tối đa 10 mục "Cần bổ sung".

Gộp các chỗ cùng gốc thành một góp ý. Ví dụ "29 FR đều chưa có Priority" là một góp ý, không phải 29. Ghi nhận rõ những phần nhóm đã làm tốt trước khi nêu góp ý.

## Cuối bản review tổng thể

Thêm một bảng ngắn, mỗi hạng mục một dòng:

| Hạng mục | Tình trạng | Việc nên làm tiếp |
| --- | --- | --- |
| proposal | chưa thấy thiếu (kiểm nhanh) / còn thiếu / chưa có | `/spm-review proposal` để xem chi tiết |

Cột tình trạng chỉ mô tả có hay thiếu sau một lượt kiểm nhanh, **không phải kết luận đạt, không phải đánh giá hay điểm số**. Gợi ý nhóm chạy review riêng từng hạng mục còn thiếu để xem chi tiết.
