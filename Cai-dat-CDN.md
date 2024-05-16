Để cài đặt một CDN riêng cho hai location (Mỹ và Việt Nam) trên máy chủ CentOS 7 sử dụng Nginx, bạn cần thiết lập và cấu hình các máy chủ tại mỗi location và sử dụng Nginx để phân phối nội dung. Dưới đây là hướng dẫn từng bước để thiết lập một CDN riêng.

## Bước 1: Chuẩn bị máy chủ tại mỗi location
Máy chủ tại Mỹ (us.example.com):

Cài đặt CentOS 7 và Nginx.
Máy chủ tại Việt Nam (vn.example.com):

Cài đặt CentOS 7 và Nginx.
## Bước 2: Cài đặt và cấu hình Nginx trên mỗi máy chủ
Cài đặt Nginx:
Trên cả hai máy chủ, cài đặt Nginx bằng các lệnh sau:
```sh
sudo yum install epel-release  
sudo yum install nginx
```sh
Cấu hình Nginx:
Tạo file cấu hình Nginx cho máy chủ CDN.

bash
Copy code
sudo nano /etc/nginx/conf.d/cdn.conf
Thêm cấu hình sau vào cdn.conf trên cả hai máy chủ:

nginx
Copy code
server {
    listen 80;
    server_name cdn.example.com;

    location / {
        root /var/www/cdn;
        autoindex on;
        expires max;
        add_header Cache-Control "public";
    }
}
Tạo thư mục để lưu trữ nội dung CDN:

bash
Copy code
sudo mkdir -p /var/www/cdn
sudo chown -R nginx:nginx /var/www/cdn
Khởi động và kích hoạt Nginx:

bash
Copy code
sudo systemctl start nginx
sudo systemctl enable nginx
Bước 3: Đồng bộ hóa nội dung giữa các máy chủ
Để đảm bảo nội dung được đồng bộ giữa hai location, bạn có thể sử dụng rsync hoặc một công cụ đồng bộ hóa khác. Dưới đây là ví dụ sử dụng rsync:

Cài đặt rsync:

bash
Copy code
sudo yum install rsync
Thiết lập đồng bộ hóa:
Trên máy chủ tại Mỹ, chạy lệnh sau để đồng bộ nội dung tới máy chủ tại Việt Nam:

bash
Copy code
rsync -avz /var/www/cdn/ user@vn.example.com:/var/www/cdn/
Bạn có thể thiết lập cron job để tự động đồng bộ hóa hàng ngày:

bash
Copy code
crontab -e
Thêm dòng sau vào file crontab:

bash
Copy code
0 2 * * * rsync -avz /var/www/cdn/ user@vn.example.com:/var/www/cdn/
Bước 4: Cấu hình DNS để phân phối tải
Bạn cần cấu hình DNS để phân phối tải dựa trên vị trí địa lý của người dùng. Sử dụng một dịch vụ DNS có hỗ trợ GeoDNS như Amazon Route 53, NS1 hoặc một dịch vụ tương tự. Dưới đây là hướng dẫn cơ bản với Amazon Route 53:

Tạo các bản ghi DNS:

Truy cập vào bảng điều khiển Route 53 và tạo các bản ghi cho cdn.example.com.
Cấu hình các bản ghi GeoDNS:

Tạo bản ghi A cho cdn.example.com trỏ đến IP của máy chủ tại Mỹ cho người dùng từ Mỹ.
Tạo bản ghi A cho cdn.example.com trỏ đến IP của máy chủ tại Việt Nam cho người dùng từ Việt Nam.
Bước 5: Kiểm tra và xác nhận
Kiểm tra cấu hình Nginx:
Truy cập http://cdn.example.com từ cả Mỹ và Việt Nam để đảm bảo rằng nội dung được phân phối từ các máy chủ tương ứng.

Kiểm tra đồng bộ hóa:
Đảm bảo rằng nội dung được đồng bộ hóa chính xác giữa hai máy chủ.

Kiểm tra DNS:
Sử dụng công cụ như DNS Checker để đảm bảo rằng bản ghi DNS đang trỏ đúng tới các máy chủ tại Mỹ và Việt Nam.

Tổng kết
Việc thiết lập CDN riêng cho hai location (Mỹ và Việt Nam) trên CentOS 7 sử dụng Nginx yêu cầu cài đặt và cấu hình Nginx trên các máy chủ tại mỗi location, đồng bộ hóa nội dung giữa các máy chủ, và sử dụng GeoDNS để phân phối tải dựa trên vị trí địa lý của người dùng. Điều này giúp cải thiện hiệu suất và độ tin cậy của trang web của bạn cho người dùng tại các khu vực khác nhau.
