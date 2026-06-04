# Lỗi 6: Revolut — Payment Refund Logic Bug (Tháng 7/2023)

* **Nguồn tham khảo:** [VnExpress](https://vnexpress.net/loi-he-thong-khien-revolut-mat-20-trieu-usd-4627915.html)
* **Mô tả lỗi:** Sự khác biệt trong cách xử lý giao dịch bị từ chối giữa hệ thống Mỹ và Châu Âu khiến một số giao dịch bị declined nhưng vẫn được hoàn tiền từ quỹ của Revolut. Kẻ xấu phát hiện và rút tiền từ ATM trước khi lỗi được vá.
* **Độ nghiêm trọng (Severity - ISTQB):** High (Cao). Tổn thất tài chính trực tiếp lớn từ lỗi business logic, không phải hack. Lộ ra khoảng trống trong kiểm thử integration giữa hệ thống thanh toán đa vùng.
* **Hậu quả:** Hơn 20 triệu USD bị đánh cắp. Lỗi tồn tại từ 2021, chỉ được phát hiện năm 2022/2023 khi đối tác thông báo quỹ thiếu hụt.
* **Giải pháp khắc phục:** Vá logic xử lý refund; đồng bộ hóa quy trình declined transaction giữa US/EU systems; bổ sung anomaly detection cho các giao dịch ATM bất thường; audit toàn bộ cross-region payment flows.
* **Nhận diện AI Ảo giác / Thiên vị:** Khi mô tả vụ Revolut, AI thường nhầm lẫn giữa 'lỗi phần mềm bị khai thác' với 'bị hack/cyberattack' — hai điều hoàn toàn khác nhau về mặt pháp lý và bảo hiểm. Đây là thiên vị phân loại (categorization bias): AI hay gán nhãn mọi tổn thất tài chính kỹ thuật số là 'tấn công mạng,' làm sai lệch hiểu biết về trách nhiệm pháp lý và cách phòng ngừa thực sự (logic testing vs. security patching).
