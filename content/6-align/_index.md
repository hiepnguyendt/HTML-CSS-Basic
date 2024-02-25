---
title : "Một số tricks và tips"
date :  "`r Sys.Date()`" 
weight : 6 
chapter : false
pre : " <b> 6. </b> "
---

#### Một số cách căn giữa trong CSS
1. Các cách căn giữa trong CSS
   - Căn giữa các phần tử trong CSS có thể được thực hiện bằng nhiều cách khác nhau, tùy thuộc vào loại phần tử và yêu cầu cụ thể của bạn. Dưới đây là một số cách phổ biến để căn giữa các phần tử:
   - Căn giữa theo chiều ngang (horizontal centering):

      - Căn giữa phần tử block: Đặt thuộc tính margin-left và margin-right thành auto và đảm bảo rằng phần tử có một chiều rộng cụ thể. 
      - Ví dụ:
         ```
         .center-element {
         margin-left: auto;
         margin-right: auto;
         width: 200px; /* Đặt chiều rộng mong muốn */
         }
         ```
   
      - Căn giữa phần tử inline hoặc inline-block: Sử dụng thuộc tính text-align của phần tử cha để căn giữa các phần tử con theo chiều ngang. 
      - Ví dụ:
         ```
         .center-parent {
         text-align: center;
         }

         .center-child {
         display: inline-block; /* hoặc inline */
         }
         ```

2. Căn giữa theo chiều dọc (vertical centering):

   - Căn giữa phần tử block: Sử dụng kỹ thuật "absolute positioning" và "transform" để căn giữa theo chiều dọc. 
   - Ví dụ:
      ```
      .center-element {
      position: relative;
      top: 50%;
      transform: translateY(-50%);
      }
      ```
   - Căn giữa phần tử inline hoặc inline-block: Sử dụng thuộc tính line-height và vertical-align của phần tử cha để căn giữa các phần tử con theo chiều dọc. 
   - Ví dụ:
      ```
      .center-parent {
      line-height: 200px; /* Đặt chiều cao mong muốn */
      text-align: center;
      }

      .center-child {
      display: inline-block; /* hoặc inline */
      vertical-align: middle;
      }
      ```
3. Căn giữa theo cả hai chiều (horizontal và vertical centering):

   - Sử dụng "flexbox": Đặt thuộc tính display của phần tử cha thành flex và sử dụng các thuộc tính justify-content và align-items để căn giữa phần tử con theo cả hai chiều. 
   - Ví dụ:
      ```
      .center-parent {
      display: flex;
      justify-content: center;
      align-items: center;
      }
      ```

   - Sử dụng "grid": Đặt thuộc tính display của phần tử cha thành grid và sử dụng các thuộc tính justify-items và align-items để căn giữa phần tử con theo cả hai chiều. 
   - Ví dụ:
      ```
      .center-parent {
      display: grid;
      justify-items: center;
      align-items: center;
      }
      ```
   ***Lưu ý rằng một số kỹ thuật căn giữa có thể yêu cầu một số điều kiện đặc biệt, chẳng hạn như phải có kích thước cụ thể cho phần tử hoặc phải có phần tử cha có kích thước xác định. Hãy kiểm tra và đảm bảo các yêu cầu đó được đáp ứng khi áp dụng các kỹ thuật căn giữa.***

#### Hiển thị ảnh dự phòng khi ảnh chính lỗi
1. Để hiển thị ảnh dự phòng (fallback image) khi ảnh chính gặp lỗi, bạn có thể sử dụng thuộc tính onerror của thẻ <img> để xử lý sự kiện lỗi và thay thế ảnh bằng ảnh dự phòng.

   - Dưới đây là một ví dụ về cách thực hiện điều này:
      ```
      <img src="duong-dan-anh-chinh.jpg" onerror="this.src='duong-dan-anh-du-phong.jpg';">
      ```

   - ***Lưu ý, thuộc tính onerror chỉ sử dụng được cho thẻ <img>***
2. Để hiển thị ảnh dự phòng cho thuộc tính background-image, chúng ta sẽ xử lí như sau:
   - Ví dụ: 
      ```
      background-image: url('duong-dan-anh-chinh.jpg'), url('duong-dan-anh-du-phong.jpg');
      ```
#### Tối ưu performance hình ảnh với srcset
 - Để tối ưu hiệu suất (performance) của hình ảnh trên trang web, bạn có thể sử dụng thuộc tính srcset cùng với thẻ <img>. Thuộc tính này cho phép bạn cung cấp nhiều phiên bản hình ảnh với các kích thước và độ phân giải khác nhau, để trình duyệt có thể tải phiên bản phù hợp nhất với thiết bị và môi trường hiện tại. Điều này giúp giảm thời gian tải và tiết kiệm băng thông mạng. 
 - Dưới đây là một ví dụ về cách sử dụng srcset:
    ```
   <img src="fcj.jpg"
     srcset="fcj-1x.jpg 1x,
             fcj-2x.jpg 2x,
             fcj-3x.jpg 3x"
     alt="FCJ">
     ```
- Trong ví dụ này, chúng ta có một thẻ <img> với thuộc tính src đặt thành đường dẫn của ảnh chính. Thuộc tính srcset chứa một danh sách các phiên bản hình ảnh với định dạng: đường-dẫn-hình-ảnh kích-thước. Trong đó, kích-thước có thể là một giá trị số và đơn vị x để chỉ định tỉ lệ độ phân giải so với kích thước ảnh gốc.

- Khi trình duyệt tải trang, nó sẽ xem xét các phiên bản hình ảnh trong srcset và chọn phiên bản phù hợp nhất dựa trên kích thước và độ phân giải thiết bị. Nếu trình duyệt không hỗ trợ srcset hoặc không tìm thấy phiên bản phù hợp, nó sẽ sử dụng đường dẫn hình ảnh trong thuộc tính src như một lựa chọn dự phòng.

- Bằng cách cung cấp nhiều phiên bản hình ảnh với srcset, bạn có thể đảm bảo rằng trình duyệt tải phiên bản tốt nhất cho từng thiết bị và môi trường, giúp cải thiện hiệu suất tải trang và trải nghiệm người dùng.