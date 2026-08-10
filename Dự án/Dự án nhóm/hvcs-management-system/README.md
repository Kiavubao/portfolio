# Phần mềm quản lý việc tham gia các cuộc thi của sinh viên HVCS

## Vai trò
Đồ án học phần Công nghệ phần mềm — thực hiện theo nhóm 3 thành viên.
**Vai trò của tôi: Trưởng nhóm** — điều phối tiến độ, tổng hợp yêu cầu nghiệp vụ (quy trình quản lý cuộc thi, đăng ký, duyệt hồ sơ, công bố kết quả), tham gia thiết kế use case và góp ý hoàn thiện chức năng hệ thống.
Điểm: 8/10

## Mục tiêu
Xây dựng hệ thống quản lý tập trung cho việc tổ chức, đăng ký và công bố kết quả các cuộc thi phong trào/học thuật của sinh viên tại Học viện, thay thế quy trình thủ công (giấy tờ, Google Form, tổng hợp Excel) trước đây.

## Công nghệ sử dụng
- **Frontend:** HTML, CSS, JavaScript (mô hình SPA — Single Page Application)
- **Backend:** Node.js, Express.js, REST API
- **Database:** SQL Server (12 bảng, chuẩn hóa 3NF)
- **Xác thực & bảo mật:** JWT (JSON Web Token), RBAC (5 vai trò: Admin, Cán bộ, Giảng viên, Sinh viên, Khách)
- **Triển khai:** Docker (node:20-alpine), dotenv quản lý biến môi trường

## Quá trình thực hiện
1. Khảo sát quy trình quản lý cuộc thi thủ công hiện tại, xác định điểm nghẽn nghiệp vụ
2. Phân tích yêu cầu chức năng theo từng nhóm người dùng, thiết kế 9 use case chính
3. Thiết kế cơ sở dữ liệu quan hệ (sơ đồ ERD, 12 bảng) và kiến trúc REST API
4. Xây dựng giao diện SPA với Dashboard cá nhân hóa theo vai trò
5. Kiểm thử toàn bộ luồng nghiệp vụ: đăng ký → xác nhận (GV) → duyệt (Cán bộ) → công bố kết quả

## Kết quả
- Hoàn thành 14/14 chức năng đề ra (100%)
- Hệ thống phân quyền RBAC đầy đủ cho 5 vai trò người dùng
- Cơ chế ghi nhật ký (logging) toàn bộ thao tác thay đổi dữ liệu, đảm bảo minh bạch và có thể truy vết

## Bài học rút ra
Hiểu được cách áp dụng kiến trúc RESTful API kết hợp xác thực JWT không trạng thái (stateless) vào một hệ thống nghiệp vụ thực tế nhiều vai trò; đồng thời rèn kỹ năng điều phối nhóm — tổng hợp yêu cầu từ nhiều phía (Cán bộ, Giảng viên, Sinh viên) thành đặc tả chức năng cụ thể cho đội phát triển.

## Mã nguồn đầy đủ
Đây là sản phẩm chung của nhóm. Toàn bộ mã nguồn được lưu trữ tại repo chính thức của nhóm:
🔗 [github.com/LeQuocHuy025/NhapMon_CongNghePhanMem](https://github.com/LeQuocHuy025/NhapMon_CongNghePhanMem)

## Lưu ý
Đây là đồ án học phần thực hiện theo nhóm. Phần tôi trực tiếp phụ trách: điều phối nhóm, phân tích và tổng hợp yêu cầu nghiệp vụ, góp ý thiết kế use case và hoàn thiện chức năng hệ thống.
