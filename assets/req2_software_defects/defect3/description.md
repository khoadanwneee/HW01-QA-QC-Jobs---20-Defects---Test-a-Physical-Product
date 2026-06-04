# Lỗi 3: FAA NOTAM System — Nationwide Ground Stop (Tháng 1/2023)

* **Nguồn tham khảo:** [Wikipedia](https://en.wikipedia.org/wiki/2023_FAA_system_outage)
* **Mô tả lỗi:** Nhân viên contractor vô tình xóa file trong quá trình đồng bộ hóa giữa database chính và backup của hệ thống NOTAM (Notice to Air Missions) — hệ thống thông báo an toàn bay có lỗi phần mềm từ thập niên 1990. Không có cơ chế rollback tự động đủ nhanh.
* **Độ nghiêm trọng (Severity - ISTQB):** Critical (Nguy kịch). Không có thương vong nhưng lộ rõ mức độ mong manh của hạ tầng không phận quốc gia Mỹ. FAA đã biết về tình trạng lỗi thời nhưng thiếu ngân sách/thứ tự ưu tiên.
* **Hậu quả:** Lần đầu tiên kể từ 11/9/2001, toàn bộ chuyến bay nội địa Mỹ bị dừng (ground stop). Hơn 11.000 chuyến bị ảnh hưởng. Thiệt hại kinh tế hàng trăm triệu USD.
* **Giải pháp khắc phục:** FAA sửa chữa ngay lập tức (khôi phục trong ~12 giờ); cam kết nâng cấp NOTAM sang hệ thống hiện đại. Quốc hội phân bổ 29,4 triệu USD cho Aeronautical Information Management Program.
* **Nhận diện AI Ảo giác / Thiên vị:** AI thường mô tả sự cố này như 'lỗi con người đơn giản' (accidental deletion), bỏ qua yếu tố hệ thống: NOTAM không có undo/versioning cấp enterprise, cơ chế sync thiếu atomic transaction. Đây là thiên vị quy kết (attribution bias) — AI đổ lỗi cho cá nhân thay vì thừa nhận lỗi thiết kế hệ thống sâu xa hơn. AI đôi khi còn ảo giác rằng FAA đã 'hoàn tất nâng cấp' sau vụ việc, trong khi Quốc hội vẫn đang tranh luận ngân sách đến năm 2025.
