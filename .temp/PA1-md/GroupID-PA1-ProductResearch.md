# GroupID-PA1-ProductResearch

**Môn học:** CSC13112 - UI/UX Design
**Giảng viên:** Dr. Lê Khánh Duy
**Nhóm:** [Tên nhóm]

| Thành viên | MSSV |
|------------|------|
| [Tên 1] | [MSSV] |
| [Tên 2] | [MSSV] |
| [Tên 3] | [MSSV] |
| [Tên 4] | [MSSV] |
| [Tên 5] | [MSSV] |

---

## Mục lục

1. [Giới thiệu](#1-giới-thiệu)
2. [Sản phẩm 1: VTVPrime](#2-sản-phẩm-1-vtvprime)
   - 2.1. Tên sản phẩm & Domain
   - 2.2. Đối tượng người dùng
   - 2.3. Core Use Cases(Xem mô tả trong PA1 requirements)
     - UC1: Xem trực tiếp một trận đấu
     - UC2: Tìm lại Highlight trận đấu
     - UC3: Tìm kiếm thông tin thể thao
   - 2.4. Phân tích ưu điểm dựa trên HCI
   - 2.5. Phân tích nhược điểm dựa trên HCI
   - 2.6. Các vấn đề với người dùng đặc biệt
3. [Sản phẩm 2: FPTPlay](#3-sản-phẩm-2-fptplay)
   - 3.1. Tên sản phẩm & Domain
   - 3.2. Đối tượng người dùng
   - 3.3. Core Use Cases(Xem mô tả trong PA1 requirements)
     - UC1: Xem trực tiếp một trận đấu
     - UC2: Lựa chọn môn thể thao để xem
     - UC3: Lựa chọn và thanh toán gói cước
   - 3.4. Phân tích ưu điểm dựa trên HCI
   - 3.5. Phân tích nhược điểm dựa trên HCI
   - 3.6. Các vấn đề với người dùng đặc biệt
4. [Tổng hợp & Nhận xét](#4-tổng-hợp--nhận-xét)

---

## 1. Giới thiệu

[Bối cảnh: Năm 2026 là năm diễn ra World Cup 2026 và ASIAD 2026. Nhu cầu xem thể thao trực tuyến tăng cao. Nhóm chọn khảo sát 2 nền tảng xem thể thao trực tuyến phổ biến tại Việt Nam: VTVPrime và FPTPlay.]

---

## 2. Sản phẩm 1: VTVPrime

### 2.1. Tên sản phẩm & Domain

| Thông tin | Chi tiết |
|-----------|----------|
| **Tên sản phẩm** | VTVPrime |
| **Domain** | **Nền tảng OTT (Over-The-Top) — Truyền hình & Giải trí trực tuyến, trọng tâm là thể thao.** |
| **Nền tảng** | Web (https://vtvprime.vn), Mobile (iOS/Android) |
| **Nhà phát hành** | Đài Truyền hình Việt Nam (VTV) — qua VTVcab |

**Phân tích Domain theo 3 khía cạnh:**

| Khía cạnh | Giải thích |
|-----------|------------|
| **① Sản phẩm làm về cái gì?** | VTVPrime là ứng dụng OTT do VTVcab phát hành, cung cấp nội dung: tường thuật thể thao trực tiếp, kênh truyền hình trực tuyến, phim và chương trình giải trí theo yêu cầu. Trọng tâm là thể thao trực tiếp (Champions League, World Cup 2026, LaLiga, Serie A, bóng chuyền). Ngoài ra còn có phim, chương trình TV và tin tức. Tích hợp hơn 120 kênh truyền hình trong nước và quốc tế. |
| **② Dùng trong hoàn cảnh nào?** | Người dùng thường thức khuya hoặc dậy sớm để xem trực tiếp World Cup 2026 (vì giải đấu tổ chức tại Mỹ - Canada - Mexico, chênh lệch múi giờ so với Việt Nam). Ban ngày, họ xem lại highlight hoặc tin tức thể thao trên đường đi làm, trong giờ nghỉ. Lúc rảnh rỗi, họ xem phim hoặc chương trình giải trí. Thiết bị dùng được: TV thông minh, laptop, máy tính bảng, điện thoại. |
| **③ Quy tắc trong lĩnh vực đó?** | Mọi ứng dụng xem thể thao trực tuyến đều phải đáp ứng 5 yêu cầu: (1) **Trận đấu đang diễn ra phải mở được ngay** — càng ít thao tác càng tốt; (2) **Nút điều khiển phải tự ẩn khi xem** — để không che mất hình, chỉ hiện ra khi người dùng chạm vào màn hình; (3) **Tỉ số, thời gian và tên đội luôn hiển thị** — ở một góc màn hình trong suốt trận đấu; (4) **Lịch thi đấu phải rõ ràng** — ghi chính xác ngày, giờ, đội đấu, vì thể thao chỉ diễn ra theo khung giờ cố định; (5) **Phân biệt rõ trạng thái trận đấu** — người dùng cần biết ngay trận nào đang Live, trận nào sắp diễn ra, trận nào đã kết thúc. |

### 2.2. Đối tượng người dùng

Dựa trên hành vi và bối cảnh sử dụng, người dùng VTVPrime có thể chia thành 5 phân khúc:

| # | Phân khúc | Hành vi & Bối cảnh | Tác động đến UI |
|---|-----------|-------------------|----------------|
| **A** | **Dân thể thao "cứng"** | Xem live hàng tuần, biết rõ lịch giải đấu, theo dõi nhiều môn. Tần suất cao, thời gian xem dài (≥ 90 phút). | Cần dashboard cá nhân hóa, bookmark đội/giải yêu thích, shortcut vào Live. |
| **B** | **Khán giả theo sự kiện (event-driven)** | Không xem thể thao thường xuyên, nhưng xem World Cup/ASIAD vì tính chất sự kiện xã hội (bạn bè rủ, quán xá bật, ai cũng bàn tán). Không rành về app, dễ choáng. | Cần onboarding nhanh, ưu tiên nội dung World Cup ngay trang chủ, hạn chế menu phức tạp. |
| **C** | **Người xem "cầu may"** | Mở app không có ý định trước, lướt xem có gì hay thì xem. | Cần gợi ý nổi bật, phân loại rõ ràng, preview nội dung (trailer, mô tả). |
| **D** | **Người xem lại (catch-up)** | Bận không xem live, sau đó tìm highlight hoặc xem lại. | Cần highlight được đẩy lên đầu, tìm kiếm theo đội/giải, lưu tiến trình xem. |
| **E** | **Người dùng phụ trợ** | Dùng app chủ yếu xem phim/TV, thỉnh thoảng mới xem thể thao. | Cần tab thể thao riêng, không lẫn với giải trí — tránh divided attention. |

*Nhận xét:* 5 phân khúc này khác nhau về **mức độ quen thuộc với app**, **mục tiêu khi mở app** (goal-directed vs exploratory), và **bối cảnh sử dụng** (xem live vs catch-up vs lướt). Mỗi phân khúc đặt ra yêu cầu khác nhau cho các thành phần UI: bố cục trang chủ, hệ thống điều hướng, tìm kiếm, tính năng cá nhân hóa và feedback.

### 2.3. Core Use Cases

---

#### UC1: Xem trực tiếp một trận đấu

| Khía cạnh | Mô tả |
|-----------|-------|
| **Ở đâu?** | Tại nhà hoặc bất cứ đâu có Internet (có thể dùng Wi-Fi hoặc 4G/5G) |
| **Khi nào?** | Trước hoặc ngay khi trận đấu bắt đầu |
| **Tư thế người dùng** | Ngồi hoặc nằm trên ghế, sofa, giường trước TV/màn hình lớn. Thời gian theo dõi kéo dài (90 phút cho bóng đá). |
| **Thiết bị** | Laptop, điện thoại thông minh, máy tính bảng |

**Các bước tương tác:**
1. Truy cập VTVPrime trên trình duyệt/app.
2. Đăng nhập tài khoản (nếu cần).
3. Tại trang chủ, banner trận đấu trực tiếp hiển thị nổi bật → chọn "Xem ngay".
4. Xem trận đấu, sử dụng các điều khiển: tạm dừng, âm lượng, phóng to/thu nhỏ, chọn chất lượng, xem bình luận.

> *Insert ảnh minh họa các bước (nếu có)*

**Ưu điểm cụ thể (dựa trên HCI):**
- [Ví dụ chi tiết - concrete, không chung chung]

**Nhược điểm cụ thể (dựa trên HCI):**
- [Ví dụ chi tiết - concrete, không chung chung]

---

#### UC2: Tìm lại Highlight + video ngắn của trận đấu

| Khía cạnh | Mô tả |
|-----------|-------|
| **Ở đâu?** | Tại nhà, trên phương tiện di chuyển, bất cứ đâu có Internet |
| **Khi nào?** | Sau khi trận đấu kết thúc (xem lại do bận hoặc xem bỏ dỡ) |
| **Tư thế người dùng** | Ngồi, nằm hoặc đứng — linh hoạt hơn UC1 vì thời gian xem ngắn hơn |
| **Thiết bị** | Laptop, điện thoại thông minh |

**Các bước tương tác:**
1. Truy cập VTVPrime → chọn "Tin nhanh".
2. Chọn mục "World Cup" hoặc môn thể thao mong muốn.
3. Duyệt danh sách Highlight/tin tức → chọn video.

**Ưu điểm cụ thể (dựa trên HCI):**
- [Ví dụ chi tiết]

**Nhược điểm cụ thể (dựa trên HCI):**
- [Ví dụ chi tiết]

---

#### UC3: Tìm kiếm thông tin thể thao

| Khía cạnh | Mô tả |
|-----------|-------|
| **Ở đâu?** | Bất cứ đâu có Internet |
| **Khi nào?** | Bất kỳ lúc nào có nhu cầu tra cứu (trước, trong, sau trận đấu) |
| **Tư thế người dùng** | Đa dạng: nằm, ngồi, đi — thao tác nhanh, thời gian ngắn |
| **Thiết bị** | Điện thoại thông minh (chủ yếu), laptop |

**Các bước tương tác:**
1. Mở VTVPrime → chọn biểu tượng kính lúp (tìm kiếm).
2. Gõ từ khóa (tên đội bóng, giải đấu, cầu thủ,...).
3. Enter → danh sách kết quả hiện ra → chọn bài viết phù hợp.

**Ưu điểm cụ thể (dựa trên HCI):**
- [Ví dụ chi tiết]

**Nhược điểm cụ thể (dựa trên HCI):**
- [Ví dụ chi tiết]

---

### 2.4. Phân tích ưu điểm dựa trên HCI

#### Recognition & Recall
- **Hiện trạng:** [Mô tả cụ thể giao diện đang làm tốt điều gì]
- **Phân tích HCI:** [Giải thích theo lý thuyết recognition vs recall — người dùng nhận ra ngay chức năng, không cần nhớ]
- **Ví dụ cụ thể:** [Tình huống thực tế, ví dụ: banner trận đấu lớn → người dùng nhìn là biết đang có trận live → click "Xem ngay" — đây là recognition]

#### Learnability
- **Hiện trạng:** Giao diện giống các nền tảng lớn (YouTube, Netflix).
- **Phân tích HCI:** External consistency — người dùng đã quen với các platform khác → dễ học, không cần đào tạo lại.
- **Ví dụ cụ thể:** [Mô tả một người dùng lần đầu dùng VTVPrime, đã từng xem YouTube → biết ngay cách dùng]

#### Memorability
- **Hiện trạng:** [Mô tả]
- **Phân tích HCI:** [Giải thích]
- **Ví dụ cụ thể:** [Tình huống]

#### Capabilities (Fitts's Law)
- **Hiện trạng:** Banner trận đấu có kích thước lớn, chiếm phần lớn màn hình.
- **Phân tích HCI:** Theo Fitts's Law (t = a + b log₂(d/s + 1)), banner lớn (s lớn) → thời gian di chuyển và click chuột giảm → giảm workload cho người dùng.
- **Ví dụ cụ thể:** [Mô tả kích thước banner, khoảng cách từ vị trí người dùng hay click tới banner → phân tích thời gian phản hồi]

#### Error Prevention
- **Hiện trạng:** [Mô tả]
- **Phân tích HCI:** [Giải thích]
- **Ví dụ cụ thể:** [Tình huống]

#### Visibility
- **Hiện trạng:** [Mô tả — trạng thái hệ thống có hiển thị rõ không? Ví dụ: trận đấu đang Live có được đánh dấu rõ trên giao diện không?]
- **Phân tích HCI:** Theo nguyên tắc Visibility, hệ thống cần thể hiện trạng thái và khả năng tương tác để người dùng biết — nếu thiếu, người dùng phải suy đoán.
- **Ví dụ cụ thể:** [Tình huống]

#### Affordances
- **Hiện trạng:** [Mô tả — các phần tử UI có gợi ý cách tương tác không? Ví dụ: banner trận đấu có cho thấy có thể click được không?]
- **Phân tích HCI:** Affordance là thuộc tính thiết kế giúp người dùng biết cách dùng mà không cần hướng dẫn — nút nổi lên cho thấy có thể nhấn, thanh trượt cho thấy có thể kéo.
- **Ví dụ cụ thể:** [Tình huống]

#### Consistency
- **Hiện trạng:** [Mô tả — icon, thuật ngữ, bố cục có đồng nhất giữa các màn hình không?]
- **Phân tích HCI:** Internal consistency giúp giảm cognitive load — người dùng không phải học lại cách dùng khi chuyển màn hình. External consistency (giống Netflix, YouTube) giúp tận dụng kinh nghiệm có sẵn.
- **Ví dụ cụ thể:** [Tình huống]

#### Mental Model
- **Hiện trạng:** [Mô tả — cách bố trí nội dung có khớp với kỳ vọng từ các OTT khác không? Ví dụ: người dùng kỳ vọng live match ở banner chính, highlight ở tab riêng?]
- **Phân tích HCI:** Người dùng xây dựng mental model từ kinh nghiệm quá khứ — nếu giao diện đi ngược mental model, họ sẽ mắc lỗi hoặc mất thời gian học lại.
- **Ví dụ cụ thể:** [Tình huống]

### 2.5. Phân tích nhược điểm dựa trên HCI

#### Error — Lỗi do thiết kế
- **Hiện trạng:** [Mô tả lỗi cụ thể — ví dụ: nút/vùng chạm quá gần nhau dẫn đến click nhầm]
- **Phân tích HCI:** [Liên hệ Fitts's Law, error prevention]
- **Ví dụ cụ thể:** [Mô tả tình huống người dùng gặp lỗi]
- **Đề xuất hướng khắc phục:** [Ý tưởng sơ bộ]

#### Inconsistency — Thiếu nhất quán
- **Hiện trạng:** Các mục "Đề xuất", "Nổi bật", "Thể thao", "Phim mới" trên trang chủ đều có format giống hệt nhau: tiêu đề trắng + danh sách thumbnail. Không có sự khác biệt trực quan để phân biệt ý nghĩa từng mục — người dùng phải đọc từng tiêu đề mới biết đang ở đâu.
- **Phân tích HCI:** Internal consistency bị vi phạm — các thành phần khác nhau về chức năng cần được thiết kế khác nhau để phản ánh đúng vai trò. Khi mọi thứ trông giống nhau, người dùng không thể ưu tiên xử lý thông tin, phải scan toàn bộ → tăng cognitive load.
- **Ví dụ cụ thể:** Giả sử người dùng muốn tìm trận đá gần đây nhất. Cả mục "Đề xuất" (gợi ý cá nhân), "Nổi bật" (hot trend), "Thể thao" (trận đấu) đều là dãy thumbnail giống nhau → phải đọc chữ mới phân biệt được.
- **Đề xuất hướng khắc phục:** Thiết kế section header khác biệt: icon + màu sắc + kích thước chữ riêng cho từng loại mục. Ví dụ: mục "Thể thao" dùng icon bóng đá + nền tối, mục "Phim mới" dùng icon film + nền sáng.

#### Efficiency — Tốn nhiều thao tác cuộn (Motor Load)
- **Hiện trạng:** Trang chủ VTVPrime dùng cơ chế cuộn vô tận (infinite scroll), tự động load thêm nội dung khi kéo đến cuối. Tuy nhiên không có nút "Go to top" — mỗi lần muốn quay lên đầu trang, người dùng phải cuộn thủ công qua hàng loạt mục đã xem. Nếu đang ở cuối trang, thao tác cuộn lên rất tốn thời gian và công sức. Việc phải lướt qua hàng chục mục cùng lúc cũng buộc người dùng phải scan và ghi nhớ vị trí nội dung — cử động mắt và tay nhiều.
- **Phân tích HCI:** Theo Fitts's Law, khoảng cách (d) càng lớn thì thời gian tương tác càng lâu — cuộn từ cuối lên đầu trang là distance cực đại. Ngoài ra, infinite scroll không có điểm dừng khiến người dùng mất phương hướng, không biết mình đang ở đâu trong không gian nội dung — vi phạm nguyên tắc Visibility.
- **Ví dụ cụ thể:** Người dùng lướt đến mục thứ 20 (ví dụ "Học Nhanh - Nhớ Sâu"), thấy không hứng thú, muốn quay lại mục "Phim Hoạt Hình Mới" đã thấy lúc đầu → phải cuộn tay hoặc lăn chuột rất nhiều để lên lại. Nếu không nhớ vị trí, họ phải vừa cuộn vừa scan lại từ đầu.
- **Đề xuất hướng khắc phục:** Thêm nút "Go to top" dạng floating (xuất hiện khi scroll xuống một ngưỡng nhất định). Hoặc chuyển sang cơ chế phân trang (pagination) để người dùng có điểm đánh dấu và dễ quay lại.

#### Capabilities — Không tối ưu cho người thuận tay trái
- **Hiện trạng:** [Mô tả — nút/khu vực tương tác chính nằm bên phải màn hình, không thuận cho người dùng tay trái]
- **Phân tích HCI:** Reachability — vùng tương tác chính nằm ngoài vùng với tay thoải mái của người thuận tay trái.
- **Ví dụ cụ thể:** [Mô tả]
- **Đề xuất hướng khắc phục:** [Ý tưởng sơ bộ]

#### Divided Attention — Phân tán sự chú ý
- **Hiện trạng:** [Mô tả — ví dụ: phần "Chương trình truyền hình" chen ngang nội dung thể thao]
- **Phân tích HCI:** Divided attention — người dùng phải xử lý nhiều luồng thông tin không liên quan cùng lúc → tăng cognitive load.
- **Ví dụ cụ thể:** [Mô tả]
- **Đề xuất hướng khắc phục:** [Ý tưởng sơ bộ]

#### Feedback — Thiếu phản hồi
- **Hiện trạng:** Khi cuộn đến cuối cùng của nội dung trên trang chủ, không có dòng text hay dấu hiệu nào cho biết "đã hết nội dung" hoặc "không còn gì để hiển thị". Hệ thống chỉ đơn giản là dừng load — người dùng không biết là do đã hết nội dung thật hay do mạng lag/đang load tiếp.
- **Phân tích HCI:** Theo nguyên tắc Feedback, hệ thống cần phản hồi trạng thái sau mỗi hành động của người dùng. Khi thiếu feedback ở trạng thái cuối trang, người dùng rơi vào tình trạng uncertainty — không biết nên chờ thêm hay đã hết, dẫn đến hành vi chờ đợi vô ích hoặc tưởng app bị lỗi.
- **Ví dụ cụ thể:** Người dùng cuộn đến cuối trang chủ, trang dừng load. Họ chờ 5-10 giây vì nghĩ mạng chậm, nhưng thực tế không còn gì nữa. Sau vài lần như vậy họ mới hiểu ra, nhưng mỗi lần vẫn phải mất thời gian "đoán" trạng thái hệ thống.
- **Đề xuất hướng khắc phục:** Thêm dòng text như "Đã hiển thị tất cả nội dung" hoặc một icon ở cuối trang. Hoặc chuyển sang phân trang (pagination) với số trang rõ ràng.

### 2.6. Các kiểu người dùng & bối cảnh phát sinh khó khăn

*Yêu cầu: Xem xét các kiểu người dùng khác nhau và các bối cảnh có thể gây khó khăn/cản trở với giao diện hiện tại.*

#### 2.6.1. Người dùng mới (First-time user) vs Người dùng quen thuộc (Power user)

| Khía cạnh | Người dùng mới | Người dùng quen thuộc |
|-----------|---------------|----------------------|
| **Đặc điểm** | Chưa từng dùng VTVPrime hoặc các nền tảng OTT trước đây | Đã dùng lâu năm, quen thuộc với mọi chức năng |
| **Khó khăn dự kiến** | [Mô tả — ví dụ: không biết chức năng "Tin nhanh" để tìm highlight, phải mò mẫm] | [Mô tả — ví dụ: phải qua nhiều bước để truy cập tính năng hay dùng] |
| **Bối cảnh cụ thể** | [Tình huống thực tế] | [Tình huống thực tế] |
| **Phân tích HCI** | [Ví dụ: Learnability — giao diện có trực quan để người mới tự học không?] | [Ví dụ: Efficiency — power user có thể thao tác nhanh không, hay bị chậm bởi UI?] |

#### 2.6.2. Người dùng xem trên thiết bị di động (Mobile) vs Desktop

| Khía cạnh | Mobile | Desktop |
|-----------|--------|---------|
| **Bối cảnh** | Xem khi đang di chuyển (trên xe bus, tàu điện), nằm trên giường, chờ đợi | Xem tại bàn làm việc, phòng khách — màn hình lớn, kết nối ổn định |
| **Khó khăn dự kiến** | [Mô tả — ví dụ: nút điều khiển quá nhỏ trên màn hình điện thoại, khó thao tác khi đi lại] | [Mô tả — ví dụ: bố cục giãn cách xa, phải di chuyển chuột nhiều] |
| **Phân tích HCI** | [Fitts's Law — size nhỏ → thời gian tương tác lâu. Reachability — vùng chạm xa tầm tay] | [Fitts's Law — distance xa → lâu hơn] |

#### 2.6.3. Người dùng ở khu vực có kết nối Internet chậm / không ổn định

- **Bối cảnh:** Ở vùng nông thôn, vùng sâu vùng xa, hoặc khi di chuyển (xe lửa, tàu).
- **Khó khăn dự kiến:** [Mô tả — ví dụ: video bị buffer kéo dài, ảnh/video không load, người dùng không biết là do Internet hay do app]
- **Phân tích HCI:** [Feedback — hệ thống không thông báo trạng thái loading/lỗi kết nối → người dùng confused]
- **Bối cảnh cụ thể:** [Tình huống thực tế]

#### 2.6.4. Người dùng nước ngoài / người không rành tiếng Việt

- **Bối cảnh:** Người nước ngoài sinh sống tại Việt Nam muốn theo dõi World Cup 2026.
- **Khó khăn dự kiến:** Tra cứu bằng tên đội bóng tiếng Anh (ví dụ: "Portugal") → không có đề xuất. Giao diện hoàn toàn bằng tiếng Việt.
- **Phân tích HCI:** Recognition bị giảm — người dùng không nhận ra từ khóa tìm kiếm do ngôn ngữ không khớp.
- **Bối cảnh cụ thể:** [Tình huống thực tế]

#### 2.6.5. Người dùng sử dụng trong môi trường ánh sáng mạnh (ngoài trời, ban ngày)

- **Bối cảnh:** Xem trận đấu ngoài trời (quán cà phê vỉa hè, công viên, màn hình ngoài trời).
- **Khó khăn dự kiến:** [Mô tả — ví dụ: độ tương phản thấp, chữ/nút quá nhỏ không đọc được, banner bị chói]
- **Phân tích HCI:** [Visibility — thông tin không còn nhìn thấy được trong điều kiện ánh sáng mạnh. Affordance mất tác dụng]
- **Bối cảnh cụ thể:** [Tình huống thực tế]

#### 2.6.6. Người dùng có nhu cầu xem cùng lúc nhiều trận đấu (Multi-task)

- **Bối cảnh:** Các giải đấu lớn (World Cup, ASIAD) diễn ra cùng giờ. Người dùng muốn theo dõi nhiều trận cùng lúc.
- **Khó khăn dự kiến:** [Mô tả — ví dụ: không có tính năng multi-view/picture-in-picture, phải chuyển qua lại giữa các tab]
- **Phân tích HCI:** [Divided attention — phải chuyển đổi liên tục gây cognitive load. Efficiency giảm]
- **Bối cảnh cụ thể:** [Tình huống thực tế]

---

## 3. Sản phẩm 2: FPTPlay

### 3.1. Tên sản phẩm & Domain

| Thông tin | Chi tiết |
|-----------|----------|
| **Tên sản phẩm** | FPTPlay |
| **Domain** | **Nền tảng OTT (Over-The-Top) — Truyền hình, phim ảnh & thể thao trực tuyến.** |
| **Nền tảng** | Web (https://fptplay.vn/), Mobile (iOS/Android) |
| **Nhà phát hành** | FPT Telecom |

**Phân tích Domain theo 3 khía cạnh:**

| Khía cạnh | Giải thích |
|-----------|------------|
| **① Sản phẩm làm về cái gì?** | FPTPlay là ứng dụng OTT do FPT Telecom phát hành, cung cấp nội dung: tường thuật thể thao trực tiếp, kênh truyền hình trực tuyến, phim và chương trình giải trí theo yêu cầu. FPTPlay tiếp sóng World Cup 2026 từ VTV, phát tất cả 104 trận. Ngoài ra còn có truyền hình trực tuyến, phim, chương trình TV và tin tức. Ứng dụng có tích hợp AI để phân tích nội dung thể thao. |
| **② Dùng trong hoàn cảnh nào?** | Tương tự VTVPrime: người dùng thức khuya xem trực tiếp thể thao (World Cup 2026, các giải đấu quốc tế) do chênh lệch múi giờ. Ban ngày xem lại highlight, tin tức thể thao. Lúc rảnh rỗi xem phim hoặc chương trình giải trí. Thiết bị dùng được: TV thông minh, laptop, máy tính bảng, điện thoại. |
| **③ Quy tắc trong lĩnh vực đó?** | Giống với VTVPrime — cùng domain OTT thể thao nên có chung 5 yêu cầu: (1) Trận đấu đang diễn ra phải mở được ngay; (2) Nút điều khiển tự ẩn khi xem; (3) Tỉ số, thời gian, tên đội luôn hiển thị; (4) Lịch thi đấu rõ ràng (ngày, giờ, đội); (5) Phân biệt rõ trạng thái Live / Sắp diễn ra / Đã kết thúc. |

### 3.2. Đối tượng người dùng

| Nhóm | Mô tả |
|------|-------|
| **Người yêu thích thể thao** | [Mô tả chi tiết] |
| **Khán giả phổ thông** | [Mô tả chi tiết] |

*Nhận xét:* [Tương tự VTVPrime — đa dạng đối tượng, độ tuổi, kinh nghiệm sử dụng]

### 3.3. Core Use Cases

---

#### UC1: Xem trực tiếp một trận đấu

| Khía cạnh | Mô tả |
|-----------|-------|
| **Ở đâu?** | Tại nhà hoặc bất cứ đâu có Internet |
| **Khi nào?** | Trước hoặc ngay khi trận đấu bắt đầu |
| **Tư thế người dùng** | Ngồi/nằm trên ghế, sofa — xem trong thời gian dài |
| **Thiết bị** | Laptop, điện thoại, máy tính bảng |

**Các bước tương tác:**
1. Truy cập FPTPlay → đăng nhập (nếu cần).
2. Banner trận đấu trực tiếp hiển thị → chọn "Xem ngay".
3. Sử dụng điều khiển: dừng, âm lượng, phóng to, chất lượng.

> *Insert ảnh minh họa (nếu có)*

**Ưu điểm cụ thể (dựa trên HCI):**
- [Ví dụ chi tiết]

**Nhược điểm cụ thể (dựa trên HCI):**
- [Ví dụ chi tiết]

---

#### UC2: Lựa chọn môn thể thao để xem

| Khía cạnh | Mô tả |
|-----------|-------|
| **Ở đâu?** | Bất cứ đâu có Internet |
| **Khi nào?** | Bất cứ khi nào muốn tìm nội dung thể thao |
| **Tư thế người dùng** | Ngồi/nằm — thao tác duyệt tìm, thời gian ngắn |
| **Thiết bị** | Laptop, điện thoại |

**Các bước tương tác:**
1. Truy cập FPTPlay.
2. Trên thanh công cụ → ấn "Xem thêm" (mũi tên bên phải).
3. Chọn môn thể thao ưa thích.
4. Duyệt danh sách trận đấu → chọn xem.

**Ưu điểm cụ thể (dựa trên HCI):**
- [Ví dụ chi tiết]

**Nhược điểm cụ thể (dựa trên HCI):**
- [Ví dụ chi tiết]

---

#### UC3: Lựa chọn và thanh toán gói cước

| Khía cạnh | Mô tả |
|-----------|-------|
| **Ở đâu?** | Bất cứ đâu có Internet |
| **Khi nào?** | Khi cần đăng ký/gia hạn gói thể thao |
| **Tư thế người dùng** | Đa dạng — thao tác ngắn |
| **Thiết bị** | Điện thoại (chủ yếu) hoặc laptop |

**Các bước tương tác:**
1. Truy cập FPTPlay → chọn "Mua gói" trên thanh công cụ.
2. Xem danh sách gói cước → chọn gói phù hợp.
3. Chuyển đến trang thanh toán → thực hiện thanh toán.

**Ưu điểm cụ thể (dựa trên HCI):**
- [Ví dụ chi tiết]

**Nhược điểm cụ thể (dựa trên HCI):**
- [Ví dụ chi tiết]

---

### 3.4. Phân tích ưu điểm dựa trên HCI

#### Recognition & Recall
- **Hiện trạng:** [Mô tả]
- **Phân tích HCI:** [Giải thích]
- **Ví dụ cụ thể:** [Tình huống]

#### Learnability & Memorability
- **Hiện trạng:** [Mô tả]
- **Phân tích HCI:** [Giải thích — external consistency với các nền tảng OTT khác]
- **Ví dụ cụ thể:** [Tình huống]

#### Consistency
- **Hiện trạng:** [Mô tả — giao diện nhất quán giữa các màn hình?]
- **Phân tích HCI:** [Giải thích — internal consistency]
- **Ví dụ cụ thể:** [Tình huống]

#### Capabilities (Fitts's Law)
- **Hiện trạng:** [Mô tả]
- **Phân tích HCI:** [Giải thích]
- **Ví dụ cụ thể:** [Tình huống]

#### Visibility
- **Hiện trạng:** [Mô tả]
- **Phân tích HCI:** [Giải thích]
- **Ví dụ cụ thể:** [Tình huống]

#### Affordances
- **Hiện trạng:** [Mô tả]
- **Phân tích HCI:** [Giải thích]
- **Ví dụ cụ thể:** [Tình huống]

#### Mental Model
- **Hiện trạng:** [Mô tả]
- **Phân tích HCI:** [Giải thích]
- **Ví dụ cụ thể:** [Tình huống]

### 3.5. Phân tích nhược điểm dựa trên HCI

#### Capabilities — Không tối ưu cho người thuận tay phải?
- **Hiện trạng:** [Mô tả — nút/khu vực tương tác nằm bên trái?]
- **Phân tích HCI:** Reachability, Fitts's Law.
- **Ví dụ cụ thể:** [Mô tả]
- **Đề xuất hướng khắc phục:** [Ý tưởng sơ bộ]

#### Visibility — Nội dung bị che khuất
- **Hiện trạng:** Tên nhà tài trợ hoặc tên đội bóng bị che bởi phần tử UI khác (poster, banner,...).
- **Phân tích HCI:** Visibility bị vi phạm — người dùng không thấy được thông tin quan trọng, phải suy đoán.
- **Ví dụ cụ thể:** [Mô tả — màn hình nào, phần nào bị che, thông tin gì bị mất]
- **Đề xuất hướng khắc phục:** Đưa description sang trái, poster sang phải — hoặc điều chỉnh layout.

#### [Nhược điểm khác — nếu có]
- **Hiện trạng:** [Mô tả]
- **Phân tích HCI:** [Giải thích]
- **Ví dụ cụ thể:** [Mô tả]
- **Đề xuất hướng khắc phục:** [Ý tưởng sơ bộ]

### 3.6. Các kiểu người dùng & bối cảnh phát sinh khó khăn

*Yêu cầu: Xem xét các kiểu người dùng khác nhau và các bối cảnh có thể gây khó khăn/cản trở với giao diện hiện tại.*

#### 3.6.1. Người dùng mới (First-time user) vs Người dùng quen thuộc (Power user)

| Khía cạnh | Người dùng mới | Người dùng quen thuộc |
|-----------|---------------|----------------------|
| **Đặc điểm** | Chưa dùng FPTPlay hoặc các nền tảng OTT trước đây | Đã dùng lâu, biết rõ cấu trúc và tính năng |
| **Khó khăn dự kiến** | [Mô tả — ví dụ: không biết phải ấn "Xem thêm" để duyệt môn thể thao] | [Mô tả — ví dụ: phải qua nhiều bước để vào đúng môn thể thao yêu thích] |
| **Bối cảnh cụ thể** | [Tình huống thực tế] | [Tình huống thực tế] |
| **Phân tích HCI** | [Learnability, Mental model — người mới có hiểu ngay cách duyệt không?] | [Efficiency — số bước thao tác có tối thiểu chưa?] |

#### 3.6.2. Người dùng xem trên thiết bị di động (Mobile) vs Desktop

| Khía cạnh | Mobile | Desktop |
|-----------|--------|---------|
| **Bối cảnh** | Xem khi đi lại, nằm trên giường, trong giờ nghỉ | Xem tại bàn, phòng khách với màn hình lớn |
| **Khó khăn dự kiến** | [Mô tả — ví dụ: phần "Xem thêm" ở góc trên cùng, khó với tay khi dùng một tay] | [Mô tả — ví dụ: các môn thể thao trải dài, phải scroll nhiều] |
| **Phân tích HCI** | [Reachability — nút ở xa tầm với ngón tay cái. Fitts's Law] | [Fitts's Law — distance lớn, phải di chuyển chuột nhiều] |

#### 3.6.3. Người dùng ở khu vực có kết nối Internet chậm / không ổn định

- **Bối cảnh:** Vùng nông thôn, khi di chuyển (xe lửa, xe khách).
- **Khó khăn dự kiến:** [Mô tả — ví dụ: danh sách gói cước không load kịp, ảnh poster bị vỡ]
- **Phân tích HCI:** [Feedback — không có indicator nào cho biết đang loading. Error prevention — dễ bấm nhầm gói cước do giao diện nhảy]
- **Bối cảnh cụ thể:** [Tình huống thực tế]

#### 3.6.4. Người dùng không rành về công nghệ / thanh toán trực tuyến

- **Bối cảnh:** Người lớn tuổi, người ít sử dụng Internet, người lo ngại về bảo mật thanh toán.
- **Khó khăn dự kiến:** [Mô tả — ví dụ: quy trình thanh toán nhiều bước không rõ ràng, sợ bấm nhầm, thiếu hướng dẫn]
- **Phân tích HCI:** [Mental model — người dùng không có mental model về thanh toán online → lo lắng. Error prevention — thiếu bước xác nhận trước khi thanh toán]
- **Bối cảnh cụ thể:** [Tình huống thực tế]

#### 3.6.5. Người dùng sử dụng trong môi trường ánh sáng mạnh (ngoài trời)

- **Bối cảnh:** Xem thông tin thể thao ngoài trời, quán cà phê ngoài trời.
- **Khó khăn dự kiến:** [Mô tả — ví dụ: chữ trên banner bị chói, khó đọc tên trận đấu]
- **Phân tích HCI:** [Visibility — thông tin mất khả năng hiển thị. Contrast không đủ cao]
- **Bối cảnh cụ thể:** [Tình huống thực tế]

#### 3.6.6. Người dùng muốn so sánh gói cước nhanh

- **Bối cảnh:** Trước khi quyết định mua gói thể thao, người dùng muốn so sánh các gói.
- **Khó khăn dự kiến:** [Mô tả — ví dụ: phải click vào từng gói để xem chi tiết, không có bảng so sánh cạnh nhau]
- **Phân tích HCI:** [Recognition — không thể nhìn thấy tất cả thông tin cùng lúc, phải dùng recall để nhớ gói trước khi xem gói sau. Efficiency giảm]
- **Bối cảnh cụ thể:** [Tình huống thực tế]

---

## 4. Tổng hợp & Nhận xét

### 4.1. So sánh nhanh giữa hai sản phẩm

| Tiêu chí HCI | VTVPrime | FPTPlay |
|-------------|----------|---------|
| **Recognition & Recall** | [Nhận xét] | [Nhận xét] |
| **Learnability** | [Nhận xét] | [Nhận xét] |
| **Consistency** | [Nhận xét] | [Nhận xét] |
| **Capabilities (Fitts)** | [Nhận xét] | [Nhận xét] |
| **Error Prevention** | [Nhận xét] | [Nhận xét] |
| **Feedback** | [Nhận xét] | [Nhận xét] |
| **Reachability** | [Nhận xét] | [Nhận xét] |
| **Inclusive Design** | [Nhận xét] | [Nhận xét] |

### 4.2. Kết luận

[Tổng kết ngắn gọn: những điểm mạnh/yếu chính của cả 2 sản phẩm, gợi mở cho phần Potential Solutions]

---

## Tài liệu tham khảo

- [Các nguồn tham khảo nếu có]

## NOTE
- Phân tích từ ngữ "Domain": Có 3 ý chính - Sản phẩm làm về cái gì(VD: Giải trí, thể thao trực tuyến)? Dùng nó trong hoàn cảnh nào(Xem phim khi đi ngủ, xem bóng đã lúc cao điểm,...)? Quy tắc trong lĩnh vực đó(Không được giật hình khi đang bàn thắng)?