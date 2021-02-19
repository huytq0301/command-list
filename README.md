### React js

Có thể group các phương thức lifecycle ra 3 nhóm, ứng với 4 giai đoạn của component: Mounting, Updating, Unmounting, Error Handling

Mounting: 
1. constructor()
2. static getDerivedStateFromProps()
3. render()
4. componentDidMount()

Updating: Các phương thức này sẽ được gọi khi có sự thay đổi của state hoặc props
1. static getDerivedStateFromProps()
2. shouldComponentUpdate()
3. render()
4. getSnapshotBeforeUpdate()
5. componentDidUpdate()

Unmounting: Phương thức được gọi trước khi remove component khỏi DOM
1. componentWillUnmount()
Error Handling: Bất kể lỗi ở đâu trong component, nó sẽ gọi đến phương thức này
componentDidCatch()

### 1.DOM ảo là gì?
DOM ảo (virtual DOM) là một đại diện được nằm trong bộ nhớ cho một thành phần HTML thật mà cấu thành nên giao diện cho chương trình. Khi một component được thông dịch lại (re-render), DOM ảo sẽ so sánh sự thay đổi với mô hình của DOM thật để tạo một danh sách cập nhật sẽ được thực hiện.
Lợi ích chính của việc này là giúp tăng hiệu năng, chỉ tập trung vào các thay đổi nhỏ và thực sự cần thiết với DOM thật hơn là phải re-render lại một tập component lớn.

### 2.Sự khác nhau giữa class component và functional component?
Component class với mục đích để lưu giữ trạng thái bên trong hay tận dụng các phương thức vòng đời.
Một component dựa theo class là một class ES6, nó mở rộng class React Component và với tối thiểu phải thực hiện phương thức render()

Functional component là không có trạng thái (stateless), 
trong function component sẽ không sử dụng life cycle của state,
muốn sử dụng state thì phải sử dụng hook API.

### 3. Vì sao cần có middleware
Vì trong reducer ko xử lý logic bất đồng bộ. Reducer chỉ cập nhật lại State.

### 4. Axios và fetch khác nhau chỗ nào:
Khi sử dụng Fetch thì chúng ta phải convert data qua JSON.stringify(), 
với Axios thì chúng ta có thể bỏ một cách thoải mái.

### 5. Redux là gì
Redux là thư viện quản lý state bên thứ 3 cho React

### 6. Sự khác nhau giữa state và props
Props là dữ liệu được truyền vào trong một component từ cha của nó. Chúng không nên bị thay đổi, và chỉ dùng để hiển thị hay tính toán các giá trị khác. State là dữ liệu bên trong của một component, nó có thể được thay đổi trong vòng đời của component và được duy trì giữa các lần re-render

### 7. Tại sao phải goi setState thay vì trực tiếp thay đổi state?


