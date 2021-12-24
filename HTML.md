### HTML - Hypertext Markup Language

Ngôn ngữ đánh dấu siêu văn bản được sử dụng để tạo ra các trang Web bằng cách sử dụng các thẻ đáng dấu.

**Trang web tĩnh** (Static web page): trang web chứa nội dung cố định không thay đổi theo thời gian. thích hợp cho dạng nội dung ít hoặc không cần cập nhật.

```
Ghi chú: Văn bản thô (plain text/unformatted text) không bao gồm thông tin định dạng. Được tạo ra từ notepad, text editor.
```

**Những thứ sẽ bị trình duyệt bỏ qua khi hiển thị:**

 - Chuỗi khoảng trắng (spaces) -> chỉ nhận khoảng trắng đầu.
 - Kí hiệu xuống hàng (line break, carriage return) -> chuyển thành 1 khoảng trắng.
 - Các Tab -> 1 khoảng trắng
 - Các thẻ tag trình duyệt không hiểu bị hiển thị dưới dạng văn bản.
 - Phần chú thích (comment) sẽ bị bỏ qua.

**Cấu trúc**

 - Tài liệu HTML tập hợp từ nhiều phần tử HTML (HTML element là 1 container, chứa text hoặc phần tử)
 - Thẻ HTML (HTML tag) chứa khóa (keyword) chứa định dạng, hiển thị nội dung. Bao gồm thẻ mở (opening tag, start tag) và thẻ đóng (closing tag, end tag)
 
 ![image](https://user-images.githubusercontent.com/69178270/147305063-c00d02a1-ea6d-44d3-9de1-7fb7ebf87ca5.png)

 - Thẻ mở và đóng giống nhau chỉ khác thẻ đóng có dấu </> (<html>...</html>)
 - _Lưu ý:_ Viết tên thẻ dưới dạng chữ thường

![image](https://user-images.githubusercontent.com/69178270/147305382-d3e2a649-cbf8-4346-9af1-71fd23b9a1d5.png)

 - <!DOCTYPE html> không phải là một dạng thẻ. Khai báo phiên bản html cho browser.
 - Phần tử <html> sẽ chứa toàn bộ nội dung -> root element, phần tử chính
 - Phần tử <head> chứa thông tin mô tả (tiêu đề title, css, javascript)
 - Phần tử <body> chứa nội dung cần hiển thị.
 
**Cấu trúc và ngữ nghĩa cho nội dung**
 
 - Cấu trúc (structure): Bố cục trang Web (Tiêu đề, logo, menu, nội dung chính, phần bên trái, phần bên phải, phân chân, v.v) -> CSS
 - Ngữ nghĩa (meaning/semantic): Thể hiện bằng các thẻ (h1, h2, a, p, v.v)
 
 HTML tập trung biểu diễn nội dung, cấu trúc, ngữ nghĩa -> tạo bố cục outline hợp lý tạo thành DOM tree (Document Object Model) -> tạo tính dễ dàng khi trang trí bắng css hay tướng tác phần tử bằng javascript.
 
 - <h1> là tiêu đề mức cao nhất, được trình duyệt ưu tiên.
 
**block và inline**
 
 Tại chế độ mặc định phần tử html sẽ thuộc 1 trong hai dạng:
 
  - block: kiểu khối, luông hiển thị ở hàng mới, _chiếm toàn bộ chiểu rộng của phần tử cha_.
  - inline: kiểu nội tuyến, trong hàng, không yêu cầu xuống hàng, _chiếm độ rộng vừa đủ_ chứa nội dung của nó.

 ![image](https://user-images.githubusercontent.com/69178270/147307435-21be842c-865b-4bec-89a8-11cd99e7a8a1.png)

**Phẩn tử rỗng**

 Là những phần tử không chứa nội dung mà mang theo chỉ dẫn cho một nhiệm vụ nào đó.
 
 ![image](https://user-images.githubusercontent.com/69178270/147307963-b711d78b-1c1b-4564-a912-2b833d6bfcb5.png)

_Phần tử rổng chỉ có thẻ mở._
 
– Cách một: <br>, <hr>, <img>, <meta>

– Cách hai: <br />, <hr />, <img />, <meta />

– Cách ba: <br/>, <hr/>, <img/>, <meta/>

Thêm thuộc tính vào phần tử: 
 
 ```
 <img src="con-vit.png" alt="Logo Con Vit">
 ```
 
 ![image](https://user-images.githubusercontent.com/69178270/147309372-b9fb16b3-c2fa-452c-a3d1-51d58b413e1c.png)

 **Thêm CSS**
 
 ```
<head>

…

<style>

body {

background-color: #faf2e4;

font-family: sans-serif;

}

h1 {

text-align: center;

font-family: serif;

}

</style>

…

</head>
 ```
 
 
