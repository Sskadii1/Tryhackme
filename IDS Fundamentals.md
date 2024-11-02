**What Is an IDS**

nếu kẻ tấn công vượt qua tường lửa thành công thông qua kết nối có vẻ hợp pháp và sau đó thực hiện bất kỳ hoạt động độc hại nào bên trong mạng, thì cần có biện pháp để phát hiện kịp thời. Vì mục đích này, chúng ta có một giải pháp bảo mật bên trong mạng. Giải pháp này được gọi là Hệ thống phát hiện xâm nhập ( IDS ).
The IDS plays the role of surveillance cameras. It sits in a corner, monitors the network traffic based on its signature and anomaly-based detections, and detects any abnormal traffic going out or inside the network. 

IDS đóng vai trò của camera giám sát. Nó nằm ở một góc, giám sát lưu lượng mạng dựa trên các phát hiện dựa trên chữ ký và bất thường của nó, và phát hiện bất kỳ lưu lượng bất thường nào ra vào mạng.

Sau mỗi lần phát hiện, một cảnh báo sẽ được tạo cho các quản trị viên bảo mật. IDS không hành động dựa trên các phát hiện đó; nó chỉ thông báo cho các quản trị viên bảo mật về hoạt động độc hại.

**Types of IDS**

IDS có thể được phân loại khác nhau tùy thuộc vào một số yếu tố nhất định. Phân loại chính của IDS phụ thuộc vào chế độ triển khai và phát hiện của nó.

Dưới đây là 2 dạng IDS có thể được triển khai:

Host Intrusion Detection System (HIDS): Các giải pháp IDS dựa trên máy chủ được cài đặt riêng lẻ trên từng máy chủ và chỉ có trách nhiệm phát hiện các mối đe dọa bảo mật tiềm ẩn liên quan đến máy chủ đó. Chúng cung cấp khả năng quan sát chi tiết về các hoạt động của máy chủ. Tuy nhiên, hệ thống phát hiện xâm nhập dựa trên máy chủ có thể gặp khó khăn khi quản lý trong các mạng lớn vì chúng tiêu tốn nhiều tài nguyên và yêu cầu quản lý trên từng máy chủ.

Network Intrusion Detection System (NIDS): Các giải pháp IDS dựa trên mạng rất quan trọng trong việc phát hiện các hoạt động có khả năng gây hại trong toàn bộ mạng, bất kể bất kỳ máy chủ cụ thể nào. Chúng giám sát lưu lượng mạng của tất cả các máy chủ liên quan để phát hiện các hoạt động đáng ngờ. Điều này cung cấp một cái nhìn tập trung về tất cả các phát hiện trong toàn bộ mạng.

Detection Modes của IDS

Signature-Based IDS:  IDS này lưu trữ chữ ký của các cuộc tấn công đã biết trong cơ sở dữ liệu và sử dụng chúng để phát hiện các cuộc tấn công tương tự trong tương lai. Tuy nhiên, nó không thể phát hiện các cuộc tấn công zero-day vì các cuộc tấn công này chưa có chữ ký trong cơ sở dữ liệu. Càng nhiều dữ liệu, nó càng tối ưu hơn và xử lý tốt hơn trong việc xứ lý tấn 

Anomaly-Based IDS: IDS này xây dựng một đường cơ sở về hành vi bình thường của mạng/hệ thống và phát hiện các sai lệch so với hành vi này. Nó có khả năng phát hiện các cuộc tấn công zero-day, nhưng dễ tạo ra kết quả dương tính giả. Cần tinh chỉnh(fine tuning) để giảm sai lệch này.

Hybrid IDS: Kết hợp hai phương pháp trên, Hybrid IDS sử dụng chữ ký để phát hiện các mối đe dọa đã biết và phương pháp phát hiện bất thường để xử lý các mối đe dọa mới.

Kết luận: IDS dựa trên chữ ký(Signature-Based IDS) có thể phát hiện các mối đe dọa nhanh chóng, trong khi các IDS khác có thể có chi phí xử lý cao.

Tuy nhiên, cũng cần phải xem xét IDS dựa trên một số yếu tố khác nhau. IDS dựa trên chữ ký có thể là một lựa chọn tốt để bao phủ một bề mặt mối đe dọa nhỏ. 

IDS dựa trên dị thường(Anomaly-Based IDS) và IDS Hybrid có thể giúp phát hiện các cuộc tấn công zero-day hiện đại, đang gia tăng hàng ngày và có thể gây ra thiệt hại lớn cho các tổ chức.

**IDS Example: Snort**
Snort là 1 dạng Signature-Based IDS, opensource và được phát triển vào năm 1998. 

Nó sử dụng các phát hiện dựa trên chữ ký và dựa trên dị thường để xác định các mối đe dọa đã biết. Những phát hiện này được định nghĩa trong các tệp quy tắc của công cụ Snort. 

Các chế độ của Snort:

Packet sniffer mode: Chế độ này chỉ đọc và hiển thị các gói tin mạng mà không phân tích chúng, hữu ích cho việc giám sát và chẩn đoán sự cố mạng. Đội ngũ mạng có thể sử dụng chế độ này của Snort để theo dõi lưu lượng khi gặp các vấn đề hiệu suất mạng.

Packet logging mode: Snort ghi lại lưu lượng mạng dưới dạng file PCAP để phân tích sau này. Chế độ này hỗ trợ đội ngũ bảo mật trong điều tra pháp y(digital forensic) bằng cách cung cấp các bản ghi(logs) lưu lượng để tìm nguyên nhân gốc rễ của các cuộc tấn công.

Network Intrusion Detection System mode: Đây là chế độ chính của Snort, giám sát lưu lượng mạng theo thời gian thực và sử dụng các quy tắc để phát hiện các mẫu tấn công đã biết. Chế độ NIDS giúp đội ngũ bảo mật phát hiện mối đe dọa tiềm ẩn.

Việc sử dụng Snort như một IDS có liên quan nhất đến chế độ NIDS của nó . Tuy nhiên, Snort có thể được sử dụng ở bất kỳ chế độ nào ở trên tùy thuộc vào yêu cầu.
