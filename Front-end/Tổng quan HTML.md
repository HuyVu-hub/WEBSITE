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

```
 - <!DOCTYPE html> không phải là một dạng thẻ. Khai báo phiên bản html cho browser.
 - Phần tử <html> sẽ chứa toàn bộ nội dung -> root element, phần tử chính
 - Phần tử <head> chứa thông tin mô tả (tiêu đề title, css, javascript)
 - Phần tử <body> chứa nội dung cần hiển thị.
```

**Cấu trúc và ngữ nghĩa cho nội dung**
 
 ```
 - Cấu trúc (structure): Bố cục trang Web (Tiêu đề, logo, menu, nội dung chính, phần bên trái, phần bên phải, phân chân, v.v) -> CSS
 - Ngữ nghĩa (meaning/semantic): Thể hiện bằng các thẻ (h1, h2, a, p, v.v)
 
 HTML tập trung biểu diễn nội dung, cấu trúc, ngữ nghĩa -> tạo bố cục outline hợp lý tạo thành DOM tree (Document Object Model) -> tạo tính dễ dàng khi trang trí bắng css hay tướng tác phần tử bằng javascript.
 
 - <h1> là tiêu đề mức cao nhất, được trình duyệt ưu tiên.
 ```
 
**block và inline**
 
 Tại chế độ mặc định phần tử html sẽ thuộc 1 trong hai dạng:
 
  - block: kiểu khối, luông hiển thị ở hàng mới, _chiếm toàn bộ chiểu rộng của phần tử cha_.
  - inline: kiểu nội tuyến, trong hàng, không yêu cầu xuống hàng, _chiếm độ rộng vừa đủ_ chứa nội dung của nó.

 ![image](https://user-images.githubusercontent.com/69178270/147307435-21be842c-865b-4bec-89a8-11cd99e7a8a1.png)

**Phẩn tử rỗng**

 Là những phần tử không chứa nội dung mà mang theo chỉ dẫn cho một nhiệm vụ nào đó.
 
 ![image](https://user-images.githubusercontent.com/69178270/147307963-b711d78b-1c1b-4564-a912-2b833d6bfcb5.png)

_Phần tử rổng chỉ có thẻ mở._
 
 ```
– Cách một: <br>, <hr>, <img>, <meta>

– Cách hai: <br />, <hr />, <img />, <meta />

– Cách ba: <br/>, <hr/>, <img/>, <meta/>
```
 
Thêm thuộc tính vào phần tử: 
 
 ```
 <img src="con-vit.png" alt="Logo Con Vit">
 ```
 
 ![image](https://user-images.githubusercontent.com/69178270/147309372-b9fb16b3-c2fa-452c-a3d1-51d58b413e1c.png)

**Hiển thị tiếng việt**

```
<head>
  <meta charset="utf-8">
</head>
```

Phẩn tử meta mô tả 1 số đặc tính của trang web

UTF-8: Unicode Transformation Format (Định dạng chuyển đổi Unicode 8-bit).

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
 
 **Hiển thị văn bản**
 
 **_Văn bản:_**
 
 ```
  <p> là phần tử cơ bản trong html, viết tắt paragraph.
  
  Ở chế độ mặc định <p> được hiểu theo kiểu block.
 ```
 
 Ngoài việc chứa văn bản, còn có thể chứa hình ảnh, các phần tử inline
 
 
 **_Đề mục:_**
 
 Heading thường là 1 từ, cụm từ, kí hiệu giúp tìm kiếm và định vị thông tin.
 
 Thường mang nhiều cấp khác nhau, thể hiện cấu trúc, bố cục hay bộ khung (outline)
 
 Tạo đề mục: h1 -> h6
 
 h1 sẽ là đề mục ở mức cao nhất.
 
 Trình duyệt sử dụng heading để tạo ra bố cục cho văn bản.
 
 Các công cụ tìm kiếm cũng sử dụng thuật toán tìm kiếm, các đề mục mức cao sẽ có trọng số lớn hơn.
 
**Đánh dấu kết thúc một chủ đề**

Sử dụng phần tử hr

```
<hr>
```

Nều chỉ muốn tạo 1 đường kẻ ngang trên trang web nên sử dụng border trong CSS thay vì sử dụng hr

![image](https://user-images.githubusercontent.com/69178270/147547399-d54e3d9b-f1c3-4291-81d8-3db50ce8b3c5.png)

**Danh sách**

3 loại danh sách

-  Danh sách không có thứ tự (unordered list)
-  Danh sách có thứ tự (ordered list)
-  Danh sách mô tả (description list)

Mặc định phần tử trong danh sách hiển thị theo kiểu block


_Danh sách không có thứ tự_

Một dãy các mục (item), tính trước sau của mỗi mục là không quan trọng.

Mỗi mục thường được dánh dấu bằng kí tự đầu dòng (bullet) -> phần lớn các danh sách sẽ thuộc loại này

Để tạo danh sách không có thứ tự sử dụng thẻ ul (unordered list, danh sách không có thứ tự)

Để tạo mỗi mục của danh sách sử dụng thẻ li (list item, mục của danh sách)

```
<ul>

            <li>phần tử 1</li>

            <li>phần tử 2</li>

</ul>

[HTML]

<ul>

            <li>Mãng cầu</li>

            <li>Trái dừa</li>

            <li>Ổ qua</li>

            <li>Khoai môn</li>

</ul>
```

Mỗi mục sẽ được đánh dấu chầm tròn.

_Danh sách có thứ tự_

Tính trước sau mang tính quan trọng.

Tạo danh sách thứ tự sử dụng thẻ ol (ordered list, danh sách có thứ tự)

Dánh sách tạo thành có đánh thứ tự.

```
Danh sách bắt đầu từ số 4

<ol start="4">

            <li>Lê Văn Bơ</li>

            <li>Trần Văn Mít</li>

            <li>Nguyễn Văn Tèo</li>

</ol>
```

Một số cấu trúc

![image](https://user-images.githubusercontent.com/69178270/147619305-33dffba2-37d7-467c-a3ca-d95cbf833c80.png)

_Danh sách mô tả_

Tạo danh sách mô tả sử dụng thẻ dl (description list)

dt (description term) tạo mục cho danh sách

dd (describe a definition/define a description) mô tả cho mục


```
Chú ý: Phần tử dl chỉ chứa các phần tử dt và dd.
```

_Danh sách lồng nhau_

```
<ol>

            <li>Mục 1</li>

            <li>Mục 2

                        <ul>

                                    <li>Nội dung 1</li>

                                    <li>Nội dung 2</li>

                        </ul>

            </li>

            <li>Mục 3</li>

</ol>
```

**Một số phần tử hiển thị nội dung khác**

Hiển thị một trích dẫn dài (long quotations)

```
- Đánh dấu nội dung được trích dẫn dài từ nguồn khác, lời nhận xét của khách hàng, phần sao chép từ nguồn khác: blockquote
- Nội dung bên trong blockquote nên được bọc lại: p,heading, ol, ul, dl.
```

```
<p>Đôi khi cũng phải nhìn lại bản thân, phải yêu bản thân mình, phải thương lấy nó, bởi nó là người bạn gần gũi nhất, trung thành nhất, yêu chứ không nuông chiều, như Sophia Loren đã nói:</p>

<blockquote>

            <p>Hãy yêu bản thân vô điều kiện, như là bạn yêu những người thân thiết với mình bất chấp khuyết điểm của họ.</p>

            <p>Love yourself unconditionally, just as you love those closest to you despite their faults.</p>

</blockquote>
```

**Hiển thị văn bản được định dạng sẵn**

Sử dụng thẻ pre trình duyệt sẽ hiển thị đúng những gì có ở đoạn mã nguồn

```
            <pre>

            NGÀY ĐẦU TIÊN ĐI HỌC

           

            Ngày đầu tiên đi học

            Mẹ dắt tay đến trường

            Em vừa đi vừa khóc

            Mẹ dỗ dành bên em

 

                        Tác giả: Viễn Phương

            </pre>
```

**Phần tử figure và figcapion**

Đây là phần tử hiển thị khối (block) chứa hình ảnh, đoạn mã, video, bảng và các dữ liệu khác.

```
[HTML]

<figure>

                        <img src="HTML-structure.png" alt="HTML document structure">

                        <figcaption>

                                    Cấu trúc một tài liệu HTML

                        </figcaption>

            </figure>

Ví dụ, hiển thị đoạn mã và chú thích

<figure>

                        <pre><code>

                                    body {

                                                background-color: #000;

                                                color: red;

                                    }

                        </code></pre>

                        <figcaption>

                                    Cú pháp viết CSS

                        </figcaption>

            </figure>
```



