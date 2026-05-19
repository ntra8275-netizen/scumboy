# Hướng dẫn Triển khai Scrumboy lên Render (Miễn phí 100%)

Tài liệu này hướng dẫn chi tiết từng bước để cấu hình và triển khai dự án bảng Kanban **Scrumboy** lên nền tảng đám mây Render sử dụng Docker và Persistent Disk để lưu trữ cơ sở dữ liệu SQLite vĩnh viễn.

## Đăng ký & Chuẩn bị tài khoản
1. Truy cập [GitHub](https://github.com) và đăng ký/đăng nhập tài khoản.
2. Truy cập [Render](https://render.com) và đăng ký tài khoản bằng cách chọn **Sign up with GitHub**.

## Các bước thực hiện chi tiết

### Bước 1: Fork mã nguồn dự án về GitHub cá nhân
1. Truy cập kho lưu trữ: `https://github.com/markrai/scrumboy` (hoặc link repo này).
2. Bấm vào nút **Fork** ở góc trên bên phải.
3. Chọn tài khoản của bạn và bấm **Create fork**.

### Bước 2: Kiểm tra file render.yaml
1. Đảm bảo file `render.yaml` đã tồn tại trong thư mục gốc của repo bạn vừa fork. File này chứa cấu hình ổ đĩa 1GB miễn phí để không bị mất dữ liệu.

### Bước 3: Thực hiện Deploy trên Render
1. Đăng nhập vào [Render Dashboard](https://dashboard.render.com).
2. Bấm vào nút **New +**, chọn **Blueprint**.
3. Kết nối với GitHub và chọn kho lưu trữ `scrumboy`.
4. Nhập tên cho Service Group (ví dụ: `scrumboy-group`) rồi bấm **Apply**.
5. Đợi 3–5 phút cho đến khi trạng thái chuyển sang **Live**.

## Quản lý và Vận hành Nhóm 5 Người
1. **Đăng ký Admin:** Người đầu tiên truy cập link sẽ đăng ký tài khoản Admin.
2. **Thêm thành viên:** Gửi link cho 4 thành viên còn lại (`Phương Anh, Huy, Yến Nhi, Hương, Hoa`) để họ đăng ký.
3. **Phân quyền:** Admin tạo Project và thêm các thành viên vào để bắt đầu làm việc.
