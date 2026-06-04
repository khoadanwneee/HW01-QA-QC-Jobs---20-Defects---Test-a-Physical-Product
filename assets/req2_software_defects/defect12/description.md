# Lỗi 12: Air Canada Chatbot Hallucination (Tháng 2/2024)

* **Nguồn tham khảo:** [CBC News](https://www.cbc.ca/news/canada/british-columbia/air-canada-chatbot-lawsuit-1.7116416)
* **Mô tả lỗi:** Chatbot hỗ trợ khách hàng của Air Canada đưa ra thông tin sai lệch về chính sách hoàn tiền vé cho người đi đám tang (bereavement fare), khuyên khách hàng mua vé trước rồi xin hoàn tiền sau (trái quy định thực tế là phải xin trước).
* **Độ nghiêm trọng (Severity - ISTQB):** High (Cao). Lỗi trực tiếp ảnh hưởng đến quy trình tài chính và pháp lý của công ty, thiết lập tiền lệ pháp lý quan trọng rằng công ty phải chịu trách nhiệm cho thông tin do AI tự sinh.
* **Hậu quả:** Tòa án Small Claims Court tại British Columbia phán quyết Air Canada phải bồi thường chênh lệch giá vé cho khách hàng. Thiệt hại uy tín thương hiệu lớn.
* **Giải pháp khắc phục:** Áp dụng kiểm thử biên (boundary testing) chặt chẽ cho chatbot; triển khai guardrails chặn chatbot tự sinh thông tin chính sách tài chính nhạy cảm và chuyển sang cho người thật.
* **Nhận diện AI Ảo giác / Thiên vị:** AI thường ảo giác quy kết lỗi này cho sự cố tích hợp API của OpenAI bị lỗi kết nối hoặc lỗi dịch vụ từ bên thứ ba, trong khi thực tế lỗi nằm ở cấu hình prompt hệ thống lỏng lẻo của đội ngũ kỹ thuật phát triển dịch vụ chatbot của Air Canada.
