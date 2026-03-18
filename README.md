# Web_Project
Đây là bài tập lớn môn học Lập trình web, học kỳ 252, trường Đại học Bách Khoa TPHCM. 

# Công việc chung
# 1. Thiết kế mô hình ứng dụng (không sử dụng PHP framework)
# Ý tưởng hệ thống
    Tên mô hình: Website bán nội thất
    Vai trò người dùng: khách, thành viên, quản trị viên
# Kiến trúc tổng thể
    Mô hình: MVC chuẩn, tách frontend và admin
    Frontend - Khách và thành viên:
        + Trang chủ
        + Giới thiệu
        + Sản phẩm
        + Chi tiết sản phẩm
        + Giỏ hàng
        + Tin tức
        + FAQ
        + Liên hệ
        + Đăng ký/đăng nhập
        + Tài khoản cá nhân
    Admin - Quản trị viên:
        + dashboard
        + quản lý user
        + quản lý sản phẩm
        + quản lý đơn hàng
        + quản lý bài viết
        + quản lý bình luận
        + quản lý liên hệ
        + quản lý FAQ
        + quản lý nội dung khác trang public
# Cấu trúc thư mục chuẩn MVC 
    Web_Project/
    │
    ├── app/
    │   ├── controllers/
    │   │   ├── frontend/
    │   │   │   ├── HomeController.php
    │   │   │   ├── PageController.php
    │   │   │   ├── ProductController.php
    │   │   │   ├── CartController.php
    │   │   │   ├── OrderController.php
    │   │   │   ├── PostController.php
    │   │   │   ├── ContactController.php
    │   │   │   ├── FaqController.php
    │   │   │   ├── AuthController.php
    │   │   │   └── UserController.php
    │   │   │
    │   │   └── admin/
    │   │       ├── DashboardController.php
    │   │       ├── UserController.php
    │   │       ├── ProductController.php
    │   │       ├── CategoryController.php
    │   │       ├── OrderController.php
    │   │       ├── PostController.php
    │   │       ├── CommentController.php
    │   │       ├── ContactController.php
    │   │       ├── FaqController.php
    │   │       └── PageController.php
    │   │
    │   ├── models/
    │   │   ├── UserModel.php
    │   │   ├── ProductModel.php
    │   │   ├── CategoryModel.php
    │   │   ├── CartModel.php
    │   │   ├── CartItemModel.php
    │   │   ├── OrderModel.php
    │   │   ├── OrderItemModel.php
    │   │   ├── PostModel.php
    │   │   ├── CommentModel.php
    │   │   ├── ContactModel.php
    │   │   ├── FaqModel.php
    │   │   └── PageModel.php
    │   │
    │   ├── views/
    │   │   ├── frontend/
    │   │   │   ├── layouts/
    │   │   │   │   ├── header.php
    │   │   │   │   ├── footer.php
    │   │   │   │   └── main.php
    │   │   │   ├── home/
    │   │   │   ├── pages/
    │   │   │   ├── products/
    │   │   │   ├── cart/
    │   │   │   ├── orders/
    │   │   │   ├── posts/
    │   │   │   ├── contacts/
    │   │   │   ├── faqs/
    │   │   │   ├── auth/
    │   │   │   └── users/
    │   │   │
    │   │   └── admin/
    │   │       ├── layouts/
    │   │       ├── dashboard/
    │   │       ├── users/
    │   │       ├── categories/
    │   │       ├── products/
    │   │       ├── orders/
    │   │       ├── posts/
    │   │       ├── comments/
    │   │       ├── contacts/
    │   │       ├── faqs/
    │   │       └── pages/
    │   │
    │   ├── core/
    │   │   ├── Database.php
    │   │   ├── Router.php
    │   │   ├── Controller.php
    │   │   ├── Model.php
    │   │   ├── Request.php
    │   │   ├── Response.php
    │   │   ├── Session.php
    │   │   ├── Auth.php
    │   │   └── Validator.php
    │   │
    │   ├── middlewares/
    │   │   ├── AuthMiddleware.php
    │   │   └── AdminMiddleware.php
    │   │
    │   └── helpers/
    │       ├── url_helper.php
    │       ├── text_helper.php
    │       └── upload_helper.php
    │
    ├── config/
    │   ├── app.php
    │   ├── database.php
    │   └── routes.php
    │
    ├── public/
    │   ├── index.php
    │   ├── .htaccess
    │   └── assets/
    │       ├── css/
    │       ├── js/
    │       ├── images/
    │       └── uploads/
    │
    ├── database/
    │   └── web_assignment.sql
    │
    └── README.md
