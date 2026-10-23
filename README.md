# Website Quảng bá Sản phẩm WordPress

## 1. Giới thiệu
Dự án triển khai website quảng bá sản phẩm bằng WordPress trên Docker, tích hợp cơ sở dữ liệu MySQL và phpMyAdmin.

Hệ thống sử dụng Nginx làm Reverse Proxy, Prometheus và Grafana để giám sát, Loki và Promtail để thu thập và truy vấn log tập trung.

## 2. Kiến trúc hệ thống

Browser
→ Nginx Reverse Proxy
→ WordPress
→ MySQL

Các thành phần giám sát:
- cAdvisor: thu thập thông tin container
- MySQL Exporter: thu thập metrics MySQL
- Prometheus: thu thập và lưu metrics
- Grafana: trực quan hóa dữ liệu giám sát
- Promtail: thu thập log Docker
- Loki: lưu trữ và truy vấn log

## 3. Công nghệ sử dụng
- Docker
- Docker Compose
- WordPress
- MySQL
- phpMyAdmin
- Nginx
- Prometheus
- Grafana
- cAdvisor
- MySQL Exporter
- Loki
- Promtail
- Git/GitHub

## 4. Các cổng dịch vụ

| Dịch vụ | Port |
|---|---|
| Nginx / WordPress | 80 |
| phpMyAdmin | 8081 |
| Grafana | 3000 |
| Prometheus | 9090 |

## 5. Khởi chạy hệ thống

Tạo file `.env` dựa trên `.env.example`, sau đó chạy:

```bash
docker compose up -d
