# Review theo vòng 1: lỗi lớn

Dùng trước vòng feedback 1. Theo chuẩn, vòng 1 tập trung vào **lỗi lớn**:

- hiểu sai bài toán;
- thiếu tài liệu;
- milestone không giao được phần chạy được;
- mâu thuẫn lớn về giá hoặc kế hoạch.

Ở vòng này chưa cần soi chi tiết từng AC hay cách trình bày. Mục tiêu là cái khung lớn của dự án đứng vững: đúng bài toán, đủ tài liệu, giá và kế hoạch không tự mâu thuẫn. Sửa được những chỗ này sớm thì các vòng sau mới có nền để làm kỹ.

## Các bước

1. **Mục lục:** chạy nhanh các bước 1–4 của [index.md](index.md). Mục lục chưa chỉ đúng thì những bước sau dễ tìm nhầm chỗ.
2. **Bài toán:** đọc phần bài toán trong proposal và phần tổng quan sản phẩm. Đối chiếu với đề bài của môn nếu nhóm có để trong repo, hoặc hỏi nhóm dán đề bài. Không có đề bài thì ghi vào "Chưa chắc" và chỉ kiểm bài toán có nhất quán giữa các tài liệu không, rồi làm tiếp. Có actor, luồng, ràng buộc nào của đề bài bị bỏ sót hoặc hiểu khác không? Phạm vi làm và không làm có hợp với bài toán không?
3. **Đủ tài liệu:** đi qua bảng "Nội dung tối thiểu" của chuẩn. Ở vòng này chỉ cần biết từng phần **đã có hay chưa**: proposal, báo giá, PRD, master plan, rủi ro, GitHub, team charter, quality, product, quản trị. Phần có tiêu đề mà chưa có nội dung thì tính là chưa có.
4. **Milestone:** với từng milestone trong kế hoạch, hỏi "sau milestone này client tự dùng thử được gì?" (xem bước 2 của [plan.md](plan.md)). Milestone thực hiện đã được khai báo trong mục lục chưa? Milestone nào đã đóng hoặc được ghi là xong thì có bằng chứng chạy được không (code, PR, kết quả test; xem bước 7 của [github.md](github.md))?
5. **Giá và kế hoạch có mâu thuẫn lớn không:**
   - tổng giá có giống nhau ở mọi nơi nhắc tới không;
   - danh sách và ngày milestone có giống nhau giữa proposal, master plan và GitHub không;
   - tổng nguồn lực có đủ cho tổng effort không. Nếu nguồn lực chỉ là vai trò, hỏi nhóm ai đảm nhận vai trò nào, không tự tính.

## Chọn góp ý

Chỉ đưa vào "Cần bổ sung" những gì thuộc 4 nhóm lỗi lớn ở trên, tối đa 7 mục. Những chỗ chuẩn có yêu cầu nhưng chi tiết hơn ghi gọn mỗi chỗ một dòng trong "Để vòng sau", ví dụ: mẫu FR thiếu mục, mã AC chưa đầy đủ, Excel chưa dùng công thức, Gantt tô tay, parent task thiếu owner hay hạn, tên milestone. Không xếp mức hay đánh giá đạt cho bất kỳ phần nào.

Cuối bản review, gợi ý nhóm: sau khi sửa xong các lỗi lớn, chạy `/spm-review prd` và `/spm-review plan` để bắt đầu làm kỹ từng phần trước vòng 2.
