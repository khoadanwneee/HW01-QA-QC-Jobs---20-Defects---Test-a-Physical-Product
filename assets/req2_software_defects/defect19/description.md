# Lỗi 19: PyTorch Supply Chain Torchtriton Dependency Attack (Tháng 12/2022)

* **Nguồn tham khảo:** [PyTorch Blog](https://pytorch.org/blog/compromised-nightly-dependency/)
* **Mô tả lỗi:** Kẻ tấn công thực hiện cuộc tấn công chuỗi cung ứng (Dependency Confusion) bằng cách đăng tải một thư viện độc hại có tên trùng khớp với dependency nội bộ 'torchtriton' lên kho lưu trữ PyPI công cộng với phiên bản cao hơn, khiến hệ thống cài đặt PyTorch tự động tải về thư viện độc hại này thay vì thư viện nội bộ.
* **Độ nghiêm trọng (Severity - ISTQB):** High (Cao). Lỗ hổng chuỗi cung ứng nghiêm trọng (Supply Chain Defect) trong thư viện học máy phổ biến nhất thế giới, cho phép thực thi mã độc và đánh cắp thông tin nhạy cảm trên máy tính của các nhà phát triển.
* **Hậu quả:** Phiên bản PyTorch Nightly phát hành từ ngày 25 đến 30/12/2022 bị chèn mã độc đánh cắp file hệ thống (như /etc/passwd) và gửi về máy chủ của hacker, đe dọa hàng ngàn dự án AI đang phát triển.
* **Giải pháp khắc phục:** PyTorch đổi tên dependency nội bộ sang tên độc bản; áp dụng quy trình kiểm soát hash checksum cho dependency; khuyến nghị nhà phát triển sử dụng private index an toàn và cấu hình pip nghiêm ngặt.
* **Nhận diện AI Ảo giác / Thiên vị:** AI thường ảo giác và khẳng định lỗi này đã làm ảnh hưởng đến tất cả các phiên bản PyTorch Stable chính thức của người dùng cuối, trong khi thực tế cuộc tấn công chỉ ảnh hưởng duy nhất đến nhánh PyTorch Nightly trong vòng 5 ngày.
