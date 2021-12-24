### DNS - Domain Name System

![image](https://user-images.githubusercontent.com/69178270/147325807-11606494-fcb3-4a38-9f0f-036944bb1f10.png)

Trình duyệt sử dụng domain trong URL để truy vấn ra IP tương ứng của tên miền và chuyển hướng yêu cầu tương ứng đền server đó.

**Các thành phần**

- DNS nemaspase (hệ thống tên miền): hệ thống DNS theo cấu trúc tree, mỗi nhánh cây chứa 1 miền domian, miễn miền chứa bản ghi (resorce record) mang thông tin ánh xạ giữa domain và ip.
- Name server: là máy tính đã được cài đặt dịch vụ DNS server.
- Resolver (DNS client): chương trình DNS client, gửi truy vấn đền DNS server. phải được chỉ dẫn để truy vấn tới ít nhất 1 server.

**Hệ thống tên DNS**

![image](https://user-images.githubusercontent.com/69178270/147326700-15920c6c-7bd4-4d29-9a88-a60a21c1b0cd.png)

INTERNIC (Internet Network Information Center) -> theo dõi domain và DNS server tương ứng.

DNS server chiệu trách nhiệm phân giải tên miền.

![image](https://user-images.githubusercontent.com/69178270/147326985-a9c2224d-2bc0-47ac-9e34-3441ef3be5f6.png)

**Tên miền quốc tế** 

Do ICANN cung cấp: 

- com: thương mại.
- net: mạng lưới network
- org: các tổ chức.
- info: thông tin.
- edu: giáo dục.

**Tên miến cấp cho quốc gia**

vd: vn, us, uk, v.v

.vn do VNNIC quản lý.

