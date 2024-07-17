1. Api cần được tối ưu
/dr/common/drjoy_info_list
2. Bối cảnh
Api này lấy dữ liệu từ các collection với các thông tin như sau:
1. drjoy_info
Tổng các document là ~ 4 nghìn document. Trong mỗi document thì có mảng officeIds. Mảng này data có thể lên tới hơn 20.0000 office id trong mảng.
2. drjoy_info_unreads
Tổng các document là ~ 7 triệu document. Query trong bảng này với đầu vào là drjoyInfoId và officeUserId.

3. Thời gian xử lý cho 1 request với từ khóa tìm kiếm là drjoy_info#officeIds chứa officeId trên là thỏa mãn trên máy tính window với cấu hình như sau:
CPU: Core i7-9700
RAM: 32GB
Tool test performance: Jmeter
Thời gian xử lý 1 request trung bình là ~ 500ms
4. Thời gian xử lý cho 100 request đồng thời với cấu hình như trên là ~ 31s

3. Tìm nguyên nhân vấn đề
1. Điều tra code
Sau khi điều tra có hai vấn đề nhóm ae nhận thấy rõ:
1. DrjoyInfo#officeIds và DrjoyInfo#createdAt (tìm kiếm theo officeId và sort theo createdAt) chưa được đánh index.
2. Query trong vòng lặp for vào collection drjoy_info_unreads với đầu vào là drjoyInfoId và officeUserId trong khi collection này có khoảng hơn 7 triệu document.
3. Api response chỉ cần các field là id, title, content, createdAt.

2. Điều tra các vấn đề khác
Không thấy có bất thường.

4. Thực hiện tối ưu
1. Đánh index cho mảng DrjoyInfo#officeIds và DrjoyInfo#createdAt
2. Thực hiện query một lần vào drjoy_info_unreads sau đó convert sang Set hoặc Map để dùng method contain (Những method này có độ phức tạp là O(1))
3. Chỉ include các field cần thiết là id, title, content, createdAt khi query ra.

5. Đo kết quả
1. Thời gian thực hiện api giảm 10 lần.