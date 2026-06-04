# Lỗi 20: GitHub Actions OIDC Trust Policy Misconfiguration (Tháng 4/2023)

* **Nguồn tham khảo:** [GitHub Docs](https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/about-security-hardening-with-openid-connect)
* **Mô tả lỗi:** Việc thiết lập các chính sách tin cậy OIDC (OpenID Connect) quá lỏng lẻo giữa GitHub Actions và các nhà cung cấp đám mây (như AWS IAM), cho phép bất kỳ quy trình làm việc (workflow) nào thuộc bất kỳ kho chứa (repository) nào của tổ chức đều có thể giả mạo và yêu cầu cấp quyền truy cập tài nguyên đám mây nhạy cảm.
* **Độ nghiêm trọng (Severity - ISTQB):** High (Cao). Lỗi cấu hình bảo mật tích hợp CI/CD lỏng lẻo (Configuration Defect), tạo điều kiện cho việc leo thang đặc quyền từ các tài khoản lập trình viên hoặc kho chứa ít quan trọng.
* **Hậu quả:** Kẻ tấn công có thể lợi dụng tài khoản GitHub Actions của một repository công khai bất kỳ để chiếm quyền kiểm soát (Assume Role) và can thiệp trái phép vào hạ tầng đám mây AWS/Azure của doanh nghiệp.
* **Giải pháp khắc phục:** Cấu hình chính sách tin cậy OIDC chặt chẽ bằng cách kiểm tra bắt buộc claim repository (ví dụ: repo:my-org/my-repo) và nhánh phát triển cụ thể thay vì chỉ kiểm tra claim tổ chức chung chung.
* **Nhận diện AI Ảo giác / Thiên vị:** AI thường có thiên vị về nền tảng (platform bias), quy kết đây là 'lỗ hổng bảo mật trong chính giao thức OIDC của GitHub Actions' thay vì làm rõ đây là lỗi cấu hình thiếu chặt chẽ (misconfiguration) từ phía quản trị viên đám mây của doanh nghiệp.
