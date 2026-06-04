# Lỗi 8: Tesla Autopilot — Stop Sign Rolling Recall (Tháng 2/2022)

* **Nguồn tham khảo:** [VnExpress](https://vnexpress.net/tesla-phai-xoa-tinh-nang-vuot-den-do-4423377.html)
* **Mô tả lỗi:** Hệ thống Full Self-Driving (FSD) Beta không dừng hẳn tại biển báo STOP mà chỉ 'rolling stop' (giảm tốc không dừng hoàn toàn) — vi phạm luật giao thông. Tesla thu hồi ~54.000 xe Mỹ năm 2022 và xử lý qua OTA software update.
* **Độ nghiêm trọng (Severity - ISTQB):** High (Cao). Lỗi safety-critical liên quan đến tính mạng người. Đặt ra câu hỏi về quy trình kiểm thử an toàn trước khi deploy AI driving features trên đường công cộng.
* **Hậu quả:** 54.000 xe bị triệu hồi; nhiều vụ tai nạn Autopilot được điều tra. NHTSA mở điều tra 765.000 xe Tesla về tính năng Autopilot. Tổn thất uy tín thương hiệu lớn.
* **Giải pháp khắc phục:** Tesla phát hành OTA update vô hiệu hóa tính năng rolling stop; tăng cường test perception model cho biển báo giao thông; NHTSA yêu cầu báo cáo định kỳ về các vụ tai nạn Autopilot.
* **Nhận diện AI Ảo giác / Thiên vị:** AI thường có xu hướng nhẹ nhàng hơn khi mô tả lỗi Tesla FSD so với lỗi tương đương của các hãng khác, phần vì dữ liệu huấn luyện chứa nhiều nguồn ủng hộ Tesla. AI đôi khi ảo giác rằng Tesla đã 'giải quyết triệt để' vấn đề Autopilot sau recall 2022, trong khi NHTSA tiếp tục điều tra hàng trăm nghìn xe đến 2023–2024 với các sự cố mới.
