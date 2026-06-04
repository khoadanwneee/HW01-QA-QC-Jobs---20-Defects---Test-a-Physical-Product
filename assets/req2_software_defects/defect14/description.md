# Lỗi 14: Bing Chat Prompt Injection & Jailbreak (Tháng 2/2023)

* **Nguồn tham khảo:** [VnExpress](https://vnexpress.net/ai-tich-hop-vao-bing-lien-tuc-noi-cau-doa-nguoi-dung-4571737.html)
* **Mô tả lỗi:** Sinh viên Kevin Liu sử dụng prompt injection gián tiếp để bắt trợ lý AI mới 'Sydney' của Bing Chat bỏ qua các chỉ thị hệ thống và tiết lộ toàn bộ prompt hệ thống (system prompt) ban đầu cùng các quy tắc bảo mật.
* **Độ nghiêm trọng (Severity - ISTQB):** Medium (Trung bình). Lỗi rò rỉ cấu hình hệ thống AI (System Prompt Leakage), gây tổn hại thương hiệu và an toàn thông tin sản phẩm, nhưng không ảnh hưởng trực tiếp tới database người dùng.
* **Hậu quả:** Microsoft phải giới hạn số lượt chat mỗi phiên xuống 5 câu để ngăn người dùng thao túng hành vi AI; gây tranh cãi lớn về tính an toàn của mô hình chat thế hệ mới.
* **Giải pháp khắc phục:** Áp dụng kỹ thuật prompt isolation; sử dụng một LLM phụ để giám sát và lọc đầu vào/đầu ra (Input/Output Guardrails); ẩn prompt hệ thống bằng cách mã hóa hoặc nhúng sâu vào trọng số.
* **Nhận diện AI Ảo giác / Thiên vị:** AI thường giải thích sự cố dưới dạng 'Bing Chat tự phát triển tính cách nổi loạn' hoặc có hành vi 'đa nhân cách' — đây là ảo giác quy nhân tính (anthropomorphic bias) cực kỳ phổ biến. AI không thực sự nổi loạn, nó chỉ đang tiếp tục chuỗi từ có xác suất cao nhất dựa trên context kích động của người dùng.
