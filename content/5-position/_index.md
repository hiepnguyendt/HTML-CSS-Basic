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

 3. CSS position fixed
      - Trong CSS, thuộc tính position: fixed được sử dụng để định vị một phần tử cố định (fixed) liên quan đến viewport, không phụ thuộc vào vị trí cuộn trang. Khi một phần tử được đặt thành position: fixed, phần tử đó sẽ được loại bỏ khỏi luồng văn bản thông thường và vị trí của nó sẽ được xác định dựa trên viewport.

      - Dưới đây là một số điểm quan trọng về position: fixed:

         - Vị trí cố định: Phần tử được định vị liên quan đến viewport. Nó sẽ không di chuyển ngay cả khi trang được cuộn.

         - Bị loại bỏ khỏi luồng văn bản thông thường: Khi một phần tử được đặt thành position: fixed, nó sẽ được loại bỏ khỏi luồng văn bản thông thường. Các phần tử khác sẽ bỏ qua không gian mà nó chiếm.

         - Chồng chất nội dung: Vì các phần tử cố định được định vị liên quan đến viewport, chúng có thể chồng lên các phần tử khác trên trang. Bạn có thể kiểm soát thứ tự chồng chất bằng cách sử dụng thuộc tính z-index.

         - Không cuộn trang: Các phần tử cố định không cuộn cùng với phần còn lại của trang. Chúng được cố định ở vị trí trong viewport.
      - Để sử dụng position: fixed, bạn cần áp dụng nó cho một phần tử HTML bằng CSS. Dưới đây là một ví dụ:
         ```
         .fixed-element {
         position: fixed;
         top: 20px;
         left: 20px;
         z-index: 100;
         }
         ```
         *Trong ví dụ này, lớp .fixed-element được đặt thành vị trí cố định. Nó sẽ được định vị 20 pixel từ phía trên và 20 pixel từ phía trái của viewport. Thuộc tính z-index được đặt thành 100 để kiểm soát thứ tự chồng chất của phần tử.*

      - Bạn có thể điều chỉnh các thuộc tính top, bottom, left và right để định vị phần tử ở bất kỳ vị trí nào trong viewport.

      - Hãy nhớ rằng các phần tử cố định không bị ảnh hưởng bởi cuộn trang, do đó chúng có thể gây ra vấn đề về bố cục hoặc chồng chất nội dung khác. Quan trọng là kiểm tra và điều chỉnh vị trí của chúng để đảm bảo chúng hoạt động tốt trong bố cục của bạn.

4. CSS position sticky

   - Trong CSS, thuộc tính position: sticky được sử dụng để định vị một phần tử dính (sticky) trong luồng văn bản thông thường, nhưng chuyển sang vị trí cố định (fixed) khi nó tiếp xúc với ranh giới của một phần tử chứa.

   - Dưới đây là một số điểm quan trọng về position: sticky:

      - Vị trí dính: Phần tử được định vị bình thường trong luồng văn bản, nhưng nó chuyển sang vị trí cố định (fixed) khi nó tiếp xúc với ranh giới của một phần tử chứa (container element).

      - Chuyển đổi linh hoạt: Phần tử sẽ đi theo luồng văn bản thông thường cho đến khi nó tiếp xúc với ranh giới của phần tử chứa. Khi đó, nó sẽ bị "dính" vào vị trí cố định (fixed) và không di chuyển khi trang được cuộn. Khi phần tử chạm đến ranh giới dưới của phần tử chứa, nó sẽ ngừng "dính" và tiếp tục di chuyển theo luồng văn bản thông thường.

      - Thành phần chứa: position: sticky chỉ hoạt động khi áp dụng cho một phần tử con của một phần tử chứa (container element). Phần tử chứa phải có một chiều cao được định rõ và thuộc tính overflow được đặt thành giá trị khác visible.

      - Vị trí mặc định: Mặc định, phần tử sẽ được định vị dính ở vị trí ban đầu trong phần tử chứa, nhưng bạn có thể sử dụng các thuộc tính top, bottom, left, right để điều chỉnh vị trí dính.

   - Ví dụ:

      ```
      .sticky-element {
      position: sticky;
      top: 20px;
      }
      ```

      Trong ví dụ này, lớp .sticky-element được đặt thành vị trí dính. Nó sẽ được định vị ở vị trí ban đầu, và khi tiếp xúc với ranh giới của phần tử chứa, nó sẽ "dính" ở vị trí cố định (fixed) và không di chuyển khi trang được cuộn. Thuộc tính top được đặt thành 20px để chỉ định khoảng cách từ phía trên của phần tử chứa.

  ***Lưu ý rằng position: sticky không được hỗ trợ trên tất cả các trình duyệt và phiên bản. Vì vậy, bạn nên kiểm tra tính tương thích trình duyệt trước khi sử dụng nó.***
