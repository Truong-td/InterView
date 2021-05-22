JAVA CORE
SQL
    1. Sự khác nhau giữa Store Proceduce và Function
        - SP thì lưu trữ giá trị trả về là zero, một hoặc nhiều giá trị. Trong khi đó function chỉ trả vê duy nhất 1 giá trị
        - SP thì có tham số đầu vào và đâu ra còn function thì chỉ có tham số đầu vào.
        - Function có thể được gọi từ SP, còn SP thì không thể được gọi từ function
        - SP thì không thể gọi trong câu lệnh Select, ở điều kiện Where/HAVING
        - Transactions có thể được sử dụng trong SP, còn function thì không
    2. Sự khác nhau giữa Store Proceduce và Trigger
        - SP là những câu lệnh SQL dùng để thực thi nhiệm vụ nhất định, Nó được xem như 1 hàm trong các ngôn ngữ lập trình khác
        - Trigger là một store procedure được tự động chạy dựa trên những sự kiện mà nó được đăng ký Khi các sự kiện này xảy ra trong database, thì nó cũng sẽ được thực thi.
        - Trigger sẽ tự động thực thi khi các có sự kiện CRUD xảy ra, còn SP thì khi được gọi thì mới thực thi
        - Trigger không thể gọi 1 triiger khác, còn SP thì được 
        - Trigger không có giá trị trả về hoặc tham số đầu vào còn SP thì có 