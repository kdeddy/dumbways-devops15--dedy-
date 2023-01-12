## Task Day 3

## 1.	Menjalankan aplikasi webserver Nginx
Berikut tampilan untuk menjalankan webserver nginx di localtunnel. Dengan perintah lt –port 80

![image](https://user-images.githubusercontent.com/62181923/212119865-f7cee083-788b-4a07-9356-c0cb71bacb8a.png)

## 2.	Menjalankan 3 aplikasi Hello Word (Node Js, Golang, Python)
### -	Node js
Pertama melakukan proses installasi nvm dengan perintah curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash , dan tunggu hingga proses instalasi selesai, lalu exec bash untuk memastikan bahwa nvm sudah dideteksi, dan pilih versi yang ingin digunakan disini akan menggunakan nvm v.12

![image](https://user-images.githubusercontent.com/62181923/212120127-5b0a64d0-df59-4204-b399-22c7e53c1184.png)

Selanjutnya yaitu membuat directory dengan nama my-app-nodejs lalu masuk ke dalam directory dengan perintah cd my-app-nodejs, lalu jalankan perintah npm init -y untuk inisialisasi project.

![image](https://user-images.githubusercontent.com/62181923/212120164-fb81e081-86d9-4863-aab0-c417ffe04ec9.png)

Jalankan perintah  npm install express –save, lalu tunggu hingga proses selesai.

![image](https://user-images.githubusercontent.com/62181923/212120193-32d7c740-ec33-408a-8b61-00d1181b5202.png)

Buat file dengan nama index.js dan isikan script seperti pada gambar dibawah untuk menampilkan text Hello Word!.

![image](https://user-images.githubusercontent.com/62181923/212120230-adab9a98-cce4-42b1-9001-9cfca42444bb.png)

Lalu jalankan file index.js dengan perintah node index.js

![image](https://user-images.githubusercontent.com/62181923/212120261-eb1d004a-6642-4533-8422-d4b6084e1138.png)

Buka browser dan masukan IP Address dari server dengan nemambahkan port 3000

![image](https://user-images.githubusercontent.com/62181923/212120823-d2a9dc29-bb4c-4234-af23-d69943c9fd50.png)

### -	Python
Pertama melakukan proses installasi python3 dengan perintah sudo apt update; sudo apt upgrade, tunggu hingga proses installasi selesai.

![image](https://user-images.githubusercontent.com/62181923/212120918-21251288-51ba-4ad3-a3a9-2ff12b29dad7.png)

Selanjutnya buat directory baru, lalu masuk kedalam directory tersebut dan jalankan perintah sudo apt install python3-pip untuk melakukan installasi package manajer untuk python. Tunggu hingga proses selesai.

![image](https://user-images.githubusercontent.com/62181923/212120962-86580127-d686-4cea-9ba2-21405e4d7888.png)

Jalankan perintah  pip install flask. Tunggu hingga proses selesai

![image](https://user-images.githubusercontent.com/62181923/212121013-75b36891-07e0-46bf-85ad-43c3e91cb3ea.png)

Buat file dengan nama index.py dan isikan script seperti pada gambar dibawah untuk menampilkan text Hello Word!.

![image](https://user-images.githubusercontent.com/62181923/212121064-25b0e229-51a7-4cb7-a703-81d0421a2b69.png)

Lalu jalankan file index.py dengan perintah python3 index.py

![image](https://user-images.githubusercontent.com/62181923/212121095-a37e88a5-f576-4814-86db-f4c07c74bb86.png)


### -	Golang
Pertama melakukan proses installasi engine golang dengan cara mengetikan perintah wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su. Tunggu hingga proses selesai.

![image](https://user-images.githubusercontent.com/62181923/212121180-212e1a4d-2e80-43bf-89b3-70784f08ca47.png)

Selanjutnya ketikan perintah rm -rf /usr/local/go && tar -C /usr/local -xzf go1.16.5.linux-amd64.tar.gz && exit

![image](https://user-images.githubusercontent.com/62181923/212121243-79dd7783-d772-425a-81ad-b583acbf7291.png)

Jalankan perintah  sudo nano .bashrc untuk masuk ke Path go. Lalu paste export PATH=$PATH:/usr/local/go/bin.

![image](https://user-images.githubusercontent.com/62181923/212121313-6062ab64-c973-41aa-80f0-5f5c8f6f4622.png)

Buat file dengan nama index.go dan isikan script seperti pada gambar dibawah untuk menampilkan text Hello Word!.

![image](https://user-images.githubusercontent.com/62181923/212121368-e620b47c-6357-44d7-bf41-e13871a6156e.png)

Lalu jalankan file index.go dengan perintah go run index.go

![image](https://user-images.githubusercontent.com/62181923/212121401-73c06ca9-7da0-4ea7-a106-d324f3e3266f.png)

## Challenge Jalankan "Hello world" di python3 melalui port 5000 (gunakan flask), lalu akses dengan localtunnel Gunakan PM2
Pertama lakukan installasi pm 2 dengan perintah npm install pm2 -g. lalu tunggu hingga proses selesai. Pastikan pm 2 sudah terinstall dengan menjalankan perintah exec bash lalu pm2 list.

![image](https://user-images.githubusercontent.com/62181923/212121549-443803d1-be14-4faf-88e3-ba6edf35c14e.png)

Selanjutnya buat file dengan nama index.py dan isikan script seperti gambar dibawah 

![image](https://user-images.githubusercontent.com/62181923/212121636-cc340c70-68a1-4fc7-8f46-1d820ce3ef9e.png)

Selanjutnya jalankan perintah pm2 start hello.py --interpreter python3

![image](https://user-images.githubusercontent.com/62181923/212121662-3fc6c8bd-fc5f-48f2-ae42-d21689be0ff3.png)


