# Báo cáo kiểm thử — Portfolio CV

- **Ngày kiểm thử:** 27/10/2026
- **Phạm vi:** Website tĩnh trong `index.html` và `assets/css/styles.css`.
- **Môi trường:** Trình duyệt tích hợp, mở trang trực tiếp bằng `file://`; chiều rộng viewport đo được là 385 px.
- **Cách kiểm thử:** Kiểm tra cấu trúc và nội dung trang, tài nguyên ảnh, điều hướng neo, CSS và tràn ngang trên viewport đã nêu. Đây là kiểm thử thủ công kết hợp kiểm tra DOM trên trình duyệt; dự án chưa có bộ kiểm thử tự động.

## Kết quả theo tiêu chí

| # | Tiêu chí | Kết quả | Nhận xét |
|---|---|---|---|
| 1 | Tính đúng đắn | Đạt có điều kiện | Trang hiển thị đủ 4 khu vực Giới thiệu, Kỹ năng, Dự án và Liên hệ; các mục kỹ năng, 4 thẻ dự án và 5 ảnh đều được tải. Các liên kết điều hướng nội bộ có đích hợp lệ. Chưa xác minh tính chính xác của nội dung cá nhân và thông tin dự án. |
| 2 | UI/UX | Đạt trên viewport đã thử; còn điểm cần cải thiện | Ở chiều rộng 385 px, trang không tràn ngang; thanh điều hướng và nội dung các khu vực hiển thị. Chưa kiểm thử trực quan trên tablet/desktop. Bốn ảnh dự án thiếu văn bản `alt`; các liên kết “Xem chi tiết”, GitHub và LinkedIn hiện dùng `href="#"`, chưa dẫn tới đích thực tế. |
| 3 | Khả năng vận hành — xử lý lỗi | Đạt trong phạm vi trang tĩnh | Trang mở trực tiếp trong trình duyệt, CSS và toàn bộ ảnh được tải; điều hướng neo hoạt động. Ứng dụng không có backend, biểu mẫu hay thao tác dữ liệu động nên không có luồng xử lý lỗi nghiệp vụ để kiểm thử. Chưa thử tình huống mất tài nguyên hoặc lỗi khi phục vụ qua HTTP. |
| 4 | Bảo mật | Chưa đánh giá đầy đủ; bề mặt rủi ro thấp | Kiểm tra mã nguồn ở mức cơ bản: trang tĩnh, không thấy mã JavaScript thực thi, biểu mẫu nhập liệu hoặc kết nối backend. Không chạy công cụ quét bảo mật; chưa đánh giá HTTPS, cấu hình máy chủ và HTTP security headers vì trang được mở bằng `file://`. |
| 5 | Chất lượng mã nguồn | Đạt một phần | HTML có cấu trúc ngữ nghĩa, CSS được tách riêng và dùng biến, Flexbox, Grid cùng media query. Cần bổ sung `alt` cho 4 ảnh dự án, thay liên kết mẫu `#` bằng địa chỉ thật và bổ sung kiểm thử/lint tự động khi phù hợp. |
| 6 | Khả năng triển khai | Chưa xác minh đầy đủ | README hướng dẫn mở trực tiếp, dùng máy chủ HTTP và Docker/Nginx. Đã xác minh cách mở trực tiếp; chưa chạy thử HTTP, Docker hoặc triển khai lên môi trường hosting thực tế. |

## Ảnh minh chứng

Các ảnh dưới đây được chụp từ trang đang chạy trong trình duyệt, ở viewport rộng 385 px:

- [Toàn trang trên viewport di động](screenshots/portfolio-mobile-toan-trang.png)
- [Khu vực giới thiệu](screenshots/portfolio-gioi-thieu.png)
- [Khu vực dự án](screenshots/portfolio-du-an.png)

## Kết luận

Các nội dung chính và cách mở trang tĩnh hoạt động trong phạm vi đã kiểm thử; không phát hiện lỗi tải ảnh hoặc tràn ngang ở viewport di động đã thử. Trước khi phát hành, nên bổ sung `alt` cho ảnh dự án, cập nhật các liên kết còn là `#`, và kiểm thử thêm trên tablet, desktop cũng như qua HTTP hoặc Docker. Báo cáo này không thay thế cho kiểm thử bảo mật hoặc kiểm thử triển khai đầy đủ.