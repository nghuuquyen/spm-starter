# Review: Nhất quán (chuỗi nối giữa các tài liệu)

Đối số: một mã FR hoặc tên tính năng, ví dụ `/spm-review consistency FR-STU-02`. Không có thì chọn 3 tính năng quan trọng nhất của PRD, ít nhất 1 tính năng thuộc milestone thực hiện, và nói rõ vì sao chọn.

## Vì sao quan trọng

Một dự án nhất quán là khi giá, effort, kế hoạch, task và test cùng kể một câu chuyện. Khi một mắt xích đứt, thay đổi ở một nơi không lan sang nơi khác: tính năng không được tính giá, task không có test, test không biết kiểm AC nào. Đây là phần cho thấy nhóm quản lý dự án thật hay chỉ viết từng tài liệu rời.

## Chuẩn yêu cầu

- Chuỗi: Proposal và báo giá → PRD → Master Plan → parent task → test → báo cáo. Tính năng chưa thực hiện chỉ cần lần đến kịch bản test.
- Mỗi yêu cầu, việc, thay đổi có mã riêng. Liên kết chỉ khai báo ở một phía.
- `traceability-matrix.md` tổng hợp theo từng AC (AC → Test → Parent task → Milestone → Báo giá), không phải nơi gốc để sửa.

## Mục tiêu chất lượng

- Chung chung: nhiều chỗ đứt giữa các tài liệu.
- Cụ thể: 3 tính năng được chọn lần được qua các tài liệu, chỉ có lỗi nhỏ.
- Dùng được ngay: giá, effort, plan, task, test khớp nhau; quyết định kỹ thuật lớn phản ánh vào effort, rủi ro, timeline.

## Các bước kiểm

Với mỗi tính năng, đi từng mắt xích và ghi **có / thiếu / mâu thuẫn** kèm vị trí:

1. **Báo giá:** hạng mục `Q-xx` nào chứa FR hoặc module này? Effort bao nhiêu, có phần tích hợp, test không?
2. **PRD:** FR ở file nào, có những AC nào?
3. **Master Plan:** thuộc `MS-xx` nào, dòng WBS nào? Effort và ngày có khớp báo giá không?
4. **GitHub:** parent task `#n` nào ghi mã FR này, cùng `MS-xx`, có owner, hạn, điều kiện hoàn thành? Nội dung task có khớp PRD không?
5. **Test:** `TS-xx` nào ghi mã các AC này? AC nào chưa có test?
6. **Kết quả và báo cáo** (chỉ tính năng thuộc milestone thực hiện): có kết quả test chạy thật, có trong báo cáo không?
7. **Ma trận truy vết:** các dòng của tính năng này có khớp với những gì vừa lần được không?

Sau đó so thêm các con số dùng ở nhiều nơi:

- tổng giá (proposal so với báo giá);
- danh sách và ngày milestone (proposal, master plan, GitHub);
- effort (báo giá so với WBS);
- số người (Resources so với Team Charter);
- thời hạn và giới hạn trong FR so với workflow, task, test.

## Cách trình bày thêm

Trước danh sách vấn đề, đặt một bảng chuỗi cho từng tính năng:

| Mắt xích | Mã | Vị trí | Trạng thái |
| --- | --- | --- | --- |
| Báo giá | | | có / thiếu / mâu thuẫn |

Với mỗi chỗ đứt, nói rõ sửa ở **nơi gốc** nào (không sửa trong ma trận truy vết trước). Không tự sửa số liệu: giá, effort, ngày là quyết định của nhóm.

## Câu hỏi để nhóm tự trả lời

- Client bỏ tính năng này: những file nào, dòng nào phải sửa? Nhóm có tìm hết được bằng mã không?
- Một quyết định kỹ thuật lớn của nhóm (ví dụ tích hợp hệ thống ngoài) đã được tính vào effort, rủi ro và timeline ở đâu?

## Lỗi hay gặp

- Chuỗi đứt ngay mắt đầu vì không có báo giá theo hạng mục.
- Proposal và Master Plan dùng hai bộ mốc khác nhau.
- Task GitHub ghi thời hạn hoặc quy tắc khác PRD.
- Test trỏ tới FR, không trỏ tới AC.
- Ma trận truy vết có cột nhưng không có cột báo giá, task, milestone; hoặc rỗng.
