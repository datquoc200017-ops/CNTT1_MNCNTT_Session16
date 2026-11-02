# BÀI TẬP VỀ NHÀ
## PHẦN A: QUẢN LÝ PROFILE VÀ BOOKMARK

**1. Rủi ro khi dùng chung Profile Chrome**

Khi đăng nhập hai tài khoản GitHub trên cùng một Profile, cookie và phiên đăng nhập có thể bị xung đột, gây nhầm lẫn tài khoản và ảnh hưởng đến công việc.

**2. Đề xuất 3 Profile**

-   **Personal:** Dùng cho công việc cá nhân.
    
-   **Company_Work:** Dùng cho công việc công ty.
    
-   **Sandbox_Test:** Dùng để thử nghiệm và kiểm tra.
    

**3. Cấu trúc Bookmark**

-   Personal: Gmail cá nhân, GitHub cá nhân.
    
-   Company_Work: GitHub công ty, công cụ nội bộ.
    
-   Sandbox_Test: MDN Web Docs, JSON Formatter.
    

**4. Khi cho người khác mượn máy**

Nên sử dụng Guest Profile để tránh người khác truy cập dữ liệu và tài khoản cá nhân.

## PHẦN B: QUẢN LÝ EXTENSION

**1. Extension xử lý JSON**

Chọn nhóm Dev Suite và cài đặt tiện ích JSON Viewer để định dạng dữ liệu JSON dễ đọc hơn.

**2. Nguyên tắc bảo mật**

Nên cấp quyền Site Access ở chế độ On click để hạn chế tiện ích truy cập website khi chưa cần thiết.

## PHẦN C: KIỂM TRA HTTP VÀ DEVTOOLS

**1. Quy trình tải trang web**

1.  Trình duyệt phân tích URL và tìm địa chỉ IP qua DNS.
    
2.  Thiết lập kết nối TCP và TLS nếu sử dụng HTTPS.
    
3.  Gửi HTTP Request đến máy chủ.
    
4.  Nhận Response và hiển thị nội dung trang web.
    

**2. Phân biệt lỗi HTTP**

-   **404 Not Found:** Không tìm thấy tài nguyên, cần kiểm tra URL hoặc đường dẫn.
    
-   **500 Internal Server Error:** Lỗi phía máy chủ, cần kiểm tra mã nguồn và nhật ký hệ thống.
    

**3. Các tab DevTools**

-   Elements: Kiểm tra HTML và CSS.
    
-   Console: Xem lỗi JavaScript.
    
-   Network: Kiểm tra Request và Response.
    
-   Application: Kiểm tra Cookie và bộ nhớ trình duyệt.
    

## PHẦN D: CACHE VÀ COOKIE

**1. Website không cập nhật CSS**

Sử dụng `Ctrl + Shift + R` để tải lại trang và bỏ qua cache cũ.

**2. Rủi ro Cookie**

Nếu Cookie `session_id` không có thuộc tính HttpOnly, JavaScript có thể đọc được nó. Khi website bị XSS, kẻ xấu có thể đánh cắp phiên đăng nhập.

**3. Đăng xuất nhưng giữ Cache**

Chọn chức năng Logout trên website để kết thúc phiên đăng nhập mà không cần xóa toàn bộ dữ liệu trình duyệt.

## PHẦN E: THỰC HÀNH DEVTOOLS

**1. Thay đổi màu nút**

Nhấn chuột phải vào nút, chọn Inspect, tìm thuộc tính `background-color` trong tab Styles và thay đổi màu sắc để quan sát kết quả.

**2. Quy trình kiểm tra lỗi API**

1.  Mở tab Network và thực hiện lại thao tác gây lỗi.
    
2.  Chọn Request bị lỗi.
    
3.  Kiểm tra Headers, Preview và Response.
    
4.  Xác định nguyên nhân, báo cáo cho lập trình viên và kiểm tra lại sau khi sửa.
    

**3. Lọc Request API**

-   Chọn bộ lọc Fetch/XHR trong tab Network.
    
-   Tích chọn Disable cache và tải lại trang để kiểm tra API chính xác hơn.

