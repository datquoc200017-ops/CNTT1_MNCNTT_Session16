# BÀI TẬP VỀ NHÀ
##   Bài 9: Thiết Kế Không Gian Đa Profile Và Kiến Trúc Bookmark Cho Trạm Khám Bệnh
### Bài làm
**Phần 1: Báo cáo phân tích kiến trúc đa Profile**

**1.** Phân tích nguyên nhân sâu xa dẫn đến hiện tượng 'văng phiên đăng nhập' (Session Conflict) dưới góc độ lưu trữ Cookies trong thư mục User Data khi dùng chung 1 Profile
**Nguyên nhân xung đột:** Chrome lưu Cookies và dữ liệu đăng nhập trong thư mục User Data của từng Profile. Dùng chung một Profile có thể gây xung đột phiên đăng nhập giữa các tài khoản.

**2.** Thiết kế Mô hình 3 Profile chuyên dụng cho máy tính trạm khám CarePulse. Với mỗi Profile, nêu rõ: Tên Profile, Mục đích sử dụng, Màu Theme nhận diện thị giác, và các loại dữ liệu được lưu trữ độc lập (Cookies, History, Bookmarks, Extensions).
**Mô hình 3 Profile:**

Profile | Mục đích | Theme
|-|-|-
Work | Công việc phòng khám | Xanh dương
Personal | Học tập, tài khoản cá nhân  |Tím
Sandbox | Kiểm thử website | Cam

**Phần 2: Thiết kế hệ thống Bookmark & Quy trình an toàn**

**3.** Dựng cây thư mục Bookmark chuẩn (`Ctrl + Shift + O`) gồm 3 thư mục chính phục vụ bác sĩ trực: `📁 01_CarePulse_Clinic`, `📁 02_Pharma_Portal`, `📁 03_Medical_Tools`. Liệt kê ít nhất 3 dịch vụ web cần lưu trong mỗi thư mục.
-   `01_CarePulse_Clinic`: CarePulse, Cổng BHYT, Bộ Y tế.
    
-   `02_Pharma_Portal`: Dược thư Quốc gia, Cục Quản lý Dược, tra cứu tương tác thuốc.
    
-   `03_Medical_Tools`: Google Dịch, PubMed, Google Scholar.



**4.** Hướng dẫn áp dụng mẹo Favicon-Only cho 4 trang web dùng hàng ngày (CarePulse, Cổng BHYT, Dược thư, Google Dịch) để tiết kiệm diện tích thanh công cụ gấp 3 lần.

**Favicon-Only:** Lưu Bookmark, chỉnh sửa và xóa tên nhưng giữ nguyên URL. Áp dụng cho CarePulse, Cổng BHYT, Dược thư và Google Dịch.

**5.** Xử lý Bẫy an ninh: Khi có đoàn thanh tra hoặc khách mượn máy tính kiểm tra trong 30 phút, nhân viên phòng khám phải kích hoạt chế độ duyệt web nào (Guest Profile hay Incognito)? Giải thích lý do và cảnh báo nguy cơ nếu bật tính năng Cloud Sync tài khoản cá nhân trên máy trạm y tế này.

**An toàn khi khách mượn máy:** Sử dụng Guest Profile, đóng cửa sổ Guest sau khi dùng. Không bật Cloud Sync cá nhân, không lưu mật khẩu hoặc dữ liệu bệnh nhân trên máy dùng chung.


