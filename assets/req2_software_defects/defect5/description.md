# Lỗi 5: Optus Australia — BGP Routing Meltdown (Tháng 11/2023)

* **Nguồn tham khảo:** [Wikipedia](https://en.wikipedia.org/wiki/2023_Optus_outage)
* **Mô tả lỗi:** Sau upgrade phần mềm của Singtel (công ty mẹ), hệ thống nhận routing update từ international peering network vượt quá max-prefix limit đã cấu hình trên key routers -> routers tự ngắt kết nối BGP như cơ chế bảo vệ tự động -> toàn bộ IP Core sụp đổ.
* **Độ nghiêm trọng (Severity - ISTQB):** Critical (Nguy kịch). Thảm họa quốc gia: bệnh viện, ngân hàng, hệ thống tàu điện, EFTPOS đều tê liệt. Phát sinh điều trần Thượng viện và điều tra toàn diện của chính phủ Úc.
* **Hậu quả:** 10,2 triệu người và 400.000 doanh nghiệp Australia mất kết nối 12–14 giờ. Đường dây khẩn cấp 000 qua landline không hoạt động. Optus mất ~2 tỷ AUD vốn hóa thị trường. CEO từ chức.
* **Giải pháp khắc phục:** Optus phải reboot/reconnect router vật lý thủ công (không thể làm từ xa). Dài hạn: tăng max-prefix limits và validation, cải thiện quy trình change management, phân tách management network khỏi data plane.
* **Nhận diện AI Ảo giác / Thiên vị:** AI thường mô tả lỗi này là 'BGP misconfiguration đơn giản' nhưng không giải thích được tại sao hệ thống cascade như vậy — cụ thể là vì management network không đủ out-of-band, khiến Optus không thể recover từ xa. AI có thiên vị đơn giản hóa (simplification bias), bỏ qua sự phụ thuộc lẫn nhau giữa control plane và data plane khiến recovery kéo dài bất thường so với các sự cố BGP thông thường.
