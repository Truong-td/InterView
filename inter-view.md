Java Interview Questions- Đề Cương chuẩn bị cho phỏng vấn với doanh nghiệp
1. Sự khác nhau giữa JDK,JRE và JVM?
   JVM
   JVM (viết tắt của Java Virtual Machine) là một thiết bị trừu tượng (ảo) có thể giúp máy tính chạy các chương trình Java.
   Nó cung cấp môi trường runtime mà trong đó Java Bytecode có thể được thực thi.

JRE
JRE (là viết tắt của Java Runtime Environment) được sử dụng để cung cấp môi trường runtime. Nó là trình triển khai của JVM. 
JRE bao gồm tập hợp các thư viện và các file khác mà JVM sử dụng tại runtime. 
Trình triển khai của JVM cũng được công bố bởi các công ty khác ngoài Sun Micro Systems.

JDK
JDK (là viết tắt của Java Development Kit) bao gồm JRE và các Development Tool.
1. Lập trình hướng đối tượng là gì?
    - Là phân tích bài toàn thành các đối tượng, trong đó các đối tượng bao gồm thuộc tính và phương thức.
    
2. Các tính chất của lập trình hướng đối tượng trong Java? 
    - Lập trình hướng đối tượng bao gồm 4 tính chất
        + Tính kế thừa: là sự liên quan giữa 2 class với nhau, trong đó lớp con kế thừa phương thức và thuộc tính của lớp cha
        + Tính đóng gói: là kỹ thuật ẩn giấu thông tin không liên quan, mục đích chính là giảm thiểu độ phức tạp của phát triển
        + Tính trừu tượng: một tiến trình ẩn các chi tiết trình triển khai và chỉ hiển thị tính năng tới người dùng
        + Tính đa hình : Là khả năng một đối tượng có thể thực hiện nhiều tác vụ theo nhiều cách khác nhau
            Tính đa hình được thể hiện qua phương thức nạp chồng và phương thức ghi đè
            + Phương thức nạp chồng - Overloading: là khả năng trong 1 class có nhiều phương thức cùng tên nhưng khác tham số hoặc các 
                tham số có kiểu dữ liệu khác nhau
            + Phương thức nạp chồng thể hiện tính đa hình khi complie
            + Phương thức ghi đè - Overriding: là phương thức được kế thừa từ lớp cha. Được thể hiện tính đa hình khi runtime
3. Hỏi về collection Framework (Cái này hầu như 100% ở đâu phỏng vấn cũng hỏi)
   3.1 ArrayList là gì ? Khi nào dùng ArrayList
        - ArrayList: là mảng động, ArrayList dùng khi lưu trữ dữ liệu và lấy dữ liệu
   3.2 LinkedList là gì ? Khi nào dùng Linkedlist
        - LinkedList: là danh sách liên kết, LinkedList sừ dụng khi muốn thao tác với dữ liệu nhiều: insert, delete, tìm kiếm
   3.3 Vector là gì ? Khi nào dùng Vector?
        - Vector
   3.4 Stack hoạt đông như thế nào ? Khi nào dùng Stack
        - Stack hoạt động theo cơ chế LIFO(Last in First out) Vào trước ra sau0. 
        - Stack được sử dụng khi 
   3.5 ArrayList với Vector khác nhau thế nào:
        - ArrayList không có cơ chế đồng bộ, còn Vector thì có
        - ArrayList khi muốn mở rộng thì chỉ mở rộng được 50% kích thước mảng, còn Vector thì có thể tăng gấp đôi
   3.6 Sự khác nhau giữa List và Set
        - List thì được dupplicate giá trị, còn Set thì không
   3.7 Sự khác nhau giữa ArrayList và LinkedList
        - ArrayList là mảng động, còn LinkedList là danh sách liên kết
        - ArrayList phù hợp cho việc lưu trữ và lấy ra data, còn LinkedList thì phù hợp với data phải thao tác nhiều: updated, remove, tìm kiếm
        - Vì ArrayList thì sẽ cấp phát bộ nhớ động và có địa chỉ ô nhớ gần nhau, khi mà add thêm phần tử thì sẽ duyệt 1 lượt xem ô nhớ có đủ không
            LinkList thì dùng đến đâu cấp đến đấy 
   3.8 sự khác nhau giữa List và ArrayList
        - List là một kiểu collection và là Interface dành cho danh sách
        - ArrayList là một mảng động, là một lớp thực thể implement lại List
   3.9 Tại sao Set không thể duplicate
        - 
3.8 Sự khác nhau giữa Map và Set
        - Set chỉ chứa giá trị, còn Map thì chứa key và value
   3.9 Sự khác nhau giữa HashSet và TreeSet
        - HashSet thì phần tử bên trong thì chưa được sắp xếp, còn TreeSet thì đã được sắp xếp theo thứ tự tăng dần
   4.0 Sự khác nhau giữa HasMap và TreeMap
        - HashMap thì các phần tử chưa được sắp xếp, còn TreeMap thì đã được sắp xếp theo thứ tự tăng dần
   4.1 Sự khác nhau giữa HashMap và HashTable
        - HashMap thì chỉ không có cơ chế đồng bộ, còn HashTable thì có
        - HashMap thì có được lưu giá trị null còn HashTable thì không
JAVA SPRING
   1. RequestMapping là gì ??
        - RequestMapping là một anotation để map các request với class hoặc method được gửi lên từ client
   2. Phương thức Post và Get khác nhau thế nào
        - Method Post: không được cache trên trình duyệt, còn Get thì có
        - Post thì sẽ thực hiện gửi ngầm dữ liệu lên server và không xuất hiện các dữ liệu bảo mật trên url
       - Post sẽ không giới hạn data gửi lên server, còn Get thì sẽ bị giới hạn số lượng param gửi đi (best practice: tối đa 2048 ký tự )
   3. Truyền dữ liệu từ Controller qua View bằng gì?
        - Bằng Dispaster serverlet
   4. Spring MVC hoạt động như thế nào??
        - Step 1: Sau khi nhận request từ HTTP, thì Dispastcher Serverlet  sẽ gọi HttpMapping để xác định xem Controller 
          nào xử lý không
        - Step 2 Sau khi xác nhận có Controller sẽ xử lý thì HttpMapping sẽ gửi request đến Controller đó
        - Step 3 Sau khi xử lý trong controller xong,thì controller sẽ thông quan ModelAndView trả về Dispastcher
        - Step 4 Dispastcher   sẽ tìm View thông qua ViewResolver
        - Step 5 sau khi tìm xong View thì Thì Dispastcher sẽ trả model vừa nhận được sau khi xử lý nghiệp vụ
   5. Spring IOC là gì ?? Nguyên lý hoạt động của IOC
        - IOC là quá trình đảo ngược, giúp thay đổi luồng điều kiện, giúp cho chương trình trở nên linh hoạt hơn
        - IOC hoạt động dựa trên IOC Container, IOC container sẽ tạo ra các đối tượng lắp ráp lại với nhau, cấu hình các đối tượng và 
        quản lý vong đời của chúng từ lúc tạo ra đến khi kết thúc
        - Spring Container là dùng DI để quản lý các đối tượng, các đối tượng này gọi là spring bean
   6. Vòng đời của Spring Bean như thế nào ??
        - IOC Container tìm thấy bean cần quản lý thì sẽ khởi tạo Contructor
        - Sau đó inject bean bằng Setter 
        - Đánh dấu hàm PostContructor
        - Tiến hành xử lý trong PostContructor được gọi 
        - Bean sẵn sàng hoạt động
        - Nếu IOC Container không quản lý bean thí bean sẽ desrtoy
        - Xoá bean
   7. Khái niệm DI (dependency injection) trong spring boot là gì?, DIP là gì, Cho ví dụ minh hoạ
        - DI là một dạng thực hiện của IOC khi inject module này vào 1 module khác và nhằm loại bỏ việc hard-code, 
          dễ dàng cho việc mở rộng code
        - IOC là một design pattern nhắm thực hiện việc code sao cho tuân thủ nguyên tắc DIP(Dependence Inversion Price) trong OOP
        - Ví dụ: Khi một ứng dụng tương tác với nhiều loại db chẳng hạn, thì nếu không sử dụng DI thì chúng ta sẽ phải check khi 
          nào dùng loại db nào. Khi áp dụng kỹ thuật DI thì bài toán được giải quyết. 
          giải quyết là chúng ta tạo 1 abstract method rồi cho các đối tượng khác kế thừa lại abstraction method đó. 
          Vậy việc Thay thế AbstractionDao bắng các lớp Dao khác chính là kỹ thuật DI
        - DIP là một nguyên lý phát triển trong SOLID của OOP.
   8. AOP là gì ? Cho ví dụ minh hoạ
        - AOP là lập một phương pháp lâp trình hướng khía cạnh, là một kỹ thuật lập trình nhắm phân tách chương trình thành những 
        module riêng biệt, không phụ thuộc vào nhau.
        - Ví dụ: 
            - Việc viêt code log trong mỗi method, thì chúng ta thấy rằng việc Viết Log này không ảnh hưởng gì đến module đang chạy cả

JPA
    1. Giải thích JPA là gì ?
        - JPA (Java Persistence API) là 1 giao diện lập trình ứng dụng Java, nó mô tả cách quản lý các mối quan hệ dữ liệu  
        trong ứng dụng sử dụng Java Platform. 
        - JPA cung cấp một mô hình POJO persistence cho phép ánh xạ các table/các mối quan hệ giữa các table trong database 
        sang các class/mối quan hệ giữa các object.
        - Entity: Entity là các đối tượng thể hiện tương ứng 1 table trong cơ sở dữ liệu. 
        Khi lập trình, entity thường là các class POJO đơn giản, chỉ gồm các method getter, setter.
        - EntityManager: EntityManager là một giao diện (interface) cung cấp các API cho việc tương tác với các Entity 
        như Persist (lưu một đối tượng mới), merge (cập nhật một đối tượng), remove (xóa 1 đối tượng).
        - EntityManagerFactory: EntityManagerFactory được dùng để tạo ra một thể hiện của EntityManager.
              
HIBERNATE
    1. Hibernate là gì ORM Framework cho phép lập trình viên thao tác với database 

JPA VÀ HIBERNATE KHÁC GÌ NHAU: 
    - JPA là tập các các giao hiện của interface còn Hibernate thì implement lại các interface đó 

8. Webservice là gì ?
    - Web service (dịch vụ web) là tập hợp các giao thức và tiêu chuẩn mở được sử dụng để trao đổi dữ liệu giữa các ứng dụng 
      hoặc giữa các hệ thống.
      
9. Restful Webservice là gì ?
    - là các webservice được thiết kế theo kiến trúc Rest
    - Kiến trúc REST là bao gồm các method http 
        + GET - READ (getlist)
        + POST - create (addnew)
        + PUT - EDIT/UPDATE/REPLACE
        + PATCH - UPDATE/MODIFY
        + DELETE - Delete
11. Sự khác nhau giữa SOAP VÀ REST API
    - SOAP call service thông qua method RPC, còn REST chỉ gọi service thông giao đường dẫn URL
    - SOAP truyền data thông qua nhiều giao thức hơn, SMTP, HTTP, còn REST thì chỉ có HTTP
    - SOAP sẽ gặp khó khăn trong việc sử dụng JS để gọi, còn REST thì rất dễ dàng 
10. Sự khác nhau giữa Session và Cookie ?
    - Cookie: được lưu trên trình duyệt, còn Session thì không
    - Cookie thì được lưu bên phía client, còn session được lưu bên máy chủ

11. Cache là gì ???
    - là bộ nhớ lưu trữ dữ liệu tạm thời, các dữ liệu này sẽ mất đi khi restart

13. Mô hình MVC là gì ? Nhiệm vụ của M là gì , V là gì ,và C là gì ?
    - là kiến mẫu kiến trúc phổ biến được sử dụng để tạo cấu trúc cho nhiều ứng dụng
    - M là model, là nơi chỉ chứa nghiệp vụ logic, xử lý nghiệp vụ logic
    - V là View, là nơi giúp người dùng có thể nhìn thấy thông tin của website
    - C là Controller chính là điều khiển, điều hướng các yêu cầu / request từ người dùng 
      và chỉ định phương thức này, phương thức kia trong Model sẽ xử

14. DESIGN PATTERN
    - SINGLETON PATTERN: là một mẫu thiết kế, nhắm đảm bảo chỉ tồn tại một thể hiện trong JVM
        + Ví dụ : Khi tạo lớp enum, lớp connect với db
    - Factory Pattern:
        + là mẫu thiết kế được sử dụng khi có 1 lớp cha, với nhiều lớp con dựa trên đầu vào và phải trả về đối tượng lớp con đó 
        + Ưu điểm: dễ bảo trì, dễ mở rộng code, dễ đọc code
    - DI (Dependence Injection)
        + là một mẫu thiết kế giúp cho loại bỏ việc hard-code
    - Builder Pattern:    
        + là một mẫu thiết kế giúp cho việc xây dựng một đối tượng phức tạp bằng cách sử dụng các đối tượng đơn giản
15. SOLID:
    - Single responsibility principle: mỗi class chỉ giữ một trách nhiệm duy nhất
    - open/close principle: có thể mở rộng class, nhưng không được sửa đổi class đó
    - Liskov Substitution Principle: Class con có thể thay thế class cha, nhưng không làm thay đổi tính đúng đắn của chương trình
    - Interface Segregation Principle: Thay vì dùng 1 interface lớn, thì chúng ta tách ra làm các interface nhỏ 
    - Dependency inversion principle: Các module cấp cao không nên phụ thuộc vào các module cấp thấp 
            
DATABASE 
    1 Các loại join
        1. Inner Join là trả về các record data khi có 1 một sự phù hợp ở 2 bảng
        2. outer join là trả về tất cả các bản ghi đúng với 1 trong các bảng 
        3. left join là trả về các bản ghi từ bảng bên trái và các bản ghi đúng với điều kiện bảng bên phải
        4. right join là trả về các bản ghi từ bảng bên phải và các bản ghi đúng với điều kiện ở bảng bên trái
    2. Index :
        - Index là một cấu trúc dữ liệu được dùng để định vị và truy vấn dữ liệu nhanh nhất
        - Các loại index:
            - B-Tree Index: là cấu trúc dữ liệu dựa trên thuật toán Binery search là các giá trị đã được sắp xếp 
            tăng dần theo chiều từ trái sang phải
            - Hash Index: là cấu trúc dữ liệu dựa trên giải thuật HashMap, HashIndex sẽ dùng mảng băm để phần biệt
        - Khi nào thì dùng B-TREE và Hash
            - HASH INDEX nên được dùng trong các biểu thức toán tử là = hoặc <>
        - Dùng Index thế nào cho tối ưu
            + Nên đánh Index những cột được dùng trong where, OrderBy
            + Không nên đánh index cho các bảng thường xuyên update và insert
            + Không nên đánh index cột nào thường xuyên bị thay đổi
    3. Sự khác nhau giữa function và store procedure là gì ??
        - SP thì lưu trữ giá trị trả về là zero, một hoặc nhiều giá trị, còn function chỉ trả về 1 giá trị duy nhất
        - SP có tham số đầu vào và tham số đầu ra, còn function chỉ có tham số đầu vào 
        - SP không thể dùng được trong mệnh đề select, trong điều kiện where hoặc having.
        - SP không thể gọi 1 function, còn 1 function có thể gọi SP
    4. Sự khác nhau giữa SP và trigger
        - SP là những câu sql, nhằm thực thì một nhiệm vụ nhất định khi được gọi, còn trigger là một SP được tự động thực thi dựa trên
        điều kiện được đăng ký sẵn với database
        - Một trigger không thể gọi 1 trigger khác, còn SP thì có thể gọi 1 SP khác
        - Trigger thì không có giá trị trả về hoặc tham số đầu vào còn SP thì không
    3. View
        - View là gì
            - View là một bảng ảo dựa trên kết quả truy vấn của câu lệnh Sql, Viw chỉ cho phép đọc dữ liệu ra , chứ không
            cho phép insert/update dữ liệu
        - View được tạo ra khi nào
            - View được tạo ra khi bạn muốn tập trung các data nhất định
            - Đơn giản hoá việc xử lý dữ liệu 
            - Customize data

UNIT TEST
    1. Unit Test là gì ?
        - là  là một loại kiểm thử phần mềm trong đó các đơn vị hay thành phần riêng lẻ của phần mềm được kiểm thử. 
        Kiểm thử đơn vị được thực hiện trong quá trình phát triển ứng dụng. 
        Mục tiêu của Kiểm thử đơn vị là cô lập một phần code và xác minh tính chính xác của đơn vị đó.
    2. Sonarque có chức năng làm gì ?
        - là một nền tảng mã nguồn mở được phát triển bởi SonarSource để liên tục kiểm tra chất lượng code, 
        review tự động với việc phân tích code để phát hiện lỗi, đoạn code không tốt, hoặc lỗ hổng bảo mật trên 20 ngôn ngữ lập trình.

Luồng CI/CD
    Push code -> build code (compile, docker compose) -> test(smoke, unit test, intergation) -> Deploy

DOCKER:
    1. Docker là gì ?
        - Docker là một dự án mã nguồn mở giúp tự động triển khai các ứng dụng Linux và Windows vào trong các container ảo hóa.
    2. Lơi ích của Docker
        - Tiện lợi, nhanh chóng
        - Tiết kiệm tài nguyên
        - hệ thống có mức độ tự động mở rộng cao hơn
        - Dễ dàng tự động hoá việc quản lý các docker container
    3. Khi nào thì dùng docker
    4. Cách hoạt động của docker
        - Chỉ cần viết 1 dockerfile (một file text tổng hợp nhiều dòng lệnh) để tạo nên image,
        sau đó khởi chạy nó là đã tạo được một docker container. 
    5. Sự khác biệt giữa Docker và Hypervisors?
        - Hypervisors là một ứng dụng phần mềm chịu trách nhiệm chạy máy ảo trên hệ thống đồng thời phải cấp riêng cho nó một dung
        lượng ổ cứng và Ram nhất định
            + Hypervisors thì quá trình shutdown và start lâu hơn và cần tạo ra nhiều máy ảo với mỗi một loại os khác nhau
            + Docker thì việc shutdown và start nhanh hơn, và không cần tạo ra nhiều máy ảo đối với mỗi loại os
    6. Docker Image:
        - Docker Image là nền tảng của Container, giúp định hình được Container 
        - Để tạo ra một docker Image chúng ta sẽ tạo 1 dockerFile, trong docker file có chứa danh sách các câu lệnh
        giúp thiết lập cấu trúc cho image

    7. Docker Container
        - có thể hiểu rằng docker container là một máy ảo, được tạo ra bằng cách chạy docker image
        
SCRUM MASTER:
    1. Scrum là gì??
        - scrum là một khung làm việc để phát triển bền vững các sản phẩm phức tạp'. 
        Có thể hiểu đây là khung tổ chức công việc tổng quát hướng đến phát triển các sản phẩm phức tạp, chủ yếu là phần mềm