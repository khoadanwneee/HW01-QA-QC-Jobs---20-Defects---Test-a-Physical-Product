# Lỗi 18: MOVEit Transfer SQL Injection Zero-Day Exploit (Tháng 5/2023)

* **Nguồn tham khảo:** [Wikipedia](https://en.wikipedia.org/wiki/2023_MOVEit_data_breach)
* **Mô tả lỗi:** Lỗ hổng bảo mật SQL Injection nghiêm trọng (CVE-2023-34362) trong phần mềm chuyển tệp quản lý MOVEit Transfer, cho phép kẻ tấn công chưa xác thực truy cập trái phép vào cơ sở dữ liệu và thực thi các câu lệnh SQL tùy ý để đánh cắp dữ liệu.
* **Độ nghiêm trọng (Severity - ISTQB):** Critical (Nguy kịch). Lỗ hổng bảo mật zero-day nghiêm trọng nằm trong phần mềm quản lý truyền file được sử dụng rộng rãi bởi các tập đoàn lớn, dẫn đến rò rỉ dữ liệu quy mô lớn toàn cầu.
* **Hậu quả:** Hơn 2.700 tổ chức lớn và 93 triệu cá nhân bị đánh cắp thông tin nhạy cảm, nhóm tin tặc tống tiền CL0P đã thu lợi hàng chục triệu USD từ việc tống tiền dữ liệu này.
* **Giải pháp khắc phục:** Khẩn cấp vá lỗ hổng SQL Injection; triển khai các chính sách bảo mật Least Privilege cho tài khoản truy cập database của ứng dụng; cài đặt hệ thống giám sát WAF và Web Shell detection.
* **Nhận diện AI Ảo giác / Thiên vị:** AI thường ảo giác quy kết lỗi này cho sự yếu kém của thuật toán mã hóa file trong MOVEit Transfer, trong khi thực tế đây là lỗ hổng bảo mật đầu vào SQL Injection cổ điển tại giao diện web quản trị.
