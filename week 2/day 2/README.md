# TASK Day 2

## 1.	Definisi Web Server
Web server merupakan sebuah software yang memberikan layanan data, dan berfungsi sebagai penerima request HTTP atau HTTPS dari client dan selanjutnya akan mengirimkan respon atas permintaan tersebut kepada client dalam bentuk halaman web.

## 2.	Jalankan 2 VM 
-	VM 1 Menjalankan App Server 
![image](https://user-images.githubusercontent.com/62181923/213376389-43b4369c-616a-42a9-9a64-75a01552dfbc.png)

-	VM 2 Menjalankan Nginx 
-	![image](https://user-images.githubusercontent.com/62181923/213376684-fec3c512-ff1f-4cbf-b123-564a2cdd77ee.png)

## 3.	VM 1 

### Jalankan Aplikasi dumbflix-frontend 
Pertama pastikan meclone dumbflix-frontend dengan github, memakai npm v 10, dan pastikan node_modules sudah ada pada directory, lalu jalankan perintah npm start.

![image](https://user-images.githubusercontent.com/62181923/213376756-e5840839-2798-4a36-886d-eed2f891d3a8.png)

Jika sudah maka coba untuk mengakses melalui browser dengan alamat ip server dengan port 3000.

![image](https://user-images.githubusercontent.com/62181923/213376771-0c3b3e63-2f9f-4d13-95ec-1b9f3aa703e1.png)

### Jalankan Aplikasi dumbflix-frontend dengan pm2 (Challange)
Pertama pastikan sudah meclone dumbflix-frontend dengan github, dan memakai npm v 10, lalu istallasi pm2 dengan perintah npm install pm2 -g. lalu jalankan pm2 dengan perintah pm2 start npm --name "dumbflix-frontend" -- start

![image](https://user-images.githubusercontent.com/62181923/213376849-cdc3b9a8-23d3-47c6-8f6b-1263ef8817a0.png)

Jika sudah maka coba untuk mengakses melalui browser dengan alamat ip server menggunakan port 3000.

![image](https://user-images.githubusercontent.com/62181923/213376873-473ff341-b374-4481-9f90-b9f782a265ad.png)


## 4.	VM 2 
### Jalankan Nginx
![image](https://user-images.githubusercontent.com/62181923/213376934-35e8d1f7-8688-4090-9a35-1e73b719122a.png)

### Konfigurasi Reverse Proxy
Pertama masuk ke dalam direktori /etc/nginx lalu daftarkan nama direktori yang akan dibuat nanti untuk menyimpan file untuk konfigurasi reverse proxy. Dengan cara edit file nginx.conf dan tambahkan nama direktori yang akan dibuat.

![image](https://user-images.githubusercontent.com/62181923/213377003-3a476258-a0b5-41bb-b922-37300b4cc768.png)

Selanjutnya buat directory sesuai dengan nama yang sudah didaftarkan dari, lalu buat file conf. dengan nemasukan nama domain, serta ip dari yang mengarah ke VM 1.

![image](https://user-images.githubusercontent.com/62181923/213377039-e72dd60e-02d2-4c86-a143-1fd2c05eb7cc.png)

Selanjutnya tambahkan ip dari webserver dan domain pada file C:\Windows\System32\drivers\etc di windows. 

![image](https://user-images.githubusercontent.com/62181923/213377060-d19595b2-ea06-42e8-b2f3-8c7a70b44f09.png)

Jika sudah maka coba untuk akses domain tadi pada browser. 

![image](https://user-images.githubusercontent.com/62181923/213377085-a5367520-538e-41ef-a5a9-83c07368f0d4.png)

Lalu lakukan test dengan mematikan App pada VM 1. 

![image](https://user-images.githubusercontent.com/62181923/213377115-5662277b-4dfb-41c7-a2ea-08d1e616daa5.png)

Maka akan muncul error Gateway 502.

![image](https://user-images.githubusercontent.com/62181923/213377138-765e0565-c6e2-46d0-8e8c-3a5062bbd878.png)

### Konfigurasi Load Balance antara VM1 dan VM2
Pertama edit file .conf yang sudah di buat sebelumnya. Dengan menambahkan 
upstream domain { 
    server (ip_app):3000;
    server (ip_webserver):3000;
    }
dan mengubah proxy pass menjadi proxy_pass http://domain; (sesuaikan dengan nama yang dipakai pada upstream)

![image](https://user-images.githubusercontent.com/62181923/213377271-13f7c5a2-ac1c-4ed7-b3b7-b221ba1b6437.png)

Lalu lakukan restart dan cek status nginx.

![image](https://user-images.githubusercontent.com/62181923/213377288-4b2e80ef-a0dd-435b-b8ef-079f961dd431.png)

## Challenge memastikan load balancer dapat berjalan dengan baik
### Kedua server dijalankan
VM 1
![image](https://user-images.githubusercontent.com/62181923/213377401-96ce3e79-79be-46e4-899d-83b47eca822f.png)

VM 2
![image](https://user-images.githubusercontent.com/62181923/213377434-7ab42359-de9f-44c8-8325-ae3bbdae910b.png)

Hasil 
![image](https://user-images.githubusercontent.com/62181923/213377454-d9c9a29a-38a0-4e20-96b2-da7d8a53321e.png)

### Server pada VM 1 dimatikan
VM 1
![image](https://user-images.githubusercontent.com/62181923/213377506-3912e603-bb3f-4e08-824b-28e7bd2955e5.png)

VM 2
![image](https://user-images.githubusercontent.com/62181923/213377535-23fc4b90-9815-4bed-9d30-b1d96baf9d46.png)

Hasil
![image](https://user-images.githubusercontent.com/62181923/213377548-deb06a95-abdc-4716-8ca5-69c4e75c4fa2.png)

### Server pada VM 2 dimatikan
VM 1
![image](https://user-images.githubusercontent.com/62181923/213377598-35f12848-3839-46ac-8148-8fdfe347aa94.png)

VM 2
![image](https://user-images.githubusercontent.com/62181923/213377615-c26c5557-7e71-471e-bee0-d5e07ae5c0e0.png)

Hasil 
![image](https://user-images.githubusercontent.com/62181923/213377630-9671f206-3e21-444d-93f1-08c90ec05692.png)

### Kudua server dimatikan 
VM 1
![image](https://user-images.githubusercontent.com/62181923/213377707-fda65adc-5f40-4b4b-810d-4fceac8acec9.png)

VM 2
![image](https://user-images.githubusercontent.com/62181923/213377738-e413b0ee-f648-4882-b5b4-49a5d9764fcf.png)

Hasil
![image](https://user-images.githubusercontent.com/62181923/213377759-7062c6fb-57ad-4b5e-9edb-bac6de976988.png)





