# Task Day 1

## 1.	Perbedaan IP Private dan IP Public
-	IP Public merupakan alamat IP yang digunakan dalam jaringan global Internet. Yang biasanya diberikan oleh penyedia layanan internet (ISP).
-	IP Private merupakan alamat IP yang digunakan dalam jaringan local dan tidak bisa diakses dari jaringan internet secara langsung.

## 2.	Jelaskan perbedaan Client-to-server & Peer-to-peer
-	Client Server adalah komputer yang menyediakan fasilitas bagi komputer-komputer lain di dalam jaringan dan client adalah komputer-komputer yang menerima atau menggunakan fasilitas yang disediakan oleh server. Server di jaringan tipe client-server disebut dengan Dedicated Server karena murni berperan sebagai penyedia fasilitas untuk workstation dan server tersebut tidak dapat berperan sebagai workstation.
-	Peer To Peer merupakan non-dedicated server, hal ini disebabkan karen server tidak berperan sebagai server murni melainkan sekaligus dapat berperan sebagai workstation.

## 3.	Menjalankan nginx di server
Langkah pertama yaitu menjalankan command sudo apt install nginx, ini berfungsi untuk melakukan proses instalasi nginx pada ubuntu server.

![image](https://user-images.githubusercontent.com/62181923/212118416-ac9864e9-79ac-4788-b867-b7c8595b8c26.png)

Setelah mejalankan command tersebut, akan terdapat konfirmasi untuk melanjutnya proses installasi, tekan Y untuk melanjutkan proses. Dan tunggu hingga proses download selesai.

![image](https://user-images.githubusercontent.com/62181923/212118506-2a43b273-f834-4d07-95e1-96362743c23f.png)
![image](https://user-images.githubusercontent.com/62181923/212118538-b1e853d9-87d3-4a9c-99e5-d0525be93b05.png)
![image](https://user-images.githubusercontent.com/62181923/212118574-1099149f-2696-4e1b-a269-a6ec52d58f45.png)

Setelah proses download atau installasi nginx selesai, pastikan nginx sudah berjalan pada ubuntu server dengan cara mengetikan command sudo systemctl status nginx seperti gambar dibawah.

![image](https://user-images.githubusercontent.com/62181923/212118674-531074e9-6192-494b-882c-312fedb2802f.png)

Berikut tampilan jik nginx berhasil berjalan, akan terdapat tulisan active(running).

![image](https://user-images.githubusercontent.com/62181923/212118741-b334d130-b273-4ae0-805f-9e5819824b9f.png)

Setelah dipastikan nginx sudah berjalan, maka buka browser lalu ketikan IP Address yang terdapat pada ubuntu server. Jika berhasil maka tampilan yang terlihat seperti gambar dibawah.

![image](https://user-images.githubusercontent.com/62181923/212118798-674d7f91-989a-45e9-9bde-4c122e652016.png)


## 4.	3 Command shell yang belum di present
-	wget, yaitu command yang digunakan untuk melakukan proses download sebuah file dengan memasukan alamat url.
-	unzip, yaitu command yang digunakan untuk melakukan ektrak file berformat zip.
-	zip, yaitu command yang digunakan untuk melakukan compress atau mengabungkan file atau direktori ke dalam bentuk zip.

## 5.	Challenge 
-	Install NVM (Node Version Manager) ref (https://emka.web.id/tutorial/tutorial-linux/cara-install-nvm-di-ubuntu-20-04-lts/) (https://tecadmin.net/how-to-install-nvm-on-ubuntu-20-04/) 

Langkah pertama yaitu melakukan proses instalasi node.js menggunakan nvm dengan cara memasukan command sudo apt install curl lalu curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash, lalu tunggu hingga proses instalasi selesai.

![image](https://user-images.githubusercontent.com/62181923/212119134-43e8325b-21ed-4e02-983b-bd3e1cc3ef7d.png)

Lakukan perintah exec bash, nvm install 10 untuk melakukan instalasi nvm versi 10, dan cek versi nvm menggunakan perintah nmv -v

![image](https://user-images.githubusercontent.com/62181923/212119162-7d6902d5-7cad-4ffa-ba8b-79d3a423080c.png)

Selanjutnya melakukan proses installasi LocalTunnel, dengan cara npm install -g localtunnel

![image](https://user-images.githubusercontent.com/62181923/212119199-02c05034-b731-48eb-b372-dea86efcffab.png)

Terakhir jalankan perinta lt –port 80 untuk menjalankan Web Server Nginx di LocalTunnel

![image](https://user-images.githubusercontent.com/62181923/212119242-6794a5fa-5403-4c0d-b0f4-5ea99a36bea0.png)

Berikut tampilan jika Nginx berhasil dijalankan pada LocalTunnel 

![image](https://user-images.githubusercontent.com/62181923/212119278-3cd6b0b4-6b67-40e7-9534-9a3dc547d7e5.png)
![image](https://user-images.githubusercontent.com/62181923/212119313-e3395de3-67d7-4fa7-a6fe-caddcef67393.png)


















