# Buổi 3: UI Design — Efficiency, Mental Model, Metaphor & Design Process

## I. Consistency & Standard

Mini tool gồm có PIN5, Natural Mapping, Performance, v.v. Rồi còn nói về Consistency (Tính nhất quán). Consistency gồm hai loại:
- **Internal Consistency (Nhất quán nội bộ):** Đảm bảo cùng một nội dung hoặc chức năng trong ứng dụng phải được hiển thị giống nhau ở mọi nơi. Tránh việc một thiết kế lại đại diện cho nhiều mục đích khác nhau gây nhầm lẫn.
- **External Consistency (Nhất quán bên ngoài):** Tuân theo các tiêu chuẩn phổ biến mà các ứng dụng khác đã sử dụng (ví dụ: biểu tượng thùng rác là để xóa), giúp người dùng không phải học lại từ đầu.

## II. Efficiency & Fitts's Law

Bây giờ chúng ta sẽ bàn về Efficiency (Tính hiệu quả) — làm thế nào để người dùng tương tác nhanh chóng và thuận tiện nhất. Để đạt được điều này, chúng ta sẽ tìm hiểu một luật cực kỳ nổi tiếng: Fitts's Law (Định luật Fitts). Đây là một mô hình toán học giúp chúng ta tối ưu hóa các thành phần UI sao cho người dùng tốn ít thời gian và công sức nhất khi di chuyển đến mục tiêu.

### Công thức Fitts's Law

Công thức được thể hiện qua t là thời gian. Giả sử chúng ta có một giao diện. Tại thời điểm hiện giờ con trỏ chuột đang ở đây. Và chúng ta muốn di chuyển con trỏ chuột tới target, mục tiêu cần di chuyển tới. Thời gian di chuyển từ vị trí hiện tại tới target được mô hình hóa bởi công thức: t = a + b log₂(d/s + 1). Trong đó a và b là hằng số, phụ thuộc vào nhiều ngữ cảnh gồm kích thước màn hình, thiết bị đang sử dụng, v.v. Chúng ta không quan tâm giá trị a, b vì chúng là hằng số. Quan trọng nhất là t phụ thuộc vào log của hai biến: d và s. d là khoảng cách từ vị trí hiện giờ của con trỏ chuột (hoặc của người dùng trên giao diện) tới target, tới trung tâm của mục tiêu. s là kích thước mục tiêu.

### Phân tích từ công thức

Dựa trên công thức này, chúng ta rút ra được gì? a, b là hằng số, 1 cũng là hằng số. t phụ thuộc vào hai đại lượng d và s. d là khoảng cách, s là kích thước. Chúng ta rút ra được: càng xa càng lâu — nó tỷ lệ thuận với d. Và càng nhỏ càng lâu. Đối tượng mục tiêu càng nhỏ thì thời gian tương tác chính xác càng lâu. Các bạn muốn tương tác với đối tượng nhỏ, các bạn phải chậm lại để tương tác cho chính xác. Còn đối tượng to, các bạn muốn tương tác đại cũng được. Khoảng cách càng xa thì di chuyển càng lâu.

Công thức tưởng chừng đơn giản nhưng ảnh hưởng rất nhiều tới quyết định thiết kế. Chúng ta sẽ gom nhóm các UI như thế nào, các object như thế nào để tối ưu cho người dùng. Rồi chúng ta quyết định kích thước của nó ra sao, cách bố trí thế nào, tùy vào ngữ cảnh người dùng sử dụng.

Nếu muốn tối ưu việc tương tác, giúp người dùng tương tác nhanh, chúng ta phải thiết kế đối tượng to lên, gần lại, trong ngữ cảnh hiện giờ của người dùng. Còn nếu muốn làm cho người dùng khó tương tác thì chúng ta làm cho nó nhỏ lại và xa hơn. Chúng ta sẽ explore một số ví dụ. Dựa trên Fitts's Law, nó đưa ra một số implications:

Thứ nhất, những target liên quan tới nhau cần phải rút lại gần nhau, để tránh di chuyển chuột quá xa, quá nhiều.

Thứ hai, những target ở cạnh màn hình thì easy to hit — chúng ta kéo chuột một phát là chạm vào đó luôn. Tại cạnh màn hình, các bạn không di chuyển được nữa nên thiết kế sẽ dễ. Trong các loại menu, pie menu là tối ưu nhất, lát nữa chúng ta sẽ explore. Những menu dạng dọc dài sẽ tránh, chúng ta sẽ nói sau.

### Power Law of Practice

Dựa trên công thức Fitts, họ cũng đưa ra một luật gọi là Power Law of Practice: thời gian để hoàn thành task tại lần thứ n, khi tập luyện lặp đi lặp lại nhiều lần, thì tₙ = T₁ × n^(−a), trong đó a dao động từ 0.2 tới 0.6. Dựa trên điều này, n càng lớn thì tₙ càng giảm, nhưng chỉ giảm tới một ngưỡng nào đó thôi, không giảm hơn được nữa. Với range 0.2 đến 0.6, mũ trừ 0.2 tới trừ 0.6 thì chỉ giảm tới ngưỡng nào đó, không giảm hoài. Từ đó dẫn ra: với UI được thiết kế tốt, càng practice thì thời gian của người dùng càng giảm, nhưng chỉ giảm tới mức nào đó thôi. Tới lúc nào đó, người expert sẽ bị chạm ngưỡng, không thể làm nhanh hơn được nữa. Đó là vấn đề của UI.

## III. Ứng dụng Fitts's Law trong thực tế

### Scroll Bar — macOS vs Windows

Chúng ta xem ứng dụng Fitts vào việc thiết kế như thế nào. Đây là hai thanh Scroll Bar — một thanh trên giao diện macOS và một thanh trên Windows. Scroll Bar này thường sử dụng trên các ứng dụng Word, v.v.

Hai thanh Scroll Bar này khác nhau thế nào? Khoan quan tâm tới chuyện kích thước của hai cái — kích thước này phụ thuộc vào kích thước của doc thôi. Doc càng to thì cái này càng nhỏ, doc càng nhỏ thì cái này càng to. Nhưng ngoài ra, hai cái khác nhau chỗ nào? Và tại sao biểu thức khác nhau của hai thanh Scroll Bar? Của macOS như thế nào, và cái ở dưới như thế nào? Tại sao lại khác nhau? Điều gì từ hành vi người dùng dẫn tới thiết kế như vậy? Tại sao có sự khác nhau trong việc bố trí hai mũi tên khác nhau như vậy?

Các bạn nhìn từ góc độ người dùng. Khi nào các bạn dùng cái này? Nhiều quá. Và để ý khi dùng cái này thường phát sinh chuyện gì? Hay có vụ bấm lố không? Có. Bấm lố xong thường phải bấm kéo lại, de lại. Các bạn de đi de lại hai đầu, di chuyển chuột thấy mất thời gian không? Đó là lý do họ gom lại. Vì hai cái này liên hệ với nhau mật thiết, thường bấm lố một đầu sẽ phải bấm đầu kia lại. Nên họ làm thế nào để tối ưu, để người dùng ít phải di chuyển? Điều này dựa trên quan sát rất kỹ về người dùng và đưa ra quyết định thiết kế.

### Nút Discard — Làm khó người dùng

So sánh nút Discard bên tay trái và nút Discard bên tay phải, khác nhau thế nào và ảnh hưởng tới hành vi người dùng ra sao? Nếu để bên tay trái, giả sử muốn ấn xem mà vô tình lệch qua Discard thì email sẽ bị mất luôn. Còn bên phải thì đỡ bị lầm hơn. Ở trường hợp này chúng ta dùng Fitts theo kiểu làm khó cho người dùng, chứ không phải làm dễ. Làm cho người dùng click nút Discard khó hơn. Vì nếu để nút Discard gần, cùng màu, người dùng vô tình click ngay lập tức. Trong khi nút Discard ít khi được sử dụng, nên phải đảm bảo người dùng chỉ click nó khi thực sự muốn. Quyết định là: thứ nhất, nút Discard nhỏ tí xíu; thứ hai, để xa ra. Muốn xóa thì mới tìm.

### Pop-up Menu & Drop-down List

Rồi, pop-up menus. Ứng dụng Fitts như thế nào trong thiết kế pop-up menus? Tại sao pop-up menus là một ví dụ minh họa rất tốt? Đơn giản thôi. Các bạn click phải là menu xuất hiện ngay đó, không cần di chuyển lên thanh menu cố định sẵn. Nó là dynamic menu.

Đây cho thấy sự tiến hóa của drop-down list UI trên điện thoại. Ngày xưa, hồi Android những năm 2011-2012, drop-down list dạng như thế này. Nó bê từ thiết kế desktop sang luôn. Vấn đề là mỗi item khá nhỏ, dẫn tới tương tác hơi khó. Theo Fitts, đối tượng càng to càng dễ tương tác, nhỏ thì khó. Sau đó họ khắc phục và thiết kế drop-down list bung to như vầy. Lúc đó mỗi item rất dễ tương tác, nhưng vấn đề là phần phía trên rơi vào vùng chết trong tương tác ngón tay của người dùng. Nên drop-down list bây giờ đa số các app sẽ cover từ đây xuống đây, và mỗi item đủ to để tương tác bằng một tay.

Đây là hai drop-down list: một trên Grab và một trên giao diện thanh toán hóa đơn trước đây của Momo. Bây giờ Momo đã cải thiện rồi. Các bạn thấy vấn đề về efficiency. Mô tả flow: ở Grab, muốn send một package, chọn option pick up now, tap vô thì nó hiện các option. Còn ở Momo, nó xuất hiện khi bấm vô chỗ gọi phí thanh toán, chọn phí thanh toán, rồi nó bung ra. Dùng Fitts, phân tích efficiency của hai cái xem thằng nào hiệu quả hơn và tại sao.

Đúng rồi. Fitts gồm hai yếu tố: distance và size. Phân tích distance và size. Ở Grab dễ tương tác hơn, rất rõ ràng. UI của Grab được thiết kế chuẩn chỉnh hơn: khoảng cách di chuyển xuống từng option ngắn hơn, và mỗi item cũng lớn hơn.

Đây là lý do chúng ta ghét những menu dài. Giả sử mở menu ở đây, click vô để open menu, và đối tượng muốn hướng tới ở lại chỗ kia — phải di chuyển một đoạn dài. Hoặc muốn click vô bottom, phải từ đây xuống bottom. Đó là lý do người ta nói giống như học thuật toán DSA. Có thể độ phức tạp trung bình là log n, nhưng nếu thiết kế không tốt thành O(n). Giống như cây tìm kiếm không cân bằng, sẽ bị lệch về phía, phải đi tới nốt cuối cùng. Nếu thiết kế vậy, xui xui đi tới nốt cuối cùng tốn thời gian.

### Pie Menu & Spatial Memory

Đó là lý do pie menu được xem là tối ưu nhất. Vì pie menu click vô menu ở đây rồi các option bung ra các hướng. Khoảng cách từ đây tới tất cả các hướng đều bằng bán kính hình tròn cả. Nên đảm bảo không rơi vào trường hợp worst case. Nhưng pie menu có một đặc tính vừa tốt vừa xấu: spatial memory. Spatial memory là việc con người có thể nhớ vị trí của vật thể trong không gian nếu sử dụng quen rồi. Giống như bàn làm việc, các bạn hay để đồ chỗ nào, quen rồi thì không cần nhìn, chỉ cần thò tay ra là biết nó nằm chỗ đó. Spatial memory chỉ hiệu quả khi mật độ vật thể trong không gian không quá dày. Mật độ dày quá thì spatial memory bị rối. Chúng ta có thể tận dụng spatial memory cho circular menu, pie menu, để tăng hiệu quả tương tác nếu số lượng đối tượng nhỏ, thường dưới 8.

Trên 8 đối tượng thì spatial menu trở nên không hiệu quả. Nếu nhiều đối tượng quá, người ta làm multilayer spatial memory. Multilayer circular menu — gom nhóm những cái thuộc cùng một nhóm, đẩy vô một. Ví dụ muốn tương tác với này, click vô, nó bật ra, tương tác vô. Khoảng cách di chuyển căn bản rơi vào worst case giả sử từ đây bật ra đây, từ đây bật ra đây, cũng không tới nỗi nào.

Đây là những ví dụ nổi tiếng về circular menu trong giao diện, nhất là ứng dụng Autodesk Sketchbook — circular menu để lựa chọn công cụ. Hoặc dạng biến thể khác của circular menu là menu thành nhiều hình dãy, như app chụp hình Nokia trên Nokia Lumia — một trong những app chụp hình được đánh giá cao nhất trong lịch sử, nhất là những năm 2020 trở về trước, nó là một dạng huyền thoại.

## IV. Nguyên tắc tăng Efficiency

Từ Fitts, chúng ta rút ra một số nguyên tắc để tăng efficiency cho người dùng:

Thứ nhất, những tính năng người dùng hay sử dụng phải to. Thứ hai, những đối tượng liên quan tới nhau, tương tự nhau, phải group lại để truy xuất thuận tiện. Thứ ba, đặt những menu item thường sử dụng ở trên top của menu. Thứ tư, sử dụng screen corners và edge để đặt những đối tượng người dùng thường xuyên sử dụng, để họ có thể di chuyển nhanh chóng xuống góc đó. Và chúng ta cũng có thể sử dụng shortcut hoặc grouping, predefined group of style để giúp người dùng tương tác với nhóm đơn giản hơn. Hỗ trợ option cho người dùng select cùng lúc nhiều đối tượng, vì nếu phải select từng cái, từng cái một thì người dùng phải di chuyển chuột quá nhiều. Hiểu Fitts, chúng ta nên có option select all và deselect all để hạn chế việc select riêng rẻ quá nhiều.

## V. History, Memories & Intent Prediction

Một số ứng dụng sẽ lưu lại history. Điều này cực kỳ quan trọng trong thời đại AI. AI bây giờ làm gì cũng phải có history. Các bạn biết một trong những vấn đề nhức nhối nhất, cạnh tranh giữa các mô hình AI là gì không? Vấn đề bộ nhớ. Nếu con ChatGPT của bạn lưu trữ bộ nhớ ít quá, assistant chỉ thực sự hiệu quả khi nhớ được lịch sử làm việc của bạn để đưa ra suggestion phù hợp. Đang làm giữa chừng, tự nhiên nó xóa bộ nhớ — bạn đang làm ngày hôm qua, nó quay lại như đứa mới, không nhớ bạn làm gì, bạn phải tốn thời gian nhồi lại kiến thức. Nên memories là vấn đề rất quan trọng. Làm thế nào để lưu trữ memories, mang tính personalize cho người dùng, để đưa ra suggestion nhanh.

Anticipation — chúng ta tìm cách dự đoán người dùng chuẩn bị làm gì và đưa ra auto prediction. Chưa bao giờ điều này lại trở nên quan trọng như trong thời đại AI bây giờ. Thời đại AI gọi là intent prediction — AI phải dự đoán được intent của người dùng để đưa ra suggestion phù hợp với nhu cầu, mà người dùng không phải mô tả quá nhiều.

Đây là menu rất tệ cho efficiency.

## VI. Mental Model

Bây giờ chúng ta sẽ tìm hiểu thêm một khái niệm nữa, mang tính hơi trừu tượng tí nhưng thực ra rất bình thường trong cuộc sống hàng ngày. Khái niệm này gọi là mental model.

Mental model là gì? Sau này đi làm mà đụng sâu về thiết kế chắc chắn sẽ gặp. Nếu các bạn đọc định nghĩa học thuật, các bạn sẽ rối ngay: "internal construction of some aspect of the external world enabling prediction to be made". Rất rối. Nhưng ý nghĩa là: chúng ta lớn lên, tương tác với cuộc sống xung quanh, tiếp nhận những thứ xung quanh, và những điều đó tạo thành kinh nghiệm. Kinh nghiệm này được lưu trữ trong bộ não. Một lúc nào đó, khi đứng trước một vật thể, dựa trên hình dáng và cảm nhận, dựa trên kinh nghiệm, chúng ta suy đoán ra vật thể này có thể hành động như thế nào. Nó giúp chúng ta suy đoán có thể làm gì với vật thể, dựa trên trải nghiệm, kinh nghiệm, kiến thức đã có trong quá khứ.

Giống như nhìn vô remote — có những cái nút nổi lên, sờ thấy mềm. Từ nhỏ đã quen remote ở nhà có những vật nổi lên mềm mềm, và những vật đó thường nhấn được. Bây giờ gặp vật thể này cũng dự đoán nhấn xuống được. Nhưng đôi khi gặp remote họ chỉ để những cục nhựa nổi lên, không biết bố trí nút gì — bấm qua không hết thu. Lúc đó, thiết kế complicate mental model. Mental model được xây dựng rằng những gì nhỏ nhỏ nổi lên thì nhấn được, nhưng thiết kế không đúng dẫn tới không chính xác.

Đó gọi là mental model. Mental model rất quan trọng vì muốn thiết kế UI mà người dùng hiểu, đa số người dùng hiểu, thì phải biết mental model của đại đa số người dùng đang hướng tới. Và muốn biết mental model đó, phải biết họ là ai, xuất phát điểm của họ ra sao, họ có trải nghiệm gì trong cuộc sống. Thiết kế robot, phải biết người thường sử dụng robot là ai, họ có thường xuyên sử dụng robot tương tự trong quá khứ hay không. Nếu không, họ chưa chắc biết làm. Thiết kế icon máy lạnh, chỉnh gió — đâu phải ai cũng biết, ví dụ người không biết tiếng Anh nhìn vô không biết có thể chỉnh độ quay khe gió. Chúng ta phải biết đối tượng người dùng để thiết kế UI phù hợp.

Mental model khác nhau giữa người này với người nọ, có thể có sự tương đồng nhưng vẫn có khác biệt. Vì mental model phát triển dựa trên trải nghiệm tương tác của con người với thế giới xung quanh, mà mỗi người có những trải nghiệm khác nhau.

Ví dụ, đây là hình chụp tủ lạnh nhà mình ở Thụy Điển — tủ lạnh này chắc tuổi thọ từ 1980-90. Bên đó xài đồ bền, đi tới đôi lúc thấy hơi lạc hậu. Đây là ngăn mát tủ lạnh, dùng để chỉnh mức độ mát. Câu hỏi: muốn tủ lạnh mát hơn thì quay qua số lớn hay số nhỏ?

Tùy vào loại tủ lạnh. Các bạn thấy chưa, bắt đầu rối rồi — nói "tùy" có nghĩa là không dự đoán được, thiết kế này đang có vấn đề, nó complicate mental model. Cách duy nhất là thử sai. Vô, thử quay qua số nhỏ, đóng cửa lại 10 phút, mở ra thử — thấy không mát hơn mà nóng hơn. Từ đó mới biết với tủ lạnh này, mát hơn phải quay qua số lớn. Khi thiết kế mà người dùng không biết phải làm thế nào, phải thử sai — đó là conflict với mental model. Tủ lạnh hiện đại bây giờ không còn như vậy nữa. Trên cửa tủ để nhiệt độ: mát là bao nhiêu? 8 độ, 6 độ, 4 độ, chứ không để mức độ mập mờ.

## VII. Metaphor trong thiết kế

Một khái niệm nữa đi lên từ mental model, làm thế nào đưa ra thiết kế phù hợp với mental model của người dùng — đó là metaphor.

Metaphor là thuật ngữ trong thiết kế, dịch ra là ẩn dụ. Metaphor chỉ việc chúng ta vay mượn cách thể hiện của một đối tượng trong ngữ cảnh này để áp dụng vào ngữ cảnh mới. Đối tượng chúng ta thiết kế trong ngữ cảnh mới có thể có một số thuộc tính giống đối tượng cũ. Chúng ta vay mượn cách thể hiện từ đối tượng cũ áp qua cái mới, để người dùng nhìn vô biết xài như thế nào.

Ví dụ, folder trên Windows — hình dáng vay mượn từ bìa kẹp hồ sơ. Khi bìa kẹp hồ sơ rỗng thì không có gì trắng trắng ở trong, họ vẽ folder là bìa kẹp hồ sơ rỗng — biết folder không có tập tin gì. Khi nhìn folder thấy miếng trắng trắng là biết trong folder có file. Đó chính là metaphor — vay mượn cách thể hiện, có thể về mặt hình ảnh, về cách tương tác với đối tượng, áp dụng lên đối tượng mới có thuộc tính tương tự.

Metaphor thường vay mượn từ những đối tượng thế giới thật mà người dùng đã quen thuộc. Nếu vay mượn thành công metaphor thì cực kỳ hiệu quả, vì người dùng nhìn vô biết xài liền. Nhưng vay mượn thế nào cho hiệu quả, lựa chọn property, thuộc tính nào để vay mượn — đó là phần khó nhất. Chúng ta phải thử sai rất nhiều, không phải thiên tài nhìn vô biết vay mượn thế nào đâu. Thiết kế là thử sai. Đôi lúc còn phụ thuộc vào nền văn hóa — vay mượn đối tượng trong văn hóa này nhưng chưa chắc văn hóa khác biết đối tượng đó.

Ví dụ thùng rác — hai cách thể hiện. Rõ ràng nền văn hóa khác nhau, mỗi nền văn hóa có cách thể hiện thùng rác khác nhau. Có thể châu Á biết thùng rác này nhưng cũng có thể châu Á không biết.

Đây là những ví dụ nhìn rất bình thường nhưng thực ra đều là metaphor. Khi Apple ra iPhone, họ tạo ứng dụng Calculator — họ đâu cần thiết kế giao diện mới, họ bê nguyên giao diện máy calculator có sẵn lên đây.

Đây là ứng dụng la bàn đầu tiên trên điện thoại, ra đời trên iPhone 2007. Nó bê y chang cái la bàn thật: khung gỗ, nền gỗ, viền kim loại chrome, bê gần như y chang toàn bộ. Nhưng sau này họ nhận ra viền kim loại, nền gỗ hơi cầu kỳ, hơi đáng. Họ strip hết, chỉ giữ lại mặt số và mũi tên, cho ra phiên bản la bàn hiện đại tối giản. Căn bản là mượn những cái signature nhất của la bàn — những cái mà người dùng dựa vào để định hướng (mặt số, kim) — họ mượn đem qua. Còn những thứ không phải signature như mặt kim loại, nền gỗ, không quan trọng nên họ bỏ.

Điều này cũng gây tranh cãi, khá controversial. Có người thích sự tối giản, nói thiết kế vậy là ok, hiện đại. Có người nói thiết kế vậy nhìn nhàm chán, họ thích retro, vintage, có sự kết nối với thế giới thật. Nhưng ý tưởng quan trọng nhất là chúng ta mượn những cái quan trọng nhất của đối tượng vật lý.

### Metaphor về cách tương tác

Trên đây là những metaphor liên quan tới cách thể hiện đồ họa. Nhưng cũng có metaphor liên quan tới cách tương tác. Ví dụ, nếu bạn nào từng chơi bong bóng hồi nhỏ, các bạn hay xem bong bóng có khả năng bị lủng hay không — thường kiểm tra xem có răng cắn không. Mình hay nói lúc nhỏ là xem bong bóng có mặt răng hay không, banh bong bóng ra xem có lỗ tiềm ẩn không. Khi banh miếng cao su ra, chi tiết trên miếng cao su đó to lên, stretch ra. iPhone và các thiết bị di động lấy ý tưởng đó làm pinch to zoom — muốn xem chi tiết nào đó to, pinch cái là zoom.

Ở đây chúng ta vay mượn metaphor không phải cách thể hiện mà vay mượn cách tương tác. Thông thường chúng ta tập trung nhiều vào yếu tố thể hiện hình ảnh đồ họa mà bỏ qua tương tác, nhưng tương tác lại là những phát minh tạo điểm nhấn cho sản phẩm.

Hoặc AirDrop trên iPhone — căn bản là chuyển file từ điện thoại này sang điện thoại kia. Chuyển file không có gì mới, Zalo cũng chuyển file được. Nhưng cách AirDrop cài đặt, cách cho phép người dùng tương tác — hai điện thoại tương tác với nhau để chuyển file — vay mượn hình ảnh cầm vật gì đó đưa cho người đối diện. AirDrop: các bạn hay lấy hai điện thoại trao đầu với nhau, tạo hiệu ứng phần chạy từ bên này qua bên kia. Đó là metaphor.

Khi thanh toán, sau khi đọc hóa đơn xong — khi thanh toán xong hóa đơn, có hình cái hóa đơn ảo chạy ngược lên trên. Nó chạy tới đâu thì phần phía trên in ra tới đó, để người dùng biết tiến độ.

### Ví dụ: Bằng lái số Phần Lan

Đây là một ví dụ khác về ứng dụng bằng lái ảo số hóa ở Phần Lan. Bằng lái ở châu Âu và Việt Nam tích hợp rất nhiều thông tin ID, có thể dùng như căn cước công dân. Ở châu Âu, có thể đi từ quốc gia này sang quốc gia khác không cần passport, chỉ cần bằng lái.

Phần Lan năm 2015 có project số hóa bằng lái trên ứng dụng di động. Công ty HiQ — một design firm rất nổi tiếng ở Bắc Âu — đứng ra nhận thầu. Nhiệm vụ của nhóm thiết kế không chỉ là số hóa chữ, mà bằng lái làm dạng thẻ cứng — thẻ cứng có vân khác nhau, in nhiều lớp, tùy góc nhìn nghiêng sẽ thấy vân ẩn ở dưới. Màn hình điện thoại làm sao thấy được vân đó? Làm sao làm được nhiều lớp? Project này muốn replicate tất cả tính chất của bằng lái vật lý sang điện thoại. Cách họ làm là sử dụng rất nhiều sensor của điện thoại để detect góc nhìn của người dùng, để render các vân. Đây là một trong những đỉnh cao của việc tận dụng công nghệ để tạo ra metaphor của bằng lái. Sử dụng rất nhiều sensor để tạo trải nghiệm thấy được vân ẩn. Yêu cầu rất khó, nhìn có vẻ nhỏ nhưng về mặt design rất khó. Khi làm sản phẩm đôi lúc người ta yêu cầu tới mức như vậy.

## VIII. UI Design Process

Bây giờ chúng ta sẽ nói về quy trình thiết kế User Interface / User Interaction, gọi là UI Design Process. Chúng ta sẽ đi qua nhiều dạng quy trình khác nhau, có quy trình học để biết, quy trình học để làm.

### Design là gì?

Trước khi nói về quy trình thiết kế UI, chúng ta phải hiểu design là gì. Design bản thân nó là quy trình tạo ra hoặc định hướng tool, artifact, mà mục tiêu phục vụ việc sử dụng trực tiếp của người dùng. Artifact là sự kết hợp từ "artificial" (do con người tạo ra) và "fact" (những cái hiện hữu). Artifact là những cái hiện hữu do con người tạo ra, nhưng không phải random ngẫu nhiên, mà tạo ra để phục vụ mục tiêu sử dụng trực tiếp của con người. Nên design là quy trình.

Mà quy trình thì có các bước, thứ tự các bước. Input của bước này là output của bước kia, step by step. Mục tiêu của quy trình là creative endeavour — chúng ta đang tạo ra cái mới. Nếu các bạn chỉ đơn giản thấy "hôm nay tôi cần thiết kế giao diện website này, tôi biết có website bán hàng tương tự, tôi clone giao diện đó về" — lúc đó không gọi là design nữa, gọi là reproduction, sản xuất lại sản phẩm. Design là phải tạo ra cái mới. Cái mới phát sinh thông qua việc thấy rằng cái cũ không giải quyết trọn vẹn vấn đề người dùng đang gặp phải. Cùng là website bán hàng, nhưng sản phẩm khác, phân khúc khách hàng khác. Nên clone toàn bộ design bên kia về xài không được. Chúng ta phải thay đổi design để phù hợp với mặt hàng và đối tượng khách hàng. Đó mới là design.

Nên design là creative endeavour. Sản phẩm của creative endeavour này là tangible things — cụ thể, người dùng có thể cầm nắm, thấy, tương tác, trải nghiệm. Mục tiêu trải nghiệm đó cuối cùng để phục vụ con người. Quy trình này luôn đặt con người vào trung tâm.

### Thuộc tính của Design

Một số thuộc tính của design:

**1. Đặt con người vào trung tâm.** Nghe có vẻ lý thuyết, nhưng không thấm được điều này thì học môn này không thích. "Đặt con người trung tâm" nghe đơn giản lắm, nhưng tới hồi làm thì các bạn toàn thích làm kiểu mình thích chứ không thực sự đặt người dùng vào trung tâm — đặt câu hỏi "cái này phục vụ người dùng như thế nào?", test người dùng ra sao để biết có thực sự giải quyết vấn đề hay không.

Creative. Như đã nói, đơn giản chỉ clone UI có sẵn là không creative. UI có sẵn có thể giải quyết vấn đề của người dùng khác, nhưng chúng ta có đối tượng khác, bài toán khác, phải cân nhắc UI mới.

**2. Design là conversation với material.** Quan trọng: design là conversation giữa người designer với material, nguyên vật liệu họ đang có. Design là câu chuyện giữa designer và môi trường. Designer phải biết nguyên vật liệu họ đang cầm có ưu nhược điểm gì. Thiết kế trên điện thoại khác với thiết kế trên tablet hay laptop như thế nào. Điện thoại có ưu nhược điểm gì so với tablet hay laptop?

Ví dụ đơn giản: thử mở Google Maps trên điện thoại và trên laptop. Tìm đường về nhà, xem flow khác nhau thế nào. Mô tả flow tìm đường trên Google Maps trên điện thoại — từng bước một. Mở app lên, làm gì? Trên laptop thì khác — phải set điểm bắt đầu ở đâu. Trên laptop có GPS thì không nói, nhưng laptop không có GPS thì phải set điểm bắt đầu. Còn điện thoại sẽ để đi từ vị trí hiện tại. Chúng ta phải hiểu sự khác biệt về material: điện thoại có GPS, laptop không có GPS. Điều đó ảnh hưởng tới flow của người dùng khi tương tác UI. Những chi tiết nhỏ nhưng chúng ta phải nắm được — phải biết thiết bị đang hướng tới có thể làm gì và không làm gì.

Ví dụ làm app báo thức trên laptop — chỉ có thể báo thức qua speaker, cùng lắm thêm animation trên màn hình. Nhưng app báo thức trên điện thoại — ngoài speaker còn rung, thậm chí bật flash. Giả sử để trong phòng tối, rung hoài không dậy thì bật flash sáng lên. Chúng ta phải biết thiết bị triển khai có khả năng gì để tận dụng, và cũng phải biết nhược điểm của nó. Không thể bê hoàn toàn giao diện desktop lên điện thoại — điện thoại màn hình nhỏ, dọc, trong khi desktop lớn, ngang.

Chúng ta phải biết ưu nhược điểm của material để vận dụng khả năng và khắc phục nhược điểm.

### Design vs Engineering

Một số thuộc tính khác của design: người làm design khác người làm engineer. Giống như kỹ sư xây cầu — ngày nhận dự án, tiếp nhận bản thiết kế và hiện thực hóa nó. Còn kiến trúc sư — trước mặt không phải là cái cầu, trước mặt là con sông. Cần xây cầu bắc ngang con sông, phải đặt những câu hỏi gì? Mỗi bạn sẽ đặt câu hỏi.

Giả sử các bạn ở vị trí kiến trúc sư cần thiết kế cây cầu bắc ngang sông, các bạn sẽ đặt câu hỏi gì để đưa ra thiết kế? Giấy xây dựng chưa? Câu hỏi là giấy xây dựng có nhiều yếu tố như: chất liệu gì? Mực nước sông cao nhất lên bao nhiêu? Tải trọng tối đa cầu chịu được bao nhiêu? Hình dạng cầu như thế nào? Cầu dành cho ai, đi từ đâu tới đâu? Thời gian dự kiến hoàn thành? Kinh phí để xây cầu? Thời tiết xung quanh?

Khi đặt câu hỏi, phải đặt câu hỏi gốc rễ chứ không phải bề mặt qua dự án. Những câu hỏi mang tính gốc rễ: cây cầu này làm gì? Lưu lượng xe đi qua thế nào? Phương tiện nào đi ngang nó? Thậm chí câu hỏi đầu tiên: đặt cây cầu này chỗ nào? Hai bên bờ sông dài mười mấy cây số, tại sao chốt chỗ này mà không phải chỗ kia? Để chốt vị trí, phải quan tâm lưu lượng, khoảng cách hai bên bờ, dòng chảy, nền đất, yêu cầu bảo vệ hệ sinh thái. Ví dụ dưới đất có rừng, có động vật quý hiếm được bảo vệ — đặt cầu ở đây coi như phá hủy hệ sinh thái. Mực nước đi ngang khu vực cầu trong năm ra sao? Không ai muốn đặt cầu ở chỗ chi phí đào móng quá sâu, đội vốn. Cũng phải cân nhắc tàu bè đi ngang — loại tàu bè nào, chiều cao thông thường ra sao.

#### Case study: Cầu Phú Mỹ và Cầu Gothenburg

Các bạn có biết tại sao cầu Phú Mỹ hay gây tai nạn không? Vì không độ (khoảng không gian bên dưới cầu) quá cao, nhưng hướng đổ về phía Quận 2 lại ngắn — cầu quá dốc. Xe container đổ xuống, mà container ở Việt Nam nhập về đã 20 năm tuổi, bên Trung Quốc bỏ xài rồi nhập về. Xe 20 năm tuổi, xác định chạy hết công suất, không có thời gian bảo trì, lại chở hàng nặng, thường quá tải. Xuống dốc như vậy, thắng phanh hư là chuyện bình thường. Mà tại sao không độ cao như vậy? Vì bên dưới cầu Phú Mỹ, đôi lúc có sà lan container chất cao vút lên. Khi thiết kế cầu phải đảm bảo cầu đủ cao để sà lan đi ngang.

Nên thiết kế độ cao cầu phải xem tàu thuyền đi phía dưới độ cao thế nào. Nó dẫn tới các giải pháp thiết kế khác nhau. Việt Nam xây cầu cao lên. Nhưng ở Gothenburg (Thụy Điển) — thành phố cảng, tàu bè đi lại rất nhiều, có cây cầu nối hai bờ ngay trung tâm. Họ thấy không thể xây không độ quá cao, vì nếu xây quá cao, cầu sẽ rất dài hai bên và cắm thẳng vô trung tâm thành phố, ảnh hưởng giao thông. Họ buộc phải xây cầu với không độ không quá cao, vì ước lượng 90% tàu bè có chiều cao thấp hơn không độ đó. Nhưng vẫn có 10% tàu bè cao hơn — giải pháp của họ là thiết kế cầu có thể bật ra, chẻ đôi ra khi cần. Tính năng đó phục vụ 10% trường hợp tàu bè có cổng cao quá. Có những buổi sáng đi làm, thấy xe xếp hàng là biết — cầu bật ra cho tàu bè đi qua, tàu bè đi qua xong cầu ráp lại.

Các bạn thiết kế cầu phải cân nhắc rất nhiều yếu tố. Designer chính là kiến trúc sư. Các bạn phải envision những possibilities, những khả năng khác nhau, những khả năng mới hoàn toàn mà chưa ai nghĩ tới. Các bạn phải đưa ra tầm nhìn, envision nó. Và phải cân nhắc nhiều khả năng để ra quyết định. Có rất nhiều cách thiết kế cầu — tại sao hình dáng này mà không phải vòng lên, vòng xuống? Tại sao cao thế này, không phải thấp hơn hoặc cao hơn? Tại sao hình dạng này mà không phải cầu văng?

Nhiệm vụ của designer là nghĩ đến tất cả các cách thiết kế khác nhau có thể để giải quyết vấn đề, và lựa chọn option tối ưu nhất. Trong quá trình nghĩ ra các option, các possibilities và đưa ra quyết định, lúc nào cũng gặp nhu cầu của con người — nhu cầu của chủ đầu tư, nhu cầu của người đi trên cầu. Ngoài khả năng vận chuyển, cầu có thể phục vụ du lịch. Cầu Rồng Đà Nẵng — thiết kế con rồng có khả năng phun lửa, không chỉ kết nối hai bờ, giao thông thông suốt, mà còn phục vụ du lịch, chụp hình. Đặt vị trí thế nào để chụp đẹp? Nếu hai bên bờ toàn nhà ổ chuột, không quy hoạch chỉnh chu, chụp lên không được đẹp. Đó là thực tế, ảnh hưởng tới quyết định thiết kế.

Và lúc nào cũng dựa trên quy trình. Làm thế nào để ra quyết định chốt thiết kế? Chốt thiết kế đó phải test ở các mức độ, đưa vào thực tế. Phải có quy trình từng bước — test ở small scale, test large scale, rồi mới deploy.

### Design vs Art

Và thiết kế khác nghệ thuật. Nhiều người nghĩ thiết kế là vẽ tranh nghệ thuật — buồn cười chứ. Thiết kế và nghệ thuật có hai mục đích khác nhau. Thiết kế phục vụ chuyện con người sẽ xài nó thế nào. Nghệ thuật không đặt câu hỏi người ta sẽ xài nó thế nào. Ví dụ một góc nghệ thuật chưa hẳn làm đúng nhiệm vụ của nó — có thể là sản phẩm nghệ thuật nhưng chưa chắc là thiết kế tốt. Cái khó của người làm thiết kế là vừa đảm bảo người dùng xài được, vừa đảm bảo yếu tố thẩm mỹ, thu hút. Cái khó là bỏ bớt đi chứ không phải thêm vào.

### Waterfall Model

Về mô hình thiết kế, mô hình kinh điển truyền thống nhất là waterfall — lấy requirement, thiết kế, cài đặt, test, triển khai. Nhưng bây giờ chả ai xài waterfall. Ở mô hình này, test phút cuối, nếu có lỗi quay lại chỉnh sửa, tốn rất nhiều chi phí.

Nguyên tắc của Schneiderman: phải lúc nào cũng thu thập và test thông tin, test người dùng nhanh nhất có thể. Đây là lý thuyết. Cái chúng ta sẽ làm là quy trình đơn giản: đưa thiết kế, implement nhanh nhất có thể, evaluate nhanh nhất có thể, chỉnh sửa thiết kế, cứ đọc đi đọc lại. Đi từ tính năng nhỏ tới mở rộng. Đảm bảo mỗi tính năng khi thiết kế ra phải test với người dùng và chỉnh sửa trước khi scale up giải pháp và đưa ra tính năng mới.

### Spiral Model

Đây là spiral process hoặc spiral model mà các bạn sẽ sử dụng. Từ công đoạn lên concept, phát triển từng tính năng nhỏ, prototype tính năng nhỏ, test với người dùng, chỉnh sửa, phát triển tiếp, thực hiện tiếp. Cứ mỗi vòng lặp: một là chỉnh sửa tính năng đã có để cải thiện, hai là nếu đã fix rồi thì mở rộng, thêm tính năng mới.

Spiral model: design, implement, evaluate. Mỗi bước tùy process trong quy trình. Ở giai đoạn đầu, làm prototype rẻ, nhanh, test nhanh concept, ý tưởng — đó là paper prototype, sketch, quick prototyping tools. Làm prototype của nhiều ý tưởng khác nhau cùng lúc để test. Nói dễ nhưng tới hồi làm có xu hướng stick vô một design, bám vô đó, không explore nhiều design khác nhau. Trong khi ý tưởng của design là phải prototype nhiều ý tưởng cùng lúc để test. Đảm bảo sau mỗi vòng lặp design đã được improve, tốt hơn vì đã test với người dùng, phát hiện lỗi.

#### Lỗi thường gặp: Ngại test với người dùng

Đây chính là lỗi của mọi người: ngại test với người dùng. Mọi người thường nói "dạ em test rồi" — test với ai? Thành viên trong nhóm. Design ra rồi tự test — đó là thói quen. Thường lười test với người ngoài. Nhưng test với người ngoài sẽ thấy những insight rất thú vị, những phát hiện thú vị để design trọn vẹn, hoàn hảo hơn.

User center design còn gọi là participatory design — quy trình thiết kế có sự tham gia của người dùng. Ở mỗi bước ra ý tưởng thiết kế phải test với người dùng ngay lập tức, xem người dùng hiểu chúng ta đang thiết kế gì hay không. Hoặc cho người dùng xài có như kỳ vọng không. Phân tích hành vi và improve. Quy trình involve user trong quy trình, user đóng vai trò evaluator đánh giá giải pháp. Ưu điểm: lúc nào cũng có user tham gia, phát hiện vấn đề trải nghiệm từ sớm, chỉnh sửa. Nhược điểm: tốn thời gian, tốn chi phí, không phải lúc nào cũng tìm được user để test.

### 5-Stage Design Process (Apple)

Đây là quy trình gồm 5 stage. Stage đầu tiên là investigation hoặc user research — công đoạn hiểu nhiều nhất về người dùng, xác định vấn đề, ideate các ý tưởng giải quyết vấn đề. Có ý tưởng rồi thì prototype — thể hiện ý tưởng thành tangible things để người dùng trải nghiệm, biết nó là gì. Tangible things không chỉ minh họa ý tưởng mà còn evaluate trực tiếp với người dùng để biết thiết kế có hiệu quả hay không.

Mỗi stage có goal riêng:
- Investigate: hiểu người dùng sâu nhất có thể, mọi thứ, mọi khía cạnh.
- Idea: không chỉ đưa ra ý tưởng hay nhất, mà bước đầu tiên là có nhiều ý tưởng nhất. Đây là vấn đề thường gặp: chúng ta hay pick ý tưởng phổ biến nhất. Ví dụ thiết kế ứng dụng xem tin tức thể thao, pick app phổ biến nhất và stick vô design đó — nhưng đó không phải design. Design là explore. Tính năng tóm tắt tin tức trong tuần — phải nghĩ ra ít nhất 3-4 thiết kế khác nhau. Tính năng xem lại trận đấu bóng đá, bóng rổ — phải nghĩ ra nhiều thiết kế khác nhau.
- Prototype: tạo ra tangible things, thông qua đó xác định challenge trong việc test giải pháp, phát hiện những điều không biết được nếu chỉ vẽ trên giấy.
- Evaluate: phát hiện vấn đề, đánh giá tiến độ, xác định bước tiếp theo.

Quy trình này là của Apple. Apple nổi tiếng về sự linh hoạt. Có thể từ bước investigate nhảy thẳng qua prototype, trước khi qua idea. Cách nào test nhanh nhất ý tưởng đó, fail, chỉnh sửa lại.

Trong môn này, quy trình đơn giản hơn. Proposed project sẽ có chủ đề cho các bạn. Các bạn làm user research để phân tích một cách nghiêm túc — phải đi phỏng vấn, quan sát người dùng thực tế, chứ không chỉ tự đóng vai bản thân là người dùng. Các bạn được quyền làm chuyện đó nhưng một mình là không đủ — chỉ là góc nhìn chủ quan. Phải chứng minh người dùng là ai, càng nhiều càng tốt. Câu chuyện không chỉ là bao nhiêu người mà còn phỏng vấn sâu tới mức nào. Với mỗi người, phỏng vấn tối thiểu 10-15 người. Phỏng vấn chất lượng tối thiểu — thầy làm thường khoảng 1 tiếng mỗi buổi. Số lượng tùy, phỏng vấn 5 người cũng không sao, nhưng chất lượng buổi phỏng vấn mới quan trọng.

Còn quan sát nữa — thầy đánh giá cao quan sát lắm. Quan sát là kỹ năng cực kỳ quan trọng trước khi nói chuyện với phỏng vấn. Rồi đưa ra sketch sơ bộ, generate càng nhiều sketch càng tốt, đánh giá với người dùng, phát triển high-fidelity prototype.

Các bạn sẽ không chỉ một prototype là xong — phải có nhiều prototype.

## IX. IDEO Case Study — Thiết kế xe đẩy siêu thị

Bây giờ xem video này. Video quay ở công ty IDEO — công ty design lớn nhất thế giới hiện giờ. Thành lập năm 1980 (cuối 1980) bởi Tom Kelly và John Kelly. Trước khi IDEO thành lập, design thường được thực hiện in-house. IBM có nhóm thiết kế riêng, Apple có nhóm thiết kế riêng. Nhưng vấn đề là nuôi nhóm thiết kế riêng chi phí cao. Nếu công ty không có nhu cầu thiết kế thường xuyên thì rất phiền. Nhóm thiết kế in-house đôi lúc bị saturated — bão hòa về ý tưởng, vì làm việc in-house không à. IDEO đặt câu hỏi: tại sao việc thiết kế không làm outsource? Họ là đơn vị outsource thiết kế — thiết kế mọi thứ, từ bàn chải đánh răng tới máy tính, máy chẩn đoán y tế. Vũ khí của họ là design thinking, quy trình thiết kế. Với quy trình đó, họ thiết kế mọi thứ.

Đài ABC làm phim tài liệu về IDEO, họ đưa ra thử thách: trong 5 ngày hãy thiết kế lại một vật bình thường nhất — xe đẩy siêu thị. Họ đi theo IDEO suốt 5 ngày để quay lại hoạt động, xem IDEO ứng dụng design thinking, quy trình thiết kế như thế nào. Tất nhiên IDEO đang thiết kế sản phẩm chung chung, nhưng trong project này chúng ta hướng tới digital solution. Tuy nhiên thầy tin chúng ta hoàn toàn có thể áp dụng kỹ thuật của IDEO vào bài toán thực tế.

[Video: "Tonight, the Deep Dive. Welcome to the supermarket for innovation..."]

Khi họ chính thức đi thực địa, họ tìm hiểu nguồn online, báo chí, document, và đem luôn xe đẩy siêu thị về phân tích. Họ xem vấn đề nào người ta hay quan tâm nhất, báo chí đề cập nhiều nhất, để có cái nhìn tổng quan trước khi đi sâu chi tiết. Critical issues trong xe đẩy siêu thị — setting của nó như thế nào. Họ biết có bao nhiêu ngàn người bị thương, xe đẩy bị thế nào, người sử dụng thế nào. Nhưng những report đó không có, họ phải đi thực tế. Tuy nhiên, họ có kiến nhìn tổng quan.

Thời gian ở siêu thị rất dài. Ở Mỹ đất rộng, đẩy xe 30-40 mét trên bãi đất rộng, gió thổi. Đó là thử thách khi thiết kế xe đẩy siêu thị — phải hỗ trợ những người đó thế nào, không chỉ người đi siêu thị. Thể hiện cách nhìn tổng quan, comprehensive về đối tượng người dùng và vấn đề họ gặp phải.

Khi đi, họ phải có máy chụp hình. Thầy cũng kỳ vọng các bạn làm tương tự — có máy chụp hình, ghi lại những điều hay, hành vi thú vị. Các bạn cứ nhớ người dùng gặp vấn đề gì. Nếu không, 1-2 ngày còn nhớ, tuần sau quên. Nhưng chụp hình thì nó luôn ở đó, khi design nhìn lại biết người dùng gặp vấn đề gì.

Xe đẩy siêu thị để chở đồ, nhưng người ta vẫn dùng nó để... ngồi. Nhu cầu của người dùng đi siêu thị và lên xe đẩy là có. Chúng ta không thể bỏ qua. Phải thiết kế lại xe đẩy để hỗ trợ tính năng này.

Họ thấy có điều: nhiều người để xe đó rồi đi shopping chỗ khác, mua xong mới quay lại để đồ lên xe. Tại sao có thói quen đó? Đẩy xe cồng kềnh, xe to, đi trong siêu thị có nhiều ngõ ngách, quẹo rất phiền, nhất là đông người. Thường họ đậu xe ở chỗ và đi shopping. Nếu redesign lại xe thì phải design như thế nào? Những điều này các bạn quan sát thực tế là hiểu.

Đây là user trend thú vị. Họ thấy đường đất xẹp — những use case thú vị. Khi thiết kế xe đẩy không nghĩ tới nhưng thực tế người dùng sẽ làm điều đó. Chúng ta phải chấp nhận sự tồn tại đó và thiết kế xe đẩy phù hợp.

Đội đã làm việc 9 giờ liên tục. Mantra của IDEO về innovation được viết khắp nơi: "One conversation at a time. Stay focused. Encourage wild ideas. Defer judgment. Build on the ideas of others." Điều khó nhất là kiềm chế không chỉ trích ý tưởng. Họ brainstorming, các ý tưởng được post lên tường.

Họ chia mỗi nhóm một bài toán nhỏ, cụ thể. Mỗi nhóm tập trung thiết kế giải quyết bài toán đó, sau đó tổng hợp lại các giải pháp vô sản phẩm cuối cùng. Thầy kỳ vọng các bạn làm tương tự. Ví dụ sản phẩm có nhiều tính năng, mỗi nhóm tập trung vô một vấn đề, giải quyết thật tốt, rồi tích hợp. Môn này không cần thiết kế hệ thống 7-8 tính năng — chỉ cần 2-3 tính năng nhưng giải quyết 2-3 vấn đề chưa được giải quyết thực sự. Các bạn nên chọn bài toán còn không gian để giải quyết. Đừng chọn bài toán kiểu form đăng nhập, không thể làm cái mới được.

Prototype đầu tiên của họ là modular shopping cart — nhiều vỏ nhỏ để người dùng có thể linh hoạt. Bây giờ ở Aeon đang dùng loại xe đẩy modular shopping cart — khung xe, và người dùng chọn để bao nhiêu vỏ (tối đa 2-3 vỏ). Đó là sự phát triển từ ý tưởng này.

Họ có ý tưởng scanner trên xe đẩy — khách hàng tự scan từng món khi lấy khỏi kệ. Các bạn đi siêu thị mua đồ cả tuần, có budget 1 triệu chẳng hạn — mua xong tới hồi thanh toán không biết tổng cộng bao nhiêu. Lúc đó, một là cắn răng trả thêm, hai là xin trả lại bớt. Rất phổ biến. Hồi đi du học Pháp, có học bổng, mỗi tuần chỉ chi 50 euro tiền ăn. Lúc đầu không có công cụ kiểm soát, mỗi lần mua xong thường dư ra 60-70 euro.

Scanner là giải pháp. Sau này nó trở thành sản phẩm thực tế: scanner cầm tay. Đăng ký thành viên siêu thị, được cấp barcode. Vô siêu thị, ghé quầy lấy scanner, quét barcode, máy random assign cho bạn. Cầm scanner đi mua đồ, scan code từng món — biết giá chính xác, thấy tổng tiền, quyết định mua thêm hay không. Khi thanh toán, không cần cashier, đi thẳng vô quầy tự động, cắm máy vô, tất cả thông tin tự động nhập, quẹt thẻ thanh toán, đi về. Mọi thứ rất nhanh. Thầy đã xài từ 2011-2012 ở Pháp.

Ý tưởng đầu tiên của họ là gắn scanner trên tay đẩy. Phiên bản đầu tiên của scanner — đâu có lập trình gì đâu, chỉ làm cục boot, cục soft, vẽ minh họa lên. User Interface mà, chưa cần lập trình — minh họa cho người ta biết tương tác thế nào, hiển thị thông tin gì.

Một ý tưởng khác: child safety. Một ý tưởng khác: shopper có thể nói chuyện với nhân viên siêu thị từ xa. Đi siêu thị không biết mặt hàng ở quầy nào — phải hỏi nhân viên, phải kiếm người mặc đồng phục. Ý tưởng của họ: thay vì đi tìm, có bộ đàm gọi nhân viên. Và họ prototype bộ đàm bằng cái gì? Dùng đồ chơi (toy). Đây là graphic prototyping — biến ý tưởng thành sản phẩm nhanh nhất, chi phí thấp nhất, người ta hiểu được ý tưởng. Dùng đồ chơi (toy) chính là principle trong process của chúng ta.

Phiên bản cuối cùng của scanner chuyển thành máy cầm tay. Trong quy trình user centered design, lúc nào cũng phải làm việc với user. Những phiên bản đầu tiên có thể là thành viên trong nhóm review design, nhưng càng về sau cần user bên ngoài — họ mới có khách quan và review feedback cho tiến độ project.

Nguyên tắc của nhóm thành công: lúc nào cũng phải đặt mục tiêu rất cụ thể cho project, sản phẩm. Chúng ta muốn giải quyết vấn đề gì cũng được. Nếu không đặt vấn đề cụ thể, chúng ta sẽ rơi lại tình trạng mơ hồ.

[Trao đổi về điểm số, bài thi, hình thức tốt nghiệp]

Chúng ta bây giờ sao? Lời khuyên của thầy cho các bạn: đừng chọn option dễ mà làm, hay chọn option khó mà làm. Đề khuyến nghị chân thành.

## X. User Research

Bây giờ chúng ta sẽ nói về user research và phân tích người dùng. Bài này chắc phải làm 2 buổi. Phần user research này là thu thập càng nhiều dữ liệu về người dùng càng tốt. Sau khi thu thập dữ liệu, chúng ta hình thành bức tranh về họ — bức chân dung toàn diện nhất có thể. Phải hiểu thật sâu về người dùng mới biết họ đang gặp vấn đề gì, muốn giải quyết vấn đề gì.

Khi nghiên cứu người dùng xong, ít nhất phải hiểu về họ những điều sau: tuổi tác, giới tính, văn hóa, ngôn ngữ, trình độ học vấn, kiến thức về lĩnh vực chuyên ngành, kiến thức về các mảng khác trong cuộc sống, tần suất sử dụng máy tính, tần suất sử dụng công cụ trong công việc, vấn đề về khả năng vật lý (cận, vấn đề về màu sắc, đi lại, nghe...), vấn đề về khả năng xử lý của não bộ. Trình độ giáo dục, trình độ phỏng vấn, động lực trong cuộc sống. Động lực quyết định mục tiêu cuộc sống, mục tiêu ảnh hưởng việc họ làm gì để đạt được. Và để làm công việc đó, họ đang làm công việc gì, môi trường làm việc ra sao, họ sử dụng những công cụ gì. Với công cụ đó thì họ làm được gì và không làm được gì. Mối quan hệ xã hội của họ, quan hệ đó ảnh hưởng tới cuộc sống công việc hàng ngày thế nào.

Nghe chung chung, nghe nhiều quá, nhưng tất cả đều ảnh hưởng tới hành vi người dùng. Hành vi đó là cái chúng ta khai thác để thiết kế giải pháp.

Mô tả đối tượng người dùng gồm: thông tin chung (tuổi tác, nghề nghiệp), thông tin cụ thể về môi trường làm việc, công việc chính, mục tiêu chính trong cuộc sống hàng ngày, tại sao họ quyết định làm điều gì đó. Mục tiêu trong công việc, mục tiêu trong cuộc sống.

Ví dụ: không phải ai chạy xe công nghệ cũng vì tiền. Có những người là công chức về hưu, có lương hưu đàng hoàng, con cái không phải lo. Ở nhà buồn quá nên đăng ký chạy để có người nói chuyện hàng ngày. Với người đó, tính năng họ ghét nhất trên app là tính năng yên lặng trên xe — vì mục tiêu của họ là giao tiếp xã hội.

Giống trường mình có cô lao công. Lý do cô làm lao công 13 năm? Nhà có 3 căn mặt tiền cho thuê. Cô làm lao công ở trường đại học vì thích môi trường này — lịch sự, tiếp xúc với giảng viên, sinh viên. Đi làm chỉ vì tương tác xã hội. Năm 2023 cô nghỉ vì đi định cư.

Nên không phải ai chạy xe công nghệ cũng vì tiền. Không phải ai làm lao công cũng vì tiền. Chúng ta phải biết bức tranh người dùng là ai. Những điều đó phải phỏng vấn, khảo sát, nói chuyện với họ mới ra được.

### Kỹ thuật User Research

Làm user research giống như làm bạn, hỏi, hiểu hết về cuộc sống của họ. Tại sao họ làm công việc này? Động lực là gì? Và để làm công việc này, họ đang sử dụng gì?

Kỹ thuật user research: quan sát, record, interview, questionnaire. Questionnaire thường không cho dữ liệu thực sự về cuộc sống. Mỗi năm các bạn làm khảo sát môn học, dành bao nhiêu thời gian? Một câu multiple choice — click, click — không quá 2 phút. Làm sao kỳ vọng questionnaire cho insight về cuộc sống? Công cụ này ít đáng tin cậy. Preferred: observation, substantive interview. Có thể record behavior của người dùng khi tương tác với hệ thống. Thường kết hợp tất cả.

Cái khó của người làm kỹ thuật: thầy biết các bạn không tự tin về giao tiếp xã hội. Nếu thích giao tiếp xã hội đã đi học Kinh tế hoặc Ngôn ngữ văn, không chui vô lĩnh vực này. Nhưng với sự phát triển công nghệ hiện giờ, người làm công nghệ không thể giam mình với máy tính. Trước đây người ta trả tiền code 8 tiếng/ngày. Bây giờ có AI code, vị trí của engineer là biết cái đó giải quyết vấn đề gì cho người dùng. Engineer muốn hay không cũng phải bước ra xã hội, nói chuyện với người ta, xác định vấn đề, biết giá trị mình làm.

Thầy đang tham gia chương trình Sài Gòn AI Hub — initiative của PNJ kết hợp với ĐHQG, ươm tạo dự án AI. Google vô làm tư vấn. Khi nói chuyện với người Google, họ luôn hỏi: "Nghiên cứu này ứng dụng vô use case nào? Commercialize thế nào?" Đều là engineer, nhưng bây giờ họ quan tâm những điều đó. Engineer không thể ở trong vùng an toàn chỉ tập trung code — phải mở rộng. Thầy phải đi gặp sếp công ty này, công ty nọ để xem áp dụng giải pháp nghiên cứu vô ngữ cảnh nào. Bắt đầu từ nhu cầu của họ, customize giải pháp.

Quy trình cuối cùng là hiểu người dùng để trả lời câu hỏi: What needs to be done? Người dùng muốn làm gì? Để làm điều đó, họ đang làm gì, trong điều kiện nào, môi trường thế nào, công cụ gì, họ làm được gì, không làm được gì? Với những thứ họ không làm được, họ đang dùng trick, tip gì — thuật ngữ gọi là hacks hoặc workarounds. Các bạn phải xác định những điều đó mới biết thiết kế cái gì.

### Ba loại Model phân tích hành vi

Có ba loại model chính để mô hình hóa hành vi người dùng:

**Flow model:** cung cấp bức tranh tổng quát nhất về người dùng, hoạt động họ đang thực hiện và stakeholder trong ecosystem xung quanh. Ví dụ: flow model với nhân vật chính là giảng viên. Công việc: soạn slide môn học và post lên trang web chia sẻ, trình bày. Quá trình soạn slide cần access một số nguồn tài nguyên: slide library, ổ cứng, internet. Để lên internet tìm hình ảnh video minh họa — internet đâu phải ngẫu nhiên tồn tại, phải có người upload — colleague professor upload tài nguyên. Xuất hiện nhân vật thứ hai. Rồi media service để request media. Sau khi soạn xong slide, up lên kênh trang web môn học, trình diễn slide cho sinh viên.

Đây là bức tranh tổng quát để thấy hoạt động của user và đối tượng involved. Trong bức tranh có các mũi tên — đó là breakdown. Breakdown là vấn đề, incident làm cho việc thực hiện tác vụ bị cản trở. Giống như chạy xe, không biết đường — phải tìm bản đồ. Search đường đi, chuyển sang navigation board, nhìn đường, cố nhớ, bỏ điện thoại vô túi chạy. Một đoạn không nhớ — dừng lại lấy điện thoại. Đó là breakdown. Trong global flow, phải chú ý breakdown — nó cho biết giới hạn của công cụ người dùng đang sử dụng. Và còn workarounds nữa.

**Sequence model:** Flow model cho bức tranh tổng quát, nhưng chưa trả lời chi tiết: khi làm một tác vụ có những bước nào? Hồi nãy search đường Google Maps trên điện thoại và laptop — mô tả từng bước. Bước đầu: điền địa điểm cần đi, chọn navigation search, chọn get directions. Trên laptop phải xác định thêm bước bắt đầu — vì laptop không có GPS. Liệt kê từng bước gọi là sequence model. Vẽ sequence model mới biết bước nào để làm gì, có cần thiết không. Kiểm tra: trên laptop phải điền địa điểm khởi đầu vì không có GPS. Trên điện thoại có GPS — có cần cho người dùng điền địa điểm khởi đầu không? Không. Liệt kê từng bước và đặt câu hỏi: bước này có cần thiết không? Nếu không, làm cách nào xóa bỏ nó? Mục tiêu là làm cho người dùng thực hiện tác vụ hiệu quả hơn, ngắn hơn.

**Cultural model:** Mô hình này ít phổ biến hơn, nhưng nếu đi làm sản phẩm, phát triển sản phẩm lâu dài thì phải quan tâm. Phải biết người dùng sống trong mối quan hệ xã hội thế nào, chịu ảnh hưởng bởi cộng đồng văn hóa gì, và cộng đồng đó ảnh hưởng hành vi họ ra sao. Từ đó quyết định thiết kế thế nào. Giống như thiết kế giao diện cho người Trung Quốc thế hệ 60 tuổi — yêu cầu sẽ khác thế hệ mới. Hoặc thiết kế ứng dụng cho người bị bệnh xã hội — phải xem họ chịu ảnh hưởng của yếu tố gì.

Có nhiều kỹ thuật thu thập thông tin: recording (record khi người dùng sử dụng app, log lại thông tin), phỏng vấn, quan sát, questionnaire, phân tích task dựa trên sequence flow/sequence model. Dữ liệu thu thập dạng: document, manual, instruction, audio, chụp hình.

Hôm nay chúng ta tới đây thôi. Lần sau sẽ nói cụ thể hơn về các kỹ thuật khác như observation, interview. Những kỹ thuật này tốn rất nhiều thời gian. PA chắc tối nay hoặc ngày mai sẽ lên. PA1. Ok?
