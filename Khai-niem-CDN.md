## CDN là gì?  

`CDN` viết tắt của ***Content Delivery Networks*** là hệ thống máy chủ trên toàn cầu, hỗ trợ sao lưu bản sao của những nội dung tĩnh nằm bên trong trang web và phân phối nội dung ra nhiều máy chủ PoP. Mạng lưới máy chủ CDN được đặt ở khắp mọi nơi trên thế giới. Từ đó, các điểm truy cập PoP (Points of Presence) sẽ gửi tới cho người dùng khi họ truy cập vào website.  

<img src="/image/cdn.png">

`CDN` được coi là xương sống trong suốt của Internet, có nhiệm vụ phân phối nội dung. Mỗi người trong chúng ta đều tương tác với nó hàng ngày. Chẳng hạn khi chúng ta đọc các bài báo trên các trang tin tức, mua sắm trực tuyến, xem video YouTube hoặc xem các trang mạng xã hội.

Bất kể bạn làm gì hoặc sử dụng loại nội dung nào, rất có thể bạn sẽ tìm thấy CDN đằng sau mọi ký tự văn bản, mọi image pixel và mọi frame phim được chuyển đến PC và trình duyệt trên thiết bị di động của bạn.

Để hiểu tại sao CDN được sử dụng rộng rãi như vậy, trước tiên bạn cần biết chúng được thiết kế như thế nào để giải quyết vấn đề. Bạn có biết latency là gì không? Đó là khoảng thời gian delay xảy ra từ thời điểm bạn request tải một trang web đến thời điểm content của trang đó thực sự xuất hiện trên màn hình.

Khoảng thời gian delay đó bị ảnh hưởng bởi một số yếu tố cụ thể. Tuy nhiên trong mọi trường hợp, thời gian delay bị ảnh hưởng bởi khoảng cách vật lý giữa bạn và hosting server chứa trang web đó.

Nhiệm vụ của công cụ này là hầu như rút ngắn khoảng cách vật lý đó. Mục tiêu là cải thiện tốc độ và hiệu suất hiển thị trang web. Như vậy, trên đây là toàn bộ định nghĩa CDN là gì, trong phần dưới đây Vietnix tiếp tục làm rõ các định nghĩa xung quanh Content Delivery Network.
### 1. Hiểu về nội dung  
Trước khi đi tìm hiểu về cách thức hoạt động của CDN (mạng phân phối nội dung) hay Content Delivery Network là gì ta cần hiểu rõ Nội dung (Content) là gì? Như chúng ta đã biết, nội dung (content) bao gồm các định dạng: Văn bản, hình ảnh, video,…

Tuy nhiên, định nghĩa nội dung được chia ra làm hai loại chỉnh: Nội dung động và nội dung tĩnh.

Nội dung tĩnh: Vừa là nội dung ban đầu (input) tuy nhiên cũng là nội dung cuối cùng người dùng có thể thấy (output). Nó không chịu tác động của người dùng và thay đổi theo thời gian. Máy chủ sẽ truyền tải cùng một nội dung cho mọi người. Tức là, khi được yêu cầu 1 file A từ web server, server sẽ trả lại đúng file A đó.
Nội dung động (Dynamic content): Đúng như tên gọi, nội dung động trái ngược với định nghĩa nội dung tĩnh ta vừa tìm hiểu ở trên. Đó là nội dung sẽ thay đổi dựa vào dữ liệu đầu vào và được cá nhân hóa trên mỗi trang, dựa vào dữ liệu nhập của người dùng.
Vậy CDN phân phối nộ dung hay cách hoạt động như thế nào. Cùng tìm hiểu trong phần dưới đây.  
### Cách thức hoạt động của CDN  
Như đã đề cập ở trên, `CDN` hay ***Content Delivery Network*** hoạt động bằng cách đưa content đến gần vị trí người dùng cuối. Điều này được thực hiện bằng cách thông qua các data center được định vị được gọi là Points of Presence (PoPs). Đây là các data center nằm trên khắp thế giới và bên trong mỗi PoP là hàng nghìn caching server. Cả PoP và server đều giúp cải thiện kết nối và tăng tốc độ phân phối content đến end user.


