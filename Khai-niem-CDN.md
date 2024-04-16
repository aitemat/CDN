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
CDN hoạt động bằng cách lưu vào bộ nhớ đệm nội dung trang web của bạn, chẳng hạn như hình ảnh, trang HTML, tệp JavaScript, stylesheets, video, v.v.  
<img src="/image/cach-thuc-hoat-dong.png">  
Nội dung tĩnh này sau đó được lưu trữ trên mỗi máy chủ và khi người dùng cố gắng tải một trang web, họ sẽ nhận được các tệp từ máy chủ có vị trí địa lý gần họ nhất. Vì vậy, CDN được sử dụng để phục vụ nội dung cho người dùng cuối với tính sẵn sàng cao và hiệu suất cao.  
### Ưu điểm và nhược điểm của việc sử dụng CDN  
#### Lợi ích của việc sử dụng CDN  
Mục đích chính của CDN là tăng tốc độ nội dung đến tay người dùng. Tuy nhiên, như bạn sẽ thấy, việc sử dụng CDN cũng có rất nhiều lợi ích khác:

Tốc độ trang web – Bằng cách gửi nội dung đến người dùng từ máy chủ gần nhất của họ, thời gian tải trang web có thể giảm đáng kể. Điều này cải thiện trải nghiệm người dùng, từ đó có thể tăng số liệu thống kê về thời gian trên trang web, số lượng khách truy cập quay lại và cuối cùng là tỷ lệ chuyển đổi cho trang web của bạn.
Phân phối nhất quán và chất lượng cao – Sử dụng CDN giúp phân phối nội dung nhất quán hơn, đặc biệt khi phát trực tuyến video hoặc tải hình ảnh có độ phân giải cao. Bằng cách cung cấp khả năng phân phối nội dung chất lượng cao, CDN có ảnh hưởng sâu sắc đến hiệu suất của trang web, cho dù người dùng ở đâu.
Giảm tải máy chủ – Nếu trang web của bạn nhận được lưu lượng truy cập lớn, tăng đột biến vào những thời điểm nhất định trong ngày thì sử dụng CDN là một cách tuyệt vời để giảm tải máy chủ, vì các tệp sẽ được yêu cầu từ nhiều máy chủ trên mạng.
SEO – Việc cải thiện thời gian tốc độ, độ tin cậy và hiệu suất tổng thể của trang web sẽ giúp ích cho SEO. Và với các trang và bài đăng được xếp hạng cao hơn trong Google cũng như các công cụ tìm kiếm khác, bạn sẽ tiếp cận được nhiều đối tượng hơn.
Bảo mật – Phần lớn các CDN tốt nhất thực hiện các biện pháp bảo mật bổ sung, giúp giữ cho trang web của bạn và dữ liệu của nó an toàn và bảo mật.
Chống sự cố – ​​Một máy chủ có thể gặp khó khăn trong việc đối phó với lưu lượng truy cập vào thời gian cao điểm. CDN có thể phân bổ khối lượng công việc, giảm nguy cơ trang web của bạn bị sập.
Hỗ trợ – Tùy thuộc vào dịch vụ, nhà cung cấp CDN thường cung cấp hỗ trợ hàng đầu suốt ngày đêm. Đây có thể là cứu cánh khi gặp khó khăn nhưng cũng có thể trợ giúp trong quá trình thiết lập và là một dịch vụ liên tục để đảm bảo quá trình phân phối nội dung của bạn diễn ra suôn sẻ.
#### Nhược điểm của CDN  
Rõ ràng là có thể thu được nhiều lợi ích từ việc sử dụng CDN. Nhưng còn nhược điểm thì sao? Chúng ta hãy xem xét.

Chi phí – Nếu bạn chọn dịch vụ CDN cao cấp, bạn sẽ phải trả phí. Vì vậy, nếu trang web của bạn chưa nhận được lượng truy cập lớn và khách truy cập chủ yếu là người địa phương thì CDN có thể không đáng tiền. Tuy nhiên, như chúng ta sẽ thấy ở phần sau của hướng dẫn này, có một số dịch vụ CDN miễn phí hiện có.
Hạn chế – Một số quốc gia và tổ chức chặn tên miền hoặc địa chỉ IP của CDN phổ biến. Nếu điều này xảy ra, khán giả từ các quốc gia này sẽ không thể truy cập trang web của bạn.
Vị trí của máy chủ – Nếu CDN bạn đang sử dụng không có bất kỳ máy chủ nào ở các quốc gia nơi phần lớn khán giả của bạn sinh sống, thì có thể dữ liệu trang web của bạn phải di chuyển xa hơn so với khi bạn đang sử dụng máy chủ của công ty lưu trữ.



