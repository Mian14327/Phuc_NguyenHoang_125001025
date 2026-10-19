# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

- **Họ và tên:** Nguyễn Hoàng Phúc
- **MSSV:** 125001025
- **Tên đề tài Website:** AI Hub - Nền tảng tổng hợp & Đánh giá công cụ Trí tuệ nhân tạo
- **Học phần:** Thiết kế Web (Giữa kỳ) - Khoa Công nghệ Thông tin, Đại học Lạc Hồng (LHU)
- **Công cụ AI đã sử dụng:** Antigravity AI / Gemini 3.8 Flash (Phương pháp Vibe Coding)

---

## 1. Yêu cầu ban đầu (System/Initial Prompt)

> **Prompt khởi tạo:**  
> *"Tôi đang làm bài thi Thiết kế Web với đề tài AI Hub, một website tổng hợp công cụ trí tuệ nhân tạo. Hãy tạo website một trang bằng HTML5, CSS3 ko có JavaScript, không dùng framework. Phong cách hiện đại, chuyên nghiệp, nền sáng, màu xanh dương và tím. Website gồm header, hero có thanh tìm kiếm, danh mục, lưới 6 công cụ AI, section lợi ích và footer. Bắt buộc dùng header, nav, main, section, article và footer đúng ngữ nghĩa; dùng CSS Variables, Flexbox, Grid và responsive. Tách thành index.html, style.css. Chưa thêm chức năng phức tạp. Hãy giải thích ngắn cấu trúc trước khi xuất mã nguồn đầy đủ."*

---

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iteration Steps)

### Lần 1: Dựng khung Semantic HTML & Hệ thống CSS Variables cơ bản
- **Prompt đã dùng:** Prompt 1 (như mục 1 trên).
- **Kết quả AI tạo ra:**
  - Cấu trúc 2 file mã nguồn cốt lõi: `index.html` và `style.css`.
  - Khung HTML phân chia các khối: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`.
  - Thiết lập CSS Variables cho màu sắc chủ đạo (blue, purple), spacing và typography.
- **Nhận xét & Tinh chỉnh của SV:**
  - AI ban đầu có xu hướng dùng thẻ `<div>` lồng nhau ở các thẻ công cụ.
  - Sinh viên đã yêu cầu chuyển toàn bộ các card công cụ thành thẻ `<article>` độc lập để đạt chuẩn ngữ nghĩa HTML5 theo đúng barem chấm của đề thi (tiêu chí Semantic HTML5 - 2.0 điểm).
  - Tách bạch rõ ràng giữa phần header của card, body chứa mô tả và footer chứa nút bấm điều hướng.

---

### Lần 2: Nâng cấp giao diện & Chuẩn hóa bảng màu UI/UX
- **Prompt đã dùng (Prompt 2):**  
  > *"Hãy kiểm tra giao diện AI Hub vừa tạo và cải thiện UI/UX theo hướng chuyên nghiệp. Sử dụng bảng màu #0F172A, #2563EB, #7C3AED, #F8FAFC và #FFFFFF thông qua CSS Variables. Căn chỉnh khoảng cách, typography, kích thước card, thanh tìm kiếm và CTA. Dùng CSS Grid cho danh sách công cụ, Flexbox cho header. Bổ sung responsive cho desktop, tablet và mobile. Không xóa các thẻ Semantic HTML5 và không viết lại toàn bộ nếu không cần. Nêu rõ các file và phần đã thay đổi."*
- **Kết quả AI tạo ra:**
  - Khai báo biến CSS Variables chuẩn 5 mã màu: `--color-dark: #0F172A`, `--color-primary: #2563EB`, `--color-secondary: #7C3AED`, `--color-bg-body: #F8FAFC`, `--color-bg-card: #FFFFFF`.
  - Sử dụng CSS Grid `repeat(3, 1fr)` cho màn hình máy tính, tự động chuyển về `repeat(2, 1fr)` trên tablet và `1fr` trên mobile.
  - Sử dụng Flexbox cho Header, Search bar, Category filters và Card action.
  - Căn chỉnh typography với font `Plus Jakarta Sans`, bo góc card `border-radius: 1rem` và đổ bóng mềm mại `box-shadow`.
- **Nhận xét & Tinh chỉnh của SV:**
  - Kiểm tra thanh tìm kiếm trên màn hình điện thoại (dưới 768px) ban đầu bị tràn viền; đã chỉ đạo AI bổ sung `flex-direction: column` cho form tìm kiếm trên mobile để nút "Tìm kiếm" không bị co rúm, tăng trải nghiệm người dùng (UX).

---

### Lần 3: Tích hợp thư viện hiệu ứng (Animate.css, AOS) & Tương tác thuần CSS
- **Prompt đã dùng (Prompt 3):**  
  > *"Tiếp tục trên mã nguồn AI Hub hiện tại. Hãy triển khai tìm kiếm công cụ theo tên và lọc theo danh mục bằng liên kết điều hướng. Tích hợp Animate.css cho tiêu đề Hero và CTA, AOS cho section và card. Tự viết hover và focus-visible bằng CSS. Giữ nguyên cấu trúc file, không dùng framework và không dùng JavaScript do môn học chưa dạy tới. Kiểm tra thứ tự nạp thư viện và responsive."*
- **Kết quả AI tạo ra:**
  - Nhúng CSS Animate.css v4.1.1 và AOS CSS.
  - Áp dụng class `animate__animated animate__fadeInDown` cho Tiêu đề Hero, `animate__pulse` cho nút CTA Khám phá.
  - Áp dụng hiệu ứng hover nâng card mượt mà `transform: translateY(-8px)` và bóng mờ `box-shadow: var(--shadow-xl)`.
  - Áp dụng `:focus-visible` với viền xanh 3px chuẩn Accessibility.
- **Thách thức gặp phải & Debug prompt:**
  - *Thách thức:* AI ban đầu có ý định tạo file JavaScript để xử lý mở/đóng menu trên mobile. Vì học phần hiện tại chưa học JavaScript, nếu đưa mã JS vào sẽ không đúng chương trình học của trường.
  - *Cách xử lý của SV:* Yêu cầu AI loại bỏ hoàn toàn các thẻ `<script>`, áp dụng giải pháp sáng tạo **Checkbox Hack thuần 100% CSS** (`#nav-toggle:checked ~ .main-nav`) để menu mobile tự động đóng/mở và chuyển đổi icon hamburger thành dấu "X" cực kỳ mượt mà.

---

### Lần 4: Debug và Rà soát hoàn thiện theo Checklist đề thi
- **Prompt đã dùng (Prompt 4):**  
  > *"Hãy rà soát mã nguồn AI Hub hiện tại theo checklist: Semantic HTML5, CSS Variables, Flexbox/Grid, responsive 3 cấp, liên kết điều hướng, Animate.css và hover/focus. Tuyệt đối không dùng JavaScript. Sửa tối thiểu để hoàn thiện chuẩn xác đạt điểm tối đa."*
- **Checklist nghiệm thu thực tế:**
  1. [x] **Chuẩn Semantic HTML5 (2.0 điểm):** Đầy đủ `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`. Không lạm dụng thẻ `<div>`.
  2. [x] **Kỹ thuật CSS & Variables (2.5 điểm):** Khai báo đầy đủ trên `:root`, áp dụng triệt để cho 5 mã màu chuẩn, khoảng cách, chuyển động. Layout kết hợp Flexbox và CSS Grid.
  3. [x] **Hiệu ứng & Thư viện (1.5 điểm):** Tích hợp thành công Animate.css ở Hero và CTA; Hover nâng thẻ mềm mại; Focus-visible viền rõ ràng đạt chuẩn Accessibility; Menu mobile chạy 100% bằng CSS.
  4. [x] **Quy chuẩn không dùng JS:** Toàn bộ dự án chỉ gồm 2 file mã nguồn `index.html` và `style.css`, không có bất kỳ thẻ `<script>` hay file `.js` nào.
  5. [x] **Nhật ký Vibe Coding (3.0 điểm):** File `PROMPT_LOG.md` theo chuẩn mẫu đề thi.

---

## 3. Đánh giá cá nhân về quá trình Vibe Coding

- **AI đã giúp bạn tiết kiệm thời gian ở phần nào nhất?**  
  - Tiết kiệm hơn 90% thời gian viết CSS boilerplate, căn chỉnh bố cục Flexbox/Grid phức tạp và thiết lập hệ thống biến CSS Variables.
  - Tự động sinh nội dung mô tả thực tế cho 6 công cụ AI (ChatGPT, Midjourney, Copilot, Claude, Runway, Perplexity) đúng chuyên môn và chân thực.
  - Hỗ trợ xây dựng giải pháp menu mobile và điều hướng danh mục 100% thuần CSS3 (Checkbox Hack), không cần dùng JavaScript mà vẫn đảm bảo trải nghiệm tương tác mượt mà.

- **Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web:**  
  1. **Nêu rõ ràng các giới hạn kỹ thuật (Constraints):** Cần nhắc rõ ngay từ đầu các yêu cầu như "chỉ dùng HTML5 và CSS3", "tuyệt đối không dùng JavaScript", "không dùng framework" để AI không tự ý thêm các công nghệ ngoài phạm vi môn học.
  2. **Chia nhỏ từng bước (Step-by-step):** Tiến hành qua 4 bước: Dựng khung Semantic -> Phối màu & Grid/Flexbox -> Thêm thư viện CSS & Hiệu ứng tương tác -> Debug kiểm tra checklist.
  3. **Vai trò chỉ đạo của sinh viên:** AI là trợ lý lập trình mạnh mẽ, nhưng sinh viên phải là người làm chủ bài thi, nắm vững kiến thức ngữ nghĩa HTML và CSS để kiểm tra, tinh chỉnh và định hướng sản phẩm đạt kết quả cao nhất.
