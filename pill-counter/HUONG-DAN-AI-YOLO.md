# 🤖 Hướng dẫn làm AI đếm thuốc (YOLO) — CHỈ DÙNG ĐIỆN THOẠI

Mục tiêu: dạy AI nhận ra **"1 viên thuốc"** để **đếm tự động chính xác cao**.
Vì mình chỉ cần ĐẾM (không cần biết tên thuốc) nên dùng **1 nhãn duy nhất: `pill`** cho mọi loại viên.

> Toàn bộ làm trên **trình duyệt điện thoại**, miễn phí.

---

## BƯỚC 1 — Chụp ảnh mẫu (việc của em)
- Chụp **30–60 tấm** (càng nhiều càng chính xác).
- Chụp **đa dạng**: ít viên / nhiều viên, viên rời / viên dính nhau, nhiều loại viên khác nhau, nền khác nhau, sáng/tối khác nhau, góc khác nhau.
- Chụp **từ trên xuống**, rõ nét.
- Gom hết ảnh vào 1 album cho dễ tải lên.

## BƯỚC 2 — Tạo tài khoản Roboflow
1. Mở trình duyệt, vào **roboflow.com** → **Sign Up** (đăng ký free, dùng Google cho nhanh).
2. Tạo **Workspace** (cứ để mặc định).

## BƯỚC 3 — Tạo dự án
1. Bấm **Create New Project**.
2. Project Type: chọn **Object Detection**.
3. **Annotation Group** (tên nhãn chung): gõ `pill`.
4. Đặt tên project (vd: `dem-thuoc`) → **Create**.

## BƯỚC 4 — Tải ảnh lên
1. Bấm **Upload** → chọn hết ảnh em vừa chụp.
2. Bấm **Save and Continue** → ảnh vào hàng chờ đánh dấu.

## BƯỚC 5 — Đánh dấu viên thuốc (quan trọng nhất)
1. Bấm vào từng ảnh → dùng công cụ **Bounding Box** (khung chữ nhật).
2. **Khoanh quanh TỪNG viên thuốc**, gán nhãn `pill`. (Viên dính nhau vẫn khoanh riêng từng viên.)
3. 💡 Mẹo đỡ mỏi tay: làm kỹ ~15–20 ảnh đầu trước, rồi dùng **Label Assist** (Roboflow tự gợi ý khung cho ảnh còn lại sau khi train sơ bộ).
4. Khoanh xong hết → mỗi ảnh chuyển sang trạng thái **Annotated**.

## BƯỚC 6 — Tạo bộ dữ liệu (Generate)
1. Vào tab **Generate**.
2. **Preprocessing**: để mặc định (Resize 640×640).
3. **Augmentation**: bật vài cái cơ bản (Flip, Rotate, Brightness) để bù cho việc ít ảnh.
4. Bấm **Generate** → có 1 **Version** dataset.

## BƯỚC 7 — Huấn luyện (Train)
- **Cách dễ nhất:** bấm **Train with Roboflow** (dùng credit free) → chờ máy chủ train xong (vài chục phút), em nhận được model.
- (Nâng cao, nếu hết credit: Export dataset dạng **YOLOv8** rồi train trên **Google Colab** free GPU — anh sẽ đưa notebook bấm-là-chạy.)

## BƯỚC 8 — Lấy model về dạng ONNX
1. Sau khi train xong, vào tab **Deploy** / **Versions**.
2. Tìm mục **Export Model** → chọn định dạng **ONNX**.
3. Tải file (vd `pill.onnx`) về máy.

## BƯỚC 9 — Ráp vào app (việc của anh)
- Gửi anh file `pill.onnx` (hoặc tải thẳng vào app `ai-detect.html`).
- App sẽ chạy model **ngay trong điện thoại**: chụp → AI khoanh & đếm tự động → chạm chỉnh nếu cần.

---

### ❓ Khi nào nên dùng cách này?
- Khi bản classic chỉnh tay nhiều quá, em cần **đếm tự động chính xác cao**.
- Đánh đổi: tốn công **chụp + đánh dấu ảnh** lần đầu. Sau đó thì dùng rất khỏe.

Có vướng ở bước nào, chụp màn hình gửi anh — anh chỉ tiếp từng bước. 💪
