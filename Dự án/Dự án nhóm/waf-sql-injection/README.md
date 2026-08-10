# 🛡️ WAF Deployment & SQL Injection Bypass Analysis

> ⚠️ Nội dung trích xuất từ Đồ án nhóm (chỉ gồm các phần do tôi trực tiếp phụ trách: 1.1, 2.1, 2.4, 3.1).

---

## 📌 Công việc phụ trách
* Phân tích kiến trúc Web 4 tầng & luồng xử lý dữ liệu.
* Triển khai OWASP ModSecurity WAF trên Nginx (Docker).
* Cấu hình Custom Rule chặn SQLi & thực nghiệm Bypass WAF.

---

## 1. Kiến trúc hệ thống (Mục 1.1 & 2.1)
* **Thành phần:** Client ➔ WAF (ModSecurity) ➔ Web Server ➔ Application Server ➔ Database Server.
* **Luồng xử lý:** Request đi qua WAF để lọc payload độc hại trước khi vào Backend. 
Nếu vi phạm rule sẽ trả về **403 Forbidden**.

---

## 2. Cấu hình WAF ModSecurity (Mục 2.4)
* **Docker Compose:** Chạy `owasp/modsecurity-crs:nginx` làm Reverse Proxy (Port 80 -> 8080).
* **Custom Rule (`my_sqli_rules.conf`):**
  * Tăng ngưỡng anomaly score lên 20 (`id:900110`).
  * Chuyển các rule SQLi tiêu chuẩn sang log-only (`942100`, `942160`, `949110`).
  * **Rule 10001:** Bắt regex `--` trong tham số ➔ Chặn ngay lập tức (Status 403).

---

## 3. Thử nghiệm & Bypass WAF (Mục 3.1)

| Kịch bản | Payload | Phản hồi | Kết quả |
| :--- | :--- | :---: | :--- |
| **1. Bị chặn** | `admin@gmail.com' or '1'='1--` | **403 Forbidden** | Kích hoạt Rule 10001 |
| **2. Bypass** | `admin@gmail.com' or '1'='1#` | **200 OK** | Đăng nhập thành công |

* **Đánh giá:** Rule `10001` chỉ chặn comment `--` nên dễ bị bypass bằng ký tự comment tương đương (`#`) trong MySQL.
* **Bài học:** Không nên viết rule quá hẹp (Signature-based), cần giữ đầy đủ bộ quy tắc OWASP CRS và validate dữ liệu ở cả tầng App.
