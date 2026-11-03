# Portfolio CV - Lục Mạnh Tôn

## Mô tả

Website portfolio cá nhân giới thiệu Lục Mạnh Tôn và định hướng Frontend Developer. Trang gồm phần giới thiệu, kỹ năng, các dự án tiêu biểu và thông tin liên hệ. Dự án được xây dựng bằng HTML và CSS tĩnh, không cần backend.

## Chức năng

- Điều hướng đến các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Hiển thị thông tin cá nhân và các kỹ năng.
- Trình bày dự án dưới dạng các thẻ.
- Cung cấp liên kết email, GitHub và Facebook.
- Có liên kết quay lại đầu trang.

## Công nghệ

- HTML5
- CSS3
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
└── assets
	├── css
	│   └── styles.css
	└── img
		├── avatar.jpg
		├── img1.jpg
		├── img2.jpg
		├── img3.jpg
		└── img4.jpg
```

Đảm bảo các tệp CSS và hình ảnh tồn tại đúng vị trí để trang hiển thị đầy đủ.

## Cài đặt

1. Tải hoặc sao chép mã nguồn về máy.
2. Mở thư mục dự án bằng Visual Studio Code hoặc trình soạn thảo tùy chọn.
3. Kiểm tra cấu trúc thư mục và các tệp trong `assets`.

Dự án không cần cài đặt thư viện hoặc chạy lệnh build.

## Cấu hình

- Tệp CSS được liên kết tại `assets/css/styles.css`.
- Hình ảnh được tham chiếu trong thư mục `assets/img/`.
- Có thể thay đổi nội dung, thông tin liên hệ và đường dẫn ảnh trong `index.html`.
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

## Thông tin liên hệ

- **Email:** [lucmanhtonn@gmail.com](mailto:lucmanhtonn@gmail.com)
- **GitHub:** [luccmanhton-sketch](https://github.com/luccmanhton-sketch)
- **Facebook:** [Manh Ton](https://www.facebook.com/bbyoianhnhoem/)
