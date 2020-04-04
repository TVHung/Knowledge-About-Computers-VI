Hôm nay chúng ta sẽ tìm hiểu về kernel
1.	Định nghĩa
-	Kernel 
o	Nó có nghĩa là nhân của hệ điều hành.
o	Nó là một chương trình máy tính điều khiển mọi thứ khác trong hệ điều hành.
o	Quản lý tài nguyên của hệ thống (Liên lạc giữa thành phần phần cứng và phần mềm của hệ thống).
 
2.	Vai trò
-	Bạn có thể tưởng tượng kernel như một người phiên dịch. Nó chuyển đổi các yêu cầu đầu vào / đầu ra từ phần mềm thành một tập lệnh cho CPU và GPU. Nói một cách đơn giản, đó là một lớp ở giữa phần mềm và phần cứng giúp mọi thứ đều có thể hoạt động. Kernel quản lý:
o	CPU / GPU.
o	Bộ nhớ Memory.
o	Thiết bị đầu vào / đầu ra hoặc IO.
o	Quản lý nguồn tài nguyên.
o	Quản lý thiết bị.
o	Hệ thống gọi.
 
-	Kernel có tác dụng bảo vệ máy tính. Nếu không có bảo vệ bất kì máy tính nào cũng có thể thực hiện bất kì tác vụ nào trên máy tính dẫn đến làm hỏng máy tính và hỏng dữ liệu của bạn.
-	Kernel thường cung cấp các tiện ích xử lý này cho các tiến trình của các phần mềm ứng dụng qua các cơ chế liên lạc giữa các tiến trình (inter-process communication) và các hàm hệ thống (system call).

3.	Cách hoạt động
-	Sau đây tôi sẽ giải thích một cách dễ hiểu về hoạt động của kernel cho các bạn:






o	Khi bạn mở camera, ứng dụng camera sẽ gửi một lệnh yêu cầu mở cảm biến camera đến kernel.
 
o	Lúc đó kernel sẽ tiếp nhận yêu cầu và chuyển thành dữ liệu xử lý rồi gửi đến chip xử lý trung tâm(CPU).
    
o	Tiếp đó CPU sẽ tiến hành điều khiển các cảm biến camera mở ra. 
 
o	Tiếp tục kernel sẽ chuyển đổi các dữ liệu hình ảnh cảm biến camera thu được và trả về cho ứng dụng camera.
   
o	Sau đó ứng dụng sẽ xử lý dữ liệu hình ảnh để hoàn thiện một bức ảnh thành 1 hình ảnh hoàn chỉnh và hiển thị trên màn hình.

 
4.	Các loại kernel
•	Kernel nguyên khối (Monolithic Kernel)
o	Ở đây, cả OS và Kernel đều chạy trong cùng một không gian bộ nhớ và phù hợp trong đó bảo mật không phải là vấn đề đáng lo ngại. Nó dẫn đến truy cập nhanh hơn, nhưng nếu có lỗi trong trình điều khiển thiết bị, toàn bộ hệ thống sẽ gặp sự cố.
•	Kernel vi mô (Micro Kernel)
o	Đây là phiên bản rút gọn của Kernel Monolithic, trong đó Kernel có thể thực hiện hầu hết các công việc được thực hiện và không cần thêm GUI. Chúng nên được sử dụng khi bảo mật và hệ thống sự cố không xảy ra.
•	Kernel lai (Hybrid Kernel)
o	Kernel này chúng ta thấy nhiều nhất - Microsoft Windows, Apple MacOS. Chúng là sự pha trộn giữa Kernel nguyên khối và Kernel vi mô. Nó di chuyển trình điều khiển nhưng giữ các dịch vụ hệ thống bên trong Kernel - tương tự như cách driver được tải khi Windows bắt đầu quá trình khởi động.
•	Kernel Nano
o	Nếu bạn cần phải có Kernel, nhưng phần lớn chức năng của nó được thiết lập bên ngoài, thì xem hình ví dụ bên trên.
•	Kernel Exo
o	Kernel này chỉ cung cấp bảo vệ quá trình và xử lý tài nguyên. Tuy nhiên, nó chủ yếu được sử dụng khi bạn đang thử nghiệm một dự án đường phố và bạn nâng cấp lên loại Kernel tốt hơn.

