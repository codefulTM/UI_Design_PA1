# Buổi 2: UI Design — Human Capabilities, Cognition, Usability & Affordances

## I. Tổng quan: Con người như một hệ thống xử lý thông tin

Trong tâm lý học, chúng ta tấn công nền tảng liên quan tới con người, liên quan tới những khả năng của con người về khả năng xử lý thông tin. Tại sao phải học cái này? Bởi vì giao diện là cách mà con người tiếp nhận thông tin từ thế giới xung quanh. Giao diện là cách chúng ta bố trí thông tin để con người tiếp nhận một cách hiệu quả nhất, tránh gây ra workload, làm tăng tải thông tin. Trước khi thiết kế được như vậy, chúng ta phải hiểu khả năng của con người có thể làm được gì và con người có những giới hạn gì trong việc tiếp nhận và xử lý thông tin.

Đây là những fundamental concepts, khái niệm nền tảng. Những ai làm về hiểu vấn đề con người, user research, nên biết để sau này nếu làm việc với dân thiết kế hoặc tìm hiểu thêm về thiết kế, gặp những thuật ngữ này sẽ không bỡ ngỡ, vì nó là nền tảng của ngành thiết kế.

### Con người như một hệ thống

Chúng ta có thể nhìn con người một cách đơn giản hóa như máy tính. Máy tính có thiết bị ngoại vi nhập liệu (chuột, bàn phím, màn hình chạm), thiết bị xuất thông tin (màn hình, loa, bộ rung). Máy tính cũng có CPU là bộ xử lý. Con người cũng có cấu tạo như vậy:

- **Kênh nhập liệu (Input):** các giác quan — tiếp nhận thông tin từ thế giới xung quanh.
- **Bộ xử lý (Processor):** hệ nhận thức (cognition system) — xử lý thông tin từ các giác quan. Cognition có khả năng lưu trữ thông tin (bộ nhớ), lựa chọn thông tin và xử lý.
- **Kênh xuất (Output):** hệ thống vận động (motor system) — phản hồi lại thế giới thông qua tứ chi, cổ, các bộ phận cơ thể.

Ví dụ: đặt tay lên bề mặt nóng. Tay (kênh xúc giác) thu được thông tin nhiệt độ. Nhiệt độ đó cần được xử lý bởi bộ não — xét ngưỡng nhiệt độ nguy hiểm. Nếu vượt ngưỡng, não ra lệnh cho hệ thống vận động rút tay lại. Đó là quy trình đơn giản của hành động, có sự tham gia của kênh nhập liệu, bộ xử lý và kênh xuất.

## II. Các giác quan của con người

Con người có 5 giác quan chính: thị giác, thính giác, khứu giác, vị giác và xúc giác. Thị giác là kênh tiếp nhận thông tin nhiều nhất — khoảng 80-90% lượng thông tin tại một thời điểm. Khi người ta nói về giao diện, người ta nói về thị giác là chủ yếu — giao diện cho người bình thường. Sẽ có trường hợp người khiếm khuyết thị giác, lúc đó phải communicate với họ qua giác quan khác.

### Thị giác

#### Vùng nhìn của mắt người

Mắt người có hai loại vùng nhìn:
- **Vùng nhìn ngang (Horizontal viewing frustum):** khoảng 180-200 độ. Khi nhìn thẳng, mắt cover được tới đây. Không thấy rõ nhưng cảm nhận được sự xuất hiện của vật thể.
- **Vùng nhìn dọc (Vertical viewing frustum):** hẹp hơn, chỉ khoảng 130 độ.

#### Độ phân giải của mắt — Foveal vision

Dù vùng nhìn rộng, không phải hình ảnh nào cũng rõ ràng. Mắt có điểm tập trung (tâm). Các vùng:
- **Foveal vision:** bán kính ~2 độ xung quanh tâm — hình ảnh cực kỳ sắc nét.
- **Parafoveal vision:** bán kính ~10 độ — hình ảnh vẫn rõ nhưng hơi mờ hơn.
- **Near Peripheral vision:** thấy tương đối hình ảnh, màu sắc, hình dáng nhưng mờ, không sắc nét.
- **Peripheral vision:** gần như chỉ thấy sự xuất hiện của vật thể, không thấy rõ màu sắc.

Mỗi vùng có độ phân giải khác nhau. Khi thiết kế giao diện, phải xem đối tượng xuất hiện trên màn hình sẽ rơi vào vùng nào của mắt để quyết định thể hiện nó như thế nào. Có trường hợp người ta cố ý thể hiện dữ liệu không quá sắc nét vì biết mắt người không cần nhìn quá rõ ở vùng đó — giúp giảm computing power, tiết kiệm năng lượng.

#### Cảm nhận màu sắc

Cấu tạo mắt người: ánh sáng đi qua thủy tinh thể vào võng mạc. Trên võng mạc có hai loại tế bào:

- **Tế bào hình que (Rods):** phân biệt sáng tối, đậm nhạt — chỉ tập trung vào sắc trắng đen. Có khoảng 120 triệu tế bào, nhạy gấp 1000 lần tế bào hình nón.
- **Tế bào hình nón (Cones):** phân biệt màu sắc. Mỗi tế bào chỉ tiếp nhận một trong ba loại màu: đỏ, xanh lá, xanh dương. Não tổng hợp ba màu này để tạo ra các màu khác nhau. Có khoảng 6-7 triệu tế bào.

Tỷ lệ tế bào hình nón:
- Màu đỏ: 60%
- Màu xanh lá: 30%
- Màu xanh dương: 10%

Tỷ lệ này giải thích công thức chuyển đổi RGB sang trắng đen: 0.6R + 0.3G + 0.1B.

#### Ứng dụng của hiểu biết về màu sắc

Thứ nhất, giải thích tại sao châu Âu thiết kế tập trung vào tông màu trung tính (đen, trắng, xám), ít dùng đỏ, vàng, xanh. Mắt con người nhạy cảm với việc phân biệt mức độ quan trọng của thông tin dựa trên mức độ đen xám hơn là màu sắc. Điều này cũng liên quan tới inclusive design.

Thứ hai, mắt người nhạy cảm nhất với màu đỏ, kế tiếp là xanh lá, rồi xanh dương. Đó là lý do thiết kế logo muốn tạo cảm giác yên bình thường dùng màu xanh dương, và ai mặc đồ đỏ ra đường dễ gây chú ý.

#### Mù màu (Color Blindness)

Khoảng 7-8% đàn ông bị mù màu, tỷ lệ nữ thấp hơn (~0.4%). Loại mù màu phổ biến nhất là giữa đỏ và xanh lá. Inclusive design là design dành cho tất cả mọi người. Trước đây Windows dùng nút Yes màu xanh lá, No màu đỏ — người mù màu không phân biệt được. Bây giờ thiết kế chuyển sang dùng contrast (tương phản) thay vì màu sắc để thể hiện mức độ quan trọng. Apple có Clarity UI — API chuyển tất cả icon thành dạng tương phản trắng đen, tránh gây rối cho người dùng và đặc biệt giúp người mù màu không bị rối.

#### Stereo Vision (Nhìn nổi)

Mắt người phân biệt được độ sâu của vật thể trong không gian nhờ hai con mắt. Mỗi con mắt chụp một tấm ảnh 2D, hai tấm ảnh lệch nhau một tí. Não tổng hợp hai tấm ảnh và suy ra khoảng cách — phép triangulation.

**Ứng dụng: Phim 3D.** Camera Stereo có 2 ống kính, ghi cùng lúc 2 tấm ảnh — một tấm ở kênh màu đỏ, một tấm ở kênh màu xanh. Khi chiếu phim, 2 tấm ảnh được chồng lên nhau. Mắt kính đỏ-xanh hoạt động như bộ lọc: mỗi mắt chỉ nhìn được một tấm ảnh. Não tổng hợp lại và suy ra độ sâu.

#### Ứng dụng Foveal Vision trong thiết kế Icon

Khoảng cách từ điện thoại tới mắt khoảng 40-50cm. Vùng foveal vision (2 độ) chiếu lên điện thoại có bán kính 1.3-1.7cm. Icon nằm trong vùng này thì người dùng nhìn rõ ngay lập tức. Icon lớn hơn vùng này buộc mắt phải scan nhiều lần — gây khó chịu. Ví dụ icon Momo nằm vừa vặn trong vòng tròn 1.4cm, trong khi một số icon khác tràn ra ngoài.

#### Ứng dụng Peripheral Vision: VR và Motion Sickness

Kính VR Oculus Rift đời đầu (2011-2012) có góc nhìn chỉ 90 độ, trong khi mắt người có vùng nhìn 130-220 độ. Vùng ngoài 90 độ bị đen — không render được. Khi vật thể di chuyển từ ngoài vào trong vùng 90 độ, nó đột ngột xuất hiện, não không có sự chuẩn bị, gây motion sickness.

**Giải pháp từ CMU và Microsoft Research:** Lắp thêm đèn LED quanh viền kính, có lớp diffuser làm dịu ánh sáng. Đèn LED render màu sắc của vùng không gian xung quanh — không cần chi tiết, chỉ cần cho thấy sự xuất hiện của vật thể. Giúp não có sự chuẩn bị. Kính VR hiện đại (Meta Quest, Pico 4 Ultra, Apple Vision Pro) đã có góc nhìn 168-180 độ nên không cần giải pháp này nữa.

**Render tối ưu trong VR:** Dùng eye-tracking để xác định người dùng đang nhìn đâu — vùng đó render rõ, vùng ngoài render mờ — giảm tải tính toán.

### Thính giác

Tai người nghe được tần số 20-20,000 Hz. Nếu thiết kế giao diện âm thanh, phải đảm bảo nằm trong tầm này.

**Định vị âm thanh:** Hai nguồn âm cùng tần số, cùng độ lớn, cách nhau 5 độ thì phân biệt được — gần hơn thì không. Quan trọng trong game bắn súng (immersion), VR (âm thanh phải render chuẩn với vị trí vật thể).

**Sonar/Radar bằng sóng âm:** Apple dùng sóng có tần số dưới 20 Hz (tai người không nghe được) phát ra, đo độ lệch pha của sóng phản xạ để tính khoảng cách — ứng dụng trong smartwatch, tính năng ruler. Ứng dụng này cho thấy: muốn đạt đẳng cấp cao, chỉ code không đủ — phải biết về tâm sinh lý con người.

**Cường độ âm thanh:** Tai người tiếp nhận 30-100 dB. Tiếng chuông điện thoại ~60-70 dB. Xe chạy cao tốc 120km/h, âm thanh >75 dB là cách âm kém. Xe cách âm tốt ~50 dB.

**Timbre (chất âm):** Cùng cao độ, độ lớn, vị trí nhưng phân biệt được nhạc cụ khác nhau là do timbre.

### Xúc giác

Xúc giác giúp cảm nhận bề mặt vật thể qua áp lực (pressure), áp lực mạnh (intense pressure — đau), và nhiệt độ (temperature). Mỗi bộ phận cơ thể có mức độ nhạy cảm khác nhau — ngón tay nhạy nhất, gót chân kém nhất.

**Ảnh hưởng tới thiết kế input device:** Ngày xưa điện thoại Nokia cục gạch có các nút vật lý — người dùng có thể nhắn tin không cần nhìn nhờ phân biệt hình dáng nút và nhớ vị trí. Smartphone hiện nay thiếu touch feedback, không thể phân biệt layout bằng xúc giác — đó là lý do thời đại "Handout Era" (lúc nào cũng phải nhìn điện thoại).

**Ứng dụng trong xe hơi:** Châu Âu yêu cầu xe hơi phải giữ nút vật lý cho các chức năng cơ bản. Khi lái xe 120km/h, phân tâm 300ms có thể gây tai nạn. Nút vật lý cho phép tương tác không cần nhìn. Tesla muốn dẹp nút vật lý nhưng chỉ hiệu quả khi có autopilot thực sự. Vấn đề AI không phải lúc hoạt động ổn mà là khi có sự cố.

## III. Motor System (Hệ thống vận động)

Mỗi bộ phận cơ thể có biên độ và tốc độ vận động khác nhau. Cổ xoay ~180 độ, tay xoay 360 độ. Nguyên tắc quan trọng nhất: **con người thích tương tác với giao diện ít phải vận động.** Làm thế nào để mắt ít phải di chuyển, tay đỡ phải di chuyển.

### Nhận diện chuyển động — Bioacoustic Sensing

Cử động của cơ thể tạo ra tần số dao động. Nếu bắt được tần số đó có thể dùng AI train để nhận diện cử chỉ. Nghiên cứu từ Carnegie Mellon (2015): tăng sample rate của smartwatch accelerometer từ 100 Hz lên 4,000 Hz để capture bioacoustic signals — sóng nén truyền qua cánh tay.

**Apple AssistiveTouch:** Nhận diện cử chỉ (nắm tay, pinch, double-pinch) để tương tác Apple Watch không cần chạm — hỗ trợ người khuyết tật hoặc người dùng trong ngữ cảnh bất tiện (chạy bộ).

**Câu chuyện chip Apple M-series:** Để đạt 4,000 Hz sample rate, chip Intel không đáp ứng được — chỉ làm được mỗi việc lấy dữ liệu sensor mà không xử lý được việc khác. Apple phải phát triển dòng chip riêng M1 (nay lên M5) với kiến trúc mới. Intel mất đi đối tác lớn vì không đầu tư phát triển — gã khổng lồ ngủ quên trên chiến thắng. Vấn đề trải nghiệm người dùng ảnh hưởng tới kiến trúc công nghệ của một công ty và chiến lược kinh doanh.

## IV. Reachability — Thiết kế cho một tay

Case study từ Flick (công ty đặt xe Canada, tương tự Uber). Mở màn hình đặt xe, việc đầu tiên là gõ điểm đến. Flick đặt câu hỏi: làm thế nào người dùng sử dụng tính năng này tiện lợi trong mọi hoàn cảnh?

Khảo sát cho thấy:
- 49% trường hợp sử dụng điện thoại bằng một tay
- 36% hai tay nhưng một tay chỉ giữ điện thoại
- Chỉ 15% dùng hai tay

**Vùng Reachability của ngón tay cái:** Khi cầm điện thoại, vùng tương tác thoải mái nhất là vùng dưới, gần ngón tay cái. Vùng cam cần điều chỉnh tay. Vùng tím phải thay đổi cách cầm.

**Quyết định đột phá của Flick:** Thay vì đặt search bar trên đỉnh hoặc dưới đáy màn hình (theo khuyến nghị Material Design thời đó), họ đặt search bar ở vùng reachability thoải mái nhất. Tính năng quan trọng đều nằm ở vùng này. Vùng trên dùng để hiển thị thông tin (bản đồ). Uber sau đó copy best practice này.

Việt Nam: Momo, Lazada, Shopee chưa làm như vậy vì follow mô hình super app — nhiều tính năng, nhiều product manager muốn KPI cao, quảng cáo chất đầy vùng dưới. Thiết kế bị chi phối bởi yếu tố business hơn là trải nghiệm.

## V. Attention (Sự chú ý)

Não cần cơ chế chọn lọc thông tin. Có ba cơ chế:

1. **Selective attention:** Cùng lúc quan tâm nhiều thứ nhưng tập trung vào một, vẫn aware những cái khác.
2. **Focused attention:** Tập trung quá kỹ vào một thứ, không quan tâm xung quanh.
3. **Divided attention:** Phải quan tâm nhiều thứ cùng lúc.

**Ứng dụng:** Highlight thông tin quan trọng — làm đối tượng khác biệt phần còn lại qua màu sắc, kích thước chữ, hình ảnh. Facebook tạo post dùng selective attention: focus vào soạn post nhưng background semi-transparent vẫn cho thấy ngữ cảnh.

**Lưu ý về người tự kỷ:** Họ không có cơ chế lọc thông tin, tiếp nhận tất cả. Có trường hợp tạo ra thiên tài (nhớ và vẽ lại toàn bộ khung cảnh), có trường hợp khủng hoảng vì quá tải thông tin.

## VI. Bộ nhớ (Memory)

### Working memory (Ngắn hạn) vs Long-term memory (Dài hạn)

**Working memory:** Dung lượng ít — chỉ nhớ khoảng 7-10 chunks. Thời gian lưu trữ ~10 giây. Dữ liệu mới sẽ thay dữ liệu cũ. Cách duy nhất để nhớ sâu: lặp đi lặp lại.

**Long-term memory:** Dung lượng không giới hạn. Tương tự ổ cứng — dữ liệu lâu không dùng sẽ đưa vào vùng truy xuất chậm.

### Chunking

Chunking là gom dữ liệu thành các đơn vị để nhớ. Ví dụ: người không biết tiếng Anh thấy "Happy Valentine" là 6 chữ cái riêng lẻ (6 chunks). Người biết tiếng Anh chỉ thấy 2 từ. Ghép thành "Happy Valentine" còn 1 chunk thôi.

**Kỹ thuật siêu trí tuệ:** Họ kể một câu chuyện kết nối tất cả đối tượng rời rạc thành một chunk duy nhất.

**Ứng dụng trong thiết kế:**
- Apple gom nhóm icon trên màn hình — mỗi group là một chunk. Cần tìm Facebook, biết nó thuộc group mạng xã hội, tap vô group đó rồi tìm.
- Giao diện BHXH cũ với các chữ viết tắt (CSKCB = Cơ sở khám chữa bệnh) — mỗi ký tự là một chunk, gây quá tải.
- Momo hiển thị quá nhiều chức năng cùng lúc — người dùng không nhớ, mỗi lần mở lại phải nhìn lại.

### Recognition vs Recall

- **Recognition:** Nhìn vô nhận ra ngay (nhìn mặt Mr. Bean biết ngay).
- **Recall:** Phải lục trí nhớ (gặp bạn 30 năm chưa gặp, quen quen mà không nhớ tên).

**Nguyên tắc:** Tối ưu recognition, giảm thiểu recall.

**Ví dụ:**
- UI login: phải nhớ username/password = recall. Single Sign-On (click icon đã đăng ký) = recognition. Face ID/fingerprint = không cần nhớ gì.
- Netflix: Continue watching hiển thị phim đang xem + tiến trình — recognition.
- Momo đặt phim: thêm thời gian kết thúc slot thay vì chỉ thời gian bắt đầu — giảm recall tính toán.

## VII. Usability

Không đánh giá giao diện bằng nhận xét chung chung kiểu "thân thiện, dễ sử dụng". Phải lượng hóa qua 5 dimensions:

1. **Learnability:** Bao nhiêu thời gian người dùng sử dụng không gặp lỗi?
2. **Efficiency:** Giao diện rút ngắn thời gian thực hiện công việc tới mức nào?
3. **Memorability:** Sau bao lâu không sử dụng thì quên?
4. **Errors:** Người dùng có hay tương tác sai (do thiết kế, không phải lỗi code)?
5. **Satisfaction:** Cảm nhận chủ quan — chỉ đạt được sau 4 yếu tố khách quan trên.

### Case study: Misfit Shine

Activity tracker của Misfit Wearables (startup Việt thành công). 12 đèn LED thể hiện nhiều thông tin: pin, nhịp tim, giờ. Câu hỏi: nhìn vào biết mấy giờ không? Người dùng không biết. Thiết kế đẹp (aesthetic) nhưng thất bại về usability.

### Case study: Remote TV

- **Remote cũ (nhập số):** Mapping số-kênh. Nếu ai đó rà lại kênh, phải bấm từ 1-99 — mắc 98 lỗi, tốn hơn 3 phút.
- **Smart TV remote (4 nút điều hướng):** Nhấn menu, hiển thị danh sách kênh, di chuyển bằng 4 nút — giảm recall.
- **Remote touchpad:** Thay 4 nút điều hướng bằng touchpad — di chuyển chéo (đường thẳng), nhanh hơn đi 4 cạnh.

## VIII. Nguyên tắc thiết kế giao diện tốt

### Visibility (Khả năng hiển thị)

Hệ thống có thể làm được gì thì giao diện phải cho biết. Hệ thống đang ở trạng thái nào thì giao diện phải thể hiện. Thử thách: trade-off giữa visibility và simplicity — hiển thị nhiều nhưng phải đơn giản.

**Ví dụ máy giặt:** Máy giặt cũ hiển thị đầy đủ thông số kỹ thuật (nhiệt độ, mực nước, vòng quay, thời gian) — visibility tốt nhưng dùng ngôn ngữ của kỹ sư, không phải người dùng. Máy giặt mới dùng chế độ như Baby Care — một chạm tự động cấu hình — dùng ngôn ngữ của người dùng.

### Accessibility (Khả năng tiếp cận)

Hệ thống hỗ trợ nhiều đối tượng người dùng khác nhau, kể cả người khiếm thị, khiếm thính, khuyết tật.

**Ví dụ bàn phím ATM:** Một bàn phím có chữ Braille — người khiếm thị chạm vô nhận diện ngay (recognition). Bàn phím kia không có Braille — phải nhớ layout trong đầu (recall).

### Affordances (Tính gợi ý)

Thuộc tính của thiết kế — người ta nhìn vô biết xài như thế nào.
- Kéo: thọt ngón tay vô bật ra.
- Ấm trà: cầm quai.
- Công tắc: gạt lên/xuống.
- Tay nắm cửa: kéo hoặc đẩy.

**Thất bại của affordances:** Cửa có tay cầm nhưng phải dán chữ "Push" hoặc "Pull". Ở Việt Nam, có quán dán bảng "Cửa này mở bằng cách đẩy ra, kéo vào — phạt 2 triệu". Đây là chuyện rất phổ biến.

**Thiết kế button:** Tạo hình dáng giả 3D, hơi nổi lên — affordance cho biết có thể nhấn.

**Ví dụ Netflix scroll bar:** Thể hiện 1 phần thumbnail của phim kế tiếp — affordance cho người dùng biết có thể scroll qua trái/phải. Nhiều designer Việt Nam mắc lỗi khi không để lộ phần thumbnail, người dùng không biết có thể scroll tiếp.

### Natural Mapping

Mapping giữa cách con người tương tác tự nhiên với thiết kế giao diện. Ví dụ: cần xi nhan trái thì gạt xuống trái, xi nhan phải gạt lên phải.

## IX. Lời khuyên về HCI Research

Môn học này có thể mở ra hướng nghiên cứu HCI. Các tập đoàn lớn (Microsoft, Google, Apple) có team HCI riêng. Nếu không giỏi thuật toán, có thể làm luận văn về HCI — tương tác người-AI, AR/VR.

**Lưu ý về nghề nghiệp:** Thời kỳ chỉ cần biết code web để hành tẩu giang hồ đang kết thúc. AI sẽ thay thế những công việc đó. Cần mở rộng kiến thức — human-AI interaction, tâm lý học, HCI là những hướng đi mới.

## X. Tổng kết

- **Usability tiêu chí:** Learnability, Efficiency, Memorability, Errors, Satisfaction.
- **Thiết kế:** Visibility, Accessibility, Simplicity, Affordances, Natural Mapping.
- **Nguyên tắc vàng:** Hạn chế vận động — mắt ít di chuyển, tay đỡ di chuyển. Tối ưu recognition, giảm recall. Hiểu người dùng — không dùng ngôn ngữ kỹ thuật cho người dùng cuối. Inclusive design — thiết kế cho tất cả mọi người, không chỉ người bình thường.
