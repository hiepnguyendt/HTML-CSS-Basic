---
title : "Làm quen với HTML"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
1. Cấu trúc 1 file HTML
    {{%expand "Dưới đây là mô tả cho mỗi phần của cấu trúc file HTML:" %}}
    <!DOCTYPE html>: Khai báo kiểu tài liệu HTML, trong trường hợp này là HTML5.
    <html>: Thẻ gốc của trang web, bao gồm toàn bộ nội dung HTML.
    <head>: Phần tiêu đề của trang web, chứa các thông tin không hiển thị trực tiếp trên trang như tiêu đề, tập tin CSS, tập tin JavaScript, và các thẻ meta.
    <meta charset="UTF-8">: Định nghĩa bộ ký tự sử dụng cho trang web là UTF-8, giúp hỗ trợ hiển thị các ký tự đặc biệt và ngôn ngữ khác nhau.
    <title>: Đặt tiêu đề của trang web, hiển thị trên thanh tiêu đề của trình duyệt.
    <body>: Phần chứa nội dung chính của trang web.
    <header>: Đầu trang của trang web, thường chứa logo, tiêu đề và các phần tử đầu trang khác.
    <nav>: Phần chứa menu điều hướng trang web.
    <main>: Phần chứa nội dung chính của trang web.
    <footer>: Cuối trang web, thường chứa thông tin bản quyền, liên kết liên hệ và các phần tử chân trang khác.
    Các thẻ và nội dung khác trong <body>: Bạn có thể thêm các phần tử HTML khác như <div>, <p>, <img>, <a>, <form>, v.v. để tạo và định dạng nội dung của trang web.
    Lưu ý rằng cấu trúc trên chỉ là một cấu trúc cơ bản và bạn có thể tùy chỉnh nó tùy theo yêu cầu của dự án cụ thể.
    {{% /expand%}}
    ![html](/images/1.png)


2. Comments trong HTML

    -  Sử dụng phím tắt **ctrl /** để chú thích hoặc vô hiệu hoá những dòng code
        ```
        <!-- Đây là chú thích --> 
        
        ```

3. Các thẻ HTML thông dụng\
    Dưới đây là một số thẻ HTML thông dụng được sử dụng để xây dựng cấu trúc và định dạng nội dung trang web:
    - \<html>: Thẻ gốc của trang web.
    - \<head>: Phần tiêu đề của trang web.
    - \<title>: Đặt tiêu đề của trang web.
    - \<body>: Phần chứa nội dung chính của trang web.
    - \<h1> đến \<h6>: Định dạng tiêu đề từ lớn nhất đến nhỏ nhất.
    - \<p>: Định dạng đoạn văn bản.
    - \<a>: Tạo liên kết (hyperlink).
    - \<img>: Hiển thị hình ảnh.
    - \<ul> và \<li>: Tạo danh sách không có thứ tự.
    - \<ol> và \<li>: Tạo danh sách có thứ tự.
    - \<div>: Nhóm các phần tử HTML và tạo khu vực chứa.
    - \<span>: Định dạng một phần của văn bản.
    - \<table>, \<tr>, \<th>, \<td>: Tạo bảng và các phần tử trong bảng.
    - \<form>, \<input>, \<textarea>, \<button>: Tạo biểu mẫu và các phần tử đầu vào.
    - \<label>: Nhãn cho phần tử đầu vào trong biểu mẫu.
    - \<select>, \<option>: Tạo danh sách thả xuống.
    - \<iframe>: Nhúng nội dung từ một trang web khác.
    - \<header>, \<nav>, \<main>, \<footer>: Định dạng các phần tử chính của trang web.
    - \<section>, \<article>, \<aside>, \<figure>, \<figcaption>: Định dạng các phần tử phân đoạn và phần tử phụ.

4. Attribute trong HTML là gì?

    Trong HTML, attribute (thuộc tính) là một phần mở rộng của các thẻ HTML, được sử dụng để cung cấp thông tin bổ sung về các phần tử HTML. Mỗi thuộc tính được đặt trong cặp cú pháp **tên_thuộc_tính="giá_trị"**, trong đó:

    - **tên_thuộc_tính** là tên của thuộc tính, ví dụ: class, id, src, href, width, height, v.v.
    - **giá_trị** là giá trị được gán cho thuộc tính đó.

    Một phần tử HTML có thể có nhiều thuộc tính, và mỗi thuộc tính cung cấp thông tin cụ thể về cách nội dung hoặc hành vi của phần tử đó nên được xử lý.

    Dưới đây là một số ví dụ về các thuộc tính thường được sử dụng trong HTML:

    - **class**: Xác định một lớp (class) cho phần tử để tùy chỉnh kiểu dáng bằng CSS hoặc thao tác JavaScript.
    - **id**: Xác định một định danh duy nhất cho phần tử, thường được sử dụng để tham chiếu hoặc tạo liên kết đến phần tử đó.
    - **src**: Xác định nguồn (source) của một hình ảnh, video, âm thanh hoặc tệp tin khác được nhúng vào trang.
    - **href**: Xác định địa chỉ (URL) mà liên kết sẽ dẫn đến khi được nhấp vào.
    - **alt**: Xác định một văn bản mô tả thay thế cho hình ảnh, hiển thị khi hình ảnh không thể hiển thị.
    - **style**: Xác định các quy tắc kiểu dáng CSS trực tiếp cho phần tử.
    width và height: Xác định kích thước chiều rộng và chiều cao của một phần tử như hình ảnh hoặc bảng.
    - **disabled**: Vô hiệu hóa một phần tử hoặc phần tử đầu vào, ngăn người dùng tương tác với nó.

5. ID và Class trong HTML

    Trong HTML, **id** và **class** là hai thuộc tính quan trọng được sử dụng để xác định và định dạng các phần tử.

    - id:
        - Thuộc tính id được sử dụng để xác định một định danh duy nhất cho một phần tử HTML trên trang.
        - Giá trị của id phải là duy nhất trong toàn bộ tài liệu HTML. Không được sử dụng cùng một giá trị id cho nhiều phần tử.
        - Để chọn phần tử bằng id trong CSS hoặc thao tác JavaScript, sử dụng ký tự # trước tên id. Ví dụ: #myElement.

        - Ví dụ sử dụng id:

            ```
            <div id="header">Đây là tiêu đề</div>
            <p id="paragraph">Đây là đoạn văn bản</p>
            ```
    - class:

        -  Thuộc tính class được sử dụng để xác định một lớp (class) cho một hoặc nhiều phần tử HTML.

        - Giá trị của class có thể được sử dụng cho nhiều phần tử khác nhau trên trang.

        -  Để chọn phần tử bằng class trong CSS hoặc thao tác JavaScript, sử dụng ký tự . trước tên class. Ví dụ: .myClass.

        -  Một phần tử có thể có nhiều lớp (class) khác nhau, được phân tách bằng dấu cách.

        - Ví dụ sử dụng class:
            ```
            <div class="container">Đây là phần tử container</div>
            <p class="highlight">Đây là đoạn văn bản được làm nổi bật</p>
            ```