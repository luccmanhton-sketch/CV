# Portfolio CV - Lục Mạnh Tôn

## Mô tả

Website portfolio cá nhân giới thiệu Lục Mạnh Tôn theo vai trò Frontend Developer.
Trang là tài liệu HTML/CSS tĩnh, gồm các phần giới thiệu, kỹ năng, dự án tiêu biểu,
liên hệ và điều hướng quay lại đầu trang. Dự án không sử dụng JavaScript, framework,
backend hay quy trình build.

## Chức năng

- Điều hướng neo đến Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Hiển thị kỹ năng bằng danh sách thẻ.
- Trình bày dự án bằng lưới responsive.
- Kiểm tra dữ liệu cơ bản trong biểu mẫu bằng thuộc tính HTML `required` và `type="email"`.
- Hỗ trợ bàn phím qua kiểu `:focus-visible` và giảm chuyển động qua `prefers-reduced-motion`.

## Trạng thái

- Trang đã sẵn sàng để xem và triển khai dưới dạng nội dung tĩnh.
- Bốn liên kết dự án vẫn dùng `href="#"` và cần thay bằng URL dự án thực tế.
- Biểu mẫu liên hệ chỉ có giao diện và kiểm tra phía trình duyệt; chưa được kết nối
  backend, dịch vụ email hoặc API nhận dữ liệu.
- Nội dung giới thiệu, dự án và hình ảnh placeholder cần được thay bằng thông tin thực tế
  trước khi sử dụng chính thức.

## Công nghệ

- HTML5
- CSS3 với Flexbox và CSS Grid
- Docker và Nginx (tùy chọn để chạy thử)

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Không cần cài Node.js hay thư viện.
- Nếu chạy bằng máy chủ cục bộ: cần Python 3.
- Nếu chạy bằng Docker: cần Docker Desktop trên Windows/macOS hoặc Docker Engine trên Linux.

## Cấu trúc dự án

```text
.
├── index.html
├── assets/
│   ├── css/
│   │   └── styles.css
│   └── img/
│       ├── avatar.jpg
│       ├── img1.jpg
│       ├── img2.jpg
│       ├── img3.jpg
│       └── img4.jpg
├── docs/
│   ├── test_report.md
│   └── screenshots/
│       ├── 01-desktop.png
│       └── 02-mobile.png
├── README.md
└── CHANGELOG.md
```

Giữ nguyên cấu trúc tương đối để các liên kết CSS, ảnh và tài liệu hoạt động đúng.

## Cài đặt

1. Tải hoặc sao chép mã nguồn về máy.
2. Mở thư mục dự án bằng Visual Studio Code hoặc trình soạn thảo tùy chọn.
3. Kiểm tra cấu trúc thư mục và các tệp trong `assets`.

Dự án không cần cài đặt thư viện hoặc chạy lệnh build.

## Cấu hình

- Tệp CSS được liên kết tại `assets/css/styles.css`.
- Hình ảnh được tham chiếu trong thư mục `assets/img/`.
- Nội dung trang và đường dẫn liên hệ có thể chỉnh trong `index.html`.
- URL Facebook, GitHub và email hiện được lấy từ thông tin liên hệ của trang.
- Không cần tệp cấu hình môi trường hoặc khóa API.

## Chạy thử

### Mở trực tiếp

Mở tệp `index.html` bằng trình duyệt.

### Chạy bằng máy chủ cục bộ

Mở terminal tại thư mục dự án và chạy lệnh phù hợp với hệ điều hành.

**Windows PowerShell:**

```powershell
py -m http.server 8000
```

**macOS:**

```bash
python3 -m http.server 8000
```

**Linux:**

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### Chạy bằng Docker

Đảm bảo Docker đang hoạt động và terminal đang ở thư mục dự án.

**Windows PowerShell:**

```powershell
docker run --name portfolio -d -p 8080:80 --mount "type=bind,source=$($PWD.Path),target=/usr/share/nginx/html,readonly" nginx:alpine
```

**Windows Command Prompt:**

```cmd
docker run --name portfolio -d -p 8080:80 -v "%cd%:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS hoặc Linux:**

```bash
docker run --name portfolio -d -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Mở <http://localhost:8080> để xem trang. Dừng và xóa container bằng lệnh:

```bash
docker rm -f portfolio
```

## Tài liệu kiểm thử

- Báo cáo kết quả: [docs/test_report.md](docs/test_report.md)
- Ảnh desktop: [docs/screenshots/01-desktop.png](docs/screenshots/01-desktop.png)
- Ảnh mobile: [docs/screenshots/02-mobile.png](docs/screenshots/02-mobile.png)

## Thông tin liên hệ

- **Email:** [lucmanhtonn@gmail.com](mailto:lucmanhtonn@gmail.com)
- **GitHub:** [luccmanhton-sketch](https://github.com/luccmanhton-sketch)
- **Facebook:** [Manh Ton](https://www.facebook.com/bbyoianhnhoem/)
