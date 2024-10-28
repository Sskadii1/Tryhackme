**What are Incidents?**

Một số quy trình khác nhau chạy trên các thiết bị điện toán của bạn, ví dụ như máy tính xách tay, điện thoại di động, v.v. Quy trình này là tương tác, nghĩa là bạn thực hiện các hành động, ví dụ như chơi trò chơi hoặc xem video. Ngoài ra, còn có quy trình không tương tác chạy trong nền có thể không yêu cầu bạn tương tác với chúng. 

Bất cứ điều gì chúng làm, một sự kiện(Even) sẽ được ghi lại cho những gì chúng đã làm.

Event được tạo ra với số lượng lớn thường xuyên. Điều này là do nhiều quy trình chạy trên một thiết bị, mỗi quy trình thực hiện các tác vụ thường lệ khác nhau, tạo ra nhiều sự kiện. 

Vì vậy, khi giải pháp bảo mật tìm thấy một sự kiện hoặc nhóm sự kiện liên quan đến một hoạt động có thể gây hại, nó sẽ kích hoạt cảnh báo. Sau đó, nhóm bảo mật sẽ phân tích các cảnh báo này. Một số cảnh báo này có thể là False Positives , trong khi một số sẽ là True Positives.

False Positives là khi một giải pháp bảo mật đưa ra cảnh báo về lượng dữ liệu lớn được chuyển từ một hệ thống sang một địa chỉ IP bên ngoài. Ví dụ như sau khi phân tích cảnh báo này, nhóm bảo mật phát hiện ra rằng hệ thống chủ thể đang trải qua quá trình sao lưu vào một dịch vụ lưu trữ đám mây. Điều này được gọi là kết quả false Positives.

True Positives: Một giải pháp bảo mật đã đưa ra cảnh báo về nỗ lực lừa đảo qua email đối với một trong những người dùng của tổ chức. Sau khi phân tích cảnh báo này, nhóm bảo mật phát hiện ra rằng email là email lừa đảo được gửi đến người dùng này để xâm phạm hệ thống. Điều này được gọi là true positive.

Những cảnh báo True Positives này đôi khi được gọi là Sự cố(Incidents). 

**Types of Incidents**

Những ca incidents có thể xảy ra bởi hoạt động có hại liên quan đến thế giới kỹ thuật số. Chúng ta có thể phân loại chúng thành 5 loại, như sau

1.Malware Infections:  Phần mềm độc hại là chương trình độc hại có thể gây hại cho hệ thống, mạng hoặc ứng dụng. Phần lớn các sự cố liên quan đến nhiễm phần mềm độc hại.  Có nhiều loại phần mềm độc hại khác nhau, mỗi loại có khả năng gây thiệt hại riêng. Nhiễm phần mềm độc hại chủ yếu do các tệp có thể là văn bản, tài liệu, tệp thực thi, v.v.
    
2.Security Breaches: xảy ra khi một người không được phép truy cập vào dữ liệu bí mật. Vi phạm bảo mật có tầm quan trọng tối đa vì nhiều doanh nghiệp dựa vào dữ liệu bí mật của họ, mà chỉ những nhân viên được ủy quyền mới có thể truy cập.
    
3.Data Leaks: Rò rỉ dữ liệu là sự cố trong đó thông tin bí mật của một cá nhân hoặc một tổ chức bị tiết lộ cho các thực thể không được phép. Nhiều kẻ tấn công sử dụng rò rỉ dữ liệu để gây tổn hại đến danh tiếng của nạn nhân hoặc sử dụng kỹ thuật này để đe dọa nạn nhân và lấy những gì chúng cần từ họ. Không giống như Security Breaches, rò rỉ dữ liệu cũng có thể vô tình do lỗi của con người hoặc cấu hình sai.
    
4.Insider Attacks: Các sự cố từ bên trong một tổ chức được gọi là tấn công nội bộ. Hãy nghĩ về một nhân viên bất mãn lây nhiễm toàn bộ mạng thông qua USB vào ngày làm việc cuối cùng của mình. Đây là một ví dụ về tấn công nội bộ. Một người nào đó trong tổ chức của bạn cố tình khởi xướng một cuộc tấn công sẽ thuộc loại này. Các cuộc tấn công này có thể nguy hiểm, vì người trong cuộc luôn có quyền truy cập vào các tài nguyên lớn hơn người ngoài cuộc.
    
5.Denial Of Service Attacks: Availability(C-I-A triad) là một trong ba trụ cột của an ninh mạng. Các giải pháp bảo mật phòng thủ và con người liên tục tìm cách bảo vệ thông tin; họ đảm bảo rằng dữ liệu có sẵn cho mọi người cùng một lúc. Điều này là do không có ích gì khi bảo vệ thứ mà chúng ta không thể truy cập. Tấn công từ chối dịch vụ, hay tấn công DoS , là những sự cố mà kẻ tấn công làm ngập hệ thống/mạng/ứng dụng bằng các yêu cầu, cuối cùng khiến người dùng cần thiết/khách hàng không thể truy cập. Điều này xảy ra do cạn kiệt tài nguyên có sẵn để giải quyết các yêu cầu.

Tất cả các sự cố này đều có khả năng tác động tiêu cực đến nạn nhân. Những sự cố này không thể so sánh về mức độ nghiêm trọng của tác động mà chúng tạo ra. Điều này là do một sự cố cụ thể có thể gây ra thảm họa cho một tổ chức trong khi nó có thể gây ra thiệt hại nhỏ cho tổ chức khác. 
  
**Incident Response Process**
 
 Đôi khi, việc xử lý nhiều loại sự cố trong một môi trường có thể khó khăn. Do bản chất riêng biệt của các sự cố trong các tổ chức, nên cần có một quy trình có cấu trúc để ứng phó với sự cố. Ở đây, tôi đã học được rằng có hai dạng kế hoạch phổ biến để phản ứng trước các sự cố, đó là của SANS, và của NIST.

 Sự khác biệt ở đây, là SANS có 6 bước, và NIST có 4 bước.

 SANS: Tên gọi của kế hoạch này là **PICERL**, nó bao gồm Preparation, Identification, Containment, Eradication, Recovery, Lessons Learned.

1.Preparation: Đây là giai đoạn đầu tiên. Giai đoạn chuẩn bị bao gồm xây dựng các nguồn lực cần thiết để xử lý sự cố. 
      
2.Identification: Giai đoạn nhận dạng đề cập đến việc tìm kiếm bất kỳ hành vi bất thường nào có thể chỉ ra sự cố. Điều này bao gồm việc sử dụng các giải pháp và kỹ thuật bảo mật khác nhau để theo dõi các sự kiện bất thường.
    
3.Containment: Khi đã xác định được sự cố, bước tiếp theo là phải ngăn chặn sự cố. Điều này có nghĩa là giảm thiểu tác động của cuộc tấn công. Điều này thường được thực hiện bằng cách cô lập máy nạn nhân, vô hiệu hóa các tài khoản người dùng bị xâm phạm, v.v.
    
4.Eradication: Giai đoạn này, như tên gọi của nó, bao gồm việc loại bỏ mối đe dọa khỏi môi trường bị tấn công. Mối đe dọa có thể là bất kỳ loại nào. Giai đoạn diệt trừ sẽ đảm bảo môi trường của đối tượng được sạch sẽ và bây giờ chúng ta có thể chuyển sang giai đoạn phục hồi.
    
5.Recovery: Giai đoạn phục hồi rất quan trọng trong chuỗi này. Nó bao gồm việc khôi phục các hệ thống bị ảnh hưởng từ bản sao lưu hoặc xây dựng lại chúng. Sau đó, các hệ thống được phục hồi được kiểm tra và sẵn sàng sử dụng.
    
6.Lessons Learned: Đây cũng là một phần quan trọng của vòng đời ứng phó sự cố. Các khoảng trống trong quá trình phát hiện và phân tích sự cố được xác định và ghi lại, giúp cải thiện toàn bộ quy trình trong các sự cố trong tương lai.
    
![image](https://github.com/user-attachments/assets/19a913b2-6724-4831-9bb6-f07105d4ff90)



**Incident Response Techniques**

Rất khó để tìm kiếm hành vi bất thường và xác định sự cố theo cách thủ công. Có nhiều giải pháp bảo mật có vai trò riêng trong việc phát hiện bất kỳ sự cố nào. Một số trong số chúng thậm chí có khả năng ứng phó với sự cố và thực hiện các giai đoạn khác của vòng đời, chẳng hạn như ngăn chặn, xóa bỏ, v.v. Dưới đây là giải thích ngắn gọn về một số giải pháp này
SIEM : Giải pháp quản lý sự kiện và thông tin bảo mật ( SIEM ) thu thập tất cả các nhật ký quan trọng tại một vị trí tập trung và đối chiếu chúng để xác định sự cố.
AV : Phần mềm diệt vi-rút ( AV ) phát hiện các chương trình độc hại đã biết trong hệ thống và thường xuyên quét hệ thống của bạn để tìm các chương trình này.
EDR : Endpoint Detection and Response ( EDR ) được triển khai trên mọi hệ thống, bảo vệ hệ thống khỏi một số mối đe dọa cấp độ nâng cao. Giải pháp này cũng có thể ngăn chặn và loại bỏ mối đe dọa.

Sau khi xác định được sự cố, một số quy trình nhất định phải được tuân theo, bao gồm điều tra mức độ tấn công, thực hiện các hành động cần thiết để ngăn ngừa thiệt hại thêm và loại bỏ nó từ gốc rễ.

Các bước này có thể khác nhau đối với các loại sự cố khác nhau. Trong trường hợp này, có hướng dẫn từng bước để xử lý từng loại sự cố giúp bạn tiết kiệm rất nhiều thời gian. Các loại hướng dẫn này được gọi là Sổ tay hướng dẫn(Playbooks).

Sau đây là một ví dụ về Playbook cho một sự cố: Email lừa đảo

Thông báo cho tất cả các bên liên quan về sự cố email lừa đảo

1.Xác định xem email có độc hại hay không bằng cách tiến hành phân tích tiêu đề và nội dung của email

2.Tìm kiếm bất kỳ tệp đính kèm nào trong email và phân tích chúng

3.Xác định xem có ai đã mở tệp đính kèm không

4.Cô lập các hệ thống bị nhiễm khỏi mạng

5.Chặn người gửi email

Ngoài ra, chúng ta còn có Runbooks, là bản thực hiện chi tiết, từng bước của các bước cụ thể trong các sự cố khác nhau. Các bước này có thể khác nhau tùy thuộc vào các nguồn lực có sẵn để điều tra.




Tài liệu này giải thích về các sự cố bảo mật, những hoạt động kỹ thuật số có hại có thể gây ảnh hưởng đến hệ thống hoặc dữ liệu. Nó đề cập đến các loại sự cố chính như nhiễm phần mềm độc hại, vi phạm bảo mật, rò rỉ dữ liệu, tấn công nội bộ và tấn công từ chối dịch vụ (DoS). Quy trình ứng phó sự cố tuân theo các mô hình như SANS PICERL, bao gồm các bước từ chuẩn bị đến rút kinh nghiệm, và sử dụng các công cụ như SIEM, AV, và EDR để phát hiện và giảm thiểu sự cố. Tài liệu cũng giới thiệu playbook và runbook, là hướng dẫn chi tiết cho việc xử lý các sự cố như email lừa đảo một cách có cấu trúc và hiệu quả.



