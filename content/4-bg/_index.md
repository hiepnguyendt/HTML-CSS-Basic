---
title : "Thuộc tính tạo nền"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---


1. Thuộc tính background-image
   - Thuộc tính background-image trong CSS được sử dụng để đặt hình ảnh làm nền cho một phần tử. Bạn có thể chỉ định đường dẫn đến hình ảnh bằng cách sử dụng URL hoặc giá trị gradient để tạo hiệu ứng nền.
      - Cú pháp:
         ```
         background-image: giá-trị;
         ```
      - Ví dụ sử dụng cách đặt hình ảnh làm nền:
         ```
         .box {
         background-image: url("path/to/image.jpg");
         }   
         ```
         *Trong ví dụ trên, path/to/image.jpg là đường dẫn đến hình ảnh mà bạn muốn sử dụng làm nền cho phần tử có lớp CSS .box.*
   - Ngoài ra, bạn cũng có thể sử dụng giá trị gradient để tạo hiệu ứng nền.
      - Ví dụ:
         ```
         .box {
         background-image: linear-gradient(to bottom, #ff0000, #00ff00);
         }
         ```
         *Trong ví dụ này, chúng ta sử dụng giá trị linear-gradient để tạo một hiệu ứng gradient từ màu đỏ (#ff0000) đến màu xanh lá cây (#00ff00) từ trên xuống dưới.*

      Lưu ý rằng thuộc tính background-image có thể được kết hợp với các thuộc tính khác như background-repeat, background-position, background-size để tùy chỉnh cách hiển thị hình ảnh nền.
   
2. Thuộc tính background-size với cover, contain
   - background-size: cover;: Khi sử dụng giá trị cover, hình ảnh nền sẽ được co giãn hoặc thu nhỏ sao cho nó phủ đầy toàn bộ phần tử mà không bị méo. Điều này có nghĩa là hình ảnh có thể bị cắt bớt ở một số phần nếu tỷ lệ khung hình không khớp với tỷ lệ khung hình của phần tử.
      - Ví dụ:
         ```
         .box {
         background-image: url("path/to/image.jpg");
         background-size: cover;
         }
         ```
   - background-size: contain;: Khi sử dụng giá trị contain, hình ảnh nền sẽ được co giãn hoặc thu nhỏ sao cho nó hiển thị toàn bộ trong phần tử mà không bị cắt bớt. Điều này có thể dẫn đến việc xuất hiện dải trống (background-color) nếu tỷ lệ khung hình không khớp với tỷ lệ khung hình của hình ảnh.
      - Ví dụ:
         ```
         .box {
         background-image: url("path/to/image.jpg");
         background-size: contain;
         }
         ```
   Trên đây là cách sử dụng thuộc tính background-size với giá trị cover và contain để điều chỉnh kích thước của hình ảnh nền trong CSS.

3. Thuộc tính background-origin
   - Thuộc tính background-origin trong CSS được sử dụng để xác định điểm xuất phát (origin) của hình ảnh nền và các phần tử khác liên quan đến việc vẽ nền.
      - Cú pháp:
         ```
         background-origin: giá-trị;
         ```
   - Có ba giá trị phổ biến cho thuộc tính background-origin:

      - **padding-box** (giá trị mặc định): Hình ảnh nền và các phần tử liên quan (như padding và border) bắt đầu từ biên trong padding box của phần tử. Điều này có nghĩa là hình ảnh nền và các phần tử khác sẽ không xuyên qua phần padding và border.

      - **border-box**: Hình ảnh nền và các phần tử liên quan bắt đầu từ biên trong border box của phần tử. Điều này có nghĩa là hình ảnh nền và các phần tử có thể xuyên qua phần border, nhưng không xuyên qua phần margin.

      - **content-box**: Hình ảnh nền và các phần tử liên quan bắt đầu từ biên trong content box của phần tử. Điều này có nghĩa là hình ảnh nền và các phần tử có thể xuyên qua phần padding và border, và chỉ giới hạn bởi khu vực chứa nội dung.

      - Ví dụ:
         ```
         .box {
         background-image: url("path/to/image.jpg");
         background-origin: content-box;
         }
         ```
         *Trong ví dụ trên, thuộc tính background-origin được đặt thành content-box, điều này có nghĩa là hình ảnh nền và các phần tử liên quan sẽ bắt đầu từ biên bên trong content box của phần tử.*

   Thuộc tính background-origin thường được sử dụng kết hợp với các thuộc tính khác như background-image, background-position, background-repeat, và background-size để tùy chỉnh việc vẽ nền của một phần tử trong CSS.

4. Thuộc tính background-position
   - Thuộc tính background-position trong CSS được sử dụng để xác định vị trí xuất hiện của hình ảnh nền bên trong phần tử.
      - Cú pháp:
         ```
         background-position: giá-trị-x giá-trị-y;
         ```
   - Hai giá trị **giá-trị-x** và **giá-trị-y** trong **background-position** xác định vị trí ngang và dọc của hình ảnh nền tương đối với phần tử. Có thể sử dụng các giá trị đơn vị như pixel (px), phần trăm (%), hoặc từ khoá như left, right, top, bottom, center để chỉ định vị trí.

      - Ví dụ:
         ```
         .box {
         background-image: url("path/to/image.jpg");
         background-position: center top;
         }
         ```
         *Trong ví dụ trên, hình ảnh nền sẽ được căn giữa theo chiều ngang (center) và đặt ở phía trên cùng theo chiều dọc (top) bên trong phần tử có lớp CSS .box.*

   - Bạn cũng có thể sử dụng các giá trị số để xác định vị trí chính xác. 
      - Ví dụ:
         ```
         .box {
         background-image: url("path/to/image.jpg");
         background-position: 20px 50%;
         }
         ```
         *Trong ví dụ này, hình ảnh nền sẽ được dịch chuyển 20 pixel từ cạnh trái và căn giữa theo chiều dọc (50%) bên trong phần tử.*
   - Ngoài ra, background-position cũng hỗ trợ việc kết hợp các từ khoá và giá trị số để xác định vị trí. 
      - Ví dụ:
         ```
         .box {
         background-image: url("path/to/image.jpg");
         background-position: center 20%;
         }
         ```
         *Trong ví dụ này, hình ảnh nền sẽ được căn giữa theo chiều ngang (center) và dịch chuyển 20% từ cạnh trên cùng theo chiều dọc bên trong phần tử*
   
   Lưu ý rằng thuộc tính background-position cũng có thể được sử dụng cùng với các giá trị khác như background-repeat, background-size, và background-origin để tùy chỉnh cách hiển thị hình ảnh nền

5. Cú pháp "shorthand" cho background
   - Thuộc tính background trong CSS cho phép bạn gộp nhiều thuộc tính liên quan đến hình ảnh nền thành một cú pháp ngắn gọn. 
      - Cú pháp:
         ```
         background: giá-trị;
         ```
   - Giá trị của thuộc tính background có thể bao gồm nhiều thuộc tính con, được phân cách bằng dấu cách. Dưới đây là một số giá trị phổ biến cho thuộc tính background:
      - **background-color**: Xác định màu nền của phần tử.
      - **background-image**: Xác định hình ảnh nền.
      - **background-repeat**: Xác định cách lặp lại hình ảnh nền.
      - **background-position**: Xác định vị trí xuất hiện của hình ảnh nền.
      - **background-size**: Xác định kích thước của hình ảnh nền.
      - **background-origin**: Xác định điểm xuất phát của hình ảnh nền.

   - Ví dụ:

      ```
      .box {
       background: #F0F0F0 url("path/to/image.jpg") no-repeat center top / cover;
      }

      ```

        *Trong ví dụ trên, thuộc tính background được sử dụng để gộp background-color, background-image, background-repeat, background-position, background-size thành một cú pháp ngắn gọn. Màu nền được đặt là #F0F0F0, hình ảnh nền là url("path/to/image.jpg"), không lặp lại (no-repeat), căn giữa theo chiều ngang và đặt ở phía trên cùng theo chiều dọc (center top), và có kích thước cover.*

   Lưu ý rằng khi sử dụng cú pháp ngắn gọn background, các thuộc tính không được xác định sẽ có giá trị mặc định. Đồng thời, thứ tự của các thuộc tính con trong cú pháp background không quan trọng, nhưng giữa chúng cần có dấu cách phân cách.
