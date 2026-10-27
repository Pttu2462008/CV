# Portfolio CV - Phạm Tuấn Tú

## Mô tả dự án

Website portfolio cá nhân giới thiệu Phạm Tuấn Tú với định hướng Frontend Developer. Trang được xây dựng theo dạng website tĩnh, trình bày thông tin cá nhân, kỹ năng, các dự án tiêu biểu và cách liên hệ.

## Chức năng

- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Hiển thị phần giới thiệu, vai trò nghề nghiệp và lời kêu gọi xem dự án hoặc liên hệ.
- Trình bày kỹ năng và dự án bằng bố cục lưới.
- Bố cục responsive cho điện thoại, máy tính bảng và máy tính.
- Liên kết email và các hồ sơ mạng xã hội.
- Không cần máy chủ ứng dụng, cơ sở dữ liệu hoặc bước biên dịch.

## Công nghệ

- HTML5: cấu trúc và nội dung trang.
- CSS3: giao diện, Flexbox, CSS Grid và responsive design.
- JavaScript được nêu trong danh sách kỹ năng trên trang; phiên bản hiện tại không cần JavaScript để hoạt động.
- Nginx (tùy chọn): phục vụ trang tĩnh khi chạy bằng Docker.

## Yêu cầu môi trường

Để mở trực tiếp, chỉ cần trình duyệt web hiện đại. Để chạy máy chủ phát triển cục bộ, cài Python 3. Để chạy bằng Docker, cài Docker Desktop (Windows/macOS) hoặc Docker Engine (Linux).

Không cần cài Node.js, npm hay thư viện phụ thuộc.

## Cài đặt

Tải hoặc sao chép toàn bộ mã nguồn vào máy. Nếu dự án được lưu trong Git, có thể sao chép bằng lệnh sau (thay URL mẫu bằng địa chỉ repository thực tế):

```bash
git clone <URL_REPOSITORY>
cd <TEN_THU_MUC_DU_AN>
```

Đảm bảo giữ nguyên cấu trúc thư mục, đặc biệt là `index.html` và thư mục `assets/`.

## Cấu hình và tùy chỉnh

- Nội dung, tiêu đề, mô tả, thông tin dự án và liên kết liên hệ: chỉnh sửa trong `index.html`.
- Màu sắc, kiểu chữ, khoảng cách và bố cục: chỉnh sửa các biến CSS ở đầu `assets/css/styles.css`.
- Ảnh đại diện và ảnh minh họa: thay các ảnh trong `assets/img/` hoặc cập nhật đường dẫn ảnh trong `index.html`. Các ảnh hiện được tham chiếu gồm `avatar.jpg`, `avatar2.jpg`, `avatar3.jpg`, `avatar4.jpg` và `avatar5.jpg`.
- Trước khi xuất bản, hãy thay email `tu.pham@example.com` và các liên kết hồ sơ mẫu bằng thông tin liên hệ thực tế.

## Chạy thử

Có thể mở trực tiếp `index.html` trong trình duyệt. Nếu muốn kiểm tra trang qua máy chủ HTTP cục bộ, chạy lệnh phù hợp với hệ điều hành bên dưới, sau đó truy cập `http://localhost:8000`.

### Windows

Mở PowerShell trong thư mục dự án:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có, thử `python -m http.server 8000`. Dừng máy chủ bằng `Ctrl+C`.

### macOS

Mở Terminal trong thư mục dự án:

```bash
python3 -m http.server 8000
```

Dừng máy chủ bằng `Control+C`.

### Linux

Mở Terminal trong thư mục dự án:

```bash
python3 -m http.server 8000
```

Nếu Python 3 chưa được cài, cài đặt bằng trình quản lý gói của bản phân phối Linux rồi chạy lại lệnh. Dừng máy chủ bằng `Ctrl+C`.

## Chạy bằng Docker

Cần cài và khởi động Docker trước. Chạy lệnh tại thư mục gốc dự án để Nginx phục vụ nội dung trên cổng `8080`.

Windows PowerShell:

```powershell
docker run --rm -d --name portfolio-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

macOS hoặc Linux:

```bash
docker run --rm -d --name portfolio-cv -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Mở `http://localhost:8080` để xem trang. Dừng container bằng:

```bash
docker stop portfolio-cv
```

## Thông tin liên hệ

- Tên hiển thị: Phạm Tuấn Tú
- Email mẫu trong trang: `tu.pham@example.com`
- GitHub mẫu trong trang: `github.com/phamtuantu`
- LinkedIn mẫu trong trang: `linkedin.com/in/phamtuantu`

Các thông tin trên được lấy từ nội dung hiện tại của trang; email và liên kết hồ sơ có thể là dữ liệu mẫu. Vui lòng xác minh và cập nhật trước khi chia sẻ hoặc triển khai công khai.
