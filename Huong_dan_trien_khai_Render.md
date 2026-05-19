# Hướng dẫn Triển khai Scrumboy lên Render (Miễn phí & Lưu trữ vĩnh viễn)

Tài liệu này hướng dẫn chi tiết từng bước để triển khai **Scrumboy** lên Render sử dụng **Persistent Disk (1GB)** để đảm bảo dữ liệu của nhóm 5 người không bị mất.

## Lưu ý về Gói Free & Disk
Mặc dù Render thông báo gói Free không hỗ trợ Disk khi tạo bằng tay, nhưng khi sử dụng **Render Blueprint (file render.yaml)**, hệ thống vẫn cho phép gắn ổ đĩa 1GB miễn phí. Đây là cách duy nhất để chạy dự án này mà không bị mất dữ liệu.

## Các bước thực hiện chi tiết

### Bước 1: Fork mã nguồn dự án về GitHub cá nhân
1. Truy cập: `https://github.com/ntra8275-netizen/scumboy.git`
2. Bấm nút **Fork** ở góc trên bên phải để đưa về tài khoản của bạn.

### Bước 2: Thực hiện Deploy trên Render
1. Đăng nhập vào [Render Dashboard](https://dashboard.render.com).
2. Bấm nút **New +**, chọn **Blueprint**.
3. Kết nối với GitHub và chọn kho lưu trữ `scumboy` bạn vừa fork.
4. Nhập tên cho Service Group (ví dụ: `scrumboy-group`) rồi bấm **Apply**.
5. Đợi 3–5 phút cho đến khi trạng thái chuyển sang **Live**.

## Quản lý và Vận hành Nhóm 5 Người
1. **Đăng ký Admin:** Người đầu tiên truy cập link web sẽ đăng ký tài khoản Quản trị.
2. **Thêm thành viên:** Gửi link web cho 4 thành viên (`Phương Anh, Huy, Yến Nhi, Hương, Hoa`) để họ đăng ký tài khoản.
3. **Đồng bộ dữ liệu:** Vì dùng chung ổ đĩa `/data/app.db`, mọi thay đổi của bất kỳ ai cũng sẽ hiển thị ngay lập tức cho cả nhóm. Dữ liệu sẽ không bị xóa ngay cả khi server khởi động lại.
