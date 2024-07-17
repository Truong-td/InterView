Bài toán 1 :

Có rất nhiều services xử lý nghiệp vụ, sau khi xử lý nghiệp vụ xong thì cách lưu dữ liệu lớn vào db như thế nào để DB có thể chịu tải được 

OUTPUT:
	+ Cần giảm thông số TPS(Transaction processing systems) xuống .
	
Phương án đề ra có 2 phương án:
	1. Khi các service xử lý dữ liệu xong thì sẽ ==> Dựng 1 con Kafka ở giữa trước khi đẩy vào DB
		+ ƯU điểm: đáp ứng được yêu cầu là giảm TPS xuống
		+ Nhược điểm : chi phí dùng cho kafka sẽ cao hơn
	
	2. Dùng phương pháp chia để trị
		+ Sau khi xử lý thông tin ở tầng service  => thì chúng ta đẩy dữ liệu vào file => giới hạn số lượng bản ghi vào file
			Ví dụ: 1 service có 10.000.000 bản ghi muốn ghi cùng 1 lúc => 1 file chúng ta chứa 1.000.000 bản ghi ==> Tạo ra 10 luồng song song đọc và ghi data xuống DB
			
		+ ưu điểm: 
			đáp ứng được yêu cầu là giảm TPS xuống
			+ Chi phí thấp
			
		+ Nhược điểm:
			+ Khó kiểm soát đa luồng, dễ xảy ra việc bị sai dữ liệu nếu không kiểm soát việc xử lý đa luồng tốt (Gợi ý: Dùng Threadpool)
			

Bài toán 2:
	Có 2 servie thực hiện trừ tiền cùng 1 thời điểm => Làm thế nào để trừ tiền đúng hay nói cách khác là làm thế nào để xử lý việc trừ tiền của hai service này tuần tự
	
	Keyword: Dùng isolate architecture


Bài toán 3:
	- Việc tổng hợp các dữ liệu từ nhiều services khác nhau thì sẽ xử lý thế nào trong hệ thống và download nhiều báo cáo xuống
	- Ví dụ: 2 tháng xuất báo cáo dữ liệu tháng
	- Solution: Dựng 1 con job batch để đi tổng hợp dữ liệu từ nhiều service rồi để vào 1 chỗ, cuối tháng chỉ việc xuất báo cáo ra


Bài toán thứ 4: Liên quan đến GetWays
	- Cả webapp và mobile app cùng gọi 1 cái api Nhưng WEB thì cần lấy lượng dữ liệu A, còn mobile cần lấy dữ liệu B
	- Solution:
		- sử dụng pattern Backend and Front-End
		- Điểm mạnh của giải pháp này là: tránh việc nhập nhằng config giữa web và app, Cũng như là dễ cho việc maintain
		- Điểm hạn chế: Thì mất nhiều resource cho Developer dựng API cho từng nên tảng
Bài toán 5: 
	- Service Discovery : Để check xem các service có tồn tại hay không

QUẢN LÝ DỮ LIỆU TRONG MICROSERVICES

Rủi ro Khi đối ứng ngay cho đợt 19/04
1. Sẽ ảnh hưởng đến cả luồng show số tiền hiện tại của user đã và đang mua gói lite plan
2. Phát sinh nhiều bug và không thể fix kịp cho release 19/04
3. Thời gian test không đủ để kịp cho ngày 19.04

 https://redmine.famishare.jp/issues/141377: 
