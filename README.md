# 📚 TẬP SAN ĐIỆN TỬ 20/11/2026: LỜI CHÚC - NGHĨA NẶNG ƠN THẦY CÔ!
**Đơn vị:** Chi đoàn 12C4 — Đoàn trường THPT Thiệu Hóa  
**Ban biên tập & Thiết kế kỹ thuật:** Hoàng Thanh Long  

---

## ✨ 1. Giới thiệu dự án
Dự án nâng cấp toàn diện Tập san điện tử chào mừng Ngày Nhà giáo Việt Nam **20/11/2026** của **Chi đoàn 12C4 - Trường THPT Thiệu Hóa**, kết hợp 4 phong cách thiết kế hiện đại:
- **Liquid Glass UI:** Hiệu ứng kính mờ đa lớp, ánh sáng phản chiếu và nút điều khiển nổi hiện đại.
- **Vintage Yearbook & Digital Magazine:** Giấy màu kem cổ điển, khung ảnh Polaroid, băng dính Washi, chữ cái lớn đầu đoạn (Drop-cap), sổ nhật ký kẻ ngang.
- **3D Flipbook Engine:** Hiệu ứng lật sách 3D có chiều sâu, gáy sách, bóng đổ, độ cong trang giấy, âm thanh lật giấy tự nhiên (Web Audio API + WAV fallback).
- **YouTube IFrame Audio Player:** Tích hợp nhạc nền từ video `https://youtu.be/ciYlljR7BEM` (*Người Gieo Mầm Xanh*) với nút bật/tắt Liquid Glass kéo thả linh hoạt.

---

## 📁 2. Cấu trúc thư mục
```text
tap-san-20-11-12c4/
├── index.html                        # File giao diện chính (18 trang tập san hoàn chỉnh)
├── css/
│   └── style.css                     # Thiết kế Liquid Glass, Vintage Yearbook, Responsive & 3D Flipbook
├── js/
│   ├── flipbook.js                   # Bộ máy lật sách 3D, cảm ứng vuốt, âm thanh, mục lục, toàn màn hình
│   ├── music.js                      # Tích hợp YouTube IFrame API & nút nhạc nổi kéo thả
│   └── main.js                       # Khởi tạo ứng dụng, Lightbox xem ảnh, sửa mẫu trực tiếp & thêm lời chúc
├── assets/
│   ├── images/
│   │   ├── anh-tap-the-12c4.jpg      # Ảnh tập thể chính của lớp 12C4 (thay file trực tiếp không cần sửa JS)
│   │   ├── polaroid-1.jpg -> 6.jpg   # Các ảnh kỷ niệm trong Album & Góc Polaroid
│   ├── audio/
│   │   └── page-flip.wav             # Âm thanh lật trang giấy dự phòng
│   └── fonts/                        # Thư mục dự phòng cho font nội bộ
└── README.md                         # Tài liệu hướng dẫn chi tiết
```

---

## 💻 3. Hướng dẫn chạy trên máy tính
1. Giải nén file `tap-san-20-11-12c4-thpt-thieu-hoa.zip`.
2. **Cách 1 (Mở trực tiếp):** Nháy đúp vào file `index.html` để mở ngay trên trình duyệt (Chrome, Edge, Safari, Firefox).
3. **Cách 2 (Khuyên dùng để YouTube IFrame API hoạt động tối ưu nhất):**
   - Dùng tiện ích **Live Server** trên VS Code (nhấn chuột phải vào `index.html` -> *Open with Live Server*).
   - Hoặc mở Terminal / PowerShell tại thư mục dự án và chạy:
     ```bash
     python -m http.server 8080
     ```
     Sau đó truy cập `http://localhost:8080`.

---

## 🚀 4. Hướng dẫn tải lên GitHub & Triển khai (GitHub Pages / Render)

### Cập nhật lên kho lưu trữ `https://github.com/porccht/20-10`
```bash
git init
git remote add origin https://github.com/porccht/20-10.git
git add .
git commit -m "Upgrade 3D Flipbook Tap San 20/11/2026 - Chi doan 12C4 THPT Thieu Hoa"
git branch -M main
git push -u origin main --force
```

### Bật GitHub Pages
1. Vào trang GitHub của repository -> chọn tab **Settings** -> **Pages**.
2. Tại mục **Build and deployment**, phần **Source** chọn `Deploy from a branch`.
3. Chọn nhánh `main` và thư mục `/ (root)` -> nhấn **Save**.
4. Sau 1–2 phút, website sẽ hoạt động tại địa chỉ GitHub Pages của bạn.

### Triển khai trên Render (Static Site)
1. Đăng nhập [Render.com](https://render.com/) -> chọn **New +** -> **Static Site**.
2. Kết nối tới repository `porccht/20-10`.
3. Cấu hình:
   - **Build Command:** để trống
   - **Publish Directory:** `.`
4. Nhấn **Create Static Site**.

---

## 🖼️ 5. Hướng dẫn thay ảnh, đổi nhạc và chỉnh sửa nội dung
- **Thay ảnh tập thể 12C4:** Chép ảnh tập thể thật của lớp đè lên file `assets/images/anh-tap-the-12c4.jpg` (giữ nguyên tên file, không cần sửa bất kỳ dòng code nào).
- **Thay ảnh góc Polaroid:** Thay các file `polaroid-1.jpg` đến `polaroid-6.jpg` trong `assets/images/`.
- **Đổi bài nhạc YouTube khác:** Mở `js/main.js`, tìm dòng `new YouTubeMusicController('ciYlljR7BEM')` và thay mã ID video YouTube mong muốn.
- **Chỉnh sửa nội dung phỏng vấn thầy cô & câu chuyện:**
  - *Trực tiếp trên web:* Nhấn nút **✎ Sửa mẫu** trên thanh công cụ phía trên, nhấp vào khung phỏng vấn để gõ nội dung, sau đó nhấn **Lưu nội dung**.
  - *Cố định trong mã nguồn:* Mở `index.html`, tìm đến `data-page="9"` (Góc phỏng vấn thầy cô) và `data-page="10"` (Câu chuyện truyền cảm hứng) để điền thông tin chính thức.
