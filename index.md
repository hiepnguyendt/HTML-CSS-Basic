#### Tìm hiểu về HTML, CSS

1. HTML ( hypertext markup language). Nó giúp người dùng tạo và cấu trúc các thành phần trong trang web hoặc ứng dụng, phân chia các đoạn văn, heading, links, blockquotes,...

2. CSS là ngôn ngữ tạo phong cách cho trang web - Cascading style sheet language. Nó dùng để tạo phong cách và định kiểu cho những yếu tố được viết dưới dạng ngôn ngữ đánh dấu, như là HTML.

3. Cài đặt page ruler extension
https://drive.google.com/file/d/1yldGCtVkU3J4HuKPEvgj_H1RdRB_12J-/view


#### Cấu trúc 1 file HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <title>HTML-CSS</title> ( dùng để định nghĩa tiêu đề trang web của chúng ta)
    <meta charset="utf-8"> ( hỗ trợ hiển thị tiếng việt cho website )
</head>
<body>
    (hiển thị nội dung của trang)
</body>
</html> 

4. Comments trong HTML

<!--  -->  (ctrl /) dùng để chú thích hoặc vô hiệu hoá những dòng code

5. Các thẻ HTML thông dụng

- h1 - h6 - heading
- p - paragraph
- img - image 
- a - anchor thẻ liên kết
- ul (unordered list), li (list item): hiển thị danh sách
- table: để hiển thị bảng 
- input: tạo form để nhập dữ liệu
- button: tạo ra nút 
- div : để ra các khối 

6. Attribute trong HTML là gì?
- Là thuộc tính thêm vào các thẻ html

7. Sử dụng CSS trong HTML
- CÓ 3 cách sử dụng CSS trong  HTML: internal , external, inline
 - inline: yêu cầu mã CSS viết tại thuộc tính style. Nó phải được đặt bên trong phần tử HTML.
    <h1 style="color: red"> html-css</h1>
 - internal: Yêu cầu mã CSS nằm trong khối thẻ <style>. Nó được đặt bên trong phần đầu của tệp HTML.
    <style>
        h1{
            color: red; 
        }
    </style>
 - external: Yêu cầu mã CSS được tập hợp ở 1 tệp riêng (.css). Sau đó thông qua phần tử liên kết CSS với HTML là <link>. Sẽ đưa vào bên trong phần đầu của tệp HTML.
 
8. ID và Class
- Trong CSS, ID được sử dụng để định kiểu cho phần tử với id được chỉ định. ID thường được dùng cho các đối tượng nào là duy nhất trong website, mỗi tên id chỉ được đặt duy nhất cho một phần tử.
    - Ví du: <h1 id="first_id">html-css</h1> (html file)/
        #first_id{
            color: red;
        } ( css file)
- Trong CSS, Class được sử dụng để định kiểu cho phần tử với class được chỉ định. Class thường được dùng cho các đối tượng nhóm muốn có cùng một thuộc tính định dạng, mỗi tên class có thể được sử dụng với nhiều phần tử.
    - Ví du: <h1 class="first_class">html-css</h1> (html file)/
        .first_class{
            color: red;
        } ( css file)

9. CSS selectors cơ bản
- Trong CSS, CSS selectors là các cách chúng ta sử dụng để chọn ra các phần tử (elements) mà chúng ta muốn "style" cho chúng. Có 2 CSS selectors thân thuộc với chúng ta nhất là id và class.
- Trong cùng 1 page HTML, mỗi ID cần là duy nhất. Đây là nguyên tắc của việc sử dụng ID, nếu vi phạm sẽ gặp cảnh báo trong tab Console của dev tool, và Javascript sẽ không lấy ra được cả 2 phần tử có dùng ID (Javascript các bạn sẽ học ở khóa sau).
- CSS selectors là công cụ vô cùng mạnh mẽ. Toàn bộ các selectors trong CSS đều có thể linh động kết hợp với nhau khi sử dụng giúp lập trình viên có thể chọn được bất cứ phần tử HTML nào trong website.

#### Bảng tra cứu CSS selectors cơ bản
|Selector| Ví dụ| mô tả |
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
<h2 id="primary-heading">Tiêu đề 1</h2>
<h2 id="secondary-heading">Tiêu đề 2</h2>
...
<style>
    #primary-heading {
        color: red;
    }
</style>

Kết quả: Thẻ có id="primary-heading" thành màu đỏ.

- Ví dụ 2: Lựa chọn qua nhiều class
Một thẻ có thể có nhiều class, mỗi class cách nhau bằng 1 khoảng trắng (dấu space).

<p class="p1-normal">Đoạn văn 1</p>
<p class="p1-normal">Đoạn văn 2</p>
<p class="p1-normal p2-red">Đoạn văn 3</p>
<p class="p1-normal p2-red">Đoạn văn 4</p>

<style>
    .p1-normal {
        color: 
green;
    }

    /* Lưu ý, các tên class viết liền nhau, không có khoảng trắng */
    .p1-normal.p2-red {
        color: 
red;
    }
</style>
Kết quả, tất cả các thẻ đồng thời có cả class p1-normal và p2-red đều có màu đỏ.
Tương tự như vậy, nếu thẻ có nhiều class hơn bạn chỉ cần nối thêm tên class vào khi CSS, ví dụ: .class1.class2.class3. Trong trường hợp này, thuộc tính CSS nằm trong selector được nối bởi nhiều class hơn (chỉ ra chi tiết hơn) sẽ được ưu tiên hơn.

- Ví dụ 3: CSS cho các thẻ con
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
        color: 
green;
    }

    /* Chọn tất cả thẻ có class "children-1" là con của thẻ có class "parent" */
    .parent .children-1 {
        color: 
red;
    }
</style>


Chúng ta có thể tùy ý kết hợp các CSS selectors đã học để lựa chọn ra đúng thẻ chúng ta muốn CSS. Ở ví dụ trên, để lựa chọn thẻ con nằm trong 1 thẻ khác ta sẽ sử dụng selector có cú pháp selector-cha selector-con (lưu ý, giữa 2 selectors có một khoảng trắng - dấu cách).

10. Độ ưu tiên trong CSS

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

<p class="p1" id="p2" style="color:black;">HTML-CSS</p>
 
 Kết quả: Theo thứ tự ưu tiên, màu của "HTML-CSS" sẽ tuân theo màu ưu tiên (đen) của rule inline

 11. Sử dụng biến trong CSS
- Trong CSS, bạn không thể sử dụng biến trực tiếp như trong các ngôn ngữ lập trình như JavaScript. Tuy nhiên, từ phiên bản CSS3 trở đi, bạn có thể sử dụng các biến tùy chỉnh thông qua CSS variables (còn được gọi là CSS custom properties).

- Để sử dụng biến trong CSS, bạn cần định nghĩa biến bằng cách sử dụng syntax --tên-biến: giá-trị;. Ví dụ, để định nghĩa một biến màu sắc:

:root {
  --primary-color: #ff0000;
}

- Sau đó, bạn có thể sử dụng biến này trong các khối CSS khác bằng cách sử dụng syntax var(--tên-biến). Ví dụ, để sử dụng biến màu sắc đã định nghĩa:

h1 {
  color: var(--primary-color);
}

- Khi trình duyệt tải CSS, nó sẽ thay thế var(--primary-color) bằng giá trị thực tế của biến --primary-color (trong trường hợp này là #ff0000). Điều này cho phép bạn dễ dàng thay đổi giá trị của biến duy nhất và áp dụng thay đổi đó cho tất cả các vị trí mà biến được sử dụng.

- Bạn cũng có thể kế thừa giá trị biến từ phần tử cha bằng cách sử dụng syntax inherit. Ví dụ:

.child-element {
  color: inherit;
}

12. Các đơn vị trong CSS
12.1. Absolute units ( đơn vị tuyệt đối)
- Là các đơn vị vật lý đã được định nghĩa sẵn và đại diện cho các đơn vị đo lường vật lý. Các đơn vị này không bị phụ thuộc và không hề thay đổi bởi bất cứ tác động nào. Gồm: px, pt, cm, mm, inch, pc
- Trong CSS sẽ thường dùng px

12.2. relative units ( đơn vị tương đối)
- Là các đơn vị đo lường được sử dụng trong CSS ở mức tương đối, nghĩa là nó có thể sẽ được thay đổi bởi các thành phần khác ví dụ như thay đổi phụ thuộc vào kích thước màn hình.
- Gồm: %, rem, em, vw, vh, vmin, vmax, ex, ch
- Trong CSS thường sử dụng: %, rem, em, vw, vh

13. Một số hàm trong CSS
- CSS cung cấp một số hàm tích hợp sẵn để thực hiện các phép tính và biểu thức trong quy tắc CSS. Dưới đây là một số hàm phổ biến trong CSS:

- rgb(), rgba(): Hàm này được sử dụng để xác định một màu sắc bằng giá trị đỏ (red), xanh lá cây (green) và xanh dương (blue). Hàm rgba() còn cho phép bạn xác định một giá trị alpha (độ trong suốt) để điều chỉnh độ trong suốt của màu sắc.
Ví dụ:
    background-color: rgb(255, 0, 0); /* Màu đỏ */
    background-color: rgba(255, 0, 0, 0.5); /* Màu đỏ với độ trong suốt 50% */
- calc(): Hàm này cho phép bạn thực hiện các phép tính số học trong giá trị CSS. Bạn có thể sử dụng các phép tính cộng (+), trừ (-), nhân (*) và chia (/) để tính toán giá trị.
Ví dụ:
    width: calc(100% - 20px); /* Chiều rộng là 100% trừ đi 20px */
    height: calc(50vh + 10px); /* Chiều cao là 50% chiều cao của viewport cộng thêm 10px */
- var(): Hàm này được sử dụng để sử dụng giá trị của một biến CSS. Bạn có thể định nghĩa biến bằng cách sử dụng --tên-biến: giá-trị; và sau đó sử dụng var(--tên-biến) để sử dụng giá trị biến đó.

Ví dụ:
    :root {
    --primary-color: #ff0000;
    }
    h1 {
    color: var(--primary-color); /* Sử dụng giá trị của biến primary-color */
    }

- url(): Hàm này được sử dụng để chỉ định một đường dẫn tới một tài nguyên như hình ảnh, video hoặc font.

Ví dụ: 
    background-image: url("path/to/image.jpg"); /* Sử dụng hình ảnh từ đường dẫn */

- min() và max(): Hai hàm này được sử dụng để lấy giá trị nhỏ nhất hoặc lớn nhất từ một danh sách các giá trị.

Ví dụ:
    width: min(300px, 50%); /* Chiều rộng là giá trị nhỏ nhất giữa 300px và 50% */
    height: max(200px, 30vh); /* Chiều cao là giá trị lớn nhất giữa 200px và 30% chiều cao của viewport */
Đây chỉ là một số hàm phổ biến trong CSS. CSS cung cấp nhiều hàm khác nhau để thực hiện các phép tính và biểu thức phức tạp hơn

14. Pseudo classes trong CSS
- Pseudo classes trong CSS là các lớp ảo được áp dụng cho các phần tử dựa trên trạng thái hoặc quan hệ với phần tử khác trong cây DOM. Pseudo classes được kí hiệu bằng dấu hai chấm (::) hoặc dấu hai chấm đơn (:).
- Dưới đây là một số pseudo classes phổ biến trong CSS:
- :hover: Áp dụng cho phần tử khi con trỏ chuột di chuyển qua phần tử đó.
Ví dụ:
    
    a:hover {
    color: red;
    }
- :active: Áp dụng cho phần tử khi người dùng nhấn giữ chuột trái lên phần tử đó.
Ví dụ:

    
    button:active {
    background-color: blue;
    }
- :focus: Áp dụng cho phần tử khi đang nhận trọng tâm (focus). Thường được sử dụng cho các phần tử có thể tương tác như input, textarea.
Ví dụ:

  
    input:focus {
    border-color: green;
    }
- :first-child: Áp dụng cho phần tử đầu tiên trong danh sách các phần tử con của phần tử cha.
Ví dụ:

    
    ul li:first-child {
    font-weight: bold;
    }
- :last-child: Áp dụng cho phần tử cuối cùng trong danh sách các phần tử con của phần tử cha.
Ví dụ:

    
    ul li:last-child {
    color: red;
    }
- :nth-child(): Áp dụng cho phần tử dựa trên chỉ số của nó trong danh sách các phần tử con của phần tử cha.
Ví dụ:

  
    ul li:nth-child(odd) {
    background-color: lightgray;
    }
Trên đây chỉ là một số pseudo classes phổ biến trong CSS. CSS cung cấp nhiều pseudo classes khác nhau cho phép bạn chọn và tùy chỉnh phần tử dựa trên các trạng thái và quan hệ khác nhau trong cây DOM.

15. Pseudo elements trong CSS
- Pseudo elements trong CSS cho phép bạn tạo ra các phần tử ảo và chọn và tùy chỉnh chúng bằng CSS. Pseudo elements được kí hiệu bằng dấu hai chấm đôi (::).
- Dưới đây là một số pseudo elements phổ biến trong CSS:
- ::before: Tạo một phần tử ảo được chèn vào phần tử đầu tiên của phần tử đã chọn. Phần tử ảo này thường được sử dụng để thêm nội dung trước phần tử đã chọn.

Ví dụ:
    p::before {
    content: "Đây là nội dung trước đoạn văn.";
    font-weight: bold;
    }
- ::after: Tạo một phần tử ảo được chèn vào phần tử cuối cùng của phần tử đã chọn. Phần tử ảo này thường được sử dụng để thêm nội dung sau phần tử đã chọn.

Ví dụ:
    p::after {
    content: "Đây là nội dung sau đoạn văn.";
    color: red;
    }
- ::first-line: Chọn dòng đầu tiên trong một phần tử dài văn bản và cho phép bạn tùy chỉnh nó.

Ví dụ:
    p::first-line {
    color: blue;
    font-size: 20px;
    }
- ::first-letter: Chọn chữ cái đầu tiên trong một phần tử văn bản và cho phép bạn tùy chỉnh nó.

Ví dụ:
    p::first-letter {
    font-size: 24px;
    font-weight: bold;
    }
- ::selection: Tùy chỉnh phần được chọn trong văn bản khi người dùng chọn nó.

Ví dụ:
    ::selection {
    background-color: yellow;
    color: black;
    }
Trên đây chỉ là một số pseudo elements phổ biến trong CSS. Bằng cách sử dụng pseudo elements, bạn có thể tạo ra các phần tử ảo và điều chỉnh chúng để tạo hiệu ứng và trang trí phần tử gốc.

16. Thuộc tính padding (đệm)
- Trong CSS, thuộc tính "padding" được sử dụng để xác định khoảng cách giữa nội dung của một phần tử và ranh giới (border) của nó. Thuộc tính này thường được sử dụng để tạo ra khoảng trắng xung quanh nội dung của một phần tử.
Cú pháp: 
padding: giá-trị;
- Giá trị của thuộc tính "padding" có thể là một giá trị duy nhất hoặc là một danh sách gồm bốn giá trị, tương ứng với các cạnh top, right, bottom và left (theo thứ tự kim đồng hồ). Các giá trị có thể được xác định bằng đơn vị đo (px, em, rem, %) hoặc bằng từ khóa như "auto".

17. Thuộc tính border (đường viền)
- Trong CSS, thuộc tính "border" được sử dụng để xác định đường viền xung quanh một phần tử. Đường viền có thể là một đường thẳng, một đường nét đứt, hoặc một hình dạng khác.
Cú pháp: 
border: [kích thước] [loại] [màu];
- [kích thước]: Xác định kích thước của đường viền. Có thể là một giá trị duy nhất hoặc là một danh sách gồm bốn giá trị (top, right, bottom, left) tương ứng với các cạnh của phần tử. Các giá trị có thể là số nguyên, số thập phân hoặc sử dụng các đơn vị đo như px, em, rem.
- [loại]: Xác định loại đường viền. Có thể là "solid" (đường thẳng), "dotted" (đường nét đứt), "dashed" (đường nét gạch), "double" (đường viền kép), "groove" (đường viền rãnh), "ridge" (đường viền núi), "inset" (đường viền lồi vào), "outset" (đường viền lồi ra), hoặc "none" (không có đường viền).
- [màu]: Xác định màu sắc của đường viền. Có thể là tên màu (ví dụ: "red", "blue"), mã màu hex (ví dụ: "#ff0000"), hoặc giá trị màu rgba.
Ví dụ:
- Sử dụng giá trị duy nhất:
    .box {
    border: 2px solid red;
    }
    Đường viền có kích thước 2px, loại đường thẳng (solid) và màu đỏ.

- Sử dụng danh sách giá trị:
    .box {
    border: 1px solid red;
    border-width: 1px 2px 3px 4px;
    }
    Đường viền của phần tử có kích thước 1px ở cạnh trên, 2px ở cạnh phải, 3px ở cạnh dưới và 4px ở cạnh trái.

    Ngoài ra, cũng có thể sử dụng các thuộc tính con của "border" như "border-top", "border-right", "border-bottom" và "border-left" để chỉ định giá trị cho từng cạnh một.
Ví dụ:
    .box {
    border-top: 1px solid red;
    border-right: 2px dashed blue;
    border-bottom: 3px dotted green;
    border-left: 4px double orange;
    }
    Phần tử có đường viền ở từng cạnh với các kích thước, loại và màu sắc khác nhau.

    Trên đây là cách sử dụng thuộc tính "border" trong CSS để xác định đường viền xung quanh một phần tử.

18. Thuộc tính margin (khoảng cách lề)
- Trong CSS, thuộc tính "margin" được sử dụng để xác định khoảng cách giữa các phần tử và ranh giới của chúng. Thuộc tính này thường được sử dụng để tạo ra khoảng trắng xung quanh các phần tử và điều chỉnh khoảng cách giữa chúng.
Cú pháp:
margin: giá-trị;
- Giá trị của thuộc tính "margin" có thể là một giá trị duy nhất hoặc là một danh sách gồm bốn giá trị, tương ứng với các cạnh top, right, bottom và left (theo thứ tự kim đồng hồ). Các giá trị có thể được xác định bằng đơn vị đo (px, em, rem, %) hoặc bằng từ khóa như "auto".
Ví dụ:
-  Sử dụng giá trị duy nhất:
    .box {
    margin: 20px;
    }
- Sử dụng danh sách giá trị:
    .box {
    margin: 10px 20px 15px 5px;
    }

    Giá trị "10px" áp dụng cho cạnh trên (top), "20px" áp dụng cho cạnh phải (right), "15px" áp dụng cho cạnh dưới (bottom) và "5px" áp dụng cho cạnh trái (left).
- Ngoài ra, cũng có thể sử dụng các thuộc tính con của "margin" như "margin-top", "margin-right", "margin-bottom" và "margin-left" để chỉ định giá trị cho từng cạnh một.

Ví dụ:
    .box {
    margin-top: 10px;
    margin-right: 20px;
    margin-bottom: 15px;
    margin-left: 5px;
    }
- Giá trị của "margin" cũng có thể là âm để tạo ra sự chồng chéo giữa các phần tử.
Ví dụ:
    .box {
    margin: -10px;
    }
Trên đây là cách sử dụng thuộc tính "margin" trong CSS để xác định khoảng cách giữa các phần tử và ranh giới của chúng.

19. Thuộc tính box-sizing
- Thuộc tính "box-sizing" trong CSS được sử dụng để xác định cách tính toán kích thước của một phần tử, bao gồm cả kích thước của nội dung, padding và border.
Cú pháp:
    box-sizing: giá-trị;
- Có hai giá trị phổ biến cho thuộc tính "box-sizing":
    - Giá trị "content-box" (giá trị mặc định): Kích thước của phần tử chỉ tính toán dựa trên kích thước của nội dung bên trong phần tử, không tính thêm padding và border. Đây là cách tính toán kích thước truyền thống của các phần tử trong CSS.
    - Giá trị "border-box": Kích thước của phần tử tính toán bao gồm cả kích thước của nội dung, padding và border. Điều này có nghĩa là kích thước của phần tử sẽ bao gồm cả padding và border, mà không làm thay đổi kích thước tổng cộng của phần tử.
Ví dụ:
    .box {
    box-sizing: border-box;
    width: 200px;
    padding: 20px;
    border: 1px solid black;
    }
Trong ví dụ trên, thuộc tính "box-sizing" được đặt thành "border-box", điều này có nghĩa là kích thước của phần tử sẽ tính toán bao gồm cả padding và border. Vì vậy, dù đã đặt width là 200px, kích thước tổng cộng của phần tử vẫn là 200px (bao gồm cả nội dung, padding và border), và không bị thay đổi do padding và border.

Trên đây là ý nghĩa và cách sử dụng thuộc tính "box-sizing" trong CSS.

V. Thuộc tính tạo nền
1. Thuộc tính background-image
- Thuộc tính background-image trong CSS được sử dụng để đặt hình ảnh làm nền cho một phần tử. Bạn có thể chỉ định đường dẫn đến hình ảnh bằng cách sử dụng URL hoặc giá trị gradient để tạo hiệu ứng nền.
Cú pháp:
    background-image: giá-trị;
Ví dụ sử dụng cách đặt hình ảnh làm nền:
    .box {
    background-image: url("path/to/image.jpg");
    }   
     Trong ví dụ trên, path/to/image.jpg là đường dẫn đến hình ảnh mà bạn muốn sử dụng làm nền cho phần tử có lớp CSS .box.
- Ngoài ra, bạn cũng có thể sử dụng giá trị gradient để tạo hiệu ứng nền. Ví dụ:

    .box {
    background-image: linear-gradient(to bottom, #ff0000, #00ff00);
    }
    Trong ví dụ này, chúng ta sử dụng giá trị linear-gradient để tạo một hiệu ứng gradient từ màu đỏ (#ff0000) đến màu xanh lá cây (#00ff00) từ trên xuống dưới.

Lưu ý rằng thuộc tính background-image có thể được kết hợp với các thuộc tính khác như background-repeat, background-position, background-size để tùy chỉnh cách hiển thị hình ảnh nền.

2. Thuộc tính background-size với cover, contain
- background-size: cover;: Khi sử dụng giá trị cover, hình ảnh nền sẽ được co giãn hoặc thu nhỏ sao cho nó phủ đầy toàn bộ phần tử mà không bị méo. Điều này có nghĩa là hình ảnh có thể bị cắt bớt ở một số phần nếu tỷ lệ khung hình không khớp với tỷ lệ khung hình của phần tử.
Ví dụ:
    .box {
    background-image: url("path/to/image.jpg");
    background-size: cover;
    }
- background-size: contain;: Khi sử dụng giá trị contain, hình ảnh nền sẽ được co giãn hoặc thu nhỏ sao cho nó hiển thị toàn bộ trong phần tử mà không bị cắt bớt. Điều này có thể dẫn đến việc xuất hiện dải trống (background-color) nếu tỷ lệ khung hình không khớp với tỷ lệ khung hình của hình ảnh.
Ví dụ:
    .box {
    background-image: url("path/to/image.jpg");
    background-size: contain;
    }
Trên đây là cách sử dụng thuộc tính background-size với giá trị cover và contain để điều chỉnh kích thước của hình ảnh nền trong CSS.

3. Thuộc tính background-origin
- Thuộc tính background-origin trong CSS được sử dụng để xác định điểm xuất phát (origin) của hình ảnh nền và các phần tử khác liên quan đến việc vẽ nền.
Cú pháp:
    background-origin: giá-trị;

Có ba giá trị phổ biến cho thuộc tính background-origin:

- padding-box (giá trị mặc định): Hình ảnh nền và các phần tử liên quan (như padding và border) bắt đầu từ biên trong padding box của phần tử. Điều này có nghĩa là hình ảnh nền và các phần tử khác sẽ không xuyên qua phần padding và border.

- border-box: Hình ảnh nền và các phần tử liên quan bắt đầu từ biên trong border box của phần tử. Điều này có nghĩa là hình ảnh nền và các phần tử có thể xuyên qua phần border, nhưng không xuyên qua phần margin.

- content-box: Hình ảnh nền và các phần tử liên quan bắt đầu từ biên trong content box của phần tử. Điều này có nghĩa là hình ảnh nền và các phần tử có thể xuyên qua phần padding và border, và chỉ giới hạn bởi khu vực chứa nội dung.

Ví dụ:
    .box {
    background-image: url("path/to/image.jpg");
    background-origin: content-box;
    }
    
    Trong ví dụ trên, thuộc tính background-origin được đặt thành content-box, điều này có nghĩa là hình ảnh nền và các phần tử liên quan sẽ bắt đầu từ biên bên trong content box của phần tử.

Thuộc tính background-origin thường được sử dụng kết hợp với các thuộc tính khác như background-image, background-position, background-repeat, và background-size để tùy chỉnh việc vẽ nền của một phần tử trong CSS.

4. Thuộc tính background-position
- Thuộc tính background-position trong CSS được sử dụng để xác định vị trí xuất hiện của hình ảnh nền bên trong phần tử.
Cú pháp:
    background-position: giá-trị-x giá-trị-y;
- Hai giá trị giá-trị-x và giá-trị-y trong background-position xác định vị trí ngang và dọc của hình ảnh nền tương đối với phần tử. Có thể sử dụng các giá trị đơn vị như pixel (px), phần trăm (%), hoặc từ khoá như left, right, top, bottom, center để chỉ định vị trí.

Ví dụ:
    .box {
    background-image: url("path/to/image.jpg");
    background-position: center top;
    }
    Trong ví dụ trên, hình ảnh nền sẽ được căn giữa theo chiều ngang (center) và đặt ở phía trên cùng theo chiều dọc (top) bên trong phần tử có lớp CSS .box.

- Bạn cũng có thể sử dụng các giá trị số để xác định vị trí chính xác. Ví dụ:
    .box {
    background-image: url("path/to/image.jpg");
    background-position: 20px 50%;
    }
    Trong ví dụ này, hình ảnh nền sẽ được dịch chuyển 20 pixel từ cạnh trái và căn giữa theo chiều dọc (50%) bên trong phần tử.
- Ngoài ra, background-position cũng hỗ trợ việc kết hợp các từ khoá và giá trị số để xác định vị trí. Ví dụ:
    .box {
    background-image: url("path/to/image.jpg");
    background-position: center 20%;
    }
    Trong ví dụ này, hình ảnh nền sẽ được căn giữa theo chiều ngang (center) và dịch chuyển 20% từ cạnh trên cùng theo chiều dọc bên trong phần tử
Lưu ý rằng thuộc tính background-position cũng có thể được sử dụng cùng với các giá trị khác như background-repeat, background-size, và background-origin để tùy chỉnh cách hiển thị hình ảnh nền.

5. Cú pháp "shorthand" cho background
- Thuộc tính background trong CSS cho phép bạn gộp nhiều thuộc tính liên quan đến hình ảnh nền thành một cú pháp ngắn gọn. 
Cú pháp:
    background: giá-trị;
- Giá trị của thuộc tính background có thể bao gồm nhiều thuộc tính con, được phân cách bằng dấu cách. Dưới đây là một số giá trị phổ biến cho thuộc tính background:
    - background-color: Xác định màu nền của phần tử.
    - background-image: Xác định hình ảnh nền.
    - background-repeat: Xác định cách lặp lại hình ảnh nền.
    - background-position: Xác định vị trí xuất hiện của hình ảnh nền.
    - background-size: Xác định kích thước của hình ảnh nền.
    - background-origin: Xác định điểm xuất phát của hình ảnh nền.

Ví dụ:
    .box {
    background: #F0F0F0 url("path/to/image.jpg") no-repeat center top / cover;
    }
    Trong ví dụ trên, thuộc tính background được sử dụng để gộp background-color, background-image, background-repeat, background-position, background-size thành một cú pháp ngắn gọn. Màu nền được đặt là #F0F0F0, hình ảnh nền là url("path/to/image.jpg"), không lặp lại (no-repeat), căn giữa theo chiều ngang và đặt ở phía trên cùng theo chiều dọc (center top), và có kích thước cover.

Lưu ý rằng khi sử dụng cú pháp ngắn gọn background, các thuộc tính không được xác định sẽ có giá trị mặc định. Đồng thời, thứ tự của các thuộc tính con trong cú pháp background không quan trọng, nhưng giữa chúng cần có dấu cách phân cách.

VI. Thuộc tính vị trí
1. CSS position relative
- Trong CSS, thuộc tính position: relative; được sử dụng để xác định vị trí của một phần tử dựa trên vị trí ban đầu của nó trong luồng bình thường của tài liệu. Khi một phần tử có thuộc tính position: relative;, nó sẽ được di chuyển dựa trên giá trị của các thuộc tính top, right, bottom, và left.
Cú pháp:
    selector {
    position: relative;
    top: value;
    right: value;
    bottom: value;
    left: value;
    }
- position: relative;: Xác định rằng phần tử sẽ được xác định vị trí dựa trên vị trí ban đầu của nó.
- top, right, bottom, left: Xác định khoảng cách mà phần tử sẽ di chuyển từ vị trí ban đầu của nó. Giá trị có thể là số nguyên hoặc phần trăm.
Ví dụ:
    .box {
    position: relative;
    top: 20px;
    left: 10px;
    }

    Trong ví dụ trên, phần tử có lớp CSS .box sẽ được di chuyển 20px từ vị trí ban đầu theo hướng từ trên xuống và 10px từ vị trí ban đầu theo hướng từ trái sang phải.

Lưu ý rằng khi sử dụng position: relative;, phần tử vẫn giữ lại vị trí gốc của nó trong luồng bình thường của tài liệu. Việc di chuyển phần tử chỉ ảnh hưởng đến vị trí hiển thị của nó trên giao diện người dùng. Các phần tử khác trong tài liệu không sẽ không bị di chuyển hoặc ảnh hưởng bởi phần tử có position: relative;.

2. CSS position absolute
- Trong CSS, thuộc tính position: absolute; được sử dụng để xác định vị trí của một phần tử dựa trên vị trí của phần tử cha gần nhất có thuộc tính position được đặt là relative, absolute, hoặc fixed. Phần tử với position: absolute; sẽ được di chuyển đến vị trí cụ thể trong tài liệu, không ảnh hưởng tới vị trí của các phần tử khác.

Cú pháp:
    selector {
    position: absolute;
    top: value;
    right: value;
    bottom: value;
    left: value;
    }
- position: absolute;: Xác định rằng phần tử sẽ được xác định vị trí tuyệt đối, dựa trên vị trí của phần tử cha có thuộc tính position là relative, absolute, hoặc fixed.
- top, right, bottom, left: Xác định vị trí cụ thể của phần tử. Giá trị có thể là số nguyên hoặc phần trăm.

Ví dụ:
    .box {
    position: relative;
    }

    .box-child {
    position: absolute;
    top: 20px;
    left: 10px;
    }
    Trong ví dụ trên, phần tử có lớp CSS .child sẽ được đặt ở vị trí cách phần tử cha có lớp CSS .box 20px từ phía trên và 10px từ phía trái.

Phần tử có position: absolute; sẽ không chiếm diện tích trong luồng bình thường của tài liệu, nghĩa là các phần tử khác không được ảnh hưởng bởi nó. Nếu không có phần tử cha có position: relative;, phần tử với position: absolute; sẽ được căn chỉnh dựa trên phần tử gốc của tài liệu (thường là body hoặc phần tử gốc khác).