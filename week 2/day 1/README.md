# Task Day 1

## 1.	Apa itu terminal
Terminal merupakan sebuah command promp atau CLI yang dapat digunakan untuk mengelola file (membuat, mengedit, membaca, dll)

## 2.	BASH script untuk update dan upgrade server, dan install nginx 
Pertama membuat file script bash dengan nama update-server-install-nginx.sh dan mengetikan kode seperti gambar dibawah untuk melakukan update, upgrade, dan install nginx, #!usr/bin/env bash digunakan untuk menginformasikan Bahasa yang digunakan yaitu bash.

![image](https://user-images.githubusercontent.com/62181923/213374595-ad057e5e-adaf-463b-a6fd-56f30a0c8406.png)

Selanjutnya untuk menjalankan file tersebut dapat menggunakan perintah sh namafile (sh update-server-install-nginx.sh). maka proses yang sudah diketikan di script akan berjalan.

![image](https://user-images.githubusercontent.com/62181923/213374632-dcc0d7ad-8074-4495-9d3d-d47476727ffc.png)

Berikut tampilan jika script bash berhasil dijalankan, maka server akan melakukan update, upgrade, dan melakukan installasi nginx.

## 3.	BASH script untuk memberi akses ke port 22,80,443

Pertama pastikan firewall pada ubuntu server aktif dengan cara sudo ufw status, jika belum aktif maka aktifkan dengan perintah sudo ufw enable

![image](https://user-images.githubusercontent.com/62181923/213374718-daf49027-a25f-4648-bc5d-ef4c1a3694f6.png)

Untuk memastikan coba untuk mengakses ssh dari server ubuntu setelah firewall dinyalakan, pastikan kita tidak dapat mengaksesnya.

![image](https://user-images.githubusercontent.com/62181923/213374737-eac4fa47-22e3-468d-a06d-53b18090729c.png)

Jika sudah maka selanjutnya membuat file script bash dengan nama allow-port.sh dengan kode seperti gambar dibawah untuk mememberikan akses untuk port 22 yaitu untuk ssh,80 untuk http, dan 443 untuk https.

![image](https://user-images.githubusercontent.com/62181923/213374770-0353682a-4cdd-4dac-bcc5-820b3c20b731.png)

Selanjutnya untuk menjalankan file tersebut dapat menggunakan perintah sh namafile (sh allow-port.sh). maka proses yang sudah diketikan di script akan berjalan.

![image](https://user-images.githubusercontent.com/62181923/213374791-a9e5f315-f97d-4768-a157-f24dbffbfc3b.png)

Lalu lakukan pengecekan kembali dengan mengakses server melalui ssh, dan pastikan server dapat diakses

![image](https://user-images.githubusercontent.com/62181923/213374822-5f4dd063-4ec8-496a-ac82-ea30a78291a4.png)

## 4.	Tugas text manipulation
### - Contoh penggunaan cat, grep, echo & sort
### Cat
- Perintah cat untuk menampilkan isi dari sebuah file dengan perintah cat nama file

![image](https://user-images.githubusercontent.com/62181923/213374950-a6cfb7c0-6817-4ec2-9265-bbc24d01ec63.png)

Perintah cat untuk membuat file baru dan mengisikan teks dengan perintah cat>namafile

![image](https://user-images.githubusercontent.com/62181923/213374987-88bb6419-eedb-4a71-81de-927e9bf18a3a.png)

Perintah cat untuk menggabungkan isi dari 2 buah file dengan perintah cat namafilepertama namafilekedua > namafile yang akan disimpan.

![image](https://user-images.githubusercontent.com/62181923/213375019-db66b036-0aa2-4e9a-be2a-6d7457288003.png)

### Grep 
- Menggunakan perintah grep untuk mencari text pada fiile dengan perintah grep text yang akan dicari lalu nama file.

![image](https://user-images.githubusercontent.com/62181923/213375092-f6f2a4c2-5606-48c5-98d7-d9648aa496a9.png)

- Perintah grep untuk menghitung jumlah kata pada sebuah file dengan cara grep -c text yang akan dicari lalu nama file. -c Berarti Count atau menghitung.

![image](https://user-images.githubusercontent.com/62181923/213375148-a3ccca9d-b34a-4fbb-96b6-134730056e29.png)

Perintah grep untuk menampilkan semua text yang akan dicari pada semua file yang terdapat pada satu directory dengan cara grep nama file yang dicari *.

![image](https://user-images.githubusercontent.com/62181923/213375181-1df00921-faee-4fac-ac46-2f8d22d7a66e.png)

### Echo

- Perintah echo dapat digunakan untuk menampilkan text dengan perintah echo “text yang ingin ditampilkan”.

![image](https://user-images.githubusercontent.com/62181923/213375228-4444ee37-c0bc-425e-ac1e-a1dc380848d3.png)

Perintah echo untuk menyisipkan text kedalam file, dengan perintah echo “text yang akan disisipkan” >> namafile yang ingin disisipkan text.

![image](https://user-images.githubusercontent.com/62181923/213375258-4f5b632f-3f4f-4099-9608-709abf0eade6.png)

Perintah echo untuk mereplace atau mengganti isi text dalam file, dengan cara echo”text yang ingin dimasukan” > namafile yang ingin textnya dirubah.

![image](https://user-images.githubusercontent.com/62181923/213375291-d4adc6fb-4d1e-411e-81df-26680dfb9c0e.png)

### Sort

- Perintah sort untuk mengurutkan data dari yang terkecil (1-9/a-z) dengan cara sort namafile

![image](https://user-images.githubusercontent.com/62181923/213375345-994602a9-a0a9-4f8f-a61c-697020704af8.png)

- Perintah sort untuk mengurutkan data dari yang terkecil (9-1/z-a) dengan cara sort -r namafile. 

![image](https://user-images.githubusercontent.com/62181923/213375380-ebd9999e-32e8-4d1c-8461-6bfe2c855dd1.png)

### Mengganti text 'Dumbways' ke 'Bootcamp'

Mengganti text pada sebuah file dapat menggunakan perintah sed, dengan cara sed -I ‘/s/text yang dicari /text yang akan digantikan/g’ namafile. 
![image](https://user-images.githubusercontent.com/62181923/213375497-72bb90df-a5e3-4880-8f2b-9897ccefd6e1.png)

## 5.	Gunakan nmon untuk tampilkan CPU usage, RAM usage, Disk dan Resources OS & Proc
Pertama lakukan installasi nmon dengan perintah sudo apt nmon pada server.

![image](https://user-images.githubusercontent.com/62181923/213375553-fa913ee3-f469-4313-b919-469943662a89.png)

Selanjutnya jika proses selesai jalankan menggunakan perintah nmon, maka akan muncul tampilan seperti ini. 

![image](https://user-images.githubusercontent.com/62181923/213375583-ce5f7d30-d56e-4e42-bd67-f373c1c940e8.png)

Untuk melihat atau memonitoring beberapa proses yang diinginkan dapat mengkilik key atau huruf yang sudah tersedia, disini akan menampilkan CPU usage, RAM usage, Disk dan Resources OS & Proc. Jadi mengetikan huruf  c m d r t.

### CPU
![image](https://user-images.githubusercontent.com/62181923/213375635-65e8f210-999c-452c-a43f-831d35471765.png)

### Memory
![image](https://user-images.githubusercontent.com/62181923/213375673-98041b03-e0ff-4589-bc67-98a51c2993e4.png)

### Disk
![image](https://user-images.githubusercontent.com/62181923/213375694-c0799a3e-9a41-4ca6-86ed-be53bf3903ad.png)

### Resource
![image](https://user-images.githubusercontent.com/62181923/213375732-43a21f1d-f515-4e7d-8ea7-312a6d632ba4.png)

### Processor
![image](https://user-images.githubusercontent.com/62181923/213375778-28e1c58e-842a-4f6d-b0d5-a558381ce560.png)

## Challange 

### Buat script instalasi node version manager menggunakan BASH

Pertama membuat file script bash, dan masukan code/sript untuk installasi nvm 

![image](https://user-images.githubusercontent.com/62181923/213375877-1cec7717-a91a-4250-8271-04e2d606beb8.png)

Lalu jalankan script bash dengan perintah sh nvm-install.sh

![image](https://user-images.githubusercontent.com/62181923/213375908-1532b347-6378-455e-a093-bacf6ce06170.png)

### Jalankan aplikasi nodejs dengan kondisi ufw enable

Pertama pastikan sudah menjalankan aplikasi node js tanpa meng allow port nya, maka aplikasi tidak akan dapat dibuka.

![image](https://user-images.githubusercontent.com/62181923/213375987-dd81528d-ddbd-43c4-92ce-4c1be1292b56.png)

Lalu beriakses untuk mengakses port 3000 karena akan menjalankan aplikasi nodejs.

![image](https://user-images.githubusercontent.com/62181923/213376064-a69a75c3-fc50-4ad1-9072-fd76beca4d8d.png)

Lalu jalankan aplikasi node js dengan perintah node index.js.

![image](https://user-images.githubusercontent.com/62181923/213376108-e1f6a195-0472-4935-a189-be7d901641f1.png)










