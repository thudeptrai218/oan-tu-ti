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
### 🖥️ Giao diện đăng nhập  
Người chơi nhập **Tên** để tham gia trò chơi.  
<p align="center">
  <img src="docs/Login.png" alt="Login UI" width="400"/>
</p>  
**Hình ảnh 1: Giao diện đăng nhập**

---

### 🎮 Giao diện trò chơi Oẳn Tù Tì  
Người chơi có thể chọn **Kéo – Búa – Bao**.  
<p align="center">
  <img src="docs/GiaoDien.png" alt="Gameplay UI" width="500"/>
</p>  
**Hình ảnh 2: Giao diện trò chơi chính**

---

### 📊 Hiển thị kết quả  
Kết quả thắng/thua/hòa được hiển thị sau mỗi lượt.  

<p align="center">
  <img src="docs/Result.png" alt="Result UI" width="500"/>
</p>  
**Hình ảnh 3: Hiển thị kết quả**

---

## 📝 4. Các bước cài đặt
🔹 **Bước 1: Chuẩn bị môi trường**  
- Cài đặt **Java JDK 8+** → [Download](https://www.oracle.com/java/technologies/javase-downloads.html)  
- Kiểm tra bằng:  
  ```bash
  java -version
🔹 Bước 2: Clone dự án

bash
Sao chép mã
git clone https://github.com/your-repo/oan-tu-ti.git
cd oan-tu-ti
🔹 Bước 3: Chạy Server

bash
Sao chép mã
javac RpsServer.java
java RpsServer
🔹 Bước 4: Chạy Client

bash
Sao chép mã
javac RpsClient.java
java RpsClient
🔹 Bước 5: Bắt đầu chơi

Client nhập tên → tham gia game.

Chọn Kéo – Búa – Bao.

Server xử lý → gửi kết quả về cho client.

📬 5. Liên hệ
Họ và tên: Đoàn Tuấn Nam
Lớp CNTT 1601
Email:Dnam75603@gmail.com
Lớp: CNTT 16-01

Email:
