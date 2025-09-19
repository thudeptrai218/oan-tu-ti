<h2 align="center">
    <a href="https://dainam.edu.vn/vi/khoa-cong-nghe-thong-tin">
    🎓 Faculty of Information Technology (DaiNam University)
    </a>
</h2>
<h2 align="center">
   TRÒ CHƠI OẲN TÙ TÌ QUA MẠNG (UDP)
</h2>
<div align="center">
    <p align="center">
        <img src="docs/aiotlab_logo.png" alt="AIoTLab Logo" width="170"/>
        <img src="docs/fitdnu_logo.png" alt="FIT DNU Logo" width="180"/>
        <img src="docs/dnu_logo.png" alt="DaiNam University Logo" width="200"/>
    </p>

[![AIoTLab](https://img.shields.io/badge/AIoTLab-green?style=for-the-badge)](https://www.facebook.com/DNUAIoTLab)
[![Faculty of Information Technology](https://img.shields.io/badge/Faculty%20of%20Information%20Technology-blue?style=for-the-badge)](https://dainam.edu.vn/vi/khoa-cong-nghe-thong-tin)
[![DaiNam University](https://img.shields.io/badge/DaiNam%20University-orange?style=for-the-badge)](https://dainam.edu.vn)

</div>

## 📖 1. Giới thiệu
Đề tài **“Trò chơi Oẳn Tù Tì qua mạng sử dụng giao thức UDP”** giúp sinh viên vận dụng kiến thức nền tảng về **lập trình mạng** để xây dựng một ứng dụng có tính tương tác trực tuyến dựa trên mô hình **Client/Server**.  
Ứng dụng được phát triển thông qua cơ chế giao tiếp bằng **UDP Socket**, cho phép nhiều người chơi tham gia và thực hiện các lượt chơi theo thời gian thực.  
Kết thúc đề tài, sinh viên có khả năng:
- Thiết kế và triển khai một trò chơi mạng đơn giản.  
- Nắm vững cách thức truyền nhận dữ liệu bằng UDP.  
- Xử lý đồng bộ giữa các client thông qua server.  
- Áp dụng nguyên lý **multithreading** trong quản lý nhiều kết nối.  

### Các chức năng chính:
- **Kết nối tới server**: đảm bảo giao tiếp giữa nhiều client trong cùng một phiên chơi.  
- **Lựa chọn nước đi**: người chơi có thể chọn **Kéo – Búa – Bao**.  
- **Xử lý và gửi kết quả**: server nhận dữ liệu từ các client, so sánh lựa chọn và gửi kết quả thắng/thua/hòa.  
- **Quản lý nhiều người chơi**: hỗ trợ nhiều client tham gia cùng lúc qua đa luồng.  
- **Hiển thị kết quả**: mỗi client sẽ thấy ngay kết quả lượt chơi.  

---

## 🔧 2. Ngôn ngữ lập trình và công nghệ sử dụng
### Ngôn ngữ lập trình:
[![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white)](https://www.java.com/)  
- Hỗ trợ mạnh mẽ cho **lập trình mạng (Networking API)**.  
- Tích hợp sẵn thư viện làm việc với **UDP Socket, Thread, I/O**.  
- Đa nền tảng, dễ triển khai.  

### Công nghệ sử dụng:
- [![UDP](https://img.shields.io/badge/UDP%20Socket-006400?style=flat-square&logo=socket.io&logoColor=white)]()  
  - Sử dụng UDP để trao đổi dữ liệu Client ↔ Server.  
  - Nhanh, gọn nhẹ, không cần kết nối lâu dài như TCP.  
  - Phù hợp với trò chơi nhiều lượt đơn giản.  

- [![Client/Server](https://img.shields.io/badge/Client%2FServer-4682B4?style=flat-square&logo=serverless&logoColor=white)]()  
  - **Server**: quản lý kết nối, nhận/gửi dữ liệu, xử lý logic so sánh kết quả.  
  - **Client**: gửi lựa chọn, nhận kết quả, hiển thị lên giao diện.  

- [![Multithreading](https://img.shields.io/badge/Multithreading-8B0000?style=flat-square&logo=apache%20kafka&logoColor=white)]()  
  - Server chạy đa luồng để quản lý nhiều client đồng thời.  

- [![Java I/O](https://img.shields.io/badge/Java%20I%2FO-FF8C00?style=flat-square&logo=openjdk&logoColor=white)]()  
  - Truyền nhận dữ liệu chuỗi ký tự giữa client và server.  

- [![IDE](https://img.shields.io/badge/Eclipse%20%2F%20IntelliJ%20IDEA%20%2F%20NetBeans-800080?style=flat-square&logo=eclipseide&logoColor=white)]()  
  - IDE hỗ trợ phát triển và debug chương trình.  

---

## 🚀 3. Hình ảnh các chức năng chính
### 🖥️ 3.1 Giao diện đăng nhập 
Người chơi nhập Tên đăng nhập (Username) để tham gia trò chơi.
Sau khi đăng nhập, client sẽ kết nối tới server và chờ ghép cặp với người chơi khác.

---

### 🎮 3.2 Giao diện trò chơi Oẳn Tù Tì  
Người chơi có thể chọn Kéo – Búa – Bao. 
Sau khi chọn, lựa chọn được gửi đến server để xử lý kết quả.
Kết quả trả về sẽ hiển thị ngay trên màn hình của người chơi.
---

### 📊 3.3 Hiển thị kết quả và lịch sử chơi
Sau mỗi lượt, server gửi kết quả Thắng – Thua – Hòa cho từng client.
Người chơi có thể theo dõi lịch sử kết quả ngay trong cửa sổ ứng dụng.
Giúp người chơi nắm được tiến trình của cả phiên chơi.

## 📝 4. Các bước cài đặt
🔹 Bước 1: Chuẩn bị môi trường
- Cài đặt Java JDK 8 hoặc mới hơn
- Tải tại: https://www.oracle.com/java/technologies/javase-downloads.html
- Sau khi cài đặt, mở Command Prompt / Terminal và kiểm tra:
  - java -version
- Nếu hiển thị java version "1.8.x" hoặc cao hơn nghĩa là cài đặt thành công.
- Cài đặt một IDE để dễ chạy code (khuyến nghị IntelliJ IDEA, cũng có thể dùng Eclipse hoặc NetBeans).

🔹 Bước 2: Tải mã nguồn
- Clone dự án từ GitHub:
- git clone https://github.com/your-repo/OanTuTi-Game.git
  - cd OanTuTi-Game
- Nếu không dùng Git, bạn có thể bấm nút Download ZIP trên GitHub, sau đó giải nén.

🔹 Bước 3: Mở dự án trong IDE
- Vào File → Open Project trong IDE.
- Chọn thư mục chứa source code (Client.java và Server.java).
- Đảm bảo IDE nhận diện dự án là Java Project.

🔹 Bước 4: Biên dịch và chạy Server
- Mở file Server.java.
- Nhấn Run để chạy server.
- Server sẽ lắng nghe kết nối.
- Nếu chạy thành công, IDE sẽ hiển thị log kiểu:
  - Server started on
  - Waiting for players...

🔹 Bước 5: Biên dịch và chạy Client
- Client nhập tên → tham gia game.

- Chọn Kéo – Búa – Bao.

- Server xử lý → gửi kết quả về cho client.


## 📬 5. Liên hệ
- Họ và tên: Đoàn Tuấn Nam
- Lớp: CNTT 16-01
- SDT: 0862318469

