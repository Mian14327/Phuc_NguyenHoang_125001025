# 🚀 AI Hub - Cổng Thông Tin & Thư Viện Công Cụ Trí Tuệ Nhân Tạo

> **Bài thi giữa kỳ môn:** Thiết kế Web  
> **Khoa:** Công nghệ Thông tin - Trường Đại học Lạc Hồng (LHU)  
> **Sinh viên thực hiện:** Nguyễn Hoàng Phúc - MSSV: 125001025  
> **Link GitHub Pages (Live Demo):** `https://mian14327.github.io/Phuc_NguyenHoang_125001025/`

---

## 📌 Giới Thiệu Dự Án
**AI Hub** là website một trang (Single Page Website) chuyên giới thiệu, tổng hợp và phân loại các công cụ Trí tuệ Nhân tạo (AI) đột phá nhất trên thế giới (ChatGPT, Midjourney, Claude, GitHub Copilot, Runway, Perplexity...).

Website được thiết kế hiện đại, chuyên nghiệp, responsive 3 cấp độ (Desktop, Tablet, Mobile) và xây dựng **100% bằng HTML5 và CSS3 thuần, hoàn toàn KHÔNG sử dụng JavaScript**, đáp ứng chuẩn mực kiến thức học phần Thiết kế Web.

---

## 🛠️ Tiêu Chuẩn Kỹ Thuật (Đáp ứng 100% tiêu chí thang điểm 10)

1. **Chuẩn Semantic HTML5 (2.0 điểm):**
   - Sử dụng chuẩn xác và đầy đủ các thẻ ngữ nghĩa: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`.
   - Tuyệt đối không lạm dụng thẻ `<div>` vô nghĩa. Mỗi công cụ AI và khối lợi ích là một `<article>` độc lập.
2. **Kỹ thuật CSS & CSS Variables (2.5 điểm):**
   - Khai báo hệ thống biến `:root` quản lý màu sắc, typography, khoảng cách, bo góc và bóng đổ.
   - Bảng màu hiện đại theo quy định: `#0F172A`, `#2563EB`, `#7C3AED`, `#F8FAFC`, `#FFFFFF`.
   - Bố cục kết hợp **CSS Flexbox** (Header, Navigation, Search box) và **CSS Grid** (Lưới 6 công cụ, khối lợi ích, footer).
   - Thiết kế Responsive hoàn chỉnh trên cả 3 loại thiết bị: Desktop, Tablet và Mobile.
3. **Hiệu ứng & Thư viện CSS (1.5 điểm):**
   - **Animate.css:** Hiệu ứng chuyển động cho tiêu đề Hero và nút CTA nổi bật.
   - **Hiệu ứng :hover & :focus tự viết bằng CSS:** Nâng card mượt mà (`translateY(-8px)`), đổ bóng mềm, viền focus-visible sắc nét chuẩn Accessibility.
   - **Menu di động thuần CSS:** Áp dụng kỹ thuật Checkbox Hack không cần JavaScript.
4. **Nhật ký Vibe Coding (3.0 điểm):**
   - File `PROMPT_LOG.md` theo chuẩn mẫu đề thi, trình bày đầy đủ các bước đối thoại, tinh chỉnh và xử lý vấn đề cùng AI.
5. **Quy chuẩn nộp bài & Git (1.0 điểm):**
   - Đặt tên Repository theo chuẩn: `Ten_Ho_MSSV`.
   - Kích hoạt GitHub Pages để giảng viên xem trực tiếp.

---

## 📂 Cấu Trúc Mã Nguồn

```text
├── index.html        # Trang giao diện chính chuẩn Semantic HTML5 (KHÔNG CÓ THẺ <SCRIPT>)
├── style.css         # Toàn bộ mã nguồn CSS3, biến CSS Variables và Responsive
├── PROMPT_LOG.md     # Nhật ký Prompt Engineering (Vibe Coding Log)
└── README.md         # Hướng dẫn dự án và thông tin nộp bài
```


