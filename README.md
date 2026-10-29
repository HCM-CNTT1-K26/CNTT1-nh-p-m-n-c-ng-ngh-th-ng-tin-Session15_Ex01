# CNTT1-nh-p-m-n-c-ng-ngh-th-ng-tin-Session15_Ex01

### 1. Sơ đồ luồng dữ liệu & Xử lý xung đột

* **Luồng dữ liệu:** Bấm `Ctrl + S` ➔ Lưu xuống thư mục Local Sync (SSD) ➔ Đồng thời ghi đệm vào Offline Cache cục bộ.
* *Có mạng:* Tiến trình nền tự đẩy file lên Cloud ngay lập tức.
* *Mất mạng/Sập nguồn:* Dữ liệu nằm an toàn trong hàng đợi local, tự động đồng bộ tiếp khi có mạng trở lại, không mất một byte nào.


* **Xử lý xung đột (Version Conflict):** Khi hai người sửa cùng lúc, hệ thống không ghi đè mất dữ liệu mà tự sinh ra một file độc lập (ví dụ: `file_conflict_mayA.ext`). Cả nhóm chỉ cần mở ra đối chiếu và gộp lại.

---

### 2. Quy trình thiết lập 3 bước cho Designer

1. **Trỏ thư mục làm việc lên Cloud Drive:** Cài ứng dụng (OneDrive/Google Drive), ghim chế độ *Always keep on this device* để vừa chạy mượt trên SSD vừa đồng bộ ngầm thời gian thực.
2. **Bật bộ đệm ngoại tuyến (Offline Caches):** Đảm bảo khi sập nguồn đột ngột hoặc rớt mạng giữa chừng, file tạm vẫn nằm an toàn trong ổ cứng để chờ đẩy lên mây.
3. **Cấu hình Version History:** Chỉnh thời gian lưu lịch sử file ít nhất 30–90 ngày trên Cloud để khi file bị hỏng, chỉ cần vài click là "quay ngược thời gian" lấy lại bản ổn định.
