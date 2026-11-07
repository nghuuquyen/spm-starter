# Review theo vòng 1: lỗi lớn

Dùng trước vòng feedback 1. Theo chuẩn, vòng 1 tập trung vào **lỗi lớn**:

- hiểu sai bài toán;
- thiếu tài liệu;
- milestone không giao được phần chạy được;
- mâu thuẫn lớn về giá hoặc kế hoạch.

Ở vòng này chưa cần soi chi tiết từng AC hay cách trình bày. Mục tiêu là cái khung lớn của dự án đứng vững: đúng bài toán, đủ tài liệu, giá và kế hoạch không tự mâu thuẫn. Sửa được những chỗ này sớm thì các vòng sau mới có nền để làm kỹ.

## Các bước

1. **Mục lục:** chạy nhanh các bước 1–4 của [index.md](index.md). Mục lục chưa chỉ đúng thì những bước sau dễ tìm nhầm chỗ.
2. **Bài toán:** đọc phần bài toán trong proposal và `01-product/`. Đối chiếu với đề bài của môn nếu nhóm có để trong repo, hoặc hỏi nhóm dán đề bài. Có actor, luồng, ràng buộc nào của đề bài bị bỏ sót hoặc hiểu khác không? Phạm vi làm và không làm có hợp với bài toán không?
3. **Đủ tài liệu:** đi qua bảng "Nội dung tối thiểu" của chuẩn. Ở vòng này chỉ cần biết từng phần **đã có hay chưa**: proposal, báo giá, PRD, master plan, rủi ro, GitHub, team charter, quality, product, quản trị. Phần có tiêu đề mà chưa có nội dung thì tính là chưa có.
4. **Milestone:** với từng milestone trong kế hoạch, hỏi "sau milestone này client tự dùng thử được gì?" (xem bước 2 của [plan.md](plan.md)). Milestone thực hiện đã được khai báo trong mục lục chưa?
5. **Giá và kế hoạch có mâu thuẫn lớn không:**
   - tổng giá có giống nhau ở mọi nơi nhắc tới không;
   - danh sách và ngày milestone có giống nhau giữa proposal, master plan và GitHub không;
   - tổng effort có đủ cho tổng nguồn lực không.

## Chọn góp ý

Chỉ đưa vào "Cần bổ sung" những gì thuộc 4 nhóm lỗi lớn ở trên. Những chỗ chi tiết hơn (FR thiếu Edge Case, AC chưa có mã đầy đủ, trình bày) ghi gọn trong "Gợi ý thêm" hoặc nhắc rằng vòng 2, vòng 3 sẽ xem kỹ.

Cuối bản review, gợi ý nhóm: sau khi sửa xong các lỗi lớn, chạy `/spm-review prd` và `/spm-review plan` để bắt đầu làm kỹ từng phần trước vòng 2.
