# BÀI TẬP VỀ NHÀ
## Bài 3 : Xử lý Sự cố Giao diện Website Doanh nghiệp
### Bài làm
**5. Yêu cầu đầu ra**
**Phần 1: Báo cáo phân tích (I/O)**

-   **Sơ đồ Box Model hiện tại (gây lỗi):**
    
    -   **Content:**  `width: 100%`
        
    -   **Padding:**  `20px`
        
    -   **Border:**  `1px solid`
        
    -   **Margin:**  `margin-bottom: -30px`  _(Đây là nguyên nhân kéo khung "Nội dung bài học" thụt lên, đè vào "Danh sách video")._

    

**Phần 2: Thiết kế giải pháp (Styles)** Triển khai mã CSS sau để xử lý triệt để:

CSS

```
/* 1. Đưa tất cả về chuẩn border-box để tránh phình kích thước */
.noi-dung-bai-hoc, .danh-sach-video {
    box-sizing: border-box; 
    width: 100%;
}

/* 2. Đổi margin âm thành dương để đẩy hai khung ra xa nhau */
.noi-dung-bai-hoc {
    margin-bottom: 24px; 
}
```

