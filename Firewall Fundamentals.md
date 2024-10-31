**What Is the Purpose of a Firewall**
 Tường lửa được thiết kế để kiểm tra lưu lượng truy cập đến và đi của mạng hoặc thiết bị kỹ thuật số. Mục tiêu cũng giống như nhân viên bảo vệ ngồi bên ngoài tòa nhà: không để bất kỳ khách truy cập trái phép nào xâm nhập vào hệ thống hoặc mạng.
**Types of Firewalls**
Việc triển khai tường lửa trở nên phổ biến trong các mạng sau khi các tổ chức phát hiện ra khả năng lọc lưu lượng truy cập có hại khỏi hệ thống và mạng của họ. 

Một số loại tường lửa khác nhau đã được giới thiệu sau đó, mỗi loại có một mục đích riêng.

**Điều quan trọng cần lưu ý là các loại tường lửa khác nhau hoạt động trên các lớp mô hình OSI khác nhau.*

1. Stateless Firewalls
Loại tường lửa này hoạt động trên lớp 3 và lớp 4 của mô hình OSI

hoạt động bằng cách lọc dữ liệu dựa trên các quy tắc được xác định trước mà không lưu ý đến trạng thái của các kết nối trước đó.

Nhanh chóng xử lý các packets. Nhưng, không thể áp dùng các chính sách phức tạp cho dữ liệu dựa trên các kết nối trước đó. 

Ví dự như lẽ ra tường lửa phải chặn hết packets từ nguồn vi phạm. Lý tưởng nhất là nó sẽ loại bỏ tất cả các gói tin trong tương lai từ nguồn này vì các gói tin trước đó không tuân thủ các quy tắc của tường lửa. Tuy nhiên, tường lửa cứ quên điều này và các gói tin trong tương lai từ nguồn này sẽ được coi là mới và lại được khớp với các quy tắc của nó.

2. Stateful Firewalls
Khác với stateless, loại tường lửa này sẽ không chỉ lọc các packets được định bởi hay các quy tắc từ trước. Nó còn theo dõi các kết nối trước đó và lưu trữ chúng trong 1 bảng trạng thái. 

 Điều này bổ sung thêm một lớp bảo mật nữa bằng cách kiểm tra các  dựa trên lịch sử kết nối của chúng. 

Loại tường lửa này hoạt động trên lớp 3 và lớp 4 của mô hình OSI

3. Proxy Firewalls
Vấn đề với tường lửa trước đây là chúng không có khả năng kiểm tra nội dung của một gói tin.

Tường lửa proxy hoặc cổng cấp ứng dụng hoạt động như trung gian giữa mạng riêng và Internet và hoạt động trên lớp 7 của mô hình OSI. 

Các chính sách lọc nội dung có thể được áp dụng cho các tường lửa này để cho phép/từ chối lưu lượng truy cập đến và đi dựa trên nội dung của chúng.(content )
5. Next-gen Firewall(NGFW)
Đây là loại tường lửa tiên tiến nhất hoạt động từ lớp 3 đến lớp 7 của mô hình OSI

Nó cung cấp khả năng kiểm tra gói tin sâu và các chức năng khác giúp tăng cường bảo mật cho lưu lượng mạng đến và đi.

Nó có hệ thống ngăn chặn xâm nhập giúp chặn các hoạt động độc hại theo thời gian thực. Nó cung cấp khả năng phân tích theo phương pháp heuristic bằng cách phân tích các kiểu tấn công và chặn chúng ngay lập tức trước khi chúng xâm nhập vào mạng.

NGFW có khả năng giải mã SSL/TLS

Ngoài ra, còn có khả năng kiểm tra các gói tin sau khi giải mã chúng và liên kết dữ liệu với nguồn cấp dữ liệu tình báo về mối đe dọa để đưa ra quyết định hiệu quả.

**dưới đây là đặc điểm của từng tường lửa* 

Tường lửa không trạng thái	- Lọc cơ bản
- Không theo dõi các kết nối trước đó
- Hiệu quả cho các mạng tốc độ cao
  
Tường lửa có trạng thái	- Nhận dạng lưu lượng theo mẫu
- Có thể áp dụng các quy tắc phức tạp
- Giám sát các kết nối mạng
  
Tường lửa proxy	- Kiểm tra dữ liệu bên trong các gói tin
- Cung cấp các tùy chọn lọc nội dung
- Cung cấp khả năng kiểm soát ứng dụng
- Giải mã và kiểm tra các gói dữ liệu SSL/TLS
  
Tường lửa thế hệ tiếp theo	- Cung cấp khả năng bảo vệ trước các mối đe dọa tiên tiến
- Đi kèm với hệ thống phòng ngừa xâm nhập
- Xác định các bất thường dựa trên phân tích kinh nghiệm
- Giải mã và kiểm tra các gói dữ liệu SSL/TLS

**Rules in Firewalls**

Tường lửa cho phép bạn kiểm soát lưu lượng mạng của mình.

Mặc dù nó lọc lưu lượng dựa trên các quy tắc tích hợp sẵn, một số quy tắc tùy chỉnh có thể được xác định cho nhiều mạng khác nhau.

Ví dụ, sẽ có những mạng muốn từ chối tất cả lưu lượng SSH đi vào mạng của họ. Tuy nhiên, mạng của bạn sẽ có yêu cầu cho phép lưu lượng SSH từ một số địa chỉ IP cụ thể.

Các quy tắc cho phép bạn định cấu hình các thiết lập tùy chỉnh này cho lưu lượng đến và đi của mạng.

Các thành phần cơ bản của quy tắc tường lửa được mô tả dưới đây:

Source address: Địa chỉ IP của máy sẽ tạo ra lưu lượng truy cập.

Destination address: Địa chỉ IP của máy sẽ nhận dữ liệu.

Port: Số cổng cho lưu lượng truy cập.

Protocol: Giao thức sẽ được sử dụng trong quá trình giao tiếp.

Action: Phần này xác định hành động sẽ được thực hiện khi xác định bất kỳ lưu lượng truy cập nào có bản chất cụ thể này.

Direction: Trường này xác định khả năng áp dụng của quy tắc đối với lưu lượng truy cập đến hoặc đi.

Riêng với action, chúng ta sẽ có các loại hành động, để tạo lên 1 rule.

**Types of Actions*

Allow: cho biết lưu lượng truy cập cụ thể được xác định bên trong quy tắc sẽ được phép.
Deny:  của quy tắc có nghĩa là lưu lượng được xác định bên trong quy tắc sẽ bị chặn và không được phép. Các quy tắc này là cơ bản để nhóm bảo mật từ chối lưu lượng cụ thể đến từ các địa chỉ IP độc hại và tạo thêm các quy tắc để giảm bề mặt đe dọa của mạng.
Forward:  chuyển hướng lưu lượng đến một phân đoạn mạng khác bằng cách sử dụng các quy tắc chuyển tiếp được tạo trên tường lửa. Điều này áp dụng cho tường lửa cung cấp chức năng định tuyến(routing) và hoạt động như cổng giữa các phân đoạn mạng khác nhau.

**Directionality of Rules*

Tường lửa có nhiều loại quy tắc khác nhau, mỗi loại được phân loại dựa trên hướng lưu lượng mà các quy tắc được tạo ra.

Inbound Rules:Quy tắc được gọi là quy tắc inbound khi chúng chỉ được áp dụng cho lưu lượng truy cập đến. Ví dự như bạn chấp nhận toàn bộ lưu lượng từ port 80(http) cho cái webserver của bạn.

Outbound Rules: Các quy tắc này chỉ được tạo cho lưu lượng truy cập đi. Kiểu như, bạn chặn tất cả truy cập SMTP(port 25) ngoại trừ thiết bị máy chủ thư

Forward Rules:Quy tắc chuyển tiếp được tạo ra để chuyển tiếp lưu lượng cụ thể bên trong mạng. Ví dụ, chuyển tiếp lưu lượng HTTP port 80 đến máy chủ web server trong mạng của bạn

**Windows Defender Firewall**

**Linux iptables Firewall**
