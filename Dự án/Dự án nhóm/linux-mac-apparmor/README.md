# Bảo mật hệ điều hành Linux — Xử lý sự cố AppArmor

## Vai trò
Đồ án học phần An toàn hệ điều hành — thực hiện theo nhóm.
Phần tôi trực tiếp phụ trách: **Troubleshooting an AppArmor profile**.
Điểm nhóm: 9/10

## Mục tiêu
Tìm hiểu và thực hành xử lý sự cố với AppArmor — một cơ chế kiểm soát truy cập bắt buộc (MAC) trên Linux.

## Công nghệ sử dụng
- Ubuntu Server
- AppArmor (profile, enforce/complain mode)

## Quá trình thực hiện
1. Tìm hiểu nguyên lý MAC (Mandatory Access Control): khác với DAC (chủ sở hữu file tự quyết định quyền truy cập), MAC áp đặt chính sách kiểm soát truy cập thống nhất trên toàn hệ thống, không ai — kể cả chủ sở hữu tài nguyên — có thể tự ý thay đổi.
2. Thực hành với profile AppArmor: khi một ứng dụng bị chặn truy cập tài nguyên ngoài phạm vi cho phép, xác định nguyên nhân qua log và chỉnh sửa profile cho phù hợp.
3. Kiểm thử lại để xác nhận ứng dụng hoạt động đúng trong giới hạn chính sách đã cấu hình.

## Bài học rút ra
Hiểu được sự khác biệt giữa MAC và DAC, và vì sao AppArmor phù hợp để giới hạn phạm vi hoạt động của một ứng dụng/dịch vụ — ngay cả khi ứng dụng đó bị khai thác, thiệt hại cũng bị giới hạn trong phạm vi chính sách cho phép (defense in depth).

## Lưu ý
Đây là đồ án học phần thực hiện theo nhóm, tôi chỉ trình bày phần cá nhân phụ trách (Troubleshooting AppArmor). Không đăng toàn bộ báo cáo nhóm vì các phần khác không phải do tôi thực hiện.
