---
title : "Thuộc tính vị trí"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

1. CSS position relative
   - Trong CSS, thuộc tính position: relative; được sử dụng để xác định vị trí của một phần tử dựa trên vị trí ban đầu của nó trong luồng bình thường của tài liệu. Khi một phần tử có thuộc tính position: relative;, nó sẽ được di chuyển dựa trên giá trị của các thuộc tính top, right, bottom, và left.
      - Cú pháp:
         ```
         selector {
         position: relative;
         top: value;
         right: value;
         bottom: value;
         left: value;
         }
         ```
   - **position:relative;** : Xác định rằng phần tử sẽ được xác định vị trí dựa trên vị trí ban đầu của nó.
   - **top, right, bottom, left**: Xác định khoảng cách mà phần tử sẽ di chuyển từ vị trí ban đầu của nó. Giá trị có thể là số nguyên hoặc phần trăm.
      - Ví dụ:
         ```
         .box {
         position: relative;
         top: 20px;
         left: 10px;
         }
         ```
         *Trong ví dụ trên, phần tử có lớp CSS .box sẽ được di chuyển 20px từ vị trí ban đầu theo hướng từ trên xuống và 10px từ vị trí ban đầu theo hướng từ trái sang phải.*

   Lưu ý rằng khi sử dụng position: relative;, phần tử vẫn giữ lại vị trí gốc của nó trong luồng bình thường của tài liệu. Việc di chuyển phần tử chỉ ảnh hưởng đến vị trí hiển thị của nó trên giao diện người dùng. Các phần tử khác trong tài liệu không sẽ không bị di chuyển hoặc ảnh hưởng bởi phần tử có position: relative;.

2. CSS position absolute
   - Trong CSS, thuộc tính position: absolute; được sử dụng để xác định vị trí của một phần tử dựa trên vị trí của phần tử cha gần nhất có thuộc tính position được đặt là relative, absolute, hoặc fixed. Phần tử với position: absolute; sẽ được di chuyển đến vị trí cụ thể trong tài liệu, không ảnh hưởng tới vị trí của các phần tử khác.

      - Cú pháp:
         ```
         selector {
         position: absolute;
         top: value;
         right: value;
         bottom: value;
         left: value;
         }
         ```
   - **position: absolute;**: Xác định rằng phần tử sẽ được xác định vị trí tuyệt đối, dựa trên vị trí của phần tử cha có thuộc tính position là relative, absolute, hoặc fixed.
   - **top, right, bottom, left**: Xác định vị trí cụ thể của phần tử. Giá trị có thể là số nguyên hoặc phần trăm.

      - Ví dụ:
         ```
         .box {
         position: relative;
         }

         .box-child {
         position: absolute;
         top: 20px;
         left: 10px;
         }
         ```
         *Trong ví dụ trên, phần tử có lớp CSS .child sẽ được đặt ở vị trí cách phần tử cha có lớp CSS .box 20px từ phía trên và 10px từ phía trái.*

   Phần tử có position: absolute; sẽ không chiếm diện tích trong luồng bình thường của tài liệu, nghĩa là các phần tử khác không được ảnh hưởng bởi nó. Nếu không có phần tử cha có position: relative;, phần tử với position: absolute; sẽ được căn chỉnh dựa trên phần tử gốc của tài liệu (thường là body hoặc phần tử gốc khác).