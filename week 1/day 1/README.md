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

2.	Setelah proses download selesai buka dan jalankan proses instalasi seperti biasanya. Klik next hingga muncul tombol install.

![image](https://user-images.githubusercontent.com/62181923/212113049-e101742f-3e1d-477c-b477-d80dc443a10e.png)
![image](https://user-images.githubusercontent.com/62181923/212113061-d4eff4de-a547-4980-a544-2b91fe580877.png)

3.	Tunggu hingga proses instalasi selesai, lalu klik Finish.

![image](https://user-images.githubusercontent.com/62181923/212113113-e208fba4-7d7d-40c0-8084-e8e9887738e7.png)

4.	Berikut merupakan tampilan setelah aplikasi VMware berhasil di install. Lalu pilih Create a New Virtual Machine untuk melakukan instalasi Ubuntu Server.

![image](https://user-images.githubusercontent.com/62181923/212113164-b659569e-0bde-4197-83ed-8c6c9752af82.png)

5.	Pilih file ISO yang akan digunakan melalui tombol browse dan cari dimana file ISO diletakan. Lalu Next.

![image](https://user-images.githubusercontent.com/62181923/212113198-1011ffc9-1e15-4861-a737-f927d31ae19f.png)

6.	Masukan Fullname, Username, dan juga password, setelah itu klik Next

![image](https://user-images.githubusercontent.com/62181923/212113255-2e45b386-86ed-45d0-aae8-7167aa654944.png)

7.	Pastikan file ISO sudah benar. Lalu Next
![image](https://user-images.githubusercontent.com/62181923/212113289-88f599e4-a4d1-4d68-95f8-2ab7bcc16ea2.png)

8.	Masukan maximum disk size yaitu 20 GB, serta pilih Split virtual disk into multiple files.

![image](https://user-images.githubusercontent.com/62181923/212113349-f0af56fc-8186-4e23-aca1-851c787edd84.png)

9.	Pilih Customize Hardware, 

![image](https://user-images.githubusercontent.com/62181923/212113490-09b6d5a8-32f3-446c-8ace-3526698a9d8e.png)

10.	Rubah memory yang digunakan menjadi 2GB, Processor rubah menjadi 2 (opsional tergantung dari spek laptop/computer yang dipakai dan juga kebutuhan) dan Network Adapter rubah menjadi Bridge dan klik Configure Adapter, pilih Inter(R) Wi-Fi(sesuaikan dengan adapter Wi-Fi yang kalian gunakan)

![image](https://user-images.githubusercontent.com/62181923/212113519-388f32ac-ff67-4c57-9986-c0cc31f932da.png)

11.	Pastikan Customize Hardware yang dilakukan sudah sesuai. Lalu klik Finish.

![image](https://user-images.githubusercontent.com/62181923/212113574-f950b1f3-cb71-4fe1-82f1-fd6b4335fcc7.png)

12.	Tunggu Hingga Proses Selesai
![image](https://user-images.githubusercontent.com/62181923/212113621-fe73c991-73fb-4061-a1e8-b74d27ed131b.png)

13.	Pilih Bahasa yang akan digunakan, dan tekan Enter pada Keyboard. Dan ikuti gambar installasi Ubuntu dibawah.

![image](https://user-images.githubusercontent.com/62181923/212113672-46d8d1f7-88ab-4d5b-b96c-c553a48c8201.png)
![image](https://user-images.githubusercontent.com/62181923/212113688-7136e451-3aec-4c8f-8a71-5cb5f65a936d.png)

14.Klik ens33 dan edit IPv4 lalu Enter. Dan pilih Manual seperti gambar dibawah

![image](https://user-images.githubusercontent.com/62181923/212114113-aa5dbb3c-f5a4-4e3b-8e1b-46be1bc9f78d.png)
![image](https://user-images.githubusercontent.com/62181923/212114129-bcc1a71f-7e37-416e-80a7-9abc4ec1c9c3.png)
![image](https://user-images.githubusercontent.com/62181923/212114150-2f6826e1-d34b-4151-aa75-a72af1cf5f7e.png)

15.	Lalu masukan Subnet IP Address, Gateway, Name server, dan kosongkan pada bagian search domain sesuaikan dengan koneksi yang digunakan pada perangkat laptop/pc masing-masing. Lalu pilih save dan Done.

![image](https://user-images.githubusercontent.com/62181923/212114221-e0a17049-b2bc-4b0b-823f-975dadd839e2.png)
![image](https://user-images.githubusercontent.com/62181923/212114230-1c77896c-56b2-4e97-9e3f-06390189aaab.png)

16.	Proses sebelumnya hanya klik Done tanpa merubah apapun. Hingga muncul tampilan seperti dibawah ini. Lalu pilih Custom storage layout dan pilih Done.
![image](https://user-images.githubusercontent.com/62181923/212114337-2f8b76e6-218c-4685-a12e-db2fb5e6d4c2.png)

17.	Pilih Free Space dan pilih Add GPT Partition. Masukan 2G dengan memilih format swap, lalu pilih Create.

![image](https://user-images.githubusercontent.com/62181923/212114390-d5cce59b-7aa5-4aaa-9744-4dcaac383672.png)
![image](https://user-images.githubusercontent.com/62181923/212114455-7e10c9fa-bf3e-4531-931c-c613f217f9b9.png)

18.	Lalukan hal yang sama untuk free space yang tersisa, dengan memasukan sisa max yang tertera, dan dengan format ext4, lalu tekan Create.

![image](https://user-images.githubusercontent.com/62181923/212114499-a768abf7-bd5a-4dc7-abac-cd6eb6a8d14a.png)

19.	Pastikan Disk Patition yang dibuat sudah sesuai yang diinginkan. Lalu pilih Done. Dan Continue

![image](https://user-images.githubusercontent.com/62181923/212114548-0271e66f-c41b-44f4-abc2-58b9976fbbdd.png)

20.	Masukan nama, nama server, dan yang lainnya. Lalu pilih Done.

![image](https://user-images.githubusercontent.com/62181923/212114600-dd4574e4-2b9b-44ad-a8ae-e9164c84ffa5.png)
21.	Centang untuk install OpenSSH Server. Lalu pilih Done.

![image](https://user-images.githubusercontent.com/62181923/212114640-5ac42736-dfcb-4a64-a8f3-adc70e1011c1.png)

22.	Tahapan optional, jika ingin menginstal aplikasi yang diinginkan dapat mencentang aplikasi tersebut, jika tidak dapat langsung memilih Done.

![image](https://user-images.githubusercontent.com/62181923/212114682-f84850f5-eb16-417c-85ed-32de3021112c.png)

23.	Tunggu hingga proses instalasi selesai.
![image](https://user-images.githubusercontent.com/62181923/212114744-d42b32f3-8dee-45ac-a080-520ba1c2c4e1.png)

24.	Setelah proses selesai Pilih Reboot dan tunggu hingga proses reboot selesai.

![image](https://user-images.githubusercontent.com/62181923/212114786-f65dee59-861f-4913-85c0-aeb3bf91f3b7.png)

25.	Setelah proses reboot selesai, login menggunakan usename dan password yang telah dibuat sebelumnya, lalu tekan Enter pada Keyboard.

![image](https://user-images.githubusercontent.com/62181923/212114836-529a57e7-d2c4-4799-8e9c-7b77b778fbe5.png)

26.	Lakukan pengecekan koneksi internet dengan menggunakan dns google, yaitu dengan cara ketikan ping 8.8.8.8 pada linux.
![image](https://user-images.githubusercontent.com/62181923/212114876-66330740-d974-4676-8be9-8b400253a383.png)

















