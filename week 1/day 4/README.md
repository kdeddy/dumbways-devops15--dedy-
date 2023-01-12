# Task Day 4

## 1.	Definisi DVCS (Distributed Version Control)
DVCS (Distributed Version Control) merupakan system yang mendukung cara kerja dimana setiap pengguna memiliki repository atau penyimpanan dari pekerjaan yang mereka miliki, jadi DVCS mendukung cara kerja kolaborasi menjadi lebih efisien.

## 2.	Mebuat Repository (format dumbways-devops15-<Dedy>
Langkah pertama yaitu pastikan memiliki akun github terlebih dahulu, dan jalankan pada Ubuntu Server, lalu buat directory dengan perintah mkdir dan masuk ke dalam directory tersebut.

![image](https://user-images.githubusercontent.com/62181923/212121991-edd5a913-00ae-4791-b208-f585304ccc1c.png)
  
  Setelah masuk ke dalam directory jalankan perintah git init untuk repository github.
  
  ![image](https://user-images.githubusercontent.com/62181923/212122137-df4ca4bf-8880-4899-9ff3-73439bd70b0f.png)

  ## 3.	Menghubungkan SSH Public Key ke Github
  Langkah pertama membuat ssh key terlebih dahulu, dengan cara menjalankan perintah ssh-keygen.
  
  ![image](https://user-images.githubusercontent.com/62181923/212122286-09777038-1912-4bf5-9c5a-6807bac7acbc.png)

Selanjutnya masuk kedalam directory ssh dan buka isi file dari id_rsa.pub.

![image](https://user-images.githubusercontent.com/62181923/212122325-31ea2c59-78ef-49fa-85a6-89f23acbfa95.png)

Tahap selanjutnya yaitu melakukan copy SSH-key ke dalam config github dengan membuka https://github.com/settings/keys. Lalu pilih New SSH Key.

![image](https://user-images.githubusercontent.com/62181923/212122362-3e014ae5-1e37-4cd9-b577-39e0311ad95e.png)

Setelah itu copy SSH key yang terdapat pada file id_rsa.pub lalu klik Add SSH key.

![image](https://user-images.githubusercontent.com/62181923/212122394-cb4d60d4-9ac6-4445-a4fd-ef5a8c90f7ee.png)

Lalu cek connection ke github apakah sudah terhubung dengan perintah ssh -T git@github.com.

![image](https://user-images.githubusercontent.com/62181923/212122420-b45c91e9-5ca7-412f-b6ec-168d554ac9d2.png)

## 4.	Clone Repository dumbflix-frontend, serta membuat 3 Branch (Development, Staging, & Production)
Pertama buka link github dumbflix-frontend https://github.com/dumbwaysdev/dumbflix-frontend lalu pilih code, HTTPS dan copy HTTPS tersebut.

![image](https://user-images.githubusercontent.com/62181923/212122483-c391891f-c9e7-4f2d-94bd-3cb180822b24.png)

Selanjutnya jalankan perintah git clone dan paste https yang sudah di copy pada github dumbflix-frontend tersebut.

![image](https://user-images.githubusercontent.com/62181923/212122508-10d0fce7-b126-4d6e-aab8-f70b01d725ec.png)

Pastikan bahwa clone berhasil denngan melihat isi directory yang ada pada Ubuntu Server.

![image](https://user-images.githubusercontent.com/62181923/212122533-5e2457b9-1515-43ac-b3eb-f1cf7d47ded2.png)

Untuk membuat branch dapat menggunakan perintah git branch (name branch). Disini akan membuat 3 branch yaitu Development, Stagging, dan juga Production. Ketikan perintah git branch Development, git branch Stagging, git branch Production. Lalu perintah git branch -a untuk melihat branch yang tersedia.

![image](https://user-images.githubusercontent.com/62181923/212122588-4e7a6bc2-e0c5-4279-95e3-41dd3e300317.png)

