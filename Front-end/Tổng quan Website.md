### Tổng quan chung

```
Ghi chú:

<Tiếng Việt>
- Xem rồi làm theo.
- Đọc ebook -> đưa ra sản phẩm.

<Tiếng Anh>
- Đọc ebook, stackoverflow, w3schools, development mozilla.
- Làm dự án lớn.
- Lấy mã nguồn từ dự án lớn về đọc hiểu, làm lại.
- Đọc bài viết công nghệ chuyên xâu.

```

**1. Website**

- WWW (World Wide Web): KHông gian thông tin toàn cầu.

- Nội dung web: Đa dạng(văn bản, hình ảnh, âm thanh, video, v.v), truy cập nội dung thông qua đường dẫn URL.

- Quy ước đặt tên:
  
   * Lưu ý phần mở rộng: .html, .css, .png, v.v
   * Không sử dụng tiếng việt.
   * Không chứa khoản trắng, có thể sử dụng dấu gạch nối (-,_)
   * Không sử dụng ký tự đặt biệt.
   * Sử dụng chữ thường.
   * Tên tập tin ngắn gọn.
   * Học cách đặt tên chuyên nghiệp, tránh sai khi tìm kiếm.

- HTML (HyperText Makeup Language) - ngôn ngữ siêu văn bản. 

**2. Tình duyệt Web**

Web browser: phần mềm được dùng truy cập thông tin trên web.

Các dạng server web: Apache, ISS, Nginx, Lighttpd.

**_Web hoạt động trên kiến trúc client-server, lấy dữ liệu web thông qua các bước sau:_**
 
 1 - Yêu cầu thông tin từ 1 server cụ thể. Nhập địa chỉ vào address bar trên browser.
 
 2 - Server sau khi nhận được yêu cầu sẽ tiến hành sử lý yêu cầu. Web server sẽ xử lý và tìm kiếm file được yêu cầu đó trong bộ nhớ của web server. 
       
       * Hosting files: web server lưu trữ tất cả các file html và các file liên quan css, javascript, fonts, video, v.v
       
       * Luôn hoạt động.
       
       * Luôn kết nối internet.
       
       * Luôn có chung IP
       
       * Được bảo trì bởi 1 bên thứ 3.
       
    Cung cấp giao thức HTTP (Hypertext Transfer Protocol) 
      - Chỉ có khách được phép gửi request tới server và chỉ có server mới có quyền trả lời các request của khách.

      - Khi yêu cầu một file thông qua HTTP, khách phải cung cấp url của file.

      - Wed server phải trả lời mọi yêu cầu HTTP, ít nhất với thông báo lỗi.
 
 ![image](https://user-images.githubusercontent.com/69178270/147213001-63a724eb-1e50-4d06-8786-0a5ddf2cba48.png)

 3 - Web server gửi lại kết quả
 
 4 - Hiển thị lên trình duyệt.
 
 **_Thành phần_**
 
 ![image](https://user-images.githubusercontent.com/69178270/147213475-674a0f75-14d7-4eba-8578-5b7057d97e93.png)

 - user interface: giao diện trình duyệt, trừ nội dung trang web.
 - browser engine: ghép nối, điều phối hoạt động giữa người dùng và trình duyệt.
 - rendering/layout engine: hiển thị nội dung web.
 - networking: giao tiếp mạng.
 - javascript interpreter: thực thi mã javascript
 - UI backend: vẽ các đối tượng cơ bản (cửa sổ, combo box)
 - data persistence: lưu dữ liệu cục bộ (cookie, cache)
      * cache: tăng tốc độ truy cập website: lưu lại những file tĩnh không thay đổi.
      * cookie: lưu thông tin người dùng, số lần truy cập, cho phép đi hai chiều (s-c, c-s)
   
 **_Giao diện_**
 
 Phần 1:
 
  - Thanh địa chỉ (Address bar) -> nhập URL, nội dung cần tìm
  - Nút new tab
  - Nút tranh trạng thái (status bar) -> chứa URL, thông báo trang web đang đc tải về.
  - Nút điều kiển: reload, home page, go back, go forward, v.v
  - Menu -> chứa các thiết lập cho trình duyệt.
  - Thanh cuồn (scroll bar)
 
 Phần 2: Nội dung web
 
 ![image](https://user-images.githubusercontent.com/69178270/147216605-d0603eaf-7381-492d-bf5b-c7d8351d7823.png)

Gửi yêu cầu -> Nhận yêu cầu -> Sử lý yêu cầu -> Gửi về mã nguồn -> Hiển thị kết quả.

 - Phân tích mã html tạo ra DOM tree (các thẻ trong html)
 - Phân tích mã CSS tạo CSSOM (CSS object model - mô hình đối tượng css)
 - DOM + CSSOM -> cây kết xuất Render tree.
 - Dựng khung giao diện và hiển thị nội dung.

**3. URL**

URL (Uniform Resource Locator) - bộ định vị tài nguyên thống nhất, là địa chỉ của web.

URL tham chiếu tới các trang web (http), truyền  tập tin (ftp), email(mailto), truy cập csdl (JDBC).

Thường hiển thị trên thanh address bar.

Định dạng:

![image](https://user-images.githubusercontent.com/69178270/147218312-1ad1b86b-bf2f-4042-ae89-d198ea32fdd1.png)

- scheme: giao thức
- domain: tên miền
- port: cổng giao tiếp
- path: đường dẫn
- Chuỗi truy vấn (query string), định dạng (fragment_id)

![image](https://user-images.githubusercontent.com/69178270/147218843-cc755e00-eac1-49fb-9122-67920c7c61fd.png)

Siêu liên kết (hyperlink) là liên kết giữa các URL.

![image](https://user-images.githubusercontent.com/69178270/147219032-ecf79d60-eff5-428a-98a3-b868bd1924bb.png)

Siêu văn bản (Hypertext) chứa tham chiếu liên kết tới các văn bản khác.

![image](https://user-images.githubusercontent.com/69178270/147219190-3824c40c-d07f-444b-b969-08d0144566f1.png)







