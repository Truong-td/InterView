1. Có bao nhiêu loại join
    - inner join : là trả về tất cả các record có ở 2 bảng thoả mãn điều kiện join
    - outer join
        + left outer join : trả về data của bảng bên trái và các record của bảng bên phải thoả mãn điều kiện
        + right outer join: trả về data của bảng bên phải và các record của bảng bên trái thoả mãn điều kiện
        + full outer join: trả về mọi bản ghi ở bảng bên trái và bảng bên phải
    - cross join: là tích đề các, các bản ghi từ 2 bảng trở lên. Cách hoạt động là bảng A có n bản ghi kết hợp với M bản ghi
   trong bảng B => n*m bản ghi
      
2. Sự khác nhau giữa MySQL và PostgreSql
   - Mysql là hệ thống quản lý cơ sở dữ liệu quan hệ, Còn PostgreSQL là quản lý cơ sở dữ liệu theo đối tượng
   - Mysql là sản phẩm của Oracle, còn PostgreSql là của tập đoàn toàn cầu thế giới
   
3. Sự khác nhau giữa Mysql và oracle
   - Hệ điều hành
      - Mysql hỗ trợ hầu hết tất các hệ điều hành, còn Oracle chỉ hỗ các HĐH phổ biến; Window, linux, unix, os
   -
   
4. Các cách optimize và turning SQL
   - Sử dụng tool excution plan để đo đạt các thông số như : Index, Cost, time, data
   - sử dụng index
      + Nên đánh index ở các cột được dùng trong mệnh đề WHERE VÀ ORDERBY
      + Không nên đánh index các trường thường xuyên được UPDATE HOẶC INSERT
   - Chỉ lấy ra những giá trị cần thiết, hạn chế select *
   - Hạn chế sử dụng bảng tạm để truy vấn.Vì:
      + Trong các hệ quản trị cơ sở dữ liệu SQL, bảng tạm sẽ được coi như bảng bình thường và nó được lưu trong RAM, 
         khi bộ nhớ RAM hết không thể chứa các bảng tạm thì các bảng tạm sẽ chuyển vào ổ cứng gây ra tốc độ truy vấn sẽ bị chậm
        
   - Sử dụng View/Store Procedure

5. Store Procedure với Function khác gì nhau
   - Function thì chỉ trả về 1 kết quả duy nhất, còn SP trả về Zero, một hoặc nhiều kết quả
   - SP thì chỉ có tham số đầu ra, còn Function thì có cả tham số đầu vào và tham số đầu ra
   - SP không thể gọi 1 function, còn 1 Function thì có thể gọi 1 SP
   - SP thì không thể gọi trong câu lệnh Select, ở điều kiện Where/HAVING
   
6. Store Procedure và Trigger khác gì nhau
   - SP là những câu lệnh SQL dùng để thực hiện một nhiêm vụ nhất định khi được gọi
   - Trigger là một SP được tự động chạy dựa trên những sự kiện được đăng ký, khi mà các sự kiện này xảy ra trong db thì trigger sẽ chạy
   - Trigger thì không có giá trị trả về còn SP thì có
   - Trigger thì không thể gọi 1 trigger khác, còn SP thì gọi được 1 SP khác
   
7. View
   - View là gì
   - View là một bảng ảo dựa trên kết quả truy vấn của câu lệnh Sql, Viw chỉ cho phép đọc dữ liệu ra , chứ không
   cho phép insert/update dữ liệu
   - View được tạo ra khi nào
   - View được tạo ra khi bạn muốn tập trung các data nhất định
   - Đơn giản hoá việc xử lý dữ liệu
   - Customize data
   