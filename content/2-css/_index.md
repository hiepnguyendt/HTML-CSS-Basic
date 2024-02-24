---
title : "Làm quen với CSS"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2. </b> "
---


1. Sử dụng CSS trong HTML

    Để sử dụng CSS (Cascading Style Sheets) trong HTML, bạn có thể sử dụng phương pháp sau:
    - **Inline CSS**: Bạn có thể áp dụng kiểu dáng trực tiếp cho một phần tử bằng cách sử dụng thuộc tính "style" trong thẻ HTML. Ví dụ:
        ```
        <p style="color: blue; font-size: 18px;">Đây là đoạn văn bản có màu xanh và cỡ chữ 18px.</p>
        ```
    - **Internal CSS**: Bạn có thể định nghĩa các quy tắc CSS bên trong phần "head" của tài liệu HTML bằng cách sử dụng thẻ "style". Ví dụ:
        ```    
        <head>
            <style>
                p {
                    color: blue;
                    font-size: 18px;
                }
            </style>
        </head>
        <body>
            <p>Đây là đoạn văn bản có màu xanh và cỡ chữ 18px.</p>
        </body>
        ```
    - **External CSS**: Bạn có thể tạo một tệp CSS riêng biệt và liên kết nó với tài liệu HTML bằng cách sử dụng thẻ "link" trong phần "head" của tài liệu HTML. Ví dụ:

        - Tạo một tệp CSS với tên "style.css":
            ```
                /* style.css */
            p {
                color: blue;
                font-size: 18px;
            }
            ```

        - Liên kết tệp CSS với tài liệu HTML:
            ```
             <head>
                <link rel="stylesheet" type="text/css" href="style.css">
            </head>
            <body>
                <p>Đây là đoạn văn bản có màu xanh và cỡ chữ 18px.</p>
            </body> 
            ```

2. ID và Class trong CSS 

    Trong CSS, id và class là hai cách để xác định và áp dụng kiểu dáng cho các phần tử HTML.
    - id:

      - Selector id được sử dụng để chọn một phần tử duy nhất trên trang bằng cách sử dụng giá trị id được xác định trong HTML.

      - Để chọn - một phần tử bằng id, sử dụng ký tự # trước tên id.

      - Cú pháp: #myElement { ... }

      - Ví dụ:
          ```
          #header {
          font-size: 24px;
          color: blue;
          }
          ```
          Trong ví dụ trên, tất cả các phần tử có **id="header"** sẽ được áp dụng kiểu dáng với kích thước chữ là **24px** và màu chữ là xanh.
      
    - class:

      - Selector class được sử dụng để chọn một hoặc nhiều phần tử có cùng giá trị class.

      - Để chọn một phần tử bằng class, sử dụng ký tự . trước tên class.

      - Cú pháp: .myClass { ... }

      - Ví dụ:
          ```
          .highlight {
          background-color: yellow;
            }
          ```
          *Trong ví dụ trên, tất cả các phần tử có **class="highlight"** sẽ có màu nền là màu vàng.*
        
    - Kết hợp id và class:

        - Bạn cũng có thể kết hợp id và class để tạo ra các selector phức tạp hơn. 
        - Ví dụ:
            ```
            #header.highlight {
            font-weight: bold;
            }
            ```
          *Trong ví dụ trên, phần tử có cả **id="header"** và **class="highlight"** sẽ có kiểu dáng được đặt in đậm (font-weight: bold).*


    {{% notice note %}}
  Lưu ý: Trong CSS, id mang tính duy nhất và chỉ được sử dụng cho một phần tử duy nhất trong tài liệu HTML. Trong khi đó, class có thể được áp dụng cho nhiều phần tử khác nhau trên trang.

  {{% /notice %}}
 
3. CSS selectors cơ bản
    - Trong CSS, **CSS selectors** là các cách chúng ta sử dụng để chọn ra các phần tử (elements) mà chúng ta muốn "style" cho chúng. Có 2 **CSS selectors** thân thuộc với chúng ta nhất là **id và class.**
    - Trong cùng ***1 page HTML***, ***mỗi*** ***ID cần là duy nhất***. Đây là nguyên tắc của việc sử dụng ID, nếu vi phạm sẽ gặp cảnh báo trong tab Console của dev tool, và Javascript sẽ không lấy ra được cả 2 phần tử có dùng ID (Javascript các bạn sẽ học ở khóa sau).
    - **CSS selectors** là công cụ vô cùng mạnh mẽ. Toàn bộ các selectors trong CSS đều có thể linh động kết hợp với nhau khi sử dụng giúp lập trình viên có thể chọn được bất cứ phần tử HTML nào trong website.

      **Bảng tra cứu CSS selectors cơ bản**
      |Selector| Ví dụ| Mô tả |
      |-----|------|-----|
      |.class|.intro|Chọn tất cả các thẻ có class="intro"|
      |.class1.class2|.name1.name2|Chọn tất cả các thẻ có cả name1 và name2 được đặt trong thuộc tinh class của nó|
      |*|*|Chọn tất cả các thẻ|
      |element|h2|Chọn tất cả các thẻ h2|
      |element.class|div.box|Chọn tất cả thẻ div có class="box"|
      |element,element|div,h2|Chọn tất cả thẻ div và h2|
      |element element|div p|Chọn tất cả thẻ p trong thẻ div|
      |element > element| div > p|Chọn tất cả thẻ p là con trực tiếp của thẻ div|
      |element + element| div + p| Chọn thẻ p đứng liền kề sau thẻ div|
      |element ~ element|div ~ p| Chọn tất cả thẻ p đứng sau thẻ div|
    
    - Ví dụ:  Lựa chọn qua 1 class
        ```
        <h2 id="primary-heading">Tiêu đề 1</h2>
        <h2 id="secondary-heading">Tiêu đề 2</h2>
        ...
        <style>
            #primary-heading {
                color: red;
            }
        </style>
        ```

       ***Kết quả: Thẻ có id="primary-heading" thành màu đỏ.***

    - Ví dụ 2: Lựa chọn qua nhiều class
      
      Một thẻ có thể có nhiều class, mỗi class cách nhau bằng 1 khoảng trắng (dấu space).

      ```
      <p class="p1-normal">Đoạn văn 1</p>
      <p class="p1-normal">Đoạn văn 2</p>
      <p class="p1-normal p2-red">Đoạn văn 3</p>
      <p class="p1-normal p2-red">Đoạn văn 4</p>

      <style>
          .p1-normal {
              color: green;
          }

          <!-- Lưu ý, các tên class viết liền nhau, không có khoảng trắng  -->
          .p1-normal.p2-red {
              color: red;
          }
      </style>
      ```

      ***Kết quả, tất cả các thẻ đồng thời có cả class p1-normal và p2-red đều có màu đỏ.***

    - Tương tự như vậy, nếu thẻ có nhiều class hơn bạn chỉ cần nối thêm tên class vào khi CSS, ví dụ: **.class1.class2.class3**. Trong trường hợp này, thuộc tính CSS nằm trong selector được nối bởi nhiều class hơn (chỉ ra chi tiết hơn) sẽ được ưu tiên hơn.

    - Ví dụ 3: CSS cho các thẻ con
        ```
        <p class="children-1">Đoạn văn 1 (không parent)</p>
        <p class="children-2">Đoạn văn 2 (không parent)</p>

        <div class="parent">
            <p>Đoạn văn 1 (parent 1)</p>
            <p class="children-1">Đoạn văn 1 (con của .parent)</p>
            <p class="children-2">Đoạn văn 2 (con của .parent)</p>
        </div>

        <style>
            /* Chọn tất cả thẻ "p" là con của thẻ có class "parent" */
            .parent p {
                color: green;
            }

            /* Chọn tất cả thẻ có class "children-1" là con của thẻ có class "parent" */
            .parent .children-1 {
                color: red;
            }
        </style>
        ```

  {{% notice note %}}
  Chúng ta có thể tùy ý kết hợp các CSS selectors đã học để lựa chọn ra đúng thẻ chúng ta muốn CSS. Ở ví dụ trên, để lựa chọn thẻ con nằm trong 1 thẻ khác ta sẽ sử dụng selector có cú pháp selector-cha selector-con (lưu ý, giữa 2 selectors có một khoảng trắng - dấu cách).
  {{% /notice %}}

4. Độ ưu tiên trong CSS
    - Khi các đối tượn chịu tác động của nhiều rule khác nhau thì xảy ra hiện tượng chồng chéo.
    - Khi chồng chéo xảy ra, thử tự ưu tiên sẽ xác định định dạng của đối tượng
    10.1. Dạng chồng chéo giữa các rule khác nhau
    - Thứ tự ưu tiên của bốn dạng rule như bảng dưới đây:
    |Các dạng rule| Thứ tự ưu tiên| Phạm vi tác động|
    |----|---|---|
    |inline|1|4|
    |id|2|3|
    |class|3|2|
    |tag|4|1|

    - Theo bảng tổng hợp trên, có thể rút ra quy luật chung là: mức độ ưu tiên tỉ lệ nghịch với phạm vi ảnh hưởng. Phạm vi của rule càng lớn thì mức độ  ưu tiên càng thấp và ngược lại.
    - Ví dụ: Đoạn code "HTML-CSS" dưới đây bị ảnh hưởng bởi 4 rule thuộc 4 loại khác nhau ( inline, p, class.p1, id #p2). 4 quy tắc này chỉ định 4 màu chữ khác nhau:
      ```
      <p class="p1" id="p2" style="color:black;">HTML-CSS</p>
      ```
      *Kết quả: Theo thứ tự ưu tiên, màu của "HTML-CSS" sẽ tuân theo màu ưu tiên (đen) của rule inline*
    
5. Sử dụng biến trong CSS
    - Trong CSS, bạn không thể sử dụng biến trực tiếp như trong các ngôn ngữ lập trình như JavaScript. Tuy nhiên, từ phiên bản CSS3 trở đi, bạn có thể sử dụng các biến tùy chỉnh thông qua CSS variables (còn được gọi là CSS custom properties).

    - Để sử dụng biến trong CSS, bạn cần định nghĩa biến bằng cách sử dụng syntax --tên-biến: giá-trị;. 

        - Ví dụ, để định nghĩa một biến màu sắc:
            ```
            :root {
            --primary-color: #ff0000;
            } 
            ```
    
    - Sau đó, bạn có thể sử dụng biến này trong các khối CSS khác bằng cách sử dụng syntax **var(--tên-biến)**. 
        - Ví dụ, để sử dụng biến màu sắc đã định nghĩa:

              ```     
              h1 {
                color: var(--primary-color);
              }
              ```

    - Khi trình duyệt tải CSS, nó sẽ thay thế **var(--primary-color)** bằng giá trị thực tế của biến **--primary-color** (trong trường hợp này là #ff0000). Điều này cho phép bạn dễ dàng thay đổi giá trị của biến duy nhất và áp dụng thay đổi đó cho tất cả các vị trí mà biến được sử dụng.

    - Bạn cũng có thể kế thừa giá trị biến từ phần tử cha bằng cách sử dụng syntax inherit. 
      - Ví dụ:

        ```
        .child-element {
          color: inherit;
        }
        ```
6. Các đơn vị trong CSS
    - **Absolute units ( đơn vị tuyệt đối)** là các đơn vị vật lý đã được định nghĩa sẵn và đại diện cho các đơn vị đo lường vật lý. Các đơn vị này không bị phụ thuộc và không hề thay đổi bởi bất cứ tác động nào. Gồm: **px, pt, cm, mm, inch, pc**. Trong CSS sẽ thường dùng đơn vị **px (pixel)** 
    - **Relative units ( đơn vị tương đối)** Là các đơn vị đo lường được sử dụng trong CSS ở mức tương đối, nghĩa là nó có thể sẽ được thay đổi bởi các thành phần khác ví dụ như thay đổi phụ thuộc vào kích thước màn hình. Gồm: **%, rem, em, vw, vh, vmin, vmax, ex, ch**. Trong CSS thường sử dụng: **%, rem, em, vw, vh**

7. Một số hàm trong CSS
    - CSS cung cấp một số hàm tích hợp sẵn để thực hiện các phép tính và biểu thức trong quy tắc CSS. Dưới đây là một số hàm phổ biến trong CSS:

      - **rgb(), rgba()**: Hàm này được sử dụng để xác định một màu sắc bằng giá trị đỏ (red), xanh lá cây (green) và xanh dương (blue). Hàm rgba() còn cho phép bạn xác định một giá trị alpha (độ trong suốt) để điều chỉnh độ trong suốt của màu sắc.
      
        - Ví dụ:
            ```
            background-color: rgb(255, 0, 0); /* Màu đỏ */
            background-color: rgba(255, 0, 0, 0.5); /* Màu đỏ với độ trong suốt 50% */
            ```
      - **calc()**: Hàm này cho phép bạn thực hiện các phép tính số học trong giá trị CSS. Bạn có thể sử dụng các phép tính cộng (+), trừ (-), nhân (*) và chia (/) để tính toán giá trị.

        - Ví dụ:
          ```
          width: calc(100% - 20px); /* Chiều rộng là 100% trừ đi 20px */
          height: calc(50vh + 10px); /* Chiều cao là 50% chiều cao của viewport cộng thêm 10px */
          ```
      - **var()**: Hàm này được sử dụng để sử dụng giá trị của một biến CSS. Bạn có thể định nghĩa biến bằng cách sử dụng **--tên-biến: giá-trị;** và sau đó sử dụng **var(--tên-biến)** để sử dụng giá trị biến đó.

        - Ví dụ:
            ```
            :root {
              --primary-color: #ff0000;
              }
            h1 {
              color: var(--primary-color); /* Sử dụng giá trị của biến primary-color */
              }
            ```
      - url(): Hàm này được sử dụng để chỉ định một đường dẫn tới một tài nguyên như hình ảnh, video hoặc font.

        - Ví dụ: 
            ```
            background-image: url("path/to/image.jpg"); /* Sử dụng hình ảnh từ đường dẫn */
            ```

      - min() và max(): Hai hàm này được sử dụng để lấy giá trị nhỏ nhất hoặc lớn nhất từ một danh sách các giá trị.

        - Ví dụ:
          ```
          width: min(300px, 50%); /* Chiều rộng là giá trị nhỏ nhất giữa 300px và 50% */
          height: max(200px, 30vh); /* Chiều cao là giá trị lớn nhất giữa 200px và 30% chiều cao của viewport */
          ```

  {{% notice note %}}
  Đây chỉ là một số hàm phổ biến trong CSS. CSS cung cấp nhiều hàm khác nhau để thực hiện các phép tính và biểu thức phức tạp hơn
  {{% /notice %}}

8. Pseudo classes trong CSS

    - Pseudo classes trong CSS là các lớp ảo được áp dụng cho các phần tử dựa trên trạng thái hoặc quan hệ với phần tử khác trong cây DOM. Pseudo classes được kí hiệu bằng dấu hai chấm **(::)** hoặc dấu hai chấm đơn **(:)**.
    - Dưới đây là một số pseudo classes phổ biến trong CSS:
        - **:hover**: Áp dụng cho phần tử khi con trỏ chuột di chuyển qua phần tử đó.
            - Ví dụ:
        
              ```  
                a:hover {
                color: red;
                }```

        - **:active**: Áp dụng cho phần tử khi người dùng nhấn giữ chuột trái lên phần tử đó.
            - Ví dụ:
              ```
                button:active {
                background-color: blue;
                }
              ```
        - :focus: Áp dụng cho phần tử khi đang nhận trọng tâm (focus). Thường được sử dụng cho các phần tử có thể tương tác như input, textarea.
            - Ví dụ:
              ```
                input:focus {
                border-color: green;
                }
              ```
        - :first-child: Áp dụng cho phần tử đầu tiên trong danh sách các phần tử con của phần tử cha.
            - Ví dụ:
              ```
              ul li:first-child {
              font-weight: bold;
              }
              ```
        - :last-child: Áp dụng cho phần tử cuối cùng trong danh sách các phần tử con của phần tử cha.
            - Ví dụ:
              ```
              ul li:last-child {
              color: red;
              }
              ```
        - :nth-child(): Áp dụng cho phần tử dựa trên chỉ số của nó trong danh sách các phần tử con của phần tử cha.
            - Ví dụ:
              ```
              ul li:nth-child(odd) {
              background-color: lightgray;
              }
              ```


  {{% notice note %}}
  Trên đây chỉ là một số pseudo classes phổ biến trong CSS. CSS cung cấp nhiều pseudo classes khác nhau cho phép bạn chọn và tùy chỉnh phần tử dựa trên các trạng thái và quan hệ khác nhau trong cây DOM.
    {{% /notice %}}

9. Pseudo elements trong CSS
    - Pseudo elements trong CSS cho phép bạn tạo ra các phần tử ảo và chọn và tùy chỉnh chúng bằng CSS. Pseudo elements được kí hiệu bằng dấu hai chấm đôi **(::)**.
    - Dưới đây là một số pseudo elements phổ biến trong CSS:
      - **::before**: Tạo một phần tử ảo được chèn vào phần tử đầu tiên của phần tử đã chọn. Phần tử ảo này thường được sử dụng để thêm nội dung trước phần tử đã chọn.
        - Ví dụ:
            ```
            p::before {
            content: "Đây là nội dung trước đoạn văn.";
            font-weight: bold;
            }
            ```
      - **::after**: Tạo một phần tử ảo được chèn vào phần tử cuối cùng của phần tử đã chọn. Phần tử ảo này thường được sử dụng để thêm nội dung sau phần tử đã chọn.

        - Ví dụ:
            ```
            p::after {
            content: "Đây là nội dung sau đoạn văn.";
            color: red;
            }
            ```
      - **::first-line**: Chọn dòng đầu tiên trong một phần tử dài văn bản và cho phép bạn tùy chỉnh nó.

        - Ví dụ:
          ```
          p::first-line {
          color: blue;
          font-size: 20px;
          }
          ```
      - **::first-letter**: Chọn chữ cái đầu tiên trong một phần tử văn bản và cho phép bạn tùy chỉnh nó.

        - Ví dụ:
          ```
          p::first-letter {
          font-size: 24px;
          font-weight: bold;
          }
          ```
      - **::selection**: Tùy chỉnh phần được chọn trong văn bản khi người dùng chọn nó.

        - Ví dụ:
          ```
          ::selection {
          background-color: yellow;
          color: black;
          }
          ```
  {{% notice note %}}
  Trên đây chỉ là một số pseudo elements phổ biến trong CSS. Bằng cách sử dụng pseudo elements, bạn có thể tạo ra các phần tử ảo và điều chỉnh chúng để tạo hiệu ứng và trang trí phần tử gốc.
  {{% /notice %}}
