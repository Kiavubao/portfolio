# 🛡️ Hồ Gia Bảo — SOC Analyst Portfolio

Chào bạn! Tôi là **Hồ Gia Bảo**, định hướng trở thành **SOC Analyst / Security Engineer**. Portfolio này tổng hợp các dự án Homelab cá nhân và các đồ án môn học chuyên ngành An toàn thông tin / Mạng máy tính mà tôi đã thực hiện.

Mục tiêu chính của tôi là nghiên cứu, thiết lập hệ thống giám sát an toàn thông tin (SIEM/Wazuh), xây dựng Custom Detection Rules (nhận diện Brute Force, Malicious Activity) và phân tích log chuyên sâu.

---

## 🛠️ Kỹ năng & Công nghệ chính

- **SIEM & Monitoring**: Wazuh SIEM, Windows Event Logs (EventChannel), Sysmon.
- **System & Security Admin**: Windows Server (Active Directory, DNS, DHCP, GPO), Linux (Ubuntu, CentOS), AppArmor.
- **Rule Engineering & Threat Detection**: Custom XML Rules, MITRE ATT&CK Mapping (T1110), WAF Configuration.
- **Scripting & Automation**: Bash Shell, PowerShell, Python.
- **Networking & Protocols**: TCP/IP, NAT, ACL, Network Traffic Analysis.

---

## 📂 Danh mục Dự án (Projects Overview)

### 1. [Homelab Wazuh SIEM — Detection Engineering](./homelab-wazuh-siem/) *(Dự án cá nhân)*
- **Mô tả ngắn**: Xây dựng hệ thống giám sát tập trung Wazuh SIEM, viết Custom Rules (XML) phát hiện tấn công Brute Force tài khoản Administrator trên Windows Server 2019 theo chuẩn MITRE ATT&CK (T1110).
- **Công nghệ**: Wazuh Manager, Wazuh Agent, Windows Server 2019, MITRE ATT&CK.

### 2. [Windows Server DNS & DHCP Infrastructure](./dns-dhcp-windows-server/) *(Đồ án môn học)*
- **Mô tả ngắn**: Triển khai và cấu hình hạ tầng dịch vụ mạng cốt lõi DNS (Zone Transfer, Dynamic Update) và DHCP (Scope, Reservation, Failover) trên môi trường Windows Server.
- **Vai trò**: Phụ trách phần dựng cấu hình chi tiết dịch vụ Windows Server (W2).

### 3. [WAF Configuration & SQL Injection Protection](./waf-sql-injection/) *(Đồ án nhóm)*
- **Mô tả ngắn**: Phân tích cơ chế tấn công SQL Injection, thiết lập và tối ưu hóa luật bộ lọc WAF để chặn các payload độc hại trên mô hình ứng dụng 3 lớp (3-tier).
- **Vai trò**: Trực tiếp phân tích và viết báo cáo các mục 1.1, 2.1, 2.4, 3.1.

### 4. [Mandatory Access Control with AppArmor](./linux-mac-apparmor) *(Đồ án nhóm)*
- **Mô tả ngắn**: Nghiên cứu và thực hành cơ chế kiểm soát truy cập bắt buộc (MAC) trên hệ thống Linux/macOS sử dụng AppArmor nhằm cô lập ứng dụng và hạn chế leo thang quyền hạn.
- **Vai trò**: Phụ trách phần cấu hình và xử lý lỗi (troubleshooting) mục 1.3, 1.4.

5. 🏆 [HVCS Contest Management Platform](./hvcs-management-system) *(Phần mềm/Đồ án)*
- **Mô tả ngắn:** Xây dựng/Triển khai hệ thống phần mềm quản lý cuộc thi HVCS, hỗ trợ tổ chức, giám sát và quản lý dữ liệu thí sinh.
---

## 📄 Thông tin liên hệ
- **Email**: hogiabao17102005@gmail.com
- **GitHub**: [github.com/Kiavubao](https://github.com/Kiavubao)

---
*Lưu ý: Đối với các đồ án thực hiện theo nhóm, nội dung trong từng folder ghi rõ chính xác phần tôi phụ trách nhằm đảm bảo tính trung thực và tôn trọng bản quyền của các thành viên.*
