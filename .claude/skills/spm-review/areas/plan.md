# Review: Master Plan và rủi ro

Tìm theo mục lục của nhóm. Vị trí trong bộ khung: `docs/08-project/master-plan.xlsx` (sheet Milestones, WBS, Resources, Gantt, Change log), `master-plan.md`, `risk-register.md` (hoặc vị trí mục lục chỉ tới).

## Vì sao quan trọng

Kế hoạch trả lời: giao gì, khi nào, ai làm, và nếu có chuyện thì sao. Milestone chia theo tầng kỹ thuật ("làm xong database", "làm xong API") khiến khách không dùng thử được gì cho tới cuối dự án, và phát hiện sai thì đã muộn. Kế hoạch không chừa năng lực cho thay đổi thì CR đầu tiên sẽ làm trễ mọi thứ phía sau.

## Chuẩn yêu cầu

- `master-plan.xlsx`: sheet Milestones, WBS, Resources, Gantt, Change log. `master-plan.md`: một trang giải thích cách chia milestone.
- Mỗi milestone hướng đến một phần phần mềm chạy được để client tự dùng thử; nên chia theo workflow.
- Milestone `MS-xx` ghi phần giao được và điều kiện nghiệm thu.
- Phần mới không làm hỏng phần đã chạy: có regression test trước khi bàn giao.
- Kế hoạch nên chừa năng lực cho change request.
- Gantt vẽ từ ngày, không tô tay. Khi CR được duyệt, ghi phiên bản mới vào Change log, không ghi đè.
- **Rủi ro:** mô tả, khả năng xảy ra, tác động, owner, phương án, trạng thái.

## Mục tiêu chất lượng

- Chung chung: mốc chia theo tầng kỹ thuật hoặc chỉ giao tài liệu; thiếu nguồn lực hoặc rủi ro.
- Cụ thể: mỗi milestone giao phần chạy được; có phụ thuộc, nguồn lực, rủi ro.
- Dùng được ngay: có cách client kiểm tra, cách nhận feedback, năng lực dự phòng; rủi ro phần mềm có owner và phương án.

## Các bước kiểm

1. Có đủ 5 phần Milestones, WBS, Resources, Gantt, Change log chưa? Các phần này có thể nằm ở file hoặc sheet tên khác, miễn mục lục chỉ tới. Có trang giải thích vì sao chia milestone như vậy chưa?
2. **Từng milestone:** sau milestone này, client tự làm được việc gì trên phần mềm? Nếu câu trả lời là "chưa làm được gì" hoặc "xem tài liệu" thì milestone đó đang chia theo tầng kỹ thuật hoặc chỉ giao tài liệu.
3. Mỗi milestone có điều kiện nghiệm thu kiểm được, và cách client kiểm tra không?
4. **Chỉ một bộ mốc:** danh sách và ngày milestone có giống nhau ở proposal, master plan, GitHub và các tài liệu khác không?
5. **WBS:** mỗi hạng mục có milestone, FR hoặc module, effort, owner, ngày không? Có hạng mục cho tích hợp, test, regression, sửa lỗi không? Tích hợp có bị dồn hết vào milestone cuối không?
6. **Resources:** tổng giờ nguồn lực có đủ cho tổng effort WBS không, và có ai bị giao quá sức không? Nguồn lực là người thật trong nhóm hay vai trò mô phỏng có ghi rõ? Nếu chỉ có vai trò, hỏi nhóm ai đảm nhận vai trò nào, không tự tính.
7. **Gantt:** vẽ từ ngày trong ô hay tô màu tay? Có phụ thuộc giữa các hạng mục không?
8. **Năng lực dự phòng:** effort cho test, regression, sửa lỗi đã nằm trong WBS và báo giá chưa (đây là việc đã biết trước)? Phần chừa cho CR và rủi ro (việc chưa biết trước) là bao nhiêu, nằm ở đâu, có bị tính trùng với effort sửa lỗi không?
9. **Change log:** có dòng phiên bản đầu tiên không? Kế hoạch đã đổi mà Change log không có dòng nào là vấn đề.
10. **Rủi ro:** có đủ 6 thông tin (mô tả, khả năng, tác động, owner, phương án, trạng thái) không? Có rủi ro phần mềm thật của dự án (tích hợp, dữ liệu, hiệu năng, phụ thuộc bên ngoài, thiếu người) hay chỉ rủi ro chung chung? Owner có phải người thật không? Phương án có làm được không?
11. Milestone thực hiện đã chọn có hợp lý không: có chạy được và demo được trong thời gian môn học không?

## Câu hỏi để nhóm tự trả lời

- Sau milestone đầu tiên, client mở phần mềm và làm được gì?
- Nếu milestone 2 trễ một tuần, những gì phía sau bị ảnh hưởng?
- Rủi ro nào nhóm thấy dễ xảy ra nhất, ai theo dõi, dấu hiệu nào cho biết nó đang xảy ra?

## Chỗ hay bị sót

- Không có Master Plan, chỉ có vài bảng rời rạc ở các tài liệu khác nhau.
- Hai hoặc nhiều bộ mốc khác nhau giữa proposal, lịch trình và GitHub.
- Thiếu sheet Milestones với phần giao và điều kiện nghiệm thu; thiếu Change log.
- Gantt tô màu bằng tay.
- Toàn bộ tích hợp hệ thống dồn vào milestone cuối.
- Sổ rủi ro không có trong repo, hoặc rủi ro chung chung, owner là "cả nhóm".
