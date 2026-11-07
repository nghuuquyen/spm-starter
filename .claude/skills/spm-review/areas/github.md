# Review: GitHub

Đọc: GitHub Milestones, Issues, Pull requests, Releases của repo; `.github/ISSUE_TEMPLATE/`, `.github/pull_request_template.md`. Dùng `gh` chỉ để đọc. Không có quyền thì nhờ nhóm dán danh sách milestone và vài parent task.

## Vì sao quan trọng

Tài liệu nói kế hoạch, GitHub cho thấy thực tế. Parent task rõ ràng thì dev tự tách việc được mà không phải hỏi lại; milestone theo dõi bằng task thì biết thật sự đang trễ hay đúng hạn. Task chỉ có tiêu đề thì không ai biết khi nào là xong.

## Chuẩn yêu cầu

- Milestone `MS-xx`, khớp `master-plan.xlsx`.
- Parent task cho toàn dự án. Mỗi parent task ghi mã FR, `MS-xx`, owner, hạn, điều kiện hoàn thành.
- Mẫu issue cho bug, feedback, change request. Change request mã `CR-xx` là GitHub Issue, ghi tài liệu và task đã cập nhật.
- Với milestone thực hiện: subtask, PR, code review, release note.

## Mục tiêu chất lượng

- Chung chung: có milestone và task nhưng không khớp plan hoặc quá chung.
- Cụ thể: khớp plan; parent task có FR, owner, hạn, điều kiện hoàn thành.
- Dùng được ngay: dev tách được subtask không cần hỏi lại; milestone thực hiện theo dõi được tiến độ thật từ task.

## Các bước kiểm

1. Milestone trên GitHub có mã `MS-xx`, tên và ngày khớp `master-plan.xlsx` không? Có mô tả phần giao không? Tên milestone có dễ nhầm với mã module không?
2. Mọi FR có nằm trong ít nhất một parent task không? FR nào có trong PRD mà không có task?
3. Lấy mẫu 5 parent task: có FR, `MS-xx`, owner là người thật (assignee), hạn, điều kiện hoàn thành không? Body rỗng là vấn đề.
4. Nội dung task có khớp PRD không (thời hạn, quy tắc, phạm vi)?
5. Có mẫu issue cho bug, feedback, CR không? Issue thật có dùng mẫu không?
6. **Milestone thực hiện:**
   - parent task có subtask;
   - code vào qua PR có review;
   - issue đóng có bằng chứng (PR, commit, checklist đã tích);
   - có release note.
7. Issue đã đóng: đóng vì xong thật hay vì không làm? Checklist trong issue có được tích khi đóng không?
8. Trạng thái trên GitHub có khớp với báo cáo tiến độ không?

## Câu hỏi để nhóm tự trả lời

- Một bạn mới vào nhóm, chỉ đọc parent task, có biết phải làm gì và khi nào là xong không?
- Nhìn GitHub, nhóm trả lời được "milestone thực hiện đã xong bao nhiêu phần trăm" bằng số liệu nào?

## Lỗi hay gặp

- Issue chỉ có tiêu đề, body rỗng, không assignee, không hạn.
- Owner ghi vai trò ("Backend Dev") thay vì người thật.
- Milestone không có ngày, không có mô tả, mã khác với master plan.
- Không có mẫu issue và mẫu PR.
- PR tự merge không qua review dù Team Charter quy định có review.
- Issue được đóng mà không có bằng chứng đã xong: không có PR, checklist chưa tích.
