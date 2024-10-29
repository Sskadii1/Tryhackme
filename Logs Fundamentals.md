**Introduction to Logs**

Những kẻ tấn công rất thông minh. Chúng thường tránh để lại dấu vết, vì vậy chúng ratas khó bị phát hiện. Tuy nhiên, nhóm bảo mật có vai trò xác định, và xác định cách thức thực hiện của kẻ tấn công, đôi lúc họ còn phải tìm ra kẻ đứng sau cuộc tấn công.

Bằng cách thu chứng cứ, cô lập hiện trường và các bằng chứng, chúng ta có thể truy vết, và sử dụng biện pháp của pháp y điện tử(digital forensic).
Chúng ta có thể dò được nguyên nhân, và tác giả của vụ án. Ở đây, tôi sẽ nói kỹ về Logs.

Logs, hay digital logs, là cách thức lưu lại những gì đã xảy ra, dưới dạng thời gian biểu, nó lưu lại hết những thông tin mà ứng dụng thực hiện trong khoảng thời gian thiết bị hoạt động.

Logs có thể sử dụng như:

1. Security Events Monitoring: Nhật ký giúp chúng tôi phát hiện hành vi bất thường khi sử dụng giám sát thời gian thực.

2. Incident Investigation and Forensics: Nhật ký là dấu vết của mọi loại hoạt động. Nó cung cấp thông tin chi tiết về những gì đã xảy ra trong sự cố. Nhóm bảo mật sử dụng nhật ký để thực hiện phân tích nguyên nhân gốc rễ của sự cố.

3. Troubleshooting: Vì nhật ký cũng ghi lại lỗi trong hệ thống hoặc ứng dụng nên có thể được sử dụng để chẩn đoán sự cố và hữu ích trong việc khắc phục chúng.

4. Performance Monitoring: Nhật ký cũng có thể cung cấp thông tin chi tiết có giá trị về hiệu suất của ứng dụng/ thiết bị.

5. Auditing and Compliance: Nhật ký đóng vai trò quan trọng trong Kiểm toán và Tuân thủ, giúp dễ dàng hơn trong việc thiết lập dấu vết của nhiều loại hoạt động khác nhau.

**Types of Logs**

Hãy tưởng tượng bạn phải điều tra một vấn đề trong hệ thống thông qua nhật ký; bạn mở tệp nhật ký của hệ thống đó và bây giờ bạn bị lạc sau khi thấy nhiều sự kiện thuộc nhiều danh mục khác nhau. Thật khó để dò ra thứ gì mình cần nắm bắt để điều tra, may mắn thay Logs được lưu trữ tách biệt dưới nhiều chủng loại, vì vậy khi bạn cần tìm chúng, bạn chỉ cần dò ra đúng những dữ liệu liên quan tới vấn đề bạn điều tra.

Logs có thể có những dạng sau:
(SSAANA)

1. System Logs: Có thể hữu ích trong việc khắc phục sự cố đang chạy trong hệ điều hành . Các nhật ký này cung cấp thông tin về các hoạt động khác nhau của hệ điều hành.

2. Security Logs: Nhật ký bảo mật giúp phát hiện và điều tra các sự cố. Các nhật ký này cung cấp thông tin về các hoạt động liên quan đến bảo mật trong hệ thống.

3. Application Logs: Chứa các sự kiện cụ thể liên quan đến ứng dụng. Bất kỳ hoạt động tương tác hoặc không tương tác nào xảy ra bên trong ứng dụng sẽ được ghi lại ở đây.

4. Audit Logs: Cung cấp thông tin chi tiết về các thay đổi của hệ thống và sự kiện của người dùng. Các nhật ký này hữu ích cho các yêu cầu tuân thủ và cũng có thể đóng vai trò quan trọng trong việc giám sát bảo mật.

5. Network Logs: Nhật ký mạng cung cấp thông tin về lưu lượng truy cập ra và vào của mạng. Chúng đóng vai trò quan trọng trong việc khắc phục sự cố mạng và cũng có thể hữu ích trong quá trình điều tra sự cố.

6. Access Logs: Nhật ký truy cập cung cấp thông tin chi tiết về quyền truy cập vào các tài nguyên khác nhau. Các tài nguyên này có thể có nhiều loại khác nhau, cung cấp cho chúng ta thông tin về quyền truy cập của chúng.

**Có thể có nhiều loại nhật ký khác nhau tùy thuộc vào các ứng dụng và dịch vụ mà chúng cung cấp.*

**Windows Event Logs Analysis**

Giống như các hệ điều hành khác, Windows OS cũng ghi lại nhiều hoạt động diễn ra. 

Chúng được lưu trữ trong các tệp nhật ký tách biệt, mỗi tệp có một danh mục nhật ký cụ thể. Một số loại nhật ký quan trọng được lưu trữ trong Hệ điều hành Windows là:

Application: Bất kỳ thông tin nào liên quan đến các ứng dụng(application)đều được ghi vào tệp này. Thông tin này bao gồm lỗi, cảnh báo, sự cố tương thích, v.v.

System: Bản thân hệ điều hành có các hoạt động chạy khác nhau. Bất kỳ thông tin nào liên quan đến các hoạt động này đều được ghi vào tệp nhật ký Hệ thống. Thông tin này bao gồm các sự cố trình điều khiển(driver issues), sự cố phần cứng(hardware issues), thông tin khởi động và tắt hệ thống(system startup/shutdown information), thông tin dịch vụ(services information), v.v.

Security: là tệp nhật ký quan trọng nhất trong hệ điều hành Windows về mặt bảo mật. Tệp này ghi lại tất cả các hoạt động liên quan đến bảo mật, bao gồm xác thực người dùng, thay đổi trong tài khoản người dùng, thay đổi chính sách bảo mật, v.v.

Bên cạnh đó, một số tệp nhật ký khác trong hệ điều hành Windows được thiết kế để ghi lại các hoạt động liên quan đến các hành động và ứng dụng cụ thể.

Không giống như các tệp nhật ký khác được nghiên cứu trong các tác vụ trước, không có ứng dụng tích hợp nào để xem chúng, hệ điều hành Windows có một tiện ích được gọi là Event Viewer(eventvwr.msc), cung cấp giao diện người dùng đồ họa đẹp mắt để xem và tìm kiếm bất kỳ nội dung nào trong các nhật ký này.

4624	A user account successfully logged in
4625	A user account failed to login
4634	A user account successfully logged off
4720	A user account was created
4724	An attempt was made to reset an account’s password
4722	A user account was enabled
4725	A user account was disabled
4726	A user account was deleted

**Web Server Access Logs Analysis**

Chúng ta tương tác với nhiều trang web hàng ngày. Đôi khi, chúng ta chỉ muốn xem trang web, và đôi khi, chúng ta muốn đăng nhập hoặc tải tệp lên bất kỳ trường nhập liệu nào có sẵn. Tất cả các yêu cầu này đều được trang web ghi lại và lưu trữ trong tệp nhật ký trên máy chủ web đang chạy trang web đó.

Ví dụ như tệp nhật ký này chứa tất cả các yêu cầu được thực hiện đối với trang web cùng với thông tin về khung thời gian, IP được yêu cầu, loại yêu cầu và URL. Sau đây là các trường được lấy từ một bản ghi mẫu từ tệp nhật ký truy cập máy chủ web Apache có thể được tìm thấy trong thư mục:

**/var/log/apache2/access.log**

Trong này sẽ có IP address, Timestamp, Request(http method, url), status code, và User-agent.

Hầu hết các hệ thống đều xoay vòng nhật ký thường xuyên. Việc xoay vòng này giúp chúng tạo các tệp nhật ký riêng lẻ cho các khung thời gian cụ thể và không mang tất cả chúng trong một tệp nhật ký duy nhất. Nhưng đôi khi, chúng ta có thể cần kết hợp hai tệp nhật ký. Tiện ích dòng lệnh cat cũng có thể hữu ích trong trường hợp này.

vd : **cat access1.log access2.log > combined_access.log**

Ngoài ra, còn | Grep, less, có thể giúp truy vấn dữ liệu từ log hiệu quả hơn.





