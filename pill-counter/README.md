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

## 📱 Mở trên iPhone (chỉ 1 file, KHÔNG cần internet, KHÔNG cần GitHub)

App chỉ gồm **1 file `index.html`**. Mở file đó lên là chạy. Cách đưa vào iPhone:

**Cách 1 — Lưu vào Files rồi mở:**
1. Nhận file `index.html` (qua AirDrop, Zalo, email, Tin nhắn...).
2. Bấm **Lưu vào “Tệp” (Files)** → chọn “Trên iPhone của tôi”.
3. Mở app **Tệp (Files)** → bấm vào `index.html` → app chạy ngay.

**Cách 2 — Mở bằng Safari (mượt nhất):**
1. Trong app **Tệp**, nhấn giữ `index.html` → **Chia sẻ** → chọn **Safari** (hoặc “Mở trong…”).
2. Để dùng lại nhanh: trong Safari bấm **Chia sẻ → Thêm vào MH chính (Add to Home Screen)** → có icon như 1 app thật trên màn hình.

> Sau khi mở lần đầu, app dùng được **offline hoàn toàn**, không gửi ảnh đi đâu.

## 🚀 Các bước dùng
1. Bấm **Chụp ảnh** hoặc **Chọn ảnh**.
2. Bấm **🤖 Đếm tự động**.
3. Chạm vào chỗ thiếu để **thêm chấm**, chạm vào chấm thừa để **xóa** → số tổng cập nhật tức thì.

## 🎯 Mẹo để đếm chính xác
- Đặt thuốc trên **nền màu trơn, tương phản** (viên trắng → nền tối, và ngược lại).
- **Trải đều**, hạn chế viên chồng lên nhau.
- Chụp **từ trên xuống**, đủ sáng, tránh bóng đổ.
- Nếu AI đếm dư/thiếu nhiều: chỉnh **Kích thước viên** cho khớp rồi bấm “Đếm tự động” lại.

## 🛠️ Công nghệ
HTML + JavaScript thuần (Canvas API). Không thư viện ngoài, không backend.
