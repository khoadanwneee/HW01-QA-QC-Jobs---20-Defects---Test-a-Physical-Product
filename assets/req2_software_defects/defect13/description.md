# Lỗi 13: EchoLeak – Microsoft 365 Copilot Zero-Click Exploit (Tháng 6/2025)

* **Nguồn tham khảo:** [NIST NVD](https://nvd.nist.gov/vuln/detail/CVE-2025-32711)
* **Mô tả lỗi:** Lỗ hổng bảo mật nghiêm trọng (CVE-2025-32711) cho phép thực hiện zero-click prompt injection. Kẻ tấn công gửi email chứa prompt ẩn; khi M365 Copilot tự động quét email để tóm tắt, nó sẽ thực thi lệnh ẩn này để đánh cắp dữ liệu nhạy cảm của người dùng và gửi về máy chủ kẻ tấn công mà không cần người dùng click hay tương tác gì.
* **Độ nghiêm trọng (Severity - ISTQB):** Critical (Nguy kịch). Lỗ hổng zero-day nghiêm trọng trong hệ thống AI Agent tích hợp sâu vào dữ liệu doanh nghiệp, cho phép vượt qua hoàn toàn các cơ chế xác thực quyền truy cập thông tin và đánh cắp tài liệu tự động.
* **Hậu quả:** Nguy cơ rò rỉ thông tin doanh nghiệp nhạy cảm trên quy mô lớn, đe dọa lòng tin vào các trợ lý AI tự động hóa công việc.
* **Giải pháp khắc phục:** Microsoft vá lỗ hổng bằng cách phân tách nghiêm ngặt dữ liệu đầu vào (data channel) khỏi kênh chỉ thị (instruction channel); tăng cường lọc markdown và outbound requests từ AI agent.
* **Nhận diện AI Ảo giác / Thiên vị:** AI thường thiên vị các tài liệu quảng cáo của Microsoft, khẳng định rằng các tính năng bảo mật Purview có thể chặn đứng prompt injection, trong khi thực tế đây là lỗ hổng logic kiến trúc AI Agent không thể ngăn chặn hoàn toàn bằng các công cụ DLP truyền thống.
