# Portfolio Vy Xuân Hoàng

## Giới thiệu

Website portfolio cá nhân giới thiệu Vy Xuân Hoàng, sinh viên Công nghệ thông tin định hướng Frontend Developer. Trang trình bày phần giới thiệu, kỹ năng, các dự án tiêu biểu và thông tin liên hệ.

## Chức năng

- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Hiển thị kỹ năng và sáu dự án mẫu: bán điện thoại, đặt phòng khách sạn, quản lý thư viện, đặt vé xem phim, quản lý chi tiêu và máy tính khoa học.
- Hiển thị ảnh đại diện và ảnh minh họa dự án.
- Bố cục responsive, hỗ trợ màn hình máy tính và thiết bị di động.
- Có liên kết email và liên kết quay lại đầu trang.

## Công nghệ

- HTML5: cấu trúc và nội dung trang.
- CSS3: giao diện, bố cục responsive và hiệu ứng hiển thị.
- JavaScript được liệt kê trong phần kỹ năng và mô tả dự án; trang portfolio hiện tại không cần bước biên dịch hay cài thư viện để chạy.
- Docker tùy chọn, dùng Nginx để phục vụ các tệp tĩnh.

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Edge, Firefox hoặc Safari.
- Không bắt buộc cài Node.js, npm hay cơ sở dữ liệu.
- Để chạy máy chủ cục bộ: Python 3 (tùy chọn).
- Để chạy bằng container: Docker Engine hoặc Docker Desktop đang hoạt động.

## Cài đặt

Tải hoặc sao chép mã nguồn vào máy, sau đó mở terminal tại **thư mục gốc của dự án** — thư mục chứa `index.html` và thư mục `assets/`. File README này nằm trong `assets/`, nhưng các lệnh bên dưới đều cần chạy từ thư mục gốc.

Không cần cài đặt gói phụ thuộc. Cấu trúc chính:

```text
project/
├── index.html
└── assets/
	├── css/styles.css
	├── img/
	└── README.md
```

## Cấu hình

Dự án hiện không sử dụng tệp cấu hình môi trường, máy chủ API hay thông tin bí mật.

- Nội dung, tiêu đề trang và thông tin liên hệ: chỉnh sửa trong `index.html`.
- Màu sắc, kiểu chữ và bố cục: chỉnh sửa trong `assets/css/styles.css`.
- Ảnh: đặt trong `assets/img/` và cập nhật đường dẫn tương ứng trong `index.html`.
- Trước khi xuất bản, hãy kiểm tra lại email và cập nhật URL GitHub/LinkedIn. Hai liên kết hồ sơ trong trang hiện đang dùng `href="#"` nên chưa mở đến trang hồ sơ.

## Chạy thử

### Cách nhanh: mở trực tiếp

Mở `index.html` bằng trình duyệt. Cách này phù hợp để xem giao diện cơ bản và không cần cài thêm phần mềm.

### Windows

Mở PowerShell hoặc Command Prompt tại thư mục gốc dự án.

Với Python đã cài:

```powershell
py -m http.server 8000
```

Hoặc dùng Command Prompt nếu lệnh `py` không có nhưng `python` đã được cài:

```bat
python -m http.server 8000
```

Mở <http://localhost:8000>. Dừng máy chủ bằng `Ctrl+C`.

### macOS

Mở Terminal, chuyển đến thư mục gốc dự án rồi chạy:

```bash
cd /duong-dan/toi/project
python3 -m http.server 8000
```

Mở <http://localhost:8000>. Dừng máy chủ bằng `Ctrl+C`.

### Linux

Mở terminal, chuyển đến thư mục gốc dự án rồi chạy:

```bash
cd /duong-dan/toi/project
python3 -m http.server 8000
```

Mở <http://localhost:8000>. Dừng máy chủ bằng `Ctrl+C`.

Nếu cổng `8000` đang được sử dụng, thay `8000` trong lệnh bằng một cổng khác, ví dụ `8080`, rồi mở URL tương ứng.

### Docker

Cài và khởi động Docker Desktop (Windows/macOS) hoặc Docker Engine (Linux). Chạy lệnh từ thư mục gốc dự án để mount mã nguồn chỉ đọc vào Nginx.

PowerShell:

```powershell
docker run --rm --name portfolio -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

Command Prompt:

```bat
docker run --rm --name portfolio -p 8080:80 -v "%cd%:/usr/share/nginx/html:ro" nginx:alpine
```

macOS/Linux:

```bash
docker run --rm --name portfolio -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Mở <http://localhost:8080>. Container chạy ở foreground; nhấn `Ctrl+C` để dừng và tự xóa container. Docker sẽ tự tải image `nginx:alpine` ở lần chạy đầu tiên. Nếu cổng `8080` đã được sử dụng, đổi phần `8080:80` thành một cổng trống khác, chẳng hạn `8081:80`, rồi mở cổng đó trên trình duyệt.

## Thông tin liên hệ

- **Tên:** Vy Xuân Hoàng
- **Email:** [hvyndp02@gmail.com](mailto:hvyndp02@gmail.com)
- **GitHub:** `github.com/vyxuanhoang` (cần cập nhật liên kết hoạt động trong trang)
- **LinkedIn:** `linkedin.com/in/vyxuanhoang` (cần cập nhật liên kết hoạt động trong trang)
