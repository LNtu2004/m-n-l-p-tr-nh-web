# Lê Ngọc Tú K225480106069
# Môn PHÁT TRIỂN ỨNG DỤNG TRÊN NỀN WEB
# bài tập 1:
1. giả lập linux os: hyperV, virtualBox, vmware, wsl
2. cài đặt docker compose trên os đó
3. cài trên docker compose : các dịch vụ: nginx, nodered, mariadb, phpmyadmin, cloudflared (cần domain xịn)
4. cấu hình nginx có thể chạy 2 website  với 2 domain khác nhau.
#              Bài làm 
1. Em sử dụng giả lập wsl trên win 11
# Cách cài 
Mở PowerShell (Run as Administrator) và chạy lệnh: " wsl --install "
Sau khi cài xong bạn cần khơi động lại máy, mở lại máy tính mình thì nó sẽ hiện cửa sổ giao diện sẽ như này :
<img width="1357" height="828" alt="Ảnh chụp màn hình 2026-09-28 214418" src="https://github.com/user-attachments/assets/18f7fdfa-b2c7-48cb-9411-1bc05361c07b" />
Bước tiếp theo bạn cài Docker Desktop cho Windows từ trang chủ Docker 
Link : " https://www.docker.com/products/docker-desktop/?utm_source=gemini "

Ở đây có rất nhiều bản bạn xem máy tính mình sài chip gì thì tải cho phù hợp máy nhé 
<img width="591" height="491" alt="Ảnh chụp màn hình 2026-09-28 215334" src="https://github.com/user-attachments/assets/ad220f3c-0cbc-4796-b20d-bcb77c83df99" />

Vì máy tính mình sài chip AMD Ryzen nên mình chọn tải Windows – AMD64 ( khoảng 600mb )và giao diện khi cài xong

<img width="1583" height="898" alt="Ảnh chụp màn hình 2026-09-28 221301" src="https://github.com/user-attachments/assets/c6518873-d034-4ef6-99bf-7e075d3d56e7" />

À mình quên mất là khi bạn cài WSL xong nó bắt bạn cài tk và mk đó nha 
<img width="1474" height="561" alt="Ảnh chụp màn hình 2026-09-28 215012" src="https://github.com/user-attachments/assets/6d6d2ec1-0b25-4280-9810-1c94d5199959" />

Sau khi tạo tk và mk xong thì nó sẽ hiễn dòng chữ màu xanh lá tức là bạn đã vào ubutu thành công nhé 
2. Bây giờ mình sẽ tạo một thư mục bài tập và tạo file docker-compose.yml:
" cd /mnt/d
mkdir baitap && cd baitap
nano docker-compose.yml " 
Lệnh này nó giúp mình tạo 1 thư mục tên là baitap vào ổ D để quản lý bài tập dễ hơn. ( xem hình giống vậy là được )

<img width="1919" height="1014" alt="Ảnh chụp màn hình 2026-09-28 225726" src="https://github.com/user-attachments/assets/d9f9a8d4-20a2-4f91-85c4-a458ebc87b24" />
<img width="1919" height="1014" alt="Ảnh chụp màn hình 2026-09-28 223651" src="https://github.com/user-attachments/assets/17370791-96c8-41cc-8593-65e0366e2fc6" />

3. Cần domain xịn thì mình đăng ký tại pa vietnam nhé hoặc các bạn vô " https://www.pavietnam.vn/vn/ten-mien-mien-phi.html?utm_source=banner-idvn&utm_medium=header-right&utm_campaign=ten-mien-id-mien-phi-home-page " cái này lun cũng được.

<img width="1919" height="980" alt="image" src="https://github.com/user-attachments/assets/c816ef9a-f4f3-4780-9eeb-b9a73fef6679" />

Sau khi đăng ký xong bạn vứt nó vô clouflare là được và nhớ phải cấu hình DNS đó nha.Xong hết rồi thì hiện ra như này là ok 

<img width="1861" height="821" alt="Ảnh chụp màn hình 2026-09-28 203716" src="https://github.com/user-attachments/assets/cf417331-276c-4cb1-95fb-ecac2231f2d3" />

Giờ vào zero trust chọn Networking rồi chọn tunnels nhấn vô creat router 

<img width="1854" height="875" alt="Ảnh chụp màn hình 2026-09-28 205436" src="https://github.com/user-attachments/assets/28e87eac-2d47-4de3-a099-85b44b99f830" />
<img width="1032" height="802" alt="Ảnh chụp màn hình 2026-09-28 205652" src="https://github.com/user-attachments/assets/02443dc5-eac2-4d6c-9c32-3e85eee15936" />

Cái chỗ " ngoctu123 " là phần điền tên bạn thích điền tên gì vào cũng được.

<img width="836" height="724" alt="image" src="https://github.com/user-attachments/assets/e7e50b4e-51b0-4790-b069-56716f7cdb9b" />

Còn đây là phần add router cái chữ " kmt " là phần đứng trước tên miền của bạn bạn có thể ghi tên gì cũng dc hoặc không ghi cũng được.Đặc biệt là phần URL là cái phần mà clouflare nó quản lý và cho phép mình vào dưới dạng index.php

<img width="1865" height="889" alt="image" src="https://github.com/user-attachments/assets/56bcd839-670f-4954-a62a-eada5a205199" />

4.Cấu hình 
Ta dùng lệnh " nano docker-compose.yml " để cấu hình
<img width="998" height="50" alt="image" src="https://github.com/user-attachments/assets/2460f574-5b5a-4950-be99-9adb0e86c85f" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ab78d554-4bf5-4706-b781-97beb041787a" />

Sau đó dùng lệnh " docker compose up -d " để update lại nó.Vì nó xảy ra lỗi nên mình sài lệnh " sudo docker compose up -d " 

<img width="1911" height="782" alt="Ảnh chụp màn hình 2026-09-28 231841" src="https://github.com/user-attachments/assets/3493e913-64ec-490e-be85-a95449976e7a" />

