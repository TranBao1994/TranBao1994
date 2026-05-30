# 💊 App Đếm Viên Thuốc (qua camera)

Web app chạy trên trình duyệt điện thoại để **đếm số lượng viên thuốc tây** qua ảnh chụp.
AI đếm tự động, sau đó bạn **chạm để thêm/bớt** cho đúng 100% (bán tự động).

## ✨ Tính năng
- 📷 Chụp ảnh trực tiếp bằng camera hoặc chọn ảnh có sẵn.
- 🤖 Đếm tự động bằng xử lý ảnh (Otsu threshold + distance transform + tìm tâm viên).
- ✍️ Chạm vào ảnh để **thêm chấm** (chỗ AI bỏ sót) hoặc **xóa chấm** (chỗ thừa).
- ↩︎ Hoàn tác, xóa hết.
- ⚙️ Tinh chỉnh: kích thước viên, độ nhạy, loại nền (tối/sáng/tự động).
- 🔌 Chạy hoàn toàn trên máy — **không cần internet, không gửi ảnh đi đâu** (riêng tư).

## 🚀 Cách dùng
1. Mở file `index.html` bằng trình duyệt trên điện thoại (Chrome/Safari).
2. Bấm **Chụp ảnh** hoặc **Chọn ảnh**.
3. Bấm **🤖 Đếm tự động**.
4. Chạm vào chỗ thiếu để thêm chấm, chạm vào chấm thừa để xóa → số tổng cập nhật tức thì.

### Mở online (gợi ý)
Bật **GitHub Pages** cho repo, rồi truy cập:
`https://<tên-github>.github.io/<repo>/pill-counter/`
là dùng được trên điện thoại mà không cần copy file.

## 🎯 Mẹo để đếm chính xác
- Đặt thuốc trên **nền màu trơn, tương phản** (viên trắng → nền tối, và ngược lại).
- **Trải đều**, hạn chế viên chồng lên nhau.
- Chụp **từ trên xuống**, đủ sáng, tránh bóng đổ.
- Nếu AI đếm dư/thiếu nhiều: chỉnh **Kích thước viên** cho khớp rồi bấm “Đếm tự động” lại.

## 🛠️ Công nghệ
HTML + JavaScript thuần (Canvas API). Không thư viện ngoài, không backend.
