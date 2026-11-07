# Review: GitHub

Tìm: GitHub Milestones, Issues của repo; `.github/ISSUE_TEMPLATE/`, `.github/pull_request_template.md`. Dùng `gh` chỉ để đọc, lấy cả mục đã đóng (lệnh trong `SKILL.md`). Không có quyền thì nhờ nhóm dán danh sách milestone và vài parent task.

## Vì sao quan trọng

GitHub là nơi kế hoạch biến thành việc cụ thể. Parent task rõ ràng thì dev tự tách việc được mà không phải hỏi lại; có owner, hạn, điều kiện hoàn thành thì theo dõi được tiến độ. Task chỉ có tiêu đề thì không ai biết khi nào là xong.

## Chuẩn yêu cầu

- Milestone `MS-xx`, khớp kế hoạch.
- Parent task cho toàn dự án. Mỗi parent task ghi mã FR, `MS-xx`, owner, hạn, điều kiện hoàn thành.
- Mẫu issue cho bug, feedback, change request. Change request `CR-xx` là GitHub Issue, ghi tài liệu và task đã cập nhật.
- Chuẩn không yêu cầu subtask, code review hay release.

## Hướng tới

Dev tách được subtask không cần hỏi lại; theo dõi được tiến độ từ task.

## Các bước kiểm

1. Milestone trên GitHub có mã `MS-xx`, tên và ngày khớp kế hoạch không? Tên milestone có dễ nhầm với mã module không?
2. Mọi FR có nằm trong ít nhất một parent task không? FR nào có trong PRD mà không có task?
3. Lấy mẫu 5 parent task: có FR, `MS-xx`, owner là người thật (assignee), hạn, điều kiện hoàn thành không? Body rỗng là chỗ cần bổ sung.
4. Nội dung task có khớp PRD không (thời hạn, quy tắc, phạm vi)? Task chép lại nguyên AC thay vì dẫn mã thì dễ lệch khi PRD đổi (Gợi ý thêm).
5. Có mẫu issue cho bug, feedback, CR không?
6. Issue đã đóng có lý do hoặc dẫn tới thứ đã làm (PR sửa tài liệu, commit) không?

## Câu hỏi để nhóm tự trả lời

- Một bạn mới vào nhóm, chỉ đọc parent task, có biết phải làm gì và khi nào là xong không?
- Nhìn GitHub, nhóm trả lời được "milestone 2 đã chuẩn bị đủ việc chưa, ai làm gì" bằng cách nào?

## Chỗ hay bị sót

- Issue chỉ có tiêu đề, body rỗng, không assignee, không hạn.
- Owner ghi vai trò ("Backend Dev") thay vì người thật.
- Milestone không có ngày, không có mô tả, mã khác với kế hoạch.
- Không có mẫu issue.
