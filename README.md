# BookStore - Nền tảng Bán Sách Trực Tuyến Dựa Trên Laravel

BookStore là một ứng dụng web toàn diện được xây dựng trên framework Laravel mạnh mẽ, cho phép người dùng duyệt, tìm kiếm và mua sách trực tuyến một cách dễ dàng. Dự án này cung cấp giao diện thân thiện với người dùng, tích hợp thanh toán an toàn và một bảng điều khiển quản trị để quản lý sách, đơn hàng và thông tin khách hàng. Đây là một giải pháp lý tưởng cho các cửa hàng sách trực tuyến muốn mang lại trải nghiệm mượt mà cho cả khách hàng và quản trị viên.

## Giới thiệu

BookStore được thiết kế để đáp ứng nhu cầu của những người yêu sách trong thời đại số hóa. Với sự hỗ trợ của Laravel, ứng dụng này đảm bảo hiệu suất cao, bảo mật tốt và khả năng mở rộng dễ dàng. Từ việc tìm kiếm cuốn sách yêu thích đến thanh toán và theo dõi đơn hàng, mọi thứ đều được tối ưu hóa để mang lại trải nghiệm tốt nhất.

Dự án này phù hợp cho:
- Các nhà phát triển muốn tìm hiểu về cách xây dựng ứng dụng thương mại điện tử với Laravel.
- Các doanh nghiệp nhỏ muốn triển khai một cửa hàng sách trực tuyến.
- Những người yêu thích lập trình muốn đóng góp vào một dự án mã nguồn mở.

## Tính năng

BookStore đi kèm với hàng loạt tính năng mạnh mẽ, bao gồm:

- **Xác thực và phân quyền người dùng**: Hệ thống đăng ký, đăng nhập an toàn với phân quyền theo vai trò (khách hàng, quản trị viên).
- **Danh mục sách**: Duyệt sách theo danh mục, tác giả hoặc sử dụng chức năng tìm kiếm để tìm tiêu đề cụ thể.
- **Giỏ hàng**: Thêm sách vào giỏ, xem nội dung giỏ và tiến hành thanh toán.
- **Thanh toán**: Tích hợp cổng thanh toán Stripe để xử lý giao dịch an toàn và đáng tin cậy.
- **Quản lý đơn hàng**: Xem lịch sử đơn hàng, theo dõi trạng thái và quản lý hoàn tiền hoặc hủy đơn.
- **Bảng điều khiển quản trị**: Quản lý sách, danh mục, tác giả, đơn hàng và tài khoản người dùng.
- **Đánh giá và xếp hạng**: Cho phép khách hàng để lại nhận xét và đánh giá về sách đã mua.
- **Danh sách yêu thích**: Lưu sách để mua sau.
- **Thiết kế responsive**: Tối ưu hóa cho cả thiết bị di động và máy tính để bàn.

### Chi tiết từng tính năng

- **Xác thực người dùng**: Sử dụng hệ thống xác thực tích hợp của Laravel với các biện pháp bảo mật như mã hóa mật khẩu và kiểm tra CSRF.
- **Tìm kiếm nâng cao**: Hỗ trợ tìm kiếm theo từ khóa, lọc theo giá, danh mục hoặc tác giả.
- **Giao diện quản trị**: Được thiết kế để dễ sử dụng, với các biểu đồ và bảng dữ liệu trực quan để theo dõi doanh thu và hoạt động.

## Công nghệ sử dụng

Dự án được xây dựng với sự kết hợp của nhiều công nghệ hiện đại:

- **Backend**: 
  - Laravel 8.x - Framework PHP mạnh mẽ để xử lý logic phía server.
  - PHP 7.4 - Đảm bảo hiệu suất và tính tương thích.
- **Frontend**: 
  - Blade - Công cụ tạo template của Laravel.
  - Bootstrap 4 - Framework CSS để tạo giao diện responsive.
  - jQuery - Hỗ trợ thao tác DOM và hiệu ứng giao diện.
- **Cơ sở dữ liệu**: 
  - MySQL 5.7 - Hệ quản trị cơ sở dữ liệu quan hệ để lưu trữ thông tin.
- **Cổng thanh toán**: 
  - Stripe API - Xử lý thanh toán trực tuyến an toàn.
- **Xác thực API**: 
  - Laravel Sanctum (nếu có API) - Cung cấp token cho xác thực API.
- **Công cụ khác**: 
  - Composer - Quản lý dependencies của PHP.
  - Laravel Mix - Biên dịch và quản lý tài nguyên frontend (CSS, JS).

### Gói Composer bổ sung

- `laravel/ui` - Hỗ trợ tạo giao diện xác thực.
- `stripe/stripe-php` - Thư viện PHP để tích hợp Stripe.
- `spatie/laravel-permission` (tùy chọn) - Quản lý vai trò và quyền hạn.

## Hướng dẫn cài đặt

Để thiết lập dự án BookStore trên máy local, hãy làm theo các bước sau:

### Yêu cầu trước khi cài đặt

Trước khi bắt đầu, hãy đảm bảo bạn đã cài đặt:
- PHP 7.4 hoặc cao hơn.
- Composer - Công cụ quản lý dependencies của PHP.
- MySQL 5.7 hoặc cao hơn.
- Node.js và NPM - Để biên dịch tài nguyên frontend.

### Các bước cài đặt chi tiết

1. **Sao chép repository**:
   Mở terminal và chạy lệnh sau để tải mã nguồn về máy:
   ```bash
   git clone https://github.com/yourusername/bookstore.git
   cd bookstore
Cài đặt dependencies: Cài đặt các gói PHP và JavaScript cần thiết:
bash
Wrap
Copy
composer install
npm install
Thiết lập file môi trường (.env):
Sao chép file mẫu .env.example thành .env:
bash
Wrap
Copy
cp .env.example .env
Tạo khóa ứng dụng:
bash
Wrap
Copy
php artisan key:generate
Cấu hình cơ sở dữ liệu:
Tạo một cơ sở dữ liệu MySQL (ví dụ: bookstore_db).
Cập nhật thông tin cơ sở dữ liệu trong file .env:
text
Wrap
Copy
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=bookstore_db
DB_USERNAME=your_username
DB_PASSWORD=your_password
Chạy migration và seeder: Thiết lập cấu trúc cơ sở dữ liệu và dữ liệu mẫu:
bash
Wrap
Copy
php artisan migrate --seed
Biên dịch tài nguyên: Chạy lệnh sau để biên dịch CSS và JS:
bash
Wrap
Copy
npm run dev
Khởi động server phát triển: Khởi động ứng dụng bằng Artisan:
bash
Wrap
Copy
php artisan serve
Truy cập ứng dụng tại http://localhost:8000.
Lưu ý cài đặt
Nếu gặp lỗi liên quan đến phiên bản PHP, hãy kiểm tra composer.json để đảm bảo tương thích.
Đảm bảo bật các extension PHP như pdo_mysql, mbstring, và openssl.
Cấu hình
Biến môi trường (.env)
Dự án yêu cầu một số biến môi trường trong file .env. Dưới đây là các mục chính cần chú ý:

Cơ sở dữ liệu:
text
Wrap
Copy
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=bookstore_db
DB_USERNAME=your_username
DB_PASSWORD=your_password
Email (dùng để gửi email xác nhận đơn hàng):
text
Wrap
Copy
MAIL_MAILER=smtp
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME=your_email@gmail.com
MAIL_PASSWORD=your_app_password
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS=your_email@gmail.com
MAIL_FROM_NAME="BookStore"
Stripe (cho thanh toán):
text
Wrap
Copy
STRIPE_KEY=your_stripe_publishable_key
STRIPE_SECRET=your_stripe_secret_key
Tùy chỉnh cấu hình
Các tệp cấu hình nằm trong thư mục config/. Một số tệp quan trọng:

config/app.php: Thiết lập múi giờ, ngôn ngữ mặc định.
config/database.php: Cấu hình kết nối cơ sở dữ liệu.
config/mail.php: Cấu hình dịch vụ email.
Nếu bạn thêm các dịch vụ khác, hãy tạo tệp cấu hình riêng trong thư mục này.

Hướng dẫn sử dụng
Dành cho khách hàng
Đăng ký và đăng nhập:
Truy cập trang đăng ký, điền thông tin để tạo tài khoản.
Đăng nhập bằng email và mật khẩu.
Duyệt và tìm kiếm sách:
Sử dụng menu để xem sách theo danh mục hoặc tác giả.
Nhập từ khóa vào thanh tìm kiếm để tìm sách.
Thêm vào giỏ hàng:
Nhấn vào một cuốn sách để xem chi tiết.
Nhấn nút "Thêm vào giỏ" để thêm sách.
Thanh toán:
Xem giỏ hàng, kiểm tra sản phẩm và nhấn "Thanh toán".
Nhập thông tin giao hàng và chọn phương thức thanh toán (qua Stripe).
Hoàn tất giao dịch.
Xem lịch sử đơn hàng:
Vào trang tài khoản để kiểm tra các đơn hàng trước đây.
Dành cho quản trị viên
Truy cập bảng điều khiển:
Đăng nhập bằng tài khoản quản trị.
Chuyển đến trang dashboard tại /admin.
Quản lý sách:
Thêm sách mới (tiêu đề, giá, ảnh, mô tả).
Chỉnh sửa hoặc xóa sách hiện có.
Quản lý đơn hàng:
Xem danh sách đơn hàng, cập nhật trạng thái (đang xử lý, đã giao, hủy).
Xử lý yêu cầu hoàn tiền nếu cần.
Quản lý người dùng:
Xem danh sách tài khoản, chỉnh sửa thông tin hoặc vô hiệu hóa tài khoản.
Cơ sở dữ liệu
Tổng quan schema
Dự án sử dụng các bảng sau trong cơ sở dữ liệu:

users: Lưu thông tin người dùng.
id, name, email, password, role (customer/admin), created_at, updated_at
books: Lưu thông tin sách.
id, title, author_id, category_id, price, description, image, stock
categories: Lưu danh mục sách.
id, name
authors: Lưu thông tin tác giả.
id, name, bio
orders: Lưu thông tin đơn hàng.
id, user_id, total_amount, status, created_at
order_items: Lưu chi tiết sản phẩm trong đơn hàng.
id, order_id, book_id, quantity, price
payments: Lưu thông tin thanh toán.
id, order_id, amount, payment_method, status
reviews: Lưu đánh giá sách.
id, book_id, user_id, rating, comment
wishlists: Lưu danh sách yêu thích.
id, user_id, book_id
Quan hệ giữa các bảng
Một user có thể có nhiều orders và wishlists.
Một order có nhiều order_items, thuộc về một user.
Một book thuộc về một author và một category, có thể xuất hiện trong nhiều order_items và wishlists.
API Endpoints (Nếu có)
Nếu dự án cung cấp API, dưới đây là các endpoint mẫu:

Sách
GET /api/books: Lấy danh sách sách.
Tham số: category, author, search, page
Phản hồi: JSON chứa danh sách sách.
POST /api/books: Tạo sách mới (quản trị viên).
Body: JSON với thông tin sách.
Phản hồi: JSON sách vừa tạo.
GET /api/books/{id}: Lấy thông tin chi tiết sách.
Phản hồi: JSON của sách.
PUT /api/books/{id}: Cập nhật sách (quản trị viên).
Body: JSON với thông tin cập nhật.
Phản hồi: JSON sách đã cập nhật.
DELETE /api/books/{id}: Xóa sách (quản trị viên).
Phản hồi: Thông báo thành công.
Xác thực
POST /api/login: Đăng nhập và nhận token.
POST /api/register: Đăng ký tài khoản mới.
Lưu ý: Các endpoint API yêu cầu token xác thực qua Laravel Sanctum.

Hướng dẫn đóng góp
Chúng tôi hoan nghênh mọi đóng góp cho dự án BookStore:

Fork repository: Tạo bản sao của dự án trên GitHub của bạn.
Tạo branch mới: Làm việc trên branch riêng cho tính năng hoặc sửa lỗi.
Tuân thủ chuẩn code: Sử dụng PSR-2 cho PHP.
Viết test: Đảm bảo thay đổi được kiểm tra đầy đủ.
Gửi pull request: Mô tả chi tiết thay đổi và gửi yêu cầu xem xét.
Để báo lỗi, hãy mở issue trên GitHub với thông tin chi tiết.

Giấy phép
Dự án được phát hành theo MIT License. Xem tệp LICENSE để biết thêm chi tiết.

Liên hệ
Nếu bạn có thắc mắc hoặc cần hỗ trợ, hãy liên hệ qua:

Email: email@example.com
GitHub: https://github.com/yourusername
