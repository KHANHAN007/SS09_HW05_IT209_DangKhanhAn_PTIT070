## 1. Cấu hình dịch vụ

File `docker-compose.yml`:

```yaml
services:
  web:
    image: nginx:alpine
    ports:
      - "8082:80"
```

Dịch vụ `web` sử dụng image `nginx:alpine`.
Cổng 8082 trên máy cá nhân được ánh xạ tới cổng 80 trong container.

## 2. Kiểm tra và khởi chạy

```bash
docker compose config
docker compose up -d
docker compose ps
```

Dán kết quả thực tế của `docker compose ps` tại đây.

## 3. Kiểm tra website

```bash
curl -i http://localhost:8082
```

Dán HTTP status và đoạn HTML chứa `Welcome to nginx!` tại đây.

## 4. Hạ dịch vụ

```bash
docker compose down
docker compose ps
```

Dán kết quả thực tế sau khi hạ dịch vụ tại đây.

