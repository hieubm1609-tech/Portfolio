# Portfolio cá nhân - Bùi Mạnh Hiếu

Site tĩnh (vanilla HTML/CSS/JS, không framework, không build step) cho B2B Campaign
Marketer (ABM & Demand Generation). Gửi cho nhà tuyển dụng/đối tác dưới dạng file tải về
hoặc host tĩnh.

## Liên hệ thật (dùng đúng, không đổi)
- Email: hieubm1609@gmail.com
- Điện thoại: (+84) 0918 160 902
- LinkedIn: linkedin.com/in/hieu-bui1609
- Địa điểm: Hà Nội, Việt Nam

## Kiến trúc đã chốt (2026-08-19, cập nhật lần 2 cùng ngày)
1. **File độc lập hoàn toàn**: mỗi trang tự chứa toàn bộ CSS/JS inline. Không có
   `styles.css`/`script.js` dùng chung. Lý do: tránh lặp lại lỗi vỡ layout do người dùng tải
   file rời rạc qua nhiều lượt chat làm đứt link tương đối (trình duyệt tự đổi tên file
   trùng, ví dụ `styles (1).css`). Khi sửa style/animation dùng chung, phải sửa đồng bộ ở
   TẤT CẢ các file (hiện có 7 file: index, media, writing, media-graphic-design,
   media-presentation, media-video-editing, media-web-design).
2. **Layout**: sidebar trái cố định trên mọi trang (tham khảo bố cục carlindalee.github.io,
   không copy code/asset). Nav dọc chỉ còn 3 mục: Home / Media / Copywriting (đã bỏ mục
   Campaign Analytics - xem mục 5).
3. **Project card**: kết hợp Case-Study/Dashboard (số liệu chính hiện sẵn, không ẩn sau
   hover) + animation/overlay tinh tế khi hover (kế thừa cảm giác Editorial). Dùng cho Home
   (Key Highlights) và Copywriting.
4. **Cấu trúc site (cập nhật):**
   - **Home** (`index.html`): hero 2 cột (chữ trái + ảnh đại diện thật bên phải, có nền lưới
     grid + vòng tròn trang trí mờ để đỡ trắng trơn - 2026-08-19), About Me, Accordion Skills
     (Core Competencies / Soft Skills / Tools & Platforms), Key Highlights (lưới 6 thẻ icon
     kèm số liệu), Selected Work (1 thẻ preview: Copywriting), **Media & Events** (section
     riêng show 3 ảnh thật sự kiện AI in Action - KHÔNG link ra media.html vì trang Media giờ
     là về design skill, không phải event), Experience timeline (đầy đủ 5 vị trí: Biplus, CMC
     TS, Eni, RMIT GGC HR Manager, RMIT GGC Logistics Leader), Education, Contact.
     Sidebar KHÔNG còn hiện ảnh đại diện nhỏ (đã bỏ 2026-08-19) - chỉ còn tên + chức danh,
     ảnh đại diện giờ chỉ xuất hiện to ở Home hero.
   - **Media** (`media.html`): KHÔNG phải ảnh sự kiện - là trang danh mục "My Work" gồm 3
     thẻ danh mục thiết kế (Graphic Design, Presentation, Web Design - đã bỏ Video Editing
     ngày 2026-08-19 vì folder rỗng), mỗi thẻ dẫn ra 1 trang con riêng
     (`media-graphic-design.html`, `media-presentation.html`, `media-web-design.html`).
     Asset thật nằm trong `Media/Graphic Design/`, `Media/Presentation/`,
     `Media/Web Design/` (Hiếu tự thêm file vào các folder này). Ảnh/slide/PDF được tách ra
     bằng `sips` (PDF 1 trang) hoặc PyMuPDF/`fitz` (PDF nhiều trang, vd slide deck 23 trang
     Teamwork Collection) rồi lưu thành PNG cùng thư mục, dùng lại tên file đã đổi sang
     kebab-case. `Media/Presentation/action-kit-for-cio.html` là 1 file HTML tương tác
     (không phải ảnh) - dẫn link trực tiếp tới file, CHƯA xác minh được hình ảnh bên trong
     có tải đúng không khi mở qua `file://` (file có vẻ phụ thuộc asset ID có thể cần mạng/
     server riêng) - cần Hiếu tự mở kiểm tra.
   - **Copywriting** (`writing.html`): showcase blog/nội dung viết. Hiện có 1 case thật (GTM
     AI adoption training product) + note-box chờ bổ sung thêm bài viết/blog thật.
   - **Đã bỏ hẳn trang Campaign Analytics** (`analytics.html` đã xoá) - quyết định
     2026-08-19: không cần trang riêng cho số liệu ABM/CRM/paid demand-gen, số liệu này chỉ
     còn xuất hiện ở Home (stat-strip trong About + Key Highlights).
5. **Ràng buộc phạm vi nội dung (chốt 2026-08-19):** Portfolio tập trung vào kỹ năng
   Marketing. Kinh nghiệm tại **CMC TS** và **Eni Vietnam** CHỈ xuất hiện ở trang Home
   (phần Experience timeline). Các trang còn lại (Media, Copywriting và các trang con) CHỈ
   dùng sản phẩm/kinh nghiệm từ **Biplus Vietnam Software Solution JSC** (vai trò Marketing
   Executive). Không đưa case CMC TS/Eni vào Media hay Copywriting nữa.

## Ngôn ngữ nội dung
Toàn bộ 4 trang viết bằng **tiếng Anh** (chốt 2026-08-19) - khớp với bộ bullet CV gốc chuẩn
quốc tế đã có sẵn (xem nguồn dữ kiện bên dưới), không cần dịch.

## Nguồn dữ kiện CV chính thức (thay thế mục "Số liệu xác nhận" cũ - dùng bản này)
Nguồn sự thật đầy đủ nằm trong `cv_structure_instruction.md` của Hiếu (ngoài thư mục dự án
này, do Hiếu dán trực tiếp vào chat). Tóm tắt các dữ kiện FIXED cần dùng cho portfolio:

**Kinh nghiệm (reverse-chronological):**
- **Marketing Executive (Strategic Marketing)** - Biplus Vietnam Software Solution JSC |
  May 2025 - Jul 2026. 3 trụ cột: ABM & quản lý account, CRM, tối ưu quy trình bằng AI.
  - Teamwork Collection - ABM Campaign: leads từ outreach +20% (ICP, account segmentation,
    personalized outreach, sales enablement content cho priority enterprise accounts)
  - GTM cho "an AI adoption training product" (KHÔNG bao giờ gọi tên riêng): landing page
    content, campaign messaging, webinar materials → engagement +12-15%. Có làm on-page SEO
    + AEO (Answer Engine Optimization) cho landing page biplus.com.vn/ai-native.
  - AI in Action (flagship AI-powered System of Work event cho Atlassian's solutions, tổ
    chức bởi 1 Atlassian partner tại VN): 500+ attendees, 2 địa điểm (Hà Nội & TP.HCM).
    Verb dùng: "Organized" (không phải "Supported"). Không bao giờ gọi "the largest".
  - Enterprise Roadshows: event logistics, sales enablement content, post-event
    documentation cho priority accounts.
  - Paid Demand-Generation (độc lập, không thuộc ABM): Google/Facebook/LinkedIn → CPL
    giảm ~10-20%.
  - CRM: chuẩn hóa CRM lead data/tracking workflows; thiết kế một phần lead management
    structure trong Salesforce (không claim sở hữu toàn bộ hệ thống).
  - AI workflow: dùng AI tools để tăng tốc content production, prompt design, workflow
    documentation.
  - Cách làm việc: Agile/Scrum fluent; công cụ Jira, Confluence, Trello, Figma.
  - Bối cảnh khách hàng: chủ yếu là các ngân hàng lớn tại VN (chỉ ở góc độ marketing, không
    phải nghiệp vụ ngân hàng).
- **CCUSFA Initiatives Project Coordinator** - Eni Vietnam | Jun 2024 - Oct 2024
  - Điều phối team 7 người (engineers, researchers, local partners)
  - Lên kế hoạch & thực thi on-site project activation (timeline, budget, risk assessment)
  - Communication materials + weekly visual reports cho executive leadership & government
    agencies
  - Systems thinking trong sustainability project planning
- **Account Manager** - CMC TS | Nov 2024 - Mar 2025
  - Quản lý portfolio khách hàng, primary point of contact (năng lực lõi)
  - Dịch kỹ thuật → giá trị kinh doanh cho stakeholder không chuyên kỹ thuật
  - Phân tích nhu cầu khách hàng & market dynamics → sales pipeline +16%
  - Partner với marketing team để chạy targeted sales campaigns
  - Chuẩn bị client reports, pitch decks, proposal materials
- **Logistics Leader - Award Night** - RMIT Vietnam Green Generation Club | Oct 2021 - Jan
  2022 (team logistics 6 người, budgeting, vendor, venue, on-site ops)
- **Human Resource Manager** - RMIT Vietnam Green Generation Club | Feb 2022 - Feb 2023
  (dẫn dắt HR team 20 người, workshops/team-building cho 110 thành viên → retention 91%)

**University project:** RescueBites Startup (Design Thinking and the Digital Startup
Project, RMIT) | Jun 2023 - team 5 người, full design sprint, Top 4.

**Education:** RMIT Vietnam University | 2020-2024. Bachelor of Digital Business - Minor:
Logistics & Supply Chain Management. GPA: 2.8.

**Skills:**
- Core Competencies: Account-Based Marketing & Account Segmentation, CRM & Marketing
  Operations, Enterprise Event & Field Marketing, Market & Account Research, Sales
  Enablement Content, AI-Assisted Workflow Optimization, Vendor & Budget Management,
  Post-Event Reporting
- Tools: Google Workspace & MS Office (Advanced), Canva, Figma, Trello, Power BI,
  Salesforce (CRM lead management), Jira, Confluence, Google Forms, Plausible
- Languages: Vietnamese (Native), English (Proficient - fluent written and spoken)

**Mapping nội dung cho 4 trang portfolio (chốt 2026-08-19):**
- Home: hero + about + skills summary + experience timeline (rút gọn) + education
- Media: event/field marketing - AI in Action, Enterprise Roadshows, Eni on-site activation
- Copywriting: campaign messaging/content - GTM AI adoption training product, on-page
  SEO/AEO, CMC TS sales enablement materials (pitch decks/proposals)
- Campaign Analytics: ABM & demand-gen số liệu - Teamwork Collection (+20% leads), Paid
  Demand-Gen (CPL -10-20%), CRM/Salesforce, CMC TS pipeline (+16%)

## Ràng buộc bắt buộc
- Không bịa số liệu/tên dự án/chi tiết công việc. Chỉ dùng số liệu đã xác nhận (xem dưới).
  Chỗ nào thiếu dữ liệu thật (chức danh/thời gian tại Biplus, ảnh đại diện, PDF bằng RMIT,
  mẫu copywriting thật) → để khung placeholder ghi rõ "cần bổ sung", không suy đoán.
- Sản phẩm đào tạo AI: luôn gọi "một sản phẩm đào tạo về AI adoption" / "GTM - AI Adoption
  Training Product", không bao giờ "AI-Native Foundations".
- AI in Action: luôn "flagship", không bao giờ "lớn nhất".
- Không dùng em dash "—" ở bất kỳ đâu — luôn gạch nối thường "-".
- Không copy code/asset/font trả phí từ Framer "Lofi" template hay theme Colorlib của
  carlindalee.github.io. Chỉ học bố cục/cảm giác chuyển động, viết lại code gốc 100%.

## Số liệu xác nhận (không làm tròn/đổi khác)
- Biplus - ABM Campaign (Teamwork Collection & Service Collection): leads từ outreach +20%
- Biplus - GTM AI Adoption Training Product: engagement chiến dịch số +12-15%
- Biplus - AI in Action (flagship): 500+ người tham dự, 2 địa điểm (Hà Nội & TP.HCM)
- Biplus - Paid demand-generation (Google/Facebook/LinkedIn): CPL giảm 10-20%
- CMC TS - Account Manager: sales pipeline +16%

## Chức danh + bio cá nhân (2026-08-19)
- Đổi chức danh hiển thị từ "B2B Campaign Marketer" sang "B2B Marketing Executive" ở TẤT CẢ
  6 file (sidebar, title tag, meta description, Hero lead, About lead-text).
- Hero (Home) có thêm đoạn bio cá nhân ngắn (`.hero-bio`, sau `.lead`, trước `.btn-row`) -
  Claude tự viết dựa trên dữ kiện thật đã xác nhận (Biplus, Eni team 7 người, RMIT GGC HR
  Manager dẫn team 20 người, viết blog AI Transformation cho Biplus), lấy cảm hứng cấu trúc
  từ đoạn "About Me" mẫu của carlindalee.github.io nhưng KHÔNG copy nội dung cá nhân của
  người đó (sở thích ẩm thực/âm nhạc/mentor program của họ không liên quan đến Hiếu) - chỉ
  giữ tinh thần giọng văn (curious, professional, energetic, open).

## Cập nhật nội dung vòng 2026-08-19 (CTA, skills, Media intro)
- CTA cuối trang (cả 6 file): đổi từ "Let's talk about your next campaign." (nghe salesy)
  sang "Let's grab a coffee and talk shop." (thân thiện, năng động hơn).
- Home - đã BỎ hẳn section "Selected Work" (chỉ còn 1 card Copywriting, không đáng để giữ
  section riêng) - `.feature-grid`/`.feature-card` CSS vẫn còn trong file nhưng không dùng nữa
  (an toàn, không cần xoá).
- Home - Accordion "Core Marketing Competencies" thêm pill "Content Writing & SEO". Accordion
  "Tools & Platforms" thêm 2 nhóm mới: "Content & CMS" (WordPress, Strapi) và "AI Tools"
  (ChatGPT, Claude, Gemini).
- Media - 3 trang con (Graphic Design/Presentation/Web Design) giờ có khối giới thiệu chuẩn:
  h1 → `.page-tagline` (câu mô tả nổi bật) → `.page-tools` (dòng "Using [tool] and [tool]",
  uppercase nhỏ) → `.lead` (đoạn mô tả giá trị). Graphic Design dùng đúng nguyên văn Hiếu cung
  cấp (Canva & Figma). Presentation dùng Google Slides & Canva. Web Design dùng Strapi & AI -
  đoạn mô tả cho Presentation/Web Design do Claude viết theo đúng tinh thần/format của đoạn
  Graphic Design gốc (copy giá trị chung, không phải claim số liệu cụ thể nào mới).
- Media/Graphic Design: 5 standee đổi từ `auto-fit minmax(190px,1fr)` (tự ngắt dòng 4+1) sang
  `repeat(5,1fr)` cố định 5 cột đều nhau trên desktop, fallback `auto-fit minmax(120px,1fr)`
  ở mobile (<760px).

## Element trang trí (2026-08-19, phản hồi "nền buồn chán")
- Mọi `.eyebrow` (nhãn nhỏ đầu mỗi section, cả 6 file) giờ có chấm đen hình thoi (`::before`,
  xoay 45deg, `background:var(--ink)`) đứng trước - đây là cách thêm contrast/element đen
  "trải dài toàn trang" mà không cần thiết kế riêng từng section.
- Hero (Home) có bộ hình trang trí quanh ảnh đại diện: 1 vòng tròn viền mảnh lớn, 1 vòng tròn
  viền ĐẬM (`border:2px solid var(--ink)`), 2 chấm đen đặc (`.hero-deco-dot`), 1 dấu cộng
  (`.hero-deco-plus`, SVG).
- `.page-hero` ở 5 trang con cũng có bộ tương tự thu gọn (`.deco-circle`, `.deco-circle.bold`,
  `.deco-dot`) - dùng chung tên class, dễ tái sử dụng khi thêm trang mới. Lưu ý: các phần tử
  trang trí này là `position:absolute`, KHÔNG được gộp chung selector `> *` với nội dung thật
  (đã từng viết nhầm `.page-hero > *{position:relative}` làm hỏng vị trí decor - đã sửa thành
  liệt kê rõ `.back-link, .eyebrow, h1, .lead`).

## Copywriting - blog list (2026-08-19)
- Tên bài blog (`.blog-item-title`) tăng cỡ chữ lên `1.4rem` (từ 1.05rem) để nổi bật hơn.
- ĐÃ BỎ HẲN ngày đăng (`.blog-item-date`) - lý do: chỉ 2/4 bài có ngày thật (2 bài tiếng Việt
  có byline "Hieu Bui" + ngày), 2 bài tiếng Anh không có ngày trong nội dung gốc nên hiển thị
  lệch nhau, không đồng bộ. KHÔNG tự bịa ngày cho 2 bài còn thiếu để lấp chỗ trống.

## Chuẩn spacing/typography đã đồng bộ (2026-08-19, áp dụng cho TẤT CẢ 6 file)
- `body` có nền lưới grid toàn trang, dùng biến `--grid:rgba(14,14,14,.045)` (RẤT nhạt, không
  dùng `--line` trực tiếp vì quá đậm gây khó đọc - đã bị người dùng phản hồi 2026-08-19 là
  "lẫn nội dung vào ảnh nền"), `background-size:64px 64px` (thưa hơn 48px cũ). Nếu cần chỉnh lại
  độ đậm/thưa của grid, sửa 1 chỗ duy nhất: biến `--grid` trong `:root` và `background-size` của
  `body`, đồng bộ ở cả 6 file. Card/button có border phải có
  `background:var(--paper)` tường minh để grid không "xuyên" qua nội dung bên trong (danh sách:
  `.feature-card`, `.highlight-card`, `.edu-card`, `.doc-btn`, `.pill`, `.btn-outline`,
  `.category-card`, `.link-card`, `.case-card` - khi thêm card mới có border, nhớ thêm dòng này).
- `.section{padding:96px 64px}` / mobile `56px 24px` (giảm từ 120px/64px cũ - đỡ khoảng trắng).
- `.footer-section{padding:96px 64px 56px}` / mobile `56px 24px 32px` - đồng nhất ở cả 6 file
  (trước đây Home dùng 120px còn trang con dùng 100px, đã sửa cho khớp nhau).
- `.page-hero{padding-top:96px; padding-bottom:40px}` (trang con) - khớp với `.section` padding-top.
- `h2{font-size:clamp(1.7rem,3vw,2.3rem); margin-bottom:24px; max-width:680px;}` - BẮT BUỘC có ở
  cả 6 file. Trước đây chỉ index.html có rule này, 5 file còn lại thiếu khiến h2 rơi về cỡ chữ
  mặc định trình duyệt (không đồng bộ) - đây là lỗi đã sửa, luôn kiểm tra khi thêm file mới.
- `.footer-section h2{margin-bottom:8px;}` và `.contact-grid{margin-top:28px}` - đồng nhất ở cả
  6 file cho phần "Get in Touch" cuối trang.

## Design system (dùng đồng nhất ở cả 4 file)
- Font: Google Fonts - Lexend (heading, 500-900) + Manrope (body, 400-800). (Lato bị lỗi
  dấu tiếng Việt, đã đổi.)
- Màu: `--ink:#0e0e0e` `--paper:#fff` `--muted:#6d6d6d` `--line:#e4e4e4` `--soft:#f5f5f5`
  (đơn sắc, chưa có accent color)
- Easing chuyển động: `cubic-bezier(.16,1,.3,1)` (biến `--spring`)
- Animation gốc bắt buộc có: curtain mở trang, cursor tùy chỉnh bám chuột, chữ hiện dần
  theo từ, scroll-reveal, marquee ảnh cuộn ngang vô hạn.

## Ảnh/logo thật đã xác minh (dùng lại nguyên URL, không sourcing lại trừ khi hỏng)
- Logo Biplus: `https://img.shgstatic.com/clutch-static-prod/image/scale/100x100/s3fs-public/logos/4fe45c907d52fa5265609d78f22f1277.png`
- Logo CMC TS: `https://cmcts.com.vn/media/data/logo_v3.png`
- Logo Eni Vietnam: `https://logos-world.net/wp-content/uploads/2025/11/ENI-Logo-500x281.png`
- Atlassian Teamwork Collection: `https://dam-cdn.atl.orangelogic.com/AssetLink/gg3dd02v1403p2eyg7s6j82ofo2wlg5y.webp`
- Atlassian Service Collection: `https://dam-cdn.atl.orangelogic.com/AssetLink/4sa8a648o7gv43s0nw03u54fqdsi37l1.webp`
- AI in Action - sân khấu chính: `https://biplus.info/images/v6/update-11-03/san-khau-chinh.jpg`
- AI in Action - keynote: `https://biplus.info/images/v6/update-11-03/keynote.jpg`
- AI in Action - networking: `https://biplus.info/images/v6/update-11-03/networking.JPG`
- AI Native (Biplus) minh hoạ: `https://website-api.biplus.com.vn/uploads/aaaa_3d60e25f23.png`
- Ảnh đại diện: ĐÃ CÓ - `Home/profile-photo.jpeg`, dùng ở sidebar mọi trang (đổi từ placeholder
  2026-08-19).
- Bằng tốt nghiệp + bảng điểm RMIT: ĐÃ CÓ - `Home/RMIT-Testamur.pdf`, `Home/RMIT-Transcript.pdf`,
  gắn nút tải ở mục Education trên Home (2026-08-19).
- Asset Media (Graphic Design/Presentation/Web Design) do Hiếu tự thêm vào folder
  `Media/<Danh mục>/`, đã xử lý và gắn vào các trang con tương ứng - xem chi tiết ở mục
  "Cấu trúc site" bên trên.

## Việc còn thiếu (hỏi Hiếu khi liên quan)
- Xác minh file `Media/Presentation/action-kit-for-cio.html` (export tương tác 27 trang) có
  hiển thị đúng ảnh khi mở qua `file://` không - nghi vấn phụ thuộc asset ID cần mạng/server
  riêng, chưa kiểm tra được bằng công cụ hiện có.
