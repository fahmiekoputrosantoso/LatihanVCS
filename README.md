# PENGGUNAAN GIT

## Pengertian Git
* Git adalah salah satu sistem pengontrol versi(Version Control System) pada proyek perangkat lunak yang diciptakan Linus Torvalds.
* Pengontrol versi bertugas memcatat setiap perubahan pada file proyek yang dikerjakan oleh banyak orang maupun sendiri.
* Git dikenal juga dengan distributed revision control (VCS terdistribusi), artinya penyimpanan database Git tidak hanya berada dalam satu tempat saja.

## Instalasi Git
* Download **Git**, Buka website resminya Git [git-scm.com](https://git-scm.com).

![gbr1](Gambar/Gambar1.png)


* Kemudian unduh Git sesuai dengan arsitektur komputer kita. Kalau menggunakan 64bit, unduh yang 64bit. Begitu juga kalau menggunakan 32bit.
* Untuk pengguna linux ``sudo apt-get install git`` & untuk Mac ``brew install git``
* Selamat, Git sudah terinstal. Untuk mencobanya,silahkan buka **Terminal** atau **CMD**,kemudian ketik perintah

  ``git --version.``

  ![gbr2](Gambar/Gambar2.PNG)

## Menambahkan Global Config
* Pada saat pertama kali menggunakan git, perlu dilakukan konfigurasi
user.name dan user.email
* konfigurasi ini bisa dilakukan untuk global repostiry atau individual
repository.
* apabila belum dilakukan konfigurasi, akan mengakibatkan terjadi
kegagalan saat menjalankan perintah ```git commit```
* Config Global Repository

  ``$ git config --global user.name "nama_user"``

  ``$ git config --global user.email "nama_user"``

  ![gbr3](Gambar/Gambar3.PNG)

## Perintah Dasar Git
* ``git init`` , perintah untuk membuat repository local
* ``git add``, perintah untuk menambahkan file baru, atau perubahan pada file
pada staging sebelum proses commit.
* ``git commit``, perintah untuk menyimpan perubahan kedalam database git.
* ``git push -u origin master``, perintah untuk mengirim perubahan pada repository local menuju server repository.
* ``git clone [url]``, perintah untuk membuat working directory yang diambil dari repositry sever.
* ``git remote add origin [url]``, perintah untuk menambahkan remote server/reopsitory server pada local repositry (working directory)
* ``git pull``, perintah untuk mengambil/mendownload perubahan terbaru dari server repository ke local repository

## Membuat Repository Local
* Buka direktory aktif, misal: 'C:\Users\HP\'
* Drop direktori ke terminal / CMD
* Buat direktory project praktikum pertama dengan nama tugaseko

  ``$ mkdir tugseko``

  ``$ cd tugaseko``

![gbr4](Gambar/Gambar4.PNG)

* Sehingga terbentuk satu direktori baru dibawahnya, selanjutnya masuk kedalam direktori tersebut dengan perintah cd (change directory)
* direktory aktif menjadi: C:\Users\HP\tugaseko
* Jalankan perintah git init, untuk membuat repository local.
``$ git init``

![gbr5](Gambar/Gambar5.PNG)
* Repository baru berhasil di inisialisasi, dengan terbentuknya satu direktori hidden dengan nama .git
* Pada direktori tersebut, semua perubahan pada working directory akan disimpan.

# Menambahkan File baru pada repository
* Untuk membuat file dapat menggunakan text editor, lalu menyimpan filenya pada direktori aktif (repository)
* disini kita akan coba buat satu file bernama README.md (text file)

  ``$ echo “#latihan eko” >> README.md``

* File README.md berhasil dibuat.

  ![gbr6](Gambar/Gambar6.PNG)

# Menambahkan File baru pada repository
* Untuk menambahkan file yang baru saja dibuat tersebut gunakan perintah git add.

  ``$ git add README.md``

* File README.md berhasil ditambahkan.

  ![gbr7](Gambar/Gambar7.PNG)

# Commit (Menyimpan perubahan ke database)
* Untuk menyimpan perubahan yang ada kedalam database repository local, gunakan perintah

  ``$ git commit -m 'File pertama eko'``

* Perubahan berhasil disimpan.

  ![gbr8](Gambar/Gambar8.PNG)

# Membuat repository server
* Server reopsitory yang akan kita gunakan adalah http://github.com, Anda harus membuat akun terlebih dahulu.
* Pada laman github, klik tombol start a project, atau
* Dari menu (icon +) klik New Repository

![gbr9](Gambar/Gambar9.PNG)

# Membuat repository server
* Isi nama repository nya, misal: TugasVCS
* lalu klik tombol Create repository

  ![gbr10](Gambar/Gambar10.PNG)

# Menambahkan Remote Repository
* Remote Repository merupakan repository server yang akan digunakan untuk menyimpan setiap perubahan pada local repository, sehingga dapat diakses oleh banyak user.
* Untuk menambahkan remote repository server, gunakan perintah git remote add origin [url]

  ``$ git remote add origin https://github.com/fahmiekoputrosantoso/TugasVCS``

  ![gbr11](Gambar/Gambar11.PNG)

# Push (Mengirim perubahan ke server)
* Untuk mengirim perubahan pada local repository ke server gunakan perintah git push.

  ``$ git push -u origin master``

* Perintah ini akan meminta memasukkan username dan password pada akun github.com

  ![gbr12](Gambar/Gambar12.PNG)

# Lihat hasilnya pada server repository
* Buka laman github.com, arahkan pada repositori- nya.
* Maka perubahan akan terlihat pada laman tersebut.

  ![gbr13](Gambar/Gambar13.PNG)

# Clone Repository
* Clone repository, pada dasarnya adalah meng-copy repository server dan secara otomatis membuat satu direktory sesuai dengan nama repositorynya (working directory).
* Untuk melakukan cloning, gunakan perintah git clone [url]

  ``git clone https://github.com/fahmiekoputrosantoso/TugasVCS``

  ![gbr14](Gambar/Gambar16.PNG)
