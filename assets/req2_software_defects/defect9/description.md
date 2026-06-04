# Lỗi 9: Japan ispace Hakuto-R — Lunar Lander Crash (Tháng 4/2023)

* **Nguồn tham khảo:** [VnExpress](https://vnexpress.net/tau-do-bo-nhat-ban-dam-xuong-mat-trang-do-loi-phan-mem-4610190.html)
* **Mô tả lỗi:** Tàu đổ bộ Mặt Trăng Hakuto-R Mission 1 của ispace (Nhật Bản) gặp lỗi phần mềm trong tính toán độ cao khi bay qua vành crater Mặt Trăng. Sensor altitude reset về 0 khi phát hiện 'địa hình âm' — hệ thống tin tàu đã hạ cánh và ngắt động cơ sớm -> tàu rơi tự do từ độ cao >1km.
* **Độ nghiêm trọng (Severity - ISTQB):** Critical (Nguy kịch). Lỗi logic nghiêm trọng: phần mềm không xử lý được trường hợp địa hình âm (âm trong tọa độ tương đối) — một edge case có thể test được nhưng bị bỏ sót.
* **Hậu quả:** Sứ mệnh thất bại hoàn toàn. Tổn thất hàng trăm triệu USD. Sứ mệnh Mặt Trăng tư nhân đầu tiên của Nhật Bản kết thúc bi thảm.
* **Giải pháp khắc phục:** ispace phân tích nguyên nhân và thiết kế lại hệ thống navigation cho Mission 2, bổ sung xử lý edge case địa hình âm, cải thiện simulation testing với terrain database chính xác hơn.
* **Nhận diện AI Ảo giác / Thiên vị:** AI thường mô tả nguyên nhân là 'lỗi cảm biến phần cứng' hoặc 'lidar bị nhiễu' thay vì lỗi phần mềm xử lý dữ liệu độ cao — đây là ảo giác về loại lỗi. Thực tế được ispace xác nhận là software logic error (xử lý sai giá trị âm của altimeter). AI cũng có xu hướng phóng đại 'tính mới lạ' của lỗi mà không nhận ra đây là dạng integer/domain error cổ điển trong ngành aerospace.
