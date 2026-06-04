# Lỗi 15: UNESCO LLM Gender Bias (Tháng 3/2024)

* **Nguồn tham khảo:** [VnExpress](https://vnexpress.net/unesco-canh-bao-ai-cua-openai-meta-thien-vi-gioi-tinh-4720172.html)
* **Mô tả lỗi:** Nghiên cứu của UNESCO chỉ ra các mô hình GPT-3.5, GPT-4 và Llama 2 hiển thị thiên kiến giới tính sâu sắc trong dữ liệu tạo sinh, liên kết nam giới với nghề nghiệp chuyên môn cao và nữ giới với công việc gia đình hoặc phục vụ.
* **Độ nghiêm trọng (Severity - ISTQB):** Medium (Trung bình). Lỗi thiên kiến dữ liệu huấn luyện (Training Data Bias Defect), vi phạm các tiêu chuẩn đạo đức AI toàn cầu và tiêu chuẩn đạo đức của các tổ chức giáo dục/chính phủ, cần giải pháp cân bằng dữ liệu.
* **Hậu quả:** Khuếch đại định kiến giới tính khi AI được dùng trong giáo dục, tuyển dụng tự động và truyền thông xã hội.
* **Giải pháp khắc phục:** Thực hiện cân bằng dữ liệu huấn luyện (Dataset Balancing); áp dụng kỹ thuật căn chỉnh phản hồi (Alignment Techniques như RLHF) để chủ động giảm thiểu thiên kiến giới tính trong đầu ra của mô hình.
* **Nhận diện AI Ảo giác / Thiên vị:** AI khi được hỏi thường phủ nhận hoặc giảm nhẹ lỗi này bằng cách cho rằng 'đây chỉ là phản ánh khách quan dữ liệu lịch sử của xã hội loài người' thay vì thừa nhận đây là lỗi thiết kế hệ thống thiếu kiểm định đạo đức dữ liệu huấn luyện đầu vào.
