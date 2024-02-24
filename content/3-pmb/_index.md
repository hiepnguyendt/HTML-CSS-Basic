---
title : "Đệm, viền và khoảng lề"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

1. Thuộc tính padding (đệm)
    - Trong CSS, thuộc tính "padding" được sử dụng để xác định khoảng cách giữa nội dung của một phần tử và ranh giới (border) của nó. Thuộc tính này thường được sử dụng để tạo ra khoảng trắng xung quanh nội dung của một phần tử.
        - Cú pháp: 
            ```
            padding: giá-trị;
            ```
    - Giá trị của thuộc tính "padding" có thể là một giá trị duy nhất hoặc là một danh sách gồm bốn giá trị, tương ứng với các cạnh top, right, bottom và left (theo thứ tự kim đồng hồ). Các giá trị có thể được xác định bằng đơn vị đo ***(px, em, rem, %)*** hoặc bằng từ khóa như "auto".

2. Thuộc tính border (đường viền)
    - Trong CSS, thuộc tính ***"border"*** được sử dụng để xác định đường viền xung quanh một phần tử. Đường viền có thể là một đường thẳng, một đường nét đứt, hoặc một hình dạng khác.
       - Cú pháp: 
            ```
            border: [kích thước] [loại] [màu];
            ```
    - **[kích thước]**: Xác định kích thước của đường viền. Có thể là một giá trị duy nhất hoặc là một danh sách gồm bốn giá trị ***(top, right, bottom, left)*** tương ứng với các cạnh của phần tử. Các giá trị có thể là số nguyên, số thập phân hoặc sử dụng các đơn vị đo như px, em, rem.
    - **[loại]**: Xác định loại đường viền. Có thể là "solid" (đường thẳng), "dotted" (đường nét đứt), "dashed" (đường nét gạch), "double" (đường viền kép), "groove" (đường viền rãnh), "ridge" (đường viền núi), "inset" (đường viền lồi vào), "outset" (đường viền lồi ra), hoặc "none" (không có đường viền).
    - **[màu]**: Xác định màu sắc của đường viền. Có thể là tên màu (ví dụ: "red", "blue"), mã màu hex (ví dụ: "#ff0000"), hoặc giá trị màu rgba.
    - Ví dụ:
        - Sử dụng giá trị duy nhất:
             ```
            .box {
            border: 2px solid red;
            }
            ```
            *Đường viền có kích thước 2px, loại đường thẳng (solid) và màu đỏ*.

        - Sử dụng danh sách giá trị:
            ```
            .box {
            border: 1px solid red;
            border-width: 1px 2px 3px 4px;
            }
             ```
            *Đường viền của phần tử có kích thước 1px ở cạnh trên, 2px ở cạnh phải, 3px ở cạnh dưới và 4px ở cạnh trái.*

    - Ngoài ra, cũng có thể sử dụng các thuộc tính con của "border" như "border-top", "border-right", "border-bottom" và "border-left" để chỉ định giá trị cho từng cạnh một.
        - Ví dụ:
            ```
            .box {
                border-top: 1px solid red;
                border-right: 2px dashed blue;
                border-bottom: 3px dotted green;
                border-left: 4px double orange;
                }
            ```
            *Phần tử có đường viền ở từng cạnh với các kích thước, loại và màu sắc khác nhau.*

    Trên đây là cách sử dụng thuộc tính "border" trong CSS để xác định đường viền xung quanh một phần tử.

3. Thuộc tính margin (khoảng cách lề)
    - Trong CSS, thuộc tính "margin" được sử dụng để xác định khoảng cách giữa các phần tử và ranh giới của chúng. Thuộc tính này thường được sử dụng để tạo ra khoảng trắng xung quanh các phần tử và điều chỉnh khoảng cách giữa chúng.
       - Cú pháp:
            ```
            margin: giá-trị;
            ```
    - Giá trị của thuộc tính "margin" có thể là một giá trị duy nhất hoặc là một danh sách gồm bốn giá trị, tương ứng với các cạnh top, right, bottom và left (theo thứ tự kim đồng hồ). Các giá trị có thể được xác định bằng đơn vị đo (px, em, rem, %) hoặc bằng từ khóa như "auto".

        - Ví dụ:
            -  Sử dụng giá trị duy nhất:
                ```
                .box {
                margin: 20px;
                }
                ```
            - Sử dụng danh sách giá trị:
                ```
                .box {
                margin: 10px 20px 15px 5px;
                }
                ```
                *Giá trị "10px" áp dụng cho cạnh trên (top), "20px" áp dụng cho cạnh phải (right), "15px" áp dụng cho cạnh dưới (bottom) và "5px" áp dụng cho cạnh trái (left).*
    
    - Ngoài ra, cũng có thể sử dụng các thuộc tính con của "margin" như "margin-top", "margin-right", "margin-bottom" và "margin-left" để chỉ định giá trị cho từng cạnh một.

        - Ví dụ:
            ```
            .box {
            margin-top: 10px;
            margin-right: 20px;
            margin-bottom: 15px;
            margin-left: 5px;
            }
            ```
    - Giá trị của "margin" cũng có thể là âm để tạo ra sự chồng chéo giữa các phần tử.
        - Ví dụ:
            ```
            .box {
            margin: -10px;
            }
            ```
           *Trên đây là cách sử dụng thuộc tính "margin" trong CSS để xác định khoảng cách giữa các phần tử và ranh giới của chúng.*

4. Thuộc tính box-sizing
    - Thuộc tính "box-sizing" trong CSS được sử dụng để xác định cách tính toán kích thước của một phần tử, bao gồm cả kích thước của nội dung, padding và border.
        - Cú pháp:
            ```
            box-sizing: giá-trị;
            ```
    - Có hai giá trị phổ biến cho thuộc tính "box-sizing":

        - Giá trị "content-box" (giá trị mặc định): Kích thước của phần tử chỉ tính toán dựa trên kích thước của nội dung bên trong phần tử, không tính thêm padding và border. Đây là cách tính toán kích thước truyền thống của các phần tử trong CSS.

        - Giá trị "border-box": Kích thước của phần tử tính toán bao gồm cả kích thước của nội dung, padding và border. Điều này có nghĩa là kích thước của phần tử sẽ bao gồm cả padding và border, mà không làm thay đổi kích thước tổng cộng của phần tử.

        - Ví dụ:
            ```
            .box {
            box-sizing: border-box;
            width: 200px;
            padding: 20px;
            border: 1px solid black;
            }
            ```
            *Trong ví dụ trên, thuộc tính "box-sizing" được đặt thành "border-box", điều này có nghĩa là kích thước của phần tử sẽ tính toán bao gồm cả padding và border. Vì vậy, dù đã đặt width là 200px, kích thước tổng cộng của phần tử vẫn là 200px (bao gồm cả nội dung, padding và border), và không bị thay đổi do padding và border.*

        Trên đây là ý nghĩa và cách sử dụng thuộc tính "box-sizing" trong CSS.

