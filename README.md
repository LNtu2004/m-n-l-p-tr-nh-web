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
Vì máy tính mình sài chip AMD Ryzen nên mình chọn tải Windows – AMD64
