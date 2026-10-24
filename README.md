# Nguyễn Quân Mobile — Landing page + Decap CMS

Landing page tĩnh đọc nội dung từ các file Markdown trong `content/`. Trang quản trị Decap CMS nằm tại `admin/` và lưu thay đổi trở lại repository.

## Đưa website lên mạng

1. Đưa toàn bộ thư mục này lên một repository GitHub.
2. Trong Netlify, tạo site mới bằng cách kết nối repository đó. Để trống Build command và chọn thư mục publish là `.` (thư mục gốc repository).
3. Trong phần Identity của site Netlify, bật Netlify Identity. Chọn chế độ mời người dùng để giới hạn quyền truy cập quản trị.
4. Trong Identity, bật Git Gateway. Cấu hình trong `admin/config.yml` đang ghi nhánh `main`; nếu repository dùng nhánh khác, hãy đổi giá trị `branch` cho khớp.
5. Mở `/admin/` trên tên miền Netlify để đăng nhập. Mời tài khoản quản trị trong mục Identity nếu cần.

Sau khi xuất bản nội dung trong Admin, Decap CMS ghi thay đổi vào các file Markdown trên GitHub. Netlify sẽ tự triển khai bản cập nhật.

## Các mục nội dung

- `content/home.md`: tên cửa hàng, menu, banner, nội dung form và nhãn trang.
- `content/products.md`: danh sách điện thoại, tình trạng, giá, quà tặng và ảnh.
- `content/services.md`: nhóm dịch vụ, mô tả và giá khởi điểm.
- `content/trust.md`: các cam kết của cửa hàng.
- `content/feedback.md`: đánh giá và ảnh thực tế.
- `content/contact.md`: hotline, địa chỉ, giờ mở cửa, bản đồ, Zalo và Messenger.

Giá được nhập bằng số tiền VND, ví dụ `300000`; website tự định dạng thành `300.000đ`. Các giá dịch vụ chưa có thông tin được để `0`, nên trang hiển thị “Liên hệ” cho đến khi bạn cập nhật trong Admin.

## Xem thử

Không mở `index.html` trực tiếp bằng đường dẫn `file://`, vì trình duyệt chặn việc đọc các file Markdown trong trường hợp đó. Hãy deploy lên Netlify hoặc mở thư mục bằng một máy chủ web cục bộ.
