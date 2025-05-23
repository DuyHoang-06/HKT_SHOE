# Ứng dụng quản lý cửa hàng bán giày (HKT SHOE SHOP)
(#github)

Ứng dụng giúp bạn quản lý việc nhập hàng/bán hàng của cửa hàng giày và dữ liệu được lưu trữ trong file xml (sanpham.xml và banhang.xml), ảnh sẽ được lưu ở thư mục pic.

## Bài Tập Giữa Phần:
Phát triển ứng dụng Quản lý shop giày, yêu cầu: 
- Nhập hàng;
- Bán hàng;
- Thống kê;
- Tìm kiếm. Trong đó phần Tìm kiếm cần trả về cả hình ảnh giày dép.

## Mô tả ứng dụng
### 1. Tên ứng dụng:
Ứng dụng quản lý cửa hàng bán giày (HKT SHOE SHOP)

### 2. Login
- Tên đăng nhập: admin
- Mật khẩu: admin

### 3. Chức năng và các trường thông tin:
- Đối với cửa sổ Nhập hàng:
	* Các trường thông tin:
	+ Trường Mã sản phẩm: có kiểu dữ liệu String; các sản phẩm khác nhau không được trùng Mã sản phẩm với nhau và sẽ thông báo lỗi khi người dùng nhập trùng; không được để trống.
	+ Trường Tên sản phẩm: có kiểu dữ liệu String, các sản phẩm khác nhau không được trùng Tên sản phẩm với nhau và sẽ thông báo lỗi khi người dùng nhập trùng; không được để trống.
	+ Trường Ngày nhập: có kiểu dữ liệu Date; là một JDateChoose để người dùng lựa chọn ngày; không được để trống.
	+ Trường Loại sản phẩm: hiển thị một JComboBox để người dùng lựa chọn loại sản phẩm (hãng giày).
	+ Trường Số lượng: có kiểu dữ liệu int, để nhập số lượng (số đôi giày) được nhập vào kho; không được để trống.
	+ Trường Giá nhập: có kiểu dữ liệu int, để nhập giá nhập của sản phẩm (...nghìn/đôi giày); không được để trống.
	+ Trường Ảnh minh họa: là một Jlable, có chức năng hiển thị ảnh khi người dùng chọn; không được để trống.
	* Các chức năng:
	+ Nhập hàng (thêm sản phẩm vào kho hàng), sửa, xóa các sản phẩm trong kho hàng.
	+ Sắp xếp theo các tiêu chí trực tiếp trên bảng thống kê (nhấn vào trực tiếp các tiêu đề trên bảng thống kê).
	+ Làm mới: đưa các trường thông tin hiển thị về mặc định.

- Đối với cửa sổ Bán hàng:
	* Các trường thông tin:
	+ Trường Mã sản phẩm: có kiểu dữ liệu String; dùng để nhập mã sản phẩm cần bán, phải nhập đúng mã nếu sai sẽ thông báo lỗi hoặc người dùng có thể nhấn vào sản phẩm trên kho hàng mã sẽ tự động được điền; không được để trống.
	+ Trường Số lượng bán: có kiểu dữ liệu int, để nhập số lượng (số đôi giày) được bán, không được nhập vượt quá số lượng trong kho, nếu vượt sẽ báo lỗi; không được để trống.
	+ Trường Giá bán: có kiểu dữ liệu int, để nhập giá bán của sản phẩm (...nghìn/đôi giày); không được để trống.
	* Các chức năng:
	+ Bán hàng (thêm sản phẩm vào vào đơn hàng, xóa sản phẩm khỏi đơn hàng, hủy đơn hàng, thanh toán và trừ đi số lượng đã bán khỏi kho hàng).
	+ Sắp xếp theo các tiêu chí trực tiếp trên bảng thống kê (nhấn vào trực tiếp các tiêu đề trên bảng thống kê).
	+ Làm mới: đưa các trường thông tin hiển thị về mặc định.
	+ Tìm kiếm (trong kho hàng): gồm có tìm kiếm theo tên sản phẩm (tìm kiếm gần đúng), tìm kiếm theo giá (tìm kiếm theo khoảng, ví dụ: muốn tìm kiếm sản phẩm có giá tiền từ 100 nghìn đồng đến 200 nghìn đồng thì ta nhập 100-200 vào ô giá tiền). Trong đó phần khi Tìm kiếm sẽ trả về các thông tin nhập hàng của sản phẩm kể cả hình ảnh minh họa.
- Đối với cửa sổ Thống kê: 
	* Các trường thông tin:
	+ Trường Mã sản phẩm: có kiểu dữ liệu String; dùng để nhập mã sản phẩm cần thống kê; có thể để trống.
	+ Trường Loại sản phẩm: hiển thị một JComboBox để người dùng lựa chọn loại sản phẩm (hãng giày) cần thống kê; có thể để trống.
	+ Trường Từ ngày - Đến ngày: Có kiểu dữ liệu Date; là một JDateChoose để người dùng lựa chọn ngày để thống kê trong khoảng thời gian từ ngày... đén ngày...; mặc định thống kê từ ngày 01/1/2024 đến ngày hiện tại; người dùng có thể chọn lại ngày để thống kê theo mục đích của mình.

	* Các chức năng:
	+ Thống kê: Tính tổng số sản phẩm đã bán được, doanh thu và lợi nhuận của cửa hàng.
	+ Làm mới: đưa các trường thông tin hiển thị về mặc định.

### 4. Hướng dẫn sử dụng:
#### a. Tại màn hình Đăng nhập:
- Người dùng phải đăng nhập đúng tài khoản đã cung cấp để sử dụng. Để dễ dàng nhập mật khẩu người dùng có thể click vào biểu tượng hide hoặc unhide bên cạnh để ẩn hoặc hiện mật khẩu.
- Để đưa các trường thông tin hiển thị về mặc định, người dùng click chuột vào button Đặt lại.

#### b. Tại màn hình Lựa chọn:
- Người dùng sẽ chọn Nhập hàng, Bán hàng hoặc Thống kê theo mục đích của mình.
- Để thoát khỏi chương trình, người dùng có thể click chuột vào button Thoát hoặc close [X].

#### c. Tại màn hình Nhập hàng:
- Người dùng nhập, sửa, xóa các thông tin của sản phẩm theo các trường Mã sản phẩm, Tên sản phẩm, Ngày nhập, Loại sản phẩm, Số lượng, Giá nhập, Ảnh minh họa.
- Để thao tác thêm / sửa / xóa được thực hiện thì người dùng click chuột vào các button tương ứng Nhập hàng, Sửa, Xóa tương ứng tùy theo mục đích.
- Trong bảng kho hàng, người dùng có thể click chuột vào hàng chứa thông tin của sản phẩm để lấy và hiện thị theo các trường tương ứng trong mục Nhập hàng. Người dùng có thể tiếp tục thực hiện các thao tác với các sản phẩm.
- Để đưa các trường thông tin hiển thị về mặc định, người dùng click chuột vào button Làm mới.
- Để quay lại màn hình lựa chọn, người dùng click chuột vào button Quay lại.
- Để thoát khỏi chương trình, người dùng có thể click chuột vào button Thoát hoặc close [X].

#### d. Tại màn hình Bán hàng:
- Người dùng nhập các thông tin của sản phẩm cần bán theo các trường Mã sản phẩm (Người dùng có thể nhập thủ công hoặc click vào sản phẩm trên kho hàng thì mã sản phẩm sẽ tự động được điền), Số lượng bán, Giá bán.
- Để thêm sản phẩm vào đơn hàng, người dùng click chuột vào button Thêm.
- Để xóa sản phẩm ra khỏi kho hàng, người dùng click chuột vào sản phẩm muốn xóa và click vào button Xóa.
- Tổng giá trị đơn hàng sẽ tự động được tính.
- Để Thanh toán đơn hàng (Bán hàng), người dùng click vào button Thanh toán.
- Muốn Hủy đơn hàng (Xóa đơn hàng), người dùng click vào button Hủy đơn hàng.
- Để đưa các trường thông tin hiển thị về mặc định, người dùng click chuột vào button Làm mới.
- Tại mục TÌM KIẾM:
	+ Để tìm kiếm theo Giá tiền, người dùng nhập vào theo đúng định dạng: ...nghìn đồng-...nghìn đồng (Ví dụ: muốn tìm kiếm sản phẩm có giá tiền từ 100 nghìn đồng đến 200 nghìn đồng thì ta nhập 100-200 vào ô giá tiền). Tiếp theo, người dùng click chuột vào button Tìm kiếm, một cửa sổ sẽ hiện lên và hiển thị danh sách các sản phẩm tìm được.
	+ Để tìm kiếm theo Tên sản phẩm, người dùng nhập tên sản phẩm vào ô Tên sản phẩm. Tiếp theo, người dùng click chuột vào button Tìm kiếm, một cửa sổ sẽ hiện lên và hiển thị danh sách các sản phẩm tìm được.
	+ Để tìm kiếm theo cả Giá tiền và Tên sản phẩm, người dùng nhập vào ô Giá tiền theo đúng định dạng ...nghìn đồng-...nghìn đồng và nhập vào ô Tên sản phẩm. Tiếp theo, người dùng click chuột vào button Tìm kiếm, một cửa sổ sẽ hiện lên và hiển thị danh sách các sản phẩm tìm được.
- Để quay lại màn hình lựa chọn, người dùng click chuột vào button Quay lại.
- Để thoát khỏi chương trình, người dùng có thể click chuột vào button Thoát hoặc close [X].

#### e. Tại màn hình Thống kê:
- Người dùng có thể lựa chọn thống kê theo Mã sản phẩm, loại sản phẩm và theo khoảng thời gian bằng các trường tương ứng.
- Để thực hiện thống kê, người dùng click chuột vào button Thống kê, các thông tin: Tổng số sản phẩm bán được, Doanh thu, Lợi nhuận sẽ được hiện thị ở các trường tương ứng.
- Để đưa các trường thông tin hiển thị về mặc định, người dùng click chuột vào button Làm mới.
- Để quay lại màn hình lựa chọn, người dùng click chuột vào button Quay lại.
- Để thoát khỏi chương trình, người dùng có thể click chuột vào button Thoát hoặc close [X].
