# 📊 BÀI THUYẾT TRÌNH TRỰC QUAN HÓA DỮ LIỆU
### Dựa trên tác phẩm *Hands-On Data Visualization* (Jack Dougherty & Ilya Ilyankou)

Bộ slide thuyết trình chuyên đề gồm **88 slide** được thiết kế theo phong cách tối giản cao cấp (Modern Minimalist Beige & Deep Indigo Navy Theme), chuẩn hóa lề, cố định vị trí đề mục và tối ưu hóa cho 4 người thuyết trình.

---

## 👥 Phân Chia Vai Trò & Cấu Trúc Đề Tài

| Phần | Người trình bày | Nội dung chuyên đề | File LaTeX | File PDF |
| :--- | :---: | :--- | :--- | :--- |
| **Phần 1** | **Người 1** | **Nền tảng Dữ liệu:** Săn tìm, làm sạch dữ liệu bẩn và chuẩn hóa (Chương 3, 4, 5) — 27 slides | [`presentation_part1.tex`](presentation_part1.tex) | [`presentation_part1.pdf`](presentation_part1.pdf) |
| **Phần 2** | **Người 2** | **Trực quan hóa Biểu đồ:** Nguyên lý thiết kế, quy tắc gốc 0 & tổng 100%, 6 nhóm biểu đồ (Chương 6) — 12 slides | [`presentation_part2.tex`](presentation_part2.tex) | [`presentation_part2.pdf`](presentation_part2.pdf) |
| **Phần 3** | **Người 3** | **Trực quan hóa Không gian:** Bản chất dữ liệu địa lý, lớp nền Raster/Vector, bản đồ Choropleth & chuẩn hóa (Chương 7) — 10 slides | [`presentation_part3.tex`](presentation_part3.tex) | [`presentation_part3.pdf`](presentation_part3.pdf) |
| **Phần 4** | **Người 4** | **Đạo đức & Kể chuyện:** Phát hiện lừa dối, giảm định kiến, Cartogram, công thức Tell-Show-Why (Chương 14, 15) — 11 slides | [`presentation_part4.tex`](presentation_part4.tex) | [`presentation_part4.pdf`](presentation_part4.pdf) |
| **Master** | **Cả nhóm** | **Toàn bộ bài báo cáo tổng hợp (88 trang)** | [`presentation.tex`](presentation.tex) | [`presentation.pdf`](presentation.pdf) |

- **Bản Marp Markdown đồng bộ:** [`presentation.md`](presentation.md)

---

## 🎨 Nhận Diện Thiết Kế (Visual Identity)

- **Màu nền (Background):** Kem Be ấm `#F3EBE1` (RGB: 243, 235, 225)
- **Màu chủ đạo (Primary & Text):** Xanh Navy đậm `#262E5B` (RGB: 38, 46, 91)
- **Màu phụ (Muted Text):** `#555F8C`
- **Dải nhận diện bên phải:** Thanh sọc đứng Navy với 2 góc trong bo tròn mềm mại (`rounded corners=16pt`)
- **Badge / Callout:** Thẻ Pill Badge bo viền tròn và hộp Callout nền be sẫm viền navy sang trọng.

---

## ⚙️ Hướng Dẫn Biên Dịch & Chỉnh Sửa Dành Cho Thành Viên Nhóm

### Cách 1: Sử dụng LaTeX (Khuyến nghị để có slide chuẩn nhất)
Cần cài đặt TeX Live / MiKTeX với trình biên dịch **XeLaTeX** (để render font chữ Segoe UI tiếng Việt chuẩn xác):

```bash
# Biên dịch file Master toàn nhóm:
xelatex -interaction=nonstopmode presentation.tex
xelatex -interaction=nonstopmode presentation.tex   # Chạy lần 2 để cố định tọa độ TikZ

# Biên dịch từng phần riêng lẻ:
xelatex -interaction=nonstopmode presentation_part1.tex
xelatex -interaction=nonstopmode presentation_part2.tex
xelatex -interaction=nonstopmode presentation_part3.tex
xelatex -interaction=nonstopmode presentation_part4.tex
```

### Cách 2: Sử dụng Marp Markdown
Cài đặt extension **Marp for VS Code** để chỉnh sửa trực quan file `presentation.md` và xuất ra HTML/PDF/PPTX tùy nhu cầu.

---

## 📁 Thư Mục Hình Ảnh

Tất cả hình ảnh minh họa trích xuất từ sách nằm trong thư mục [`images/`](images/). Khi thêm hình ảnh mới, hãy lưu vào thư mục này và gọi lệnh:
```latex
\includegraphics[width=\textwidth, height=0.45\textheight, keepaspectratio]{images/ten_hinh_anh.png}
```
