# PrintMerge v3.1

Công cụ xuất hàng loạt **thiệp mời** và **giấy chứng nhận** từ ảnh template + file Excel, chạy hoàn toàn trên trình duyệt — không cần cài phần mềm.

---

## Tính năng chính

- **Hai chế độ**: Thiệp mời (Invitation) và Giấy chứng nhận (Certificate)
- **Merge dữ liệu**: Chèn thông tin từng người vào ảnh template tự động
- **Xuất hàng loạt**: Tạo file ảnh riêng cho từng người trong danh sách
- **Không cần server**: Mọi xử lý diễn ra trên trình duyệt của người dùng

---

## Cách sử dụng

### Bước 1 — Tệp đầu vào

| Tệp | Mô tả |
|-----|-------|
| **Ảnh template** | File PNG/JPG export từ PSD/Canva làm nền chung |
| **File Excel** | `.xlsx`, `.xls` hoặc `.csv` chứa danh sách người nhận |
| **Ảnh học sinh** *(chỉ chế độ Giấy CN)* | Nhiều file ảnh, tên file phải khớp với cột trong Excel |

### Bước 2 — Cấu hình trường văn bản

1. Nhấn **+ Thêm trường văn bản**
2. Nhập mẫu nội dung bằng cú pháp `{Tên_cột}` — ví dụ: `{Họ và tên}`  
   hoặc click vào chip cột bên trên để chèn tự động
3. Chỉnh font chữ, cỡ chữ, màu sắc, căn lề, in đậm/nghiêng
4. Nhấn **🎯 Chọn vị trí** → click lên ảnh xem trước để đặt toạ độ chính xác

### Bước 3 — Tên file xuất ra

- Nhập mẫu tên file bằng `{Tên_cột}`, ví dụ: `{Họ và tên}_{Chức vụ}`
- Tuỳ chọn: bỏ dấu tiếng Việt, thay khoảng trắng bằng `_`

### Bước 4 — Xuất file

| Nút | Mô tả |
|-----|-------|
| **📂 Xuất thẳng vào thư mục** | Dùng File System Access API — không bị Windows chặn (Chrome/Edge) |
| **🗜️ Xuất ZIP** | Phương án dự phòng cho mọi trình duyệt |

---

## Định dạng file xuất

- **JPEG** — file nhỏ hơn, chất lượng tuỳ chỉnh (70–100%)
- **PNG** — chất lượng cao, file lớn hơn

---

## Font chữ hỗ trợ

| Font | Tiếng Việt |
|------|-----------|
| Arial, Times New Roman | ✅ Đầy đủ |
| Caveat, Kalam | ✅ Tốt |
| Dancing Script, Great Vibes, Pacifico, ... | ⚠️ Một phần |

---

## Yêu cầu kỹ thuật

- Trình duyệt: **Chrome** hoặc **Edge** phiên bản mới (khuyên dùng)
- Tính năng "Xuất thẳng vào thư mục" yêu cầu Chrome/Edge (File System Access API)
- Không yêu cầu kết nối internet sau khi trang đã tải xong

---

## Cấu trúc Excel mẫu

| STT | Ghi trong thiệp trước tên | Họ và tên | Giới tính | Chức vụ |
|-----|--------------------------|-----------|-----------|---------|
| 1 | Ông | Nguyễn Văn A | Nam | Phụ huynh |
| 2 | Bà | Trần Thị B | Nữ | Phụ huynh |
