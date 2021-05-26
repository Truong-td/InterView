1. What is the difference between @Inject and @Autowired in Spring Framework? Which one to use under what condition?
    - Inject là một tiêu chuẩn Java CDI(Context and Dependency Injection), còn Autowire thì thể hiện riêng của Spring Framework
    
2. Anotation @Qualifier và Primary trong Spring là gì ?? sự khác nhau
    - Qualifier là chỉ định rõ bean nào được sử dụng trong khi có nhiều bean cùng kiểu dữ liệu, cũng là thể hiện của singleton pattern ở đây
    - Primary là chỉ định rõ bean nào được sử dung khi có nhiều 1 bean trong spring container
    
3. Sự khác nhau giữa context:annotation-config với context:component-scan
    - context:component-config: sẽ hỗ trợ việc tìm kiếm và kích hoạt các anotation bên trong bean đã được đăng ký trong application context
    - context:component-scan: hỗ trợ thực hiện tất cả các nhiệm vụ mà context:component-config thực hiện, nhưng context:component-scan
      còn hỗ trợ scan các package để tìm và đăng ký các bean vào appplication context.
      
4. Các anotation @Component, @Service, @Controller, @Repository Khác nhau
   - @Component là dùng để đánh dấu class đó là 1 bean 
   - @Service đánh dấu class thuộc tầng service
   - @Controller đánh dấu class thuộc tầng controller
   - @Repository đánh dấu class thuộc tầng Repository
   
5 Vòng đời của Spring container như thế nào
   - IOC Container tìm thấy bean cần quản lý thì sẽ khởi tạo Contructor
   - Sau đó inject bean bằng Setter
   - Đánh dấu hàm PostContructor
   - Tiến hành xử lý trong PostContructor được gọi
   - Bean sẵn sàng hoạt động
   - Nếu IOC Container không quản lý bean thí bean sẽ desrtoy
   - Xoá bean
6. Spring IOC là gì ?? Nguyên lý hoạt động của IOC
   - IOC là quá trình đảo ngược, giúp thay đổi luồng điều kiện, giúp cho chương trình trở nên linh hoạt hơn
   - IOC hoạt động dựa trên IOC Container, IOC container sẽ tạo ra các đối tượng lắp ráp lại với nhau, cấu hình các đối tượng và
   quản lý vong đời của chúng từ lúc tạo ra đến khi kết thúc
   - Spring Container là dùng DI để quản lý các đối tượng, các đối tượng này gọi là spring bean

7. Spring MVC hoạt động như thế nào??
   - Step 1: Sau khi nhận request từ HTTP, thì Dispastcher Serverlet  sẽ gọi HttpMapping để xác định xem Controller
   nào xử lý không
   - Step 2 Sau khi xác nhận có Controller sẽ xử lý thì HttpMapping sẽ gửi request đến Controller đó
   - Step 3 Sau khi xử lý trong controller xong,thì controller sẽ thông quan ModelAndView trả về Dispastcher
   - Step 4 Dispastcher   sẽ tìm View thông qua ViewResolver
   - Step 5 sau khi tìm xong View thì Thì Dispastcher sẽ trả model vừa nhận được sau khi xử lý nghiệp vụ

8. AOP là gì ? Cho ví dụ minh hoạ
   - AOP là lập một phương pháp lâp trình hướng khía cạnh, là một kỹ thuật lập trình nhắm phân tách chương trình thành những
   module riêng biệt, không phụ thuộc vào nhau.
   - Ví dụ:
   - Việc viêt code log trong mỗi method, thì chúng ta thấy rằng việc Viết Log này không ảnh hưởng gì đến module đang chạy cả
   
