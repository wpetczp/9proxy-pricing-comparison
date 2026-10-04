# proxy socks5 giá rẻ: Chọn gói theo IP hay theo GB cho nuôi acc, MMO và scraping mà không dính IP bẩn

Ai gõ cụm "proxy socks5 giá rẻ" lên Google thường không thiếu thông tin — họ thiếu một con số cụ thể để quyết định. Cần 50 IP để nuôi tài khoản, cần vài trăm GB để rotate khi check giá, ngân sách có hạn, và đã từng thử proxy free rồi ăn checkpoint. Vậy nên câu hỏi thật sự không phải "proxy nào rẻ nhất" mà là "rẻ theo kiểu nào, và kiểu đó có đúng với việc mình đang làm không".

Bài này trả lời theo hướng đó: ba cách tính giá phổ biến trên thị trường, SOCKS5 khác HTTP proxy ở chỗ nào, và toàn bộ bảng giá hiện hành của 9Proxy — một nhà cung cấp proxy dân cư bán theo gói thay vì bắt đóng phí tháng — để bạn tự tính xem gói nào hợp túi tiền.

## "Rẻ" trong proxy SOCKS5 phụ thuộc vào kiểu tính giá, không phải vào con số

Cùng một mức 10 đô, ba nhà cung cấp có thể bán cho bạn ba thứ hoàn toàn khác nhau. Đây là lý do nhiều người mua gói "rẻ" rồi vẫn thấy đắt.

| Kiểu tính giá | Đơn vị tính | Hợp với việc gì | Chỗ dễ phát sinh chi phí |
| --- | --- | --- | --- |
| Theo số IP | Trả một lần cho N IP, băng thông thường không giới hạn | Nuôi tài khoản, session dài, tool tải dữ liệu nặng | IP chết giữa việc nếu không có cơ chế thay tự động |
| Theo lưu lượng (GB) | Trả theo GB đã dùng, tạo endpoint không giới hạn | Rotate liên tục, mỗi request ít dữ liệu: check giá, kiểm tra quảng cáo, scraping nhẹ | Tải ảnh, video hay file lớn là hóa đơn phình rất nhanh |
| Thuê theo ngày/tháng | Trả theo cổng hoặc theo IP, tính bằng ngày | Cần IP Việt Nam cố định, dùng liên tục một địa chỉ | Không linh hoạt khi bạn cần đổi vị trí quốc gia |

Nếu công việc của bạn là nuôi 30–50 tài khoản Facebook, TikTok, hay giữ session đăng nhập ổn định, kiểu tính theo IP gần như luôn rẻ hơn. Ngược lại, nếu bạn chỉ cần bắn request liên tục lên Shopee hay Google để lấy dữ liệu, mỗi request vài chục KB, thì trả theo IP là bạn đang trả tiền cho thứ mình không dùng hết.

Còn proxy miễn phí? Nó không nằm trong bảng trên vì nó không phải một lựa chọn về giá. Proxy free thường đã nằm trong blacklist của Facebook, Google và các sàn thương mại điện tử vì bị hàng nghìn người dùng chung trước đó. Cách nhiều dịch vụ free kiếm tiền là ghi log và bán lại dữ liệu đi qua. Tính bằng rủi ro mất tài khoản thì "0 đồng" là mức giá đắt nhất trong bảng.

## SOCKS5 khác HTTP proxy ở đâu và khi nào bạn thực sự cần SOCKS5

SOCKS5 làm việc ở tầng transport, không viết lại header của request và hỗ trợ cả TCP lẫn UDP. HTTP proxy chỉ xử lý lưu lượng web và phải sửa header để làm được điều đó.

Khác biệt này nghe kỹ thuật nhưng dẫn tới hai hệ quả rất thực tế:

- **Dùng được cho mọi ứng dụng, không chỉ trình duyệt.** Tool MMO, script Python, bot, phần mềm giả lập điện thoại, thậm chí game đều đi qua SOCKS5 được. HTTP proxy thì không.
- **Request trông "sạch" hơn.** Vì header không bị sửa, request đến server đích giống request thật hơn, nên khó bị fingerprint hơn. Với các nền tảng có hệ thống chống bot gắt, đây thường là yếu tố quyết định.

Điểm cần kiểm tra trước khi mua: không phải nhà cung cấp nào cũng hỗ trợ SOCKS5 cho toàn bộ gói. Có nơi chỉ mở SOCKS5 ở gói cao cấp, có nơi chỉ có HTTP/HTTPS. 9Proxy công bố hỗ trợ cả HTTP/HTTPS lẫn SOCKS5 trên hệ thống proxy dân cư của họ, cùng pool hơn 20 triệu IP trải trên 90+ quốc gia, target được tới cấp quốc gia, bang, thành phố, mã ZIP và nhà mạng.

## 9Proxy tính giá thế nào: nạp balance, không đóng phí tháng

Đây là điểm khác biệt lớn nhất so với phần lớn nhà cung cấp proxy bạn gặp. 9Proxy không bán subscription theo tháng. Bạn nạp balance vào tài khoản rồi mua gói, và balance còn lại dùng cho lần sau.

Họ có hai mô hình song song:

**Theo số IP.** Bạn mua một số lượng IP cố định, trả tiền theo IP chứ không theo lưu lượng — băng thông không giới hạn trong thời gian IP hoạt động. IP chưa dùng không bao giờ hết hạn và nằm nguyên trong balance. IP chỉ bị trừ khi bạn forward nó ra một cổng local.

**Theo GB.** Bạn mua một lượng lưu lượng, tạo được không giới hạn endpoint, IP xoay tự động hoặc giữ cố định theo session. Gói GB có hiệu lực 180 ngày, riêng nhóm Enterprise thì không giới hạn thời gian.

Một chi tiết về giá mà bạn nên biết trước khi tính ngân sách: ngày 1/6/2026, 9Proxy điều chỉnh giá lần đầu tiên trong lịch sử hoạt động của họ, áp dụng cho **gói theo IP và gói bundle**. Gói theo GB giữ nguyên giá. Nếu bạn đọc được bảng giá cũ ở đâu đó với mức 100 IP chỉ 20 đô, đó là giá trước điều chỉnh.

> Gói theo lưu lượng (GB) của 9Proxy không thay đổi giá trong lần điều chỉnh ngày 1/6/2026. Chỉ gói theo IP và gói bundle tăng.

## Bảng giá toàn bộ gói 9Proxy hiện hành

Toàn bộ các gói đang được niêm yết, tính bằng USD, mua một lần bằng balance chứ không phải phí định kỳ.

### Gói theo số IP (băng thông không giới hạn)

| Gói | Đơn giá | Tổng | Hình thức / thời hạn | Đăng ký |
| --- | --- | --- | --- | --- |
| 100 IPs | $0.24/IP | $24 | Một lần, IP chưa dùng không hết hạn | [ Mua gói 100 IPs](https://bit.ly/9-Proxy) |
| 500 IPs | $0.144/IP | $72 | Một lần, IP chưa dùng không hết hạn | [ Mua gói 500 IPs](https://bit.ly/9-Proxy) |
| 1.000 + 500 IPs (bonus) | $0.084/IP | $126 | Một lần, IP chưa dùng không hết hạn | [ Mua gói 1.500 IPs](https://bit.ly/9-Proxy) |
| 2.500 IPs | $0.084/IP | $210 | Một lần, IP chưa dùng không hết hạn | [ Mua gói 2.500 IPs](https://bit.ly/9-Proxy) |
| 5.000 IPs | $0.072/IP | $360 | Một lần, IP chưa dùng không hết hạn | [ Mua gói 5.000 IPs](https://bit.ly/9-Proxy) |
| 15.000 IPs | $0.048/IP | $720 | Một lần, IP chưa dùng không hết hạn | [ Mua gói 15.000 IPs](https://bit.ly/9-Proxy) |
| 25.000 IPs | $0.035/IP | $863 | Một lần, IP chưa dùng không hết hạn | [ Mua gói 25.000 IPs](https://bit.ly/9-Proxy) |
| 50.000 IPs | $0.029/IP | $1.438 | Một lần, IP chưa dùng không hết hạn | [ Mua gói 50.000 IPs](https://bit.ly/9-Proxy) |

### Gói Business theo số IP (khối lượng lớn)

| Gói | Đơn giá | Tổng | Hình thức / thời hạn | Đăng ký |
| --- | --- | --- | --- | --- |
| 100.000 IPs | $0.023/IP | $2.300 | Một lần, IP chưa dùng không hết hạn | [ Mua gói 100.000 IPs](https://bit.ly/9-Proxy) |
| 200.000 IPs | $0.021/IP | $4.140 | Một lần, IP chưa dùng không hết hạn | [ Mua gói 200.000 IPs](https://bit.ly/9-Proxy) |
| 500.000 IPs | $0.018/IP | $8.625 | Một lần, IP chưa dùng không hết hạn | [ Mua gói 500.000 IPs](https://bit.ly/9-Proxy) |

### Gói theo lưu lượng GB

| Gói | Đơn giá | Tổng | Hình thức / thời hạn | Đăng ký |
| --- | --- | --- | --- | --- |
| 5 GB | $3.00/GB | $15 | Một lần, hiệu lực 180 ngày | [ Mua gói 5 GB](https://bit.ly/9-Proxy) |
| 50 GB + 5 GB | $2.10/GB | $105 | Một lần, hiệu lực 180 ngày | [ Mua gói 50 GB](https://bit.ly/9-Proxy) |
| 100 GB | $1.50/GB | $150 | Một lần, hiệu lực 180 ngày | [ Mua gói 100 GB](https://bit.ly/9-Proxy) |
| 200 GB | $1.00/GB | $200 | Một lần, hiệu lực 180 ngày | [ Mua gói 200 GB](https://bit.ly/9-Proxy) |
| 1.000 GB | $0.80/GB | $800 | Một lần, hiệu lực 180 ngày | [ Mua gói 1.000 GB](https://bit.ly/9-Proxy) |
| 2.000 GB | $0.75/GB | $1.500 | Một lần, hiệu lực 180 ngày | [ Mua gói 2.000 GB](https://bit.ly/9-Proxy) |
| 3.000 GB (Enterprise) | $0.72/GB | $2.160 | Một lần, không hết hạn | [ Mua gói 3.000 GB](https://bit.ly/9-Proxy) |
| 6.000 GB (Enterprise) | $0.70/GB | $4.200 | Một lần, không hết hạn | [ Mua gói 6.000 GB](https://bit.ly/9-Proxy) |
| 10.000 GB (Enterprise) | $0.68/GB | $6.800 | Một lần, không hết hạn | [ Mua gói 10.000 GB](https://bit.ly/9-Proxy) |

### Gói bundle (IP + GB)

| Gói | Cấu hình | Tổng | Hình thức / thời hạn | Đăng ký |
| --- | --- | --- | --- | --- |
| Starter | 100 IPs + 5 GB | $30 | Một lần, GB hiệu lực 180 ngày | [ Mua bundle Starter](https://bit.ly/9-Proxy) |
| Popular | 1.500 IPs + 50 GB | $180 | Một lần, GB hiệu lực 180 ngày | [ Mua bundle Popular](https://bit.ly/9-Proxy) |
| Pro | 5.000 IPs + 500 GB | $720 | Một lần, GB hiệu lực 180 ngày | [ Mua bundle Pro](https://bit.ly/9-Proxy) |

[👉 Tạo tài khoản 9Proxy bằng Google hoặc email để xem toàn bộ gói](https://bit.ly/9-Proxy)

## Gói nào hợp với ai: vài phép tính cụ thể

Đừng chọn theo gói to nhất trong tầm tiền. Chọn theo cái bạn tiêu nhiều hơn — IP hay băng thông.

**Bạn nuôi vài chục tài khoản, mỗi tài khoản một IP cố định.** Gói 100 IPs giá $24 là điểm bắt đầu hợp lý, khoảng 24 cent một IP. Vì băng thông không giới hạn, việc bạn để tool chạy video hay upload ảnh không làm tăng hóa đơn. Điểm cần lưu ý: IP dân cư sống tự nhiên từ vài giờ tới khoảng 24 giờ, không phải vĩnh viễn. Nếu bạn cần đúng một địa chỉ IP cho một tài khoản trong nhiều tháng, đây không phải sản phẩm dành cho việc đó.

**Bạn scale lên 1.500–5.000 IP.** Gói 1.000 + 500 IPs ở mức $126, hay gói 5.000 IPs ở mức $360 ($0.072/IP), là mức giá rơi xuống khá nhanh. Càng lên cao đơn giá càng giảm: gói 50.000 IPs còn $0.029/IP.

**Bạn rotate liên tục nhưng mỗi request rất nhẹ.** Ví dụ theo dõi giá Shopee, kiểm tra thứ hạng từ khóa theo thành phố, hay kiểm tra quảng cáo hiển thị đúng khu vực. Gói GB hợp hơn nhiều. Chỉ cần 5 GB giá $15 là đủ để chạy thử vài nghìn request; nếu chạy đều, mức $1.50/GB ở gói 100 GB hoặc $1.00/GB ở gói 200 GB rẻ hơn đáng kể so với gói nhỏ. Nhóm Enterprise từ 3.000 GB trở lên có lợi thế riêng: không hết hạn, nên bạn không bị áp lực đốt hết lưu lượng trong 180 ngày.

**Bạn cần cả hai loại trong cùng một dự án.** Bundle Starter ở $30 đưa bạn 100 IPs kèm 5 GB — rẻ hơn mua lẻ hai gói tương ứng, và đủ để biết mô hình nào hợp với workflow của mình.

**Bạn chỉ cần IP Việt Nam và dùng một địa chỉ cố định suốt tháng.** Thành thật mà nói, đây là trường hợp mà các dịch vụ proxy nội địa Việt Nam có thể hợp hơn về mặt vị trí và giá. Một số nhà cung cấp trong nước công bố mức từ 5.000đ/ngày cho IP dân cư Việt Nam (khoảng 150.000đ/tháng), hoặc các gói theo tuần và theo tháng tính bằng VND. Lợi thế của họ là IP nằm đúng trong các dải nhà mạng Viettel, FPT, VNPT. Ngược lại, nếu bạn cần IP nhiều quốc gia, cần băng thông không giới hạn, hoặc không muốn bị tính tiền theo dung lượng, gói theo IP của 9Proxy dễ tính toán hơn.

Trước khi mua gói lớn, hãy chạy thử một gói nhỏ và kiểm tra đúng mục tiêu mình cần. Một IP dân cư sạch ở Mỹ chưa chắc đã vượt được hệ thống chống bot của một sàn thương mại điện tử cụ thể, và ngược lại. [👉 Kiểm tra gói nhỏ nhất để chạy thử trước khi scale](https://bit.ly/9-Proxy)

## Những thứ cần biết trước khi trả tiền

**Gói theo IP bắt buộc dùng app desktop.** 9Proxy không đưa proxy theo IP dưới dạng host:port qua dashboard. Bạn tải app cho Windows, macOS hoặc Linux, lọc IP theo quốc gia/bang/thành phố/ZIP/nhà mạng, rồi forward IP ra một cổng local và dùng qua dạng `localhost:port`. Đây là điểm bị nhiều bài đánh giá bên thứ ba phê bình vì làm việc dùng trên nhiều thiết bị rườm rà hơn so với extension trình duyệt. Đổi lại, cách này cho phép bạn kiểm soát chính xác IP nào đang bị trừ.

**Gói GB thì không cần app.** Bạn lấy thông tin xác thực trực tiếp từ dashboard, dùng username/password hoặc whitelist IP, và có thể chạy từ server, VPS hay script mà không cài gì thêm.

**IP dân cư có thể chết tự nhiên.** Đây là bản chất của pool dân cư, không phải lỗi riêng của nhà cung cấp nào. 9Proxy xử lý bằng hai công cụ: Auto Refresh Proxy để tự thay IP chết bằng IP mới, và Auto Rotation Proxy để xoay IP theo lịch bạn đặt trên những cổng chỉ định. Một số bài đánh giá nhắc tới chính sách thay IP trong khoảng 60 giây khi IP gặp sự cố.

**Gói GB có hạn 180 ngày.** Mua 200 GB rồi dùng dở dang thì phần chưa dùng mất sau 180 ngày. Nếu bạn biết chắc lưu lượng của mình sẽ trải dài, nhóm Enterprise (không hết hạn) đáng cân nhắc hơn là mua gói lớn trong nhóm 180 ngày.

**Bản dùng thử không phải lúc nào cũng có.** 9Proxy đôi khi mở trial giới hạn cho người dùng mới, nhưng phụ thuộc vào đợt và tình trạng pool. Muốn thử thì phải hỏi support trước. Kênh hỗ trợ gồm email, live chat trên trang chủ và Telegram.

**Đánh giá bên thứ ba nói gì.** Nhìn chung các bài review độc lập xếp 9Proxy vào nhóm lựa chọn ngân sách: khen mức giá trên mỗi IP, pool sạch, tương thích với các antidetect browser phổ biến như Dolphin Anty hay AdsPower. Phần bị chê tập trung vào app bắt buộc và thời gian sống của IP không cố định. Không có bài nào trong số này xác nhận 9Proxy vượt được mọi dịch vụ streaming — nếu mục tiêu của bạn là Netflix, hãy tự test trước khi mua gói lớn.

## Bắt đầu từ đâu

1. Đăng ký tài khoản. Có thể dùng Google để đăng ký nhanh, hoặc email.
2. Chọn gói theo kiểu tính giá phù hợp: theo IP nếu bạn tiêu nhiều băng thông, theo GB nếu bạn rotate nhiều mà request nhẹ.
3. Tải app nếu dùng gói theo IP, hoặc lấy credential từ dashboard nếu dùng gói GB.
4. Test trên đúng mục tiêu thật của bạn — kiểm tra vị trí IP, tốc độ, và tỷ lệ bị chặn — trước khi nạp thêm tiền.
5. Chỉ scale lên gói lớn sau khi bước 4 cho kết quả chấp nhận được.

[👉 Đăng ký 9Proxy và chọn gói theo cách tính giá hợp với workflow của bạn](https://bit.ly/9-Proxy)

## Câu hỏi thường gặp

**Gói theo IP có bị hết hạn không?**
Không. IP chưa forward ra cổng nào thì nằm nguyên trong balance, không mất. Chỉ khi bạn kích hoạt một IP thì nó mới bị trừ và bắt đầu chạy.

**Có phải đóng phí hàng tháng không?**
Không. 9Proxy bán theo gói và trừ vào balance. Không có subscription định kỳ, cũng không có phí duy trì.

**Proxy của 9Proxy có địa chỉ Việt Nam không?**
Pool của họ trải trên 90+ quốc gia với target tới cấp thành phố và nhà mạng, nhưng danh sách quốc gia cụ thể thay đổi theo tình trạng pool. Nếu bạn cần chính xác IP Việt Nam, hãy lọc trong app hoặc dashboard, hoặc hỏi support trước khi mua — đừng giả định.

**SOCKS5 giá rẻ có dùng được với antidetect browser không?**
Được, miễn là nhà cung cấp hỗ trợ SOCKS5. Các antidetect browser phổ biến đều nhận proxy SOCKS5 với username/password hoặc whitelist IP. Điều cần kiểm tra là tốc độ và độ ổn định của IP, chứ không phải giao thức.

**IP chết giữa lúc đang chạy tool thì sao?**
Bật Auto Refresh Proxy để hệ thống tự thay IP mới, hoặc Auto Rotation Proxy nếu bạn muốn xoay theo lịch cố định. Với công việc chạy dài, nên bật sẵn thay vì xử lý thủ công.

## Tóm lại

"Giá rẻ" trong proxy SOCKS5 không phải một con số, mà là sự khớp nhau giữa kiểu tính giá và kiểu tiêu dùng của bạn. Trả theo IP khi bạn tiêu nhiều băng thông và cần session ổn định; trả theo GB khi bạn rotate nhiều nhưng mỗi request nhẹ. Mua sai kiểu thì gói rẻ nhất cũng thành đắt.

Với 9Proxy, điểm đáng chú ý là không có phí tháng, IP chưa dùng không hết hạn, và băng thông không giới hạn ở nhóm gói theo IP — ba thứ khiến việc tính ngân sách dễ hơn nhiều so với các mô hình tính theo GB thuần. Đổi lại, bạn phải chấp nhận app desktop cho gói theo IP và thời gian sống tự nhiên của IP dân cư. Chạy thử một gói nhỏ trên đúng mục tiêu của mình trước, rồi hãy quyết định scale.
