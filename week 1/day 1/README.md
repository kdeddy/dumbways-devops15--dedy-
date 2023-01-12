# Task Day 1

## Definisi DevOps
DevOps (Development dan Operation) merupakan gabungan 2 buah kata yaitu proses pengembangan (development) dari sebuah system dan juga operation (operasional). DevOps merupakan sebuha prinsip developer untuk memudahkan dalam mengkoordinasikan atar tim development dengan tim operations supaya lebih efektif dan juga efisien.

## Lifecycle DevOps dan Definisinya
![image](https://user-images.githubusercontent.com/62181923/212112570-4d5bcf12-984b-4ab7-ace5-ec51f8973c98.png)
Tahapan Lifecycle DevOps
1.	Plan (perencanaan), yaitu proses identifikasi tujuan dan persyaratan untuk merancang dan mengembangkan sistem. Selain itu yang dilakukan pada tahapan ini yaitu manajemen proyek, penjadwalan, rencana perilisa, kebijakan/persyaratn, serta rencana awal untuk pembaharuan dan perilisan di seluruh iterasi.
2.	Code (Develop), yaitu tahap pembuatan code dari aplikasi atau system yang akan dibuat. Tahapan ini memerlukan tools yang salah satunya yang populer adalah VSCode. 
3.	Build, yaitu proses yang dilakukan setelah penulisan code program selesai, untuk mengetahui apakah code tersebut masih mengalami error setelah dibuild atau sudah bisa berjalan semestinya.
4.	Test, merupakan tahapan pengujian fungsional dari apllikasi secara internal, bila masih terdapat error yang terjadi pada tahap ini maka tim developer akan melakukan perbaikan pada fungsi yang bermasalah.
5.	Release, yaitu tahap Release aplikasi yang sudah lolos dari tahap Test akan diberikan label atau nomor versi. Kapan aplikasi tersebut dirilis, apa saja perubahan yang dilakukan, dan pada tanggal berapa dilakukan release, sebelum akhirnya aplikasi tersebut akan di-deploy.
6.	Deploy, merupakan proses dimana aplikasi yang sudah dibuat akan ditempatkan atau disebarkan agar dapat diakses oleh user. Salah satu tools yang digunakan adalah AWS CodeDeploy, Jenkins, dan sebagainya.
7.	Operate, yaitu tahapan untuk memastikan aplikasi dan infrastruktur berjalan sebagaimana mestinya. Dan juga mengecek data performance, errors, dan sebagainya.
8.	Monitor, yaitu proses monitoring aplikasi atau produk yang sudah di publish ke public yang dilakukan tim operation. mencangkup monitoring dari segi infrastrukturnya, system, lain sebagainya.

## Installasi Ubuntu Server menggunakan VMware
Spesifikasi : 2 CPU, 2 GB RAM & 20GB Storage, Setup IP Static, Install OpenSSH Server
1.	Download VMWare pada website vmware.com seperti gambar dibawah. Lalu pilih download for windows atau sesuaikan dengan OS yang kalian akan digunakan.
![image](https://user-images.githubusercontent.com/62181923/212112886-e52436c4-2577-44b1-91a0-d7738aa3ee3f.png)
3.	Setelah proses download selesai buka dan jalankan proses instalasi seperti biasanya. Klik next hingga muncul tombol install.

