# Oẳn Tù Tì Qua Mạng

Đây là một ứng dụng **trò chơi Oẳn Tù Tì (Rock-Paper-Scissors)** được lập trình bằng **Java**, chạy qua mạng sử dụng **giao thức UDP**.  
Đề tài thuộc môn học **Lập Trình Mạng** – Trường Đại học Đại Nam.

---

##  Giới thiệu
Trò chơi Oẳn Tù Tì (Kéo – Búa – Bao) vốn quen thuộc trong đời sống hằng ngày.  
Trong đề tài này, chúng tôi xây dựng ứng dụng cho phép **nhiều người chơi tham gia qua mạng**, thay vì chơi trực tiếp.  
Ứng dụng gồm **Client** và **Server**, trao đổi dữ liệu thông qua **giao thức UDP** để đạt tốc độ xử lý nhanh, giảm độ trễ, phù hợp với tính chất của trò chơi.

Mặc dù UDP không đảm bảo tính toàn vẹn như TCP, nhưng ưu điểm của nó là phản hồi tức thì, đem lại trải nghiệm mượt mà.

---

## Mục tiêu
- Vận dụng kiến thức **lập trình mạng** với Java.  
- Tạo một hệ thống **Client – Server** có khả năng kết nối, gửi/nhận dữ liệu.  
- Rèn luyện kỹ năng thiết kế giao diện bằng **Java Swing**.  
- Xây dựng ứng dụng có tính thực tiễn, phục vụ giải trí.  

---

## Chức năng chính
- Người chơi nhập tên, tham gia trò chơi với server.  
- Lựa chọn **Kéo – Búa – Bao** từ giao diện.  
- Gửi lựa chọn lên server qua UDP.  
- Server xử lý kết quả và gửi phản hồi về client.  
- Hiển thị kết quả thắng / thua / hòa.  
- Hỗ trợ nhiều người chơi tham gia cùng lúc.  

---

## Công nghệ sử dụng
- **Ngôn ngữ**: Java  
- **Giao thức mạng**: UDP  
- **Giao diện người dùng**: Java Swing  
- **Kỹ thuật hỗ trợ**:  
  - **Multithreading**: xử lý nhiều client đồng thời  
  - **Serialization**: đóng gói dữ liệu gửi qua UDP  

---

## Cấu trúc thư mụcsrc/BTL/
│── Client.java # Code phía client
│── Server.java # Code phía server
│── GUI.java # Giao diện Java Swing
│── Message.java # Định nghĩa dữ liệu gửi/nhận
docs/
│── report.pdf # Báo cáo đề tài
│── diagrams/ # Hình sơ đồ UML
README.md # Giới thiệu dự án
LICENSE # Giấy phép MIT
.gitignore # File bỏ qua khi commit


---

## Hướng dẫn cài đặt & chạy chương trình
### 1. Clone repository
```bash
git clone https://github.com/<tentaikhoan>/oan-tu-ti.git
cd oan-tu-ti

2. Mở dự án

Dùng IntelliJ IDEA, Eclipse hoặc NetBeans.

Import thư mục src/BTL.

3. Chạy server

Mở file Server.java và chạy trước.

Server sẽ lắng nghe port UDP (ví dụ: 5000).

4. Chạy client

Mở file Client.java và chạy.

Nhập địa chỉ IP + port của server.

Bấm chọn Kéo – Búa – Bao trên giao diện Swing.

5. Xem kết quả

Client sẽ hiển thị kết quả ngay lập tức (thắng / thua / hòa).📸 Minh họa giao diện

 Thêm hình ảnh từ thư mục docs/diagrams để README đẹp hơn:

Giao diện Client

Màn hình Server Console

Sơ đồ kiến trúc hệ thống

Class Diagram

(Nếu đã vẽ bằng draw.io / StarUML, có thể chèn link ảnh tại đây)

 Sơ đồ UML

Component Diagram: mô tả các thành phần Client – Server.

Sequence Diagram: luồng xử lý khi người chơi gửi lựa chọn.

Class Diagram: mô hình hóa các lớp Java (Client, Server, Message, GUI).

 Tác giả

Sinh viên thực hiện: Đoàn Tuấn Nam – CNTT 16-01

MSSV: 1671020209

GVHD: Thầy Lê Tuấn Anh, Thầy Trần Vũ Đại

 Giấy phép

Dự án được phát hành theo MIT License.
Bạn có thể thoải mái sử dụng, chỉnh sửa và phát triển thêm.

 Hướng phát triển

Nâng cấp từ UDP sang TCP để tăng độ tin cậy.

Thêm tính năng xếp hạng và thống kê kết quả người chơi.

Tích hợp chat trực tuyến giữa các client.

Triển khai ứng dụng trên nền web hoặc mobile.
