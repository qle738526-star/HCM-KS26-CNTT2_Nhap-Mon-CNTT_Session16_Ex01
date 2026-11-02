**Bài 1 : Hệ thống Giám sát Sự cố Website Doanh nghiệp** 

**Phần 1: Phân tích lỗi** 

- Lập luận của Nam sai vì: Mã 500 Internal Server Error là lỗi  từ phía Server, hoàn toàn không phải do wifi hay hệ thống DNS.  
- Các mã trạng thái:   
- 200 OK: kết nối thành công, máy chủ xử lý và phản hồi tốt.  
+ 404 Not Found: lỗi do nhập sai đường dẫn hoặc trang không tồn tại trên máy chủ.  
+ 500 Internal Server Error: lỗi do Server vì yêu cầu đã đến được máy chủ nhưng máy chủ gặp sự cố lỗi mã nguồn, quá tải, nên không thể trả về trang web.

**Phần 2: Hoàn thiện**

- DNS Lookup: trình duyệt yêu cầu DNS tra cứu IP của lms.ptit.edu.vn 

- TCP / TLS Handshake: trình duyệt kết nối thành công tới IP của máy chủ.

- HTTP Request: trình duyệt sẽ gửi yêu cầu lấy nội dung từ máy chủ  
     
- Server Processing: máy chủ tiếp nhận được yêu cầu nhưng chương trình bên trong bị lỗi mã hoặc quá tải, nên không thể xử lí.  
    
- Server Response: Máy chủ sẽ tạo tin phản hồi có trạng thái là 500 Internal Server Error và gửi ngược lại cho Nam để báo lỗi hệ thống.  
