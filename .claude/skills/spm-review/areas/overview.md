# Review: Tổng thể

Dùng trước mỗi vòng feedback hoặc trước khi nộp. Mục tiêu: chọn ra những góp ý **có ích nhất** cho cả repo (tối đa 10 mục "Cần bổ sung"), không phải liệt kê mọi chỗ nhỏ.

## Các bước

1. Chạy các bước của [index.md](index.md) trước. Mục lục sai thì những phần sau có thể bị tìm nhầm chỗ.
2. Với từng hạng mục còn lại (`proposal`, `prd`, `plan`, `github`, `team-charter`, `quality`, `product`, `governance`), mở file hướng dẫn trong thư mục này và kiểm nhanh mục "Chuẩn yêu cầu": phần nào chưa có, phần nào có tiêu đề mà chưa có nội dung. Chưa cần đi sâu từng bước như khi review riêng hạng mục.
3. Chạy [consistency.md](consistency.md) cho 3 tính năng quan trọng nhất, ít nhất 1 tính năng thuộc milestone thực hiện.
4. Kiểm milestone: mỗi milestone có giao phần mềm chạy được để client tự dùng thử không? Milestone thực hiện đã khai báo và có bằng chứng chạy được chưa?
5. Kiểm `Mô phỏng`: client, feedback, báo cáo, CR mô phỏng đã ghi rõ chưa?

## Chọn góp ý

Ưu tiên theo thứ tự:

1. Hiểu sai bài toán, hoặc phạm vi mâu thuẫn với goals và non-goals.
2. Chuỗi nối bị đứt (không có báo giá theo hạng mục, task không khớp PRD, test không trỏ AC).
3. Mâu thuẫn về giá hoặc kế hoạch (hai con số giá, hai bộ mốc).
4. Milestone không giao được phần chạy được.
5. Thiếu tài liệu hoặc thiếu phần bắt buộc.
6. Nội dung có nhưng khó tìm (nhãn `ẩn`).
7. Trình bày.

Gộp các chỗ cùng gốc thành một góp ý. Ví dụ "29 FR đều chưa có Priority" là một góp ý, không phải 29. Ghi nhận rõ những phần nhóm đã làm tốt trước khi nêu góp ý.

## Cuối bản review tổng thể

Thêm một bảng ngắn, mỗi hạng mục một dòng:

| Hạng mục | Tình trạng | Việc nên làm tiếp |
| --- | --- | --- |
| proposal | đã có đủ / còn thiếu / chưa có | `/spm-review proposal` để xem chi tiết |

Cột tình trạng chỉ mô tả có hay thiếu, **không phải đánh giá hay điểm số**. Gợi ý nhóm chạy review riêng từng hạng mục còn thiếu để xem chi tiết.
