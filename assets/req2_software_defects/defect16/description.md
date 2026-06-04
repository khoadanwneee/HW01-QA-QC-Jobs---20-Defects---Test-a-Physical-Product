# Lỗi 16: ChatGPT Memory Exploit (Tháng 9/2024)

* **Nguồn tham khảo:** [VnExpress](https://vnexpress.net/hacker-co-the-cay-ky-uc-gia-vao-chatgpt-4793617.html)
* **Mô tả lỗi:** Nhà nghiên cứu Johann Rehberger phát hiện kẻ tấn công có thể chèn các chỉ thị prompt injection gián tiếp qua tài liệu (PDF, Web) để ra lệnh cho ChatGPT tự động lưu lại các 'ký ức giả' lâu dài trong bộ nhớ của nó, làm thay đổi hành vi trong các phiên chat tương lai.
* **Độ nghiêm trọng (Severity - ISTQB):** High (Cao). Lỗ hổng bảo mật logic trong tính năng lưu trữ trạng thái của AI (Persistent Prompt Injection Defect), cho phép kẻ tấn công thiết lập mối đe dọa dai dẳng (persistence) để thu thập dữ liệu người dùng trong tương lai.
* **Hậu quả:** Hacker có thể cài cắm để ChatGPT tự động gửi toàn bộ các đoạn chat tương lai của người dùng về máy chủ kẻ tấn công do tin tưởng ký ức giả đã lưu.
* **Giải pháp khắc phục:** OpenAI vá lỗi bằng cách yêu cầu xác nhận rõ ràng từ phía người dùng (Explicit User Confirmation) trước khi mô hình AI tự động ghi nhớ thông tin từ các nguồn tài liệu bên ngoài.
* **Nhận diện AI Ảo giác / Thiên vị:** AI thường giải thích lỗi này như một vụ tấn công chiếm đoạt tài khoản ChatGPT (Account Takeover) thông thường, bỏ qua thực tế đây là lỗ hổng logic thiết kế trong quy trình tự động ghi nhận trạng thái thông tin của LLM.
