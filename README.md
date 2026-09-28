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

Bây giờ mình sẽ tạo một thư mục bài tập và tạo file docker-compose.yml:
" cd /mnt/d
mkdir baitap && cd baitap
nano docker-compose.yml " 
Lệnh này nó giúp mình tạo 1 thư mục tên là baitap vào ổ D để quản lý bài tập dễ hơn.

À mình quên mất là khi bạn cài WSL xong nó bắt bạn cài tk và mk đó nha 
<img width="1474" height="561" alt="Ảnh chụp màn hình 2026-09-28 215012" src="https://github.com/user-attachments/assets/6d6d2ec1-0b25-4280-9810-1c94d5199959" />

