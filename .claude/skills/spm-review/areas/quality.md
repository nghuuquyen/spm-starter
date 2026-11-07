# Review: Quality

Đọc: `docs/09-quality/quality-plan.md`, `docs/09-quality/test-results/`, `docs/06-acceptance/test-scenarios.md` (hoặc vị trí mục lục chỉ tới).

## Vì sao quan trọng

QA giúp lỗi không xảy ra, QC giúp phát hiện lỗi trước khi khách thấy. Definition of Done chung giúp cả nhóm hiểu "xong" giống nhau. Không có mức độ lỗi và điều kiện release thì không ai dám nói khi nào được bàn giao.

## Chuẩn yêu cầu

QA, QC, Definition of Done chung, mức độ lỗi, điều kiện release, kết quả test của milestone thực hiện. Có regression test trước khi bàn giao.

## Mục tiêu chất lượng

- Chung chung: nói chung về QA và QC.
- Cụ thể: có QA, QC, Definition of Done và tiêu chí kiểm tra được.
- Dùng được ngay: có xử lý lỗi theo mức độ, điều kiện release và bằng chứng đã áp dụng ở milestone thực hiện.

## Các bước kiểm

1. QA: những hoạt động phòng ngừa cụ thể nào (review, checklist, cổng chất lượng), ai làm, khi nào?
2. QC: những loại test nào, ai test, dùng kịch bản `TS-xx` nào? Có regression test trước khi bàn giao không?
3. Definition of Done: là danh sách kiểm được (có/không), hay câu chung? Chỉ có **một** DoD chung, hay mỗi tài liệu một kiểu?
4. Mức độ lỗi: định nghĩa từng mức, thời hạn xử lý, ai quyết. Cả repo dùng **một** thang mức độ lỗi hay mỗi file một thang?
5. Điều kiện release: những điều kiện cụ thể nào (số lỗi theo mức, test đã chạy) thì được bàn giao?
6. **Milestone thực hiện:** có kết quả test chạy thật (commit, TS đã chạy, đạt/không đạt, bug tạo ra) trong `test-results/` không? Có bằng chứng QA đã áp dụng (PR có review, checklist DoD) không?
7. Hồ sơ test có trong repo không, hay để ở nơi khác mà mục lục không chỉ tới?

## Câu hỏi để nhóm tự trả lời

- Trước release còn một lỗi mức cao, quy trình của nhóm nói gì: hoãn, release kèm cảnh báo, hay sửa nóng? Ai quyết?
- Một task được coi là xong khi nào? Cả nhóm có trả lời giống nhau không?

## Lỗi hay gặp

- Kế hoạch chất lượng có đủ mục nhưng không có bằng chứng áp dụng.
- Nhiều thang mức độ lỗi khác nhau ở các file khác nhau.
- Hai nơi định nghĩa DoD khác nhau.
- Kết quả test để ngoài repo.
- File kịch bản test rỗng.
