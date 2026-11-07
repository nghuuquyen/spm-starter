# Review theo vòng 3: hoàn thiện

Dùng trước vòng feedback 3 và trước khi chốt bài. Theo chuẩn, vòng 3 tập trung vào **hoàn thiện**:

- issue cũ đã được xử lý thật chưa;
- độ sâu nội dung;
- format;
- vấn đáp thử.

Đây là lúc biến tài liệu từ "đủ" thành "dùng được ngay": người ngoài đọc hiểu, dev làm theo được, khách đủ thông tin để quyết định.

## Các bước

1. **Issue feedback cũ:** liệt kê các issue feedback của vòng 1 và 2, gồm cả issue đã đóng (dùng `gh issue list --state all` như trong `SKILL.md`, hoặc nhờ nhóm dán). Với từng issue:
   - đã có PR hoặc commit sửa chưa;
   - điều kiện "Hoàn thành khi" đã đạt chưa, mở đúng chỗ để kiểm;
   - nếu nhóm đóng issue vì không đồng ý, lý do có rõ ràng không.

   Theo chuẩn, đóng kèm lý do hợp lý thì không bị coi là chưa xử lý.
2. **Độ sâu nội dung:** với từng hạng mục, mở phần "Mục tiêu chất lượng" trong file hướng dẫn của hạng mục đó. So nội dung của nhóm với mô tả "dùng được ngay", rồi chỉ ra chỗ nào còn có thể sâu hơn. Ưu tiên những phần chạm tới milestone thực hiện.
3. **Milestone thực hiện có bằng chứng chạy thật:**
   - subtask, PR có review;
   - kết quả test thực tế;
   - release note;
   - báo cáo giải thích chênh lệch giữa kế hoạch và GitHub;
   - ít nhất một vòng feedback (mô phỏng thì ghi `Mô phỏng`).
4. **Format:**
   - mục lục chỉ đúng mọi thứ;
   - không còn file rỗng hay dòng hướng dẫn của bộ khung chưa điền;
   - mã theo quy ước;
   - file Word/Excel có người chịu trách nhiệm và lịch sử phiên bản;
   - bản proposal đã gửi nằm trong `sent/`.
5. **Vấn đáp thử:** gợi ý từng bạn chạy `/spm-defense-practice` với phần mình phụ trách. Chỗ nào bạn trả lời chưa được thường là chỗ tài liệu còn mờ.

## Chọn góp ý

Vòng này nhóm đã làm nhiều. Ghi nhận rõ những gì đã tiến bộ so với các vòng trước. "Cần bổ sung" (tối đa 10) chỉ gồm issue cũ chưa xử lý xong, phần chuẩn yêu cầu còn thiếu (gồm của milestone thực hiện), và mâu thuẫn còn sót. Những chỗ đã đủ nhưng còn làm sâu thêm được thì đưa vào "Có thể làm sâu thêm". Không xếp mức hay đánh giá đạt.

Nhắc nhóm: mọi thay đổi sau thời điểm chốt không được tính, nên hoàn tất và merge trước hạn.
