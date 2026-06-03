# NHẬT KÝ PROMPT (PROMPT LOG)

_Tài liệu này ghi lại các câu lệnh (prompts) thực tế và quan trọng nhất được sử dụng trong phiên làm việc để phân tích yêu cầu, tái cấu trúc thư mục và thiết lập môi trường kiểm thử cho bài tập **HW01-AI**._

---

## # 20260603 | 21:48 | Gemini 3.5 Flash | Phân tích yêu cầu bài tập & Đánh giá cấu trúc thư mục hiện tại

- **Ngày thực hiện:** 03/06/2026
- **Giờ thực hiện:** 21:48
- **Model sử dụng:** Gemini 3.5 Flash
- **Mục đích:** Phân tích chi tiết nội dung học thuật, quy định kỹ thuật từ `Requirements.pdf` và `Policy.pdf`, đồng thời rà soát cấu trúc thư mục hiện tại của sinh viên xem đã đáp ứng đủ yêu cầu bài tập và quy chế chống gian lận chưa.
- **Nội dung Prompt:**

```text
dựa theo Requirements.pdf và Policy.pdf phân tích và chỉ ra yêu cầu của từng requirements. Sau đó kiểm tra cấu trúc folder của tui đã đáp ứng được những requirements đó chưa, nếu chưa thì đề xuất cải tiến
```

---

## # 20260603 | 22:05 | Gemini 3.5 Flash | Tái cấu trúc thư mục dự án và thiết lập file Excel Test Case Checklist

- **Ngày thực hiện:** 03/06/2026
- **Giờ thực hiện:** 22:05
- **Model sử dụng:** Gemini 3.5 Flash
- **Mục đích:** Tiến hành tái cấu trúc lại toàn bộ các thư mục assets theo chuẩn ngắn gọn (kebab-case), khởi tạo các file cam kết AI trống trong `ai_declarations/`, dựng khung báo cáo chính `reports/main_report.md` và tạo file Excel `spreadsheet/test_cases_checklist.xlsx` chứa sẵn 15 dòng test cases mẫu với các cột thông tin yêu cầu.
- **Nội dung Prompt:**

```text
refactor lại theo cấu trúc đề xuất và ghi testcase checklist theo những field phía trên: No. | Test Case ID | Test Type | Requirement Name | Build/Release | Test case name/Objective | Precondition | Test steps | Test Data | Expected Result
```

---

## # 20260603 | 23:29 | Gemini 3.5 Flash | Khởi tạo file nhật ký prompt và đồng bộ hóa báo cáo

- **Ngày thực hiện:** 03/06/2026
- **Giờ thực hiện:** 23:29
- **Model sử dụng:** Gemini 3.5 Flash
- **Mục đích:** Khởi tạo file nhật ký prompt `prompt_log.md` trong thư mục `assets/prompt_logs/` và cập nhật lại liên kết phụ lục cuối báo cáo chính `main_report.md` để đồng bộ toàn bộ tài liệu.
- **Nội dung Prompt:**

```text
cập nhập lại những prompt quan trọng và ảnh hưởng vào prompt_logs/ với định dạng requirements đã yêu cầu
```
