# Hướng dẫn dùng bộ khung repo

Bộ khung này theo đúng mục "Format repo" của tài liệu *Software Project Management: Format nộp bài và tiêu chí chấm*. Khi có điểm khác nhau, tài liệu đó và đề bài chung của môn là căn cứ.

## Cách dùng

1. Chép `docs/`, `.github/`, `src/` và `README.md` vào repo của nhóm. Nhóm đã có tài liệu thì chuyển dần nội dung sang đúng chỗ.
2. Mỗi file có dòng hướng dẫn nằm trong `<!-- … -->`. Dòng này không hiện trên GitHub, có thể giữ lại hoặc xoá.
3. Điền nội dung thật vào chỗ trống. Phần không áp dụng ghi `N/A` kèm lý do, không để file rỗng.
4. Đổi tên hoặc gộp file thì được, nhưng phải sửa `docs/README.md` để chỉ đúng vị trí. **Nội dung không có trong mục lục và không tìm được thì không được tính.**
5. Mỗi thông tin chỉ có một nơi gốc. Nơi khác dẫn lại bằng mã (`FR-…`, `Q-…`, `MS-…`), không chép lại nội dung.
6. Client, feedback, báo cáo và change request được mô phỏng, nhưng phải ghi rõ `Mô phỏng`.
7. File này chỉ để hướng dẫn, xoá đi khi không cần nữa.

## Cấu trúc

★ là phần thuộc "Nội dung tối thiểu" và được chấm theo mục ghi bên cạnh. ○ là phần không có điểm riêng, chỉ dùng làm bằng chứng.

```text
repo/
├── README.md                      giới thiệu dự án, bảng thành viên
├── .github/
│   ├── ISSUE_TEMPLATE/            ★ GitHub: mẫu parent task, bug, feedback, change request
│   └── pull_request_template.md   ★ GitHub: mẫu PR
├── src/                           code của milestone thực hiện
└── docs/
    ├── README.md                  MỤC LỤC BẮT BUỘC
    ├── 01-product/                ★ PRD: vấn đề, actor, goals, non-goals
    ├── 02-domain/                 ○ bằng chứng
    ├── 03-modules/                ★ PRD: mỗi module một thư mục, có prd.md
    ├── 04-workflows/              ○ bằng chứng
    ├── 05-non-functional-requirements/  ★ PRD: NFR đo được
    ├── 06-acceptance/             ★ PRD, Nhất quán: kịch bản test, ma trận truy vết
    ├── 07-architecture/           ○ bằng chứng
    ├── 08-project/                ★ Proposal, Master Plan, rủi ro, Team Charter
    ├── 09-quality/                ★ Quality
    ├── 10-product-management/     ★ Product
    └── 11-governance/             ★ Quản trị và giám sát
```

## Gốc repo

| File | Dùng để | Điền gì |
| --- | --- | --- |
| `README.md` | Trang đầu khi mở repo | Giới thiệu 2–3 câu, link tới mục lục, bảng thành viên (MSSV, họ tên, tài khoản GitHub, vai trò) |
| `src/README.md` | Chỗ để code của milestone thực hiện | Cách chạy, cách chạy test. Code để ở repo riêng thì ghi link và lý do tách |

## `.github/`: mục GitHub

| File | Dùng để | Có sẵn |
| --- | --- | --- |
| `ISSUE_TEMPLATE/config.yml` | Không cho tạo issue trống, bắt chọn mẫu | |
| `ISSUE_TEMPLATE/1-parent-task.md` | Parent task của từng milestone | FR, `MS-xx`, Owner, Hạn, điều kiện hoàn thành, subtask |
| `ISSUE_TEMPLATE/2-bug.md` | Báo lỗi | Mức độ (theo `quality-plan.md`), AC/TS/MS liên quan, các bước tái hiện, kết quả mong đợi và thực tế |
| `ISSUE_TEMPLATE/3-feedback.md` | Phản hồi của client | Nguồn và kênh, nội dung, phân loại, quyết định |
| `ISSUE_TEMPLATE/4-change-request.md` | Change request `CR-xx` | Thay đổi đề xuất, bảng tác động (phạm vi, effort, giá, timeline, rủi ro, test), người duyệt, checklist tài liệu đã cập nhật |
| `pull_request_template.md` | Mẫu PR, gồm cả PR sửa theo feedback | Thay đổi và lý do, `Closes #`, mã liên quan, sheet hoặc mục đã đổi trong Word/Excel, checklist mục lục |

Trên GitHub cần tạo thêm:
- Milestones `MS-xx`, khớp với `master-plan.xlsx`;
- parent task cho toàn dự án;
- subtask, PR, review và release note cho milestone thực hiện.

## `docs/README.md`: mục lục

Đây là file bắt buộc, gồm:

1. Milestone thực hiện (`MS-xx`). Milestone này phải chạy được và demo được.
2. Thứ tự đọc, có link tới mọi file.
3. Bảng tra nhanh vị trí của scope, nguồn lực, rủi ro, change request, Definition of Done.
4. Bảng quy ước mã. `M01` là module, `MS-01` là milestone, không dùng lẫn.
5. Bảng ghi phần nào là `Mô phỏng`.
6. Người chịu trách nhiệm chính của từng file Word/Excel.

## PRD: `01`, `03`, `05`, `06`

| File | Điền gì |
| --- | --- |
| `01-product/README.md` | Vấn đề, bảng actor, goals, non-goals. Phạm vi các FR phải khớp với goals và non-goals |
| `03-modules/README.md` | Danh sách module: mã `M01`, tên, nhóm mã FR, thư mục |
| `03-modules/M01-ten-module/README.md` | Mục đích, actor, phụ thuộc của module. Đổi tên thư mục cho đúng module, mỗi module một thư mục |
| `03-modules/M01-ten-module/prd.md` | Các FR của module. **Mỗi FR đủ 10 mục:** Mô tả, Actor, Priority, Preconditions, Luồng chính, Business Rules, Alternative và Error Flows, Acceptance Criteria, Edge Case. Mỗi business rule và mỗi error flow có ít nhất một AC. Mã viết dạng `FR-XXX-01` và `FR-XXX-01/AC-01`, trong đó XXX là viết tắt module bằng 2–8 chữ in hoa |
| `05-non-functional-requirements/README.md` | NFR `NFR-PERF-01`, có ngưỡng và cách đo. "Hệ thống nhanh" là không đo được |
| `06-acceptance/test-scenarios.md` | Kịch bản `TS-01`. Mỗi kịch bản ghi mã AC hoặc NFR mà nó kiểm |
| `06-acceptance/traceability-matrix.md` | Bảng tổng hợp theo từng AC: AC → Test → Parent task → Milestone → Báo giá. Bảng này không phải nơi gốc: sửa ở nơi gốc trước rồi mới cập nhật bảng |

## Chỉ dùng làm bằng chứng

`02-domain/`, `04-workflows/`, `07-architecture/` không có điểm riêng và không bị chấm thiết kế đúng hay sai. Các phần này dùng để giải thích PRD, effort và rủi ro. Không dùng thì ghi `N/A` kèm lý do.

## `08-project/`: dự án

| File | Điền gì |
| --- | --- |
| `proposal.docx` | Tài liệu gửi khách: lịch sử phiên bản, bài toán, giải pháp, phạm vi làm và không làm, giả định, timeline tổng, giá, điều kiện nghiệm thu |
| `quotation.xlsx` | Sheet **Báo giá**: hạng mục `Q-xx` gắn module/FR, phạm vi, loại effort (gồm cả tích hợp, test, triển khai, sửa lỗi), vai trò, effort. Đơn giá, Thành tiền và Tổng là công thức, không gõ tay. Sheet **Đơn giá**: đơn giá theo vai trò, kèm căn cứ. Sheet **Giả định**: các giả định ảnh hưởng giá |
| `master-plan.xlsx` | Sheet **Milestones**: phần giao chạy được, cách client kiểm tra, điều kiện nghiệm thu. Sheet **WBS**: hạng mục, MS, FR, `Q-xx`, effort, owner, ngày. Sheet **Resources**: giờ của từng người, so với tổng effort WBS. Sheet **Gantt**: tự vẽ từ ngày trong WBS, chỉ nhập ngày bắt đầu tuần đầu ở ô E3, không tô màu tay. Sheet **Change log**: mỗi CR được duyệt ghi một dòng, không ghi đè |
| `master-plan.md` | Vì sao chia milestone như vậy, phụ thuộc giữa các milestone, năng lực dự phòng cho CR và sửa lỗi, cách nhận feedback sau mỗi milestone |
| `risk-register.md` | Rủi ro `R-01`: mô tả, khả năng, tác động, owner, phương án, trạng thái. Ưu tiên rủi ro phần mềm thật của dự án |
| `team-charter.md` | Vai trò gắn với người thật, người dự phòng, cách ra quyết định, lịch phối hợp, xử lý xung đột, khi thiếu người, quy tắc branch, PR, review, merge |
| `assumptions.md`, `constraints.md`, `open-questions.md` | Giả định, ràng buộc, câu hỏi mở. Mỗi dòng ghi ảnh hưởng tới giá hoặc plan |
| `sent/` | Bản PDF của Proposal mỗi lần gửi khách, tên có phiên bản và ngày (ví dụ `proposal-v1.0-2026-11-10.pdf`). Ghi thêm một dòng vào `sent/README.md` |

Khuyến nghị, không tính điểm riêng: biên bản nghiệm thu `acceptance-report.docx` và retrospective `closure.md`, đặt trong `08-project/`.

Mỗi file Word/Excel có một người chịu trách nhiệm chính và giữ cố định tên file. Khi sửa thì ghi rõ trong PR đã đổi sheet hoặc mục nào.

## `09-quality/`: chất lượng

| File | Điền gì |
| --- | --- |
| `quality-plan.md` | QA (phòng ngừa), QC (kiểm tra, có regression test trước khi bàn giao), Definition of Done, mức độ lỗi và cách xử lý, điều kiện release, bằng chứng đã áp dụng ở milestone thực hiện |
| `test-results/` | Kết quả test chạy thật của milestone thực hiện. Mỗi lần chạy một file, ghi commit, TS đã chạy, số đạt trên tổng, các bug tạo ra |

## `10-product-management/`: sản phẩm

| File | Điền gì |
| --- | --- |
| `feedback-process.md` | Kênh nhận feedback, phân loại (bug, CR, cải tiến), cách ưu tiên, ai quyết định sau bàn giao |
| `roadmap.md` | Các giai đoạn, mục tiêu, tính năng, điều kiện để làm |
| `success-metrics.md` | Chỉ số giá trị: mục tiêu, cách đo, tần suất, người theo dõi |

## `11-governance/`: quản trị và giám sát

| File | Điền gì |
| --- | --- |
| `reporting.md` | Báo cáo nào, ai lập, gửi cho ai, khi nào, lưu ở đâu |
| `monitoring.md` | Chỉ số theo dõi (ưu tiên lấy từ GitHub), ngưỡng bình thường, ngưỡng escalate và escalate tới ai |
| `change-control.md` | Các bước xử lý CR, cách đánh giá tác động, người duyệt, những tài liệu phải cập nhật khi CR được duyệt |
| `reports/` | Các báo cáo đã lập. Milestone thực hiện cần ít nhất một báo cáo giải thích chênh lệch giữa plan và GitHub |

## Một chuỗi nối mã hoàn chỉnh

Giảng viên sẽ chọn 3 tính năng và lần theo chuỗi sau. Mắt xích nào đứt thì mất điểm Nhất quán (20 điểm).

```text
quotation.xlsx  Q-03  ──►  prd.md  FR-STU-02/AC-04  ──►  master-plan.xlsx  MS-02
      ──►  GitHub parent task #12  ──►  test-scenarios.md  TS-05  ──►  test-results/, reports/
```
