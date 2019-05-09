Quản lý công ty

Yêu cầu: Tạo một hệ thống phân cấp các lớp - lớp trừu tượng Employee và các lớp con HourlyEmployee, SalariedEmployee, Manager và Executive. Mỗi người trả tiền được tính khác nhau, nghiên cứu một chút về nó. Sau khi bạn đã thiết lập hệ thống phân cấp nhân viên, hãy tạo một lớp Company cho phép bạn quản lý nhân viên. Bạn sẽ có thể thuê, sa thải và nâng cao nhân viên.
Bài tập này e sử dụng ngôn ngữ C#

B1: Đầu tiên ta tạo class Employee(lớp này là lớp trừu tượng có nghĩa là ko khởi tạo được đối tượng ở lớp này nhưng cho phép thừa kế tạo ra các lớp con HourlyEmployee, SalariedEmployee, Manager và Executive.

B2: Tiếp đến khai báo các biến LoaiNhanVien, Ten, ThuNhap, NgayThue, TinhLuong, NangCao. Tiếp tục tạo lớp con HourlyEmployee được kế thừa từ lớp Employee, lớp con SalariedEmployee được kế thừa từ lớp HourlyEmployee, lớp con Manager được kế thừa từ lớp SalariedEmployee, lớp con Executive được kế thừa từ lớp Manager(từ khóa Selead kế thừa từ 1 class nhưng ko cho lớp nào đó kế thừa từ nó). 

-Đối với class HourlyEmployee: Khai báo hàm dựng Constructor(khai báo các biến EmployeeName(tên nhân viên), HourlyIncome(thu nhập hằng giờ), NewEmployeeType), tiếp tục tạo phương thức trừu tượng, tính lương = tổng số giờ làm* thu nhập, khai báo phương thức raise(nâng cao nhân viên)

- Đối với class SalariedEmployee: tương tự cũng khởi tạo Constructor và khai báo các biến EmployeeName, MonthlyIncome, NewEmployeeType, tính lương = tổng số ngày * thu nhập, khai báo phương thức raise(nâng cao nhân viên)

-Đối với class Manager: tương tự cũng khai báo các biến( EmployeeName, MonthlyIncome(thu nhập hàng tháng), HesotangQuanly, NewEmployeeType), tính lương = MonthlyIncome * HesotangQuanly, khai báo phương thức raise(nâng cao nhân viên)

-Đối với class Executive: khai báo các biến(EmployeeName, MonthlyIncome, HesotangDieuhanh), tính lương = MonthlyIncome * HesotangDieuhanh, , khai báo phương thức raise(nâng cao nhân viên)

B3: Tiếp tục tạo class Company để quản lý nhân viên trong công ty
-Khai báo các biến Readonly BasicMonthlyIncome, BasicHourlyIncome có thể được sử dụng như là các hằng số khi thực thi, tiếp tục khai báo phương thức Company(các biến CompanyMonthlyIncome, CompanyHourlyIncome)

-Khai báo phương thức thuê nhân viên:khai báo các biến,tìm kiếm nhân viên đang làm việc trong danh sách công ty
Nếu thu nhập mới = 0 đúng thì thu nhập mới sẽ tính = nếu loại nhân viên trả bằng giờ đúng thì sẽ tính thu nhập cơ bản hằng giờ, nếu ko thì trả về thu nhập hằng tháng 

Sử dụng cấu trúc rẻ nhánh switch case với biểu thức là LoaiNhanVien trả về kết quả là chuỗi, và case là các giá trị của TheLoaiNhanVien, Duyệt lần lượt từ trên xuống dưới và kiểm tra xem giá trị của <LoaiNhanVien> có bằng với <giá trị thứ i> đang xét hay không. Nếu bằng thì thực hiện <câu lệnh thứ i> tương ứng. Nếu không bằng tất cả các <giá trị thứ i> thì sẽ thực hiện<câu lệnh mặc định>. Ném ra ngoại lệ

-Khai báo phương thức sa thải: khai báo các biến và tìm các nhân viên đang làm việc trong công ty, duyệt hết danh sách nhân viên trùng tên với type  thì xóa khỏi list

-Khai báo phương thức nâng cao: tương tự cũng duyệt hết danh sách nhân viên cũng kiểm tra tên với type trùng thì raise lên

-Khai báo phương thức hiển thị thông tin nhân viên: sử dụng hàm foreach để tìm nhân viên đang làm việc trong danh sách nhân viên của công ty, in ra tên nhân viên + chức vụ + bảng lương của họ

B4: tạo class Program để hiển thị chi tiết thông tin nhân viên


