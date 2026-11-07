# Review: PRD

Đọc: `docs/01-product/`, `docs/03-modules/*/prd.md`, `docs/05-non-functional-requirements/`, `docs/06-acceptance/` (hoặc vị trí mục lục chỉ tới). Có thể giới hạn một module: `/spm-review prd M02`.

## Vì sao quan trọng

PRD là thỏa thuận về "thế nào là xong". Dev dựa vào đó để làm, tester dựa vào đó để kiểm, khách dựa vào đó để nghiệm thu. FR thiếu error flow thì lỗi không ai lường trước; AC không kiểm được thì nghiệm thu thành tranh cãi; thiếu priority thì khi trễ hạn không biết bỏ gì trước.

## Chuẩn yêu cầu

- Vấn đề, actor, goals và non-goals, FR theo mẫu, NFR đo được, AC.
- **Mẫu FR:** Mô tả, Actor, Priority, Preconditions, Luồng chính, Business Rules, Alternative và Error Flows, Acceptance Criteria, ví dụ Edge Case.
- Mỗi business rule và error flow cần ít nhất một AC.
- Mã: module `M02`, FR `FR-STU-02`, AC `FR-STU-02/AC-04`, NFR `NFR-PERF-01`, test `TS-05`. Kịch bản test ghi mã AC hoặc NFR được test.
- Có kịch bản test cho các AC của toàn dự án.

## Mục tiêu chất lượng

- Chung chung: chỉ liệt kê tính năng, AC khó kiểm tra.
- Cụ thể: FR đúng mẫu, NFR đo được, AC test được.
- Dùng được ngay: mỗi rule và error flow có AC; ưu tiên hợp lý; phạm vi khớp goals và non-goals.

## Các bước kiểm

1. **Phần đầu PRD:** vấn đề, actor, goals, non-goals có cụ thể cho dự án này không?
2. **Đếm và lấy mẫu FR:** liệt kê số FR theo module. Đọc kỹ ít nhất 5 FR ở các module khác nhau, trong đó có FR quan trọng nhất của milestone thực hiện.
3. **Với mỗi FR mẫu**, kiểm đủ 10 mục. Mục có tiêu đề nhưng nội dung trống hoặc chung chung tính là thiếu. Lỗi lặp lại ở mọi FR thì gộp một vấn đề ("x/y FR thiếu Priority và Edge Case").
4. **Bảng BR/Error → AC** cho từng FR mẫu: mỗi business rule, mỗi error flow có AC nào kiểm nó? Dòng nào không có AC là vấn đề.
5. **AC kiểm được không:** mỗi AC có điều kiện, dữ liệu, kết quả mong đợi cụ thể (con số, trạng thái, thông báo)? Câu "hệ thống phản hồi nhanh", "giao diện thân thiện" là chưa kiểm được.
6. **Priority:** có không, có lý do không, có khớp goals không? Mọi FR đều "High" cũng là không có ưu tiên.
7. **NFR:** có mã, có ngưỡng đo và cách đo không? Nằm ở một nơi gốc hay rải trong tài liệu kỹ thuật?
8. **Mã:** dạng mã có theo quy ước không? AC có mã đầy đủ `FR-…/AC-…` hay chỉ `AC1` trùng nhau giữa các FR?
9. **Kịch bản test:** mỗi `TS-xx` có ghi mã AC hoặc NFR không? AC nào của FR mẫu chưa có test?
10. **Phạm vi:** có FR nào nằm ngoài goals, hay mâu thuẫn non-goals (ví dụ non-goals ghi "không tự đăng ký" mà có FR đăng ký)? Có FR nào mâu thuẫn FR khác về thời hạn, giới hạn, trạng thái?

## Câu hỏi để nhóm tự trả lời

- Với FR quan trọng nhất, người dùng làm sai thì hệ thống phản ứng thế nào? Đã có AC cho tình huống đó chưa?
- Nếu chỉ kịp làm một nửa số FR của milestone, nhóm bỏ FR nào trước? PRD có thể hiện điều đó không?
- Tester chưa từng nói chuyện với nhóm, chỉ đọc AC, có viết được test không?

## Cách kèm khi nhóm đang viết FR

Nếu nhóm chỉ có ý tưởng, đừng viết FR hộ. Hỏi lần lượt và để nhóm tự trả lời: ai dùng, dùng khi nào, cần gì có sẵn trước, các bước chính, quy tắc nào giới hạn, có cách khác để đi tới cùng kết quả không, sai ở đâu và hệ thống báo gì, trường hợp biên nào (rỗng, quá giới hạn, trùng, hết hạn). Từ câu trả lời của nhóm, chỉ ra mục nào của mẫu đã có ý, mục nào còn trống.

## Chỗ hay bị sót

- FR chỉ có mô tả và luồng chính; thiếu Priority, Alternative, Edge Case.
- Error flow có nhưng không có AC nào kiểm nó.
- AC không có mã, hoặc mã cục bộ trùng nhau giữa các FR.
- NFR viết bằng tính từ ("nhanh", "an toàn") hoặc ghi "chưa có ngưỡng".
- Kịch bản test chỉ trỏ tới FR, không trỏ tới AC, nên không biết AC nào đã được test.
- File test, ma trận truy vết có tiêu đề nhưng rỗng.
