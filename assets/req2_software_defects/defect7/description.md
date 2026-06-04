# Lỗi 7: IRS — Rò rỉ 120.000 Hồ sơ Thuế (Tháng 9/2022)

* **Nguồn tham khảo:** [VnExpress](https://vnexpress.net/co-quan-thue-my-lo-thong-tin-cua-120-000-nguoi-4507021.html)
* **Mô tả lỗi:** IRS (Cơ quan Thuế Mỹ) vô tình tiết lộ một tập con dữ liệu từ 120.000 hồ sơ khai thuế do 'lỗi lập trình' trong hệ thống xử lý khi deploy code mới. Báo cáo gửi Quốc hội xác nhận dữ liệu thuế bị hiển thị công khai trên web dưới định dạng tệp tải về.
* **Độ nghiêm trọng (Severity - ISTQB):** High (Cao). Rò rỉ dữ liệu chính phủ diện rộng từ lỗi phần mềm — đe dọa niềm tin vào cơ quan thuế và có thể tạo điều kiện cho gian lận danh tính quy mô lớn.
* **Hậu quả:** Thông tin tài chính nhạy cảm của hàng chục nghìn công dân Mỹ bị lộ. Điều tra Quốc hội, vi phạm nghiêm trọng các quy định bảo mật liên bang (IRC § 6103).
* **Giải pháp khắc phục:** IRS vá lỗi lập trình liên quan; thông báo cho những người bị ảnh hưởng; tăng cường audit code review cho các hệ thống xử lý dữ liệu nhạy cảm; áp dụng data masking trước khi output.
* **Nhận diện AI Ảo giác / Thiên vị:** AI thường mô tả sự cố IRS mà không phân biệt rõ đây là lỗi vô ý (accidental disclosure) chứ không phải breach bởi bên ngoài. AI có xu hướng thêm chi tiết không có căn cứ về 'loại lỗi lập trình cụ thể' (như buffer overflow hay SQL injection) trong khi IRS chỉ công bố đây là 'programming error' — AI đang hallucinate về bản chất kỹ thuật của lỗi.
