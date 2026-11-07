# Review: Proposal và báo giá

Đọc: `docs/08-project/proposal.docx`, `docs/08-project/quotation.xlsx`, `docs/08-project/sent/`, `assumptions.md`, `constraints.md` (hoặc vị trí mục lục chỉ tới).

## Vì sao quan trọng

Proposal là cam kết đầu tiên với khách: làm gì, không làm gì, bao lâu, bao nhiêu tiền, nghiệm thu thế nào. Báo giá là cơ sở của con số đó. Giá không suy ra được từ effort thì nhóm không bảo vệ được giá khi khách mặc cả, và cũng không biết dự án lỗ hay lãi khi phạm vi đổi.

## Chuẩn yêu cầu

- **Proposal:** bài toán, giải pháp, phạm vi làm và không làm, giả định, timeline tổng, giá, điều kiện nghiệm thu.
- **Báo giá:** hạng mục `Q-xx`, phạm vi, effort, đơn giá, tổng tiền, công thức. Effort gồm cả tích hợp, test, triển khai, sửa lỗi. Mỗi `Q-xx` ghi module hoặc FR thuộc hạng mục.
- Proposal là Word, kèm PDF khi gửi. Bản đã gửi lưu trong `sent/`, có phiên bản và ngày.
- Excel: số liệu nằm trong ô dữ liệu, tổng là công thức.

## Mục tiêu chất lượng

- Chung chung: mô tả chung, giá không có cơ sở.
- Cụ thể: rõ bài toán và phạm vi; giá tính được từ effort.
- Dùng được ngay: effort có cả tích hợp, test, triển khai, sửa lỗi; giả định ảnh hưởng giá được nêu rõ; khách đủ thông tin để quyết định.

## Các bước kiểm

1. Proposal có đủ 7 phần ở trên không? Phần "không làm" có cụ thể không, hay chỉ một câu chung?
2. Bài toán có nói rõ ai đang gặp vấn đề gì, hiện xử lý ra sao, vì sao cần hệ thống mới không? Hay chỉ mô tả tính năng?
3. Báo giá có mã `Q-xx` cho từng hạng mục, và mỗi hạng mục ghi module hoặc FR không?
4. **Lần ngược con số:** tổng giá trong proposal = tổng trong báo giá? Tổng báo giá = tổng (effort × đơn giá) bằng công thức? Có chỗ nào gõ tay con số tổng không?
5. Effort có các dòng tích hợp, test, triển khai, sửa lỗi (và bảo hành nếu có cam kết) không? Hay chỉ có effort "code tính năng"?
6. Đơn giá có căn cứ không (theo vai trò, theo thị trường)? Chi phí nội bộ và giá bán cho khách có bị nhầm lẫn không?
7. Giả định nào ảnh hưởng tới giá? Nếu giả định sai thì giá đổi thế nào? Proposal có nói không?
8. Timeline tổng trong proposal có khớp danh sách và ngày milestone trong `master-plan.xlsx` không?
9. Điều kiện nghiệm thu có kiểm được không, có dẫn tới AC hay demo cụ thể không?
10. Có bản đã gửi trong `sent/` với phiên bản và ngày không? Khách là mô phỏng thì đã ghi `Mô phỏng` chưa?

## Câu hỏi để nhóm tự trả lời

- Khách đề nghị giảm giá 20%: nhóm bỏ hạng mục `Q-xx` nào, và phạm vi đổi ra sao?
- Một tính năng tốn effort nhiều nhất nằm ở `Q-xx` nào? Effort đó tính thế nào?
- Nếu thời gian tích hợp gấp đôi dự kiến, giá và timeline đổi thế nào?

## Lỗi hay gặp

- Không có báo giá theo hạng mục; chỉ có bảng ngân sách nhân sự theo tháng.
- Giá bán không suy ra được từ chi phí hay effort, hoặc chênh lệch lớn mà không giải thích.
- Hai con số giá khác nhau ở hai tài liệu (ví dụ proposal một giá, file ngân sách một giá khác).
- Effort chỉ có phần phát triển, không có tích hợp, test, triển khai, sửa lỗi.
- Proposal gốc bị xoá hoặc thay bằng bản "điều chỉnh" không còn đủ các phần.
- Timeline trong proposal dùng bộ mốc khác với master plan.
