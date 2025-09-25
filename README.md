Prometheus, Node Exporter, cAdvisor → thu thập metrics (CPU, RAM, Storage, Docker stats).

Loki, Promtail → thu thập logs từ host + container.

Grafana → hiển thị tất cả trên dashboard.

🚀 Chạy stack

docker compose up -d

📊 Truy cập:
Truy cập http://SERVER_IP:3000

- Đăng nhập (admin/admin, đổi mật khẩu mới)

- Add Data Source → chọn Prometheus → nhập URL: http://prometheus:9090

- Import dashboard có sẵn từ Grafana:

- Node Exporter Full (ID: 1860)

- Docker Container metrics (ID: 193)

- cAdvisor (ID: 14282)

Grafana: http://localhost:3000
 (admin/admin)

Prometheus: http://localhost:9090

cAdvisor: http://localhost:8080

Loki API: http://localhost:3100

Trong Grafana, bạn có thể add:

Prometheus datasource (http://prometheus:9090)

Loki datasource (http://loki:3100)

Rồi import dashboard có sẵn từ Grafana.com (ví dụ: Node Exporter Full, Docker monitoring, Loki log explorer).

import file loki-promtail-views.json vào daskboard để xem log theo container hoặc log của host một cách trực quan
