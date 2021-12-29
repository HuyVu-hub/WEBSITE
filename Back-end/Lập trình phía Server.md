### Lập trình phía server

Web server sẽ nhận yêu cầu, xử lý và trả về cho trình duyệt mã HTML, CSS, JavaScript và các tài nguyên web khác (hình ảnh, âm thanh, video)

![image](https://user-images.githubusercontent.com/69178270/147636068-a1736843-46b3-4ba0-a146-64f0138a9f2e.png)

**Ngôn ngữ lập trình**

high-level programming language (ngôn ngữ lập trình cấp cao)
 
  - Có tính tương thích tốt
  - Chạy trên nhiều nền tảng, họ máy khác nhau

Có nhiều ngôn ngữ lập trình khác nhau

Điều khiển máy tính, chuyển đổi ngôn ngữ lập trình thành mã máy -> quá trình dịch ngôn ngữ (thông dịch, biên dịch)

**Trình thông dịch**

Interpreter là 1 chương trình máy tính thực thi trực tiếp các lệnh viết bằng ngôn ngữ lập trình mà không yêu cầu phải biên dịch trước thành 1 chương trình ngôn ngữ máy.

![image](https://user-images.githubusercontent.com/69178270/147637813-c001bbbb-7899-40e9-a7e0-4c13e35ac88f.png)

Không thấy tập tin kết quả của trình dịch

**Trình biên dịch**

Compiler là 1 chương trình dịch mã nguồn thánh mã nguồn mới tường đương ở dạng ngôn ngữ máy thường ở cấp thấp hơn.

CPU hoặc máy ảo sẽ thực thi mã đối tượng do trình biên dịch tạo ra.

Bộ biên dịch ngược chuyển từ mã cấp thấp sang mã cấp cao.

Bộ biên dịch phân tần chuyển ngôn ngữ cấp cao này sang cấp cao khác hay cấp trung gian để xử lý.

Thấy được tập tin kết quả của quá trình dịch.

```
Lưu ý:
Nhiều ngôn ngữ lập trình được thiết kế để chạy theo kiểu vừa thông dịch vừa biên dịch.
```

**Chương trình dịch cho hệ thống web server**

Web server chứa chương trình dịch nhằm chuyển mã nguồn thành ngôn ngữ trung gian, mã máy. Giúp máy server thực hiện sử lý logic và trả về kết quả cho web client.

**Framework và CMS**

**Framework** là bộ khung được thiết kế sẵn, gồm: mã, thư viện, mô hình, kiến trúc hệ thống, v.v

Hạn chế:

 - Học cách làm việc với framework.
 - Kích thước dự án lớn.
 - Tuân thủ các quy định, các chuẩn.
 - Không thích hợp cho các ứng dụng web nhỏ, đơn giản.

**CMS** content management system (hệ thống quản trị nội dung)

Giúp thay đổi, cập nhật nội dung của 1 website.

Hạn chế:

 - Giao diện bị đồng nhất.
 - Tính linh hoạt, khả năng tùy chỉnh thấp.
 - Kích thước website lớn.
 - Chạy chậm








