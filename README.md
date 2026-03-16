# SEO Doctor Image Backup

SEO Doctor Image Backup là một **tiện ích nhỏ** giúp bạn lọc và tối ưu thư mục lưu trữ hình ảnh của website, đặc biệt hữu ích với các website có nhiều bài viết đã xóa hoặc di chuyển server lưu trữ, nhưng vẫn còn rất nhiều file ảnh không còn được sử dụng. 

## Tính năng chính

- Đọc danh sách URL ảnh từ file `.txt` (crawl từ các công cụ như Website Auditor, Screaming Frog…). 
- Tự động đối chiếu danh sách URL ảnh với thư mục chứa ảnh gốc (ví dụ: `/uploads/`) bạn đã tải về từ server. 
- Sao chép toàn bộ ảnh vẫn đang được sử dụng sang một thư mục mới (mặc định: `newuploads`). 
- Hỗ trợ dọn dẹp dung lượng hosting, giúp thao tác backup/restore nhanh và nhẹ hơn. 
- Chạy trực tiếp trên Windows, tận dụng tài nguyên máy nên xử lý nhanh với số lượng lớn file. 

## Khi nào nên dùng công cụ này?

Công cụ đặc biệt phù hợp trong các tình huống:

- Bạn thay đổi server lưu trữ hình ảnh, còn thư mục ảnh cũ nhưng thiếu đồng bộ với dữ liệu website. 
- Website có hàng ngàn bài viết, sau một đợt dọn dẹp/xóa bài lớn, trên hosting còn lại rất nhiều ảnh “mồ côi” không còn được gắn trong bài. 
- Bạn muốn giảm dung lượng thư mục uploads trước khi backup hoặc tối ưu chi phí lưu trữ. 

Ví dụ điển hình: sau khi xóa hàng ngàn bài cũ trên một website lớn, bạn cần lọc lại thư mục `/uploads/` để chỉ giữ ảnh còn đang được sử dụng trên site. 

## Cách hoạt động (luồng xử lý)

1. Tải toàn bộ thư mục ảnh từ server về máy tính, ví dụ: `uploads/`. 
2. Dùng công cụ crawl (Website Auditor, Screaming Frog…) để trích xuất toàn bộ URL hình ảnh đang được sử dụng trên website, lưu thành file `.txt`. 
3. Mở phần mềm SEO Doctor Image Backup, cấu hình:
   - Đường dẫn file `.txt` chứa danh sách ảnh.  
   - Đường dẫn thư mục ảnh gốc (ví dụ: `uploads/`).  
   - Thư mục đích để xuất ảnh mới (ví dụ: `newuploads/`).  
   - Domain cần thay thế/chuẩn hóa trong file danh sách ảnh (mặc định là thanhtrungmobile.vn)
4. Nhấn nút `Start Extraction` để phần mềm:
   - Đọc từng URL ảnh trong file `.txt`.  
   - Tìm file tương ứng trong thư mục `uploads/`.  
   - Nếu tìm thấy, sao chép sang thư mục `newuploads/`. 
5. Sau khi hoàn tất, bạn có thể:
   - Xóa thư mục `uploads` cũ trên server.  
   - Upload lại nội dung thư mục `newuploads` để sử dụng làm thư mục ảnh chuẩn đã được “làm sạch”. 

## Yêu cầu hệ thống

- Hệ điều hành: Windows (đã được kiểm thử hoạt động tốt trên Windows 11). 
- Dung lượng file chạy: khoảng 11.202 KB. 

## Cài đặt và sử dụng

1. Tải bản phát hành mới nhất tại phần **Releases** trên GitHub hoặc link phát hành kèm theo. 
2. Giải nén (nếu cần) và chạy file `SeoDoctor_Image_Backup.exe` trên máy Windows. 
3. Chuẩn bị:
   - Thư mục ảnh tải về từ server, ví dụ: `uploads/`.  
   - File `.txt` chứa danh sách URL ảnh đang sử dụng.  
4. Mở phần mềm, cấu hình các đường dẫn và domain như hướng dẫn, sau đó bấm `Start Extraction`. 

Phần mềm không yêu cầu cài đặt thêm, không cần đăng ký tài khoản và không yêu cầu quyền đặc biệt; chỉ cần tải về và chạy. 

## Lưu ý quan trọng

- Đảm bảo bạn thay **đúng domain** trong phần cấu hình để khớp với domain trong file chứa danh sách ảnh, tránh việc phần mềm không nhận diện được đường dẫn file tương ứng. 
- Nên thử trước trên một bản sao thư mục ảnh (hoặc môi trường staging) trước khi áp dụng đại trà lên hệ thống chính thức.  

## Bảo mật & Quyền riêng tư

- SEO Doctor Image Backup xử lý dữ liệu cục bộ trên máy của bạn, không gửi dữ liệu lên server bên ngoài. 
- Bạn hoàn toàn kiểm soát nguồn và đích của thư mục ảnh.

## Đóng góp

Bạn có thể:

- Tạo issue để báo lỗi, đề xuất tính năng mới.  
- Gửi pull request nếu muốn đóng góp mã nguồn hoặc cải thiện tài liệu.  

Hãy đọc kỹ hướng dẫn sử dụng trước khi chạy trên hệ thống thật, đặc biệt với những website có dung lượng lớn.

## Tác giả & giấy phép

- Tác giả: SEO Doctor (Tú Cao). 
- Website: https://seodoctor.vn  
- Mã nguồn: được public tại repository này để cộng đồng có thể tham khảo, kiểm tra và tùy chỉnh cho nhu cầu riêng. [seodoctor](https://seodoctor.vn/cong-cu-phan-mem-seo/phan-mem-lam-loc-toi-uu-luu-tru-hinh-anh-cho-website-seo-doctor-image-backup.html)
