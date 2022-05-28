Nama : Christio Danny Gratia Ambarita
NIM : 14117153

Judul Program : Aliens

Deskripsi Program : Program ini adalah sebuah game sederhana berformat python dan menggunakan pygame. Program ini terdapat sebuah pesawat luar angkasa dan user dapat mengontrolnya dan dapat meluncurkan serangan. Kemudian tujuan dari game ini yaitu untuk menembak pesawat alien yang ada sebanyak-banyaknya. Pesawat alien dapat menembak user secara random, dan jika user terkena serangan, maka user akan kalah

Cara menjalankan Container :

1. Pertama meng-clone git dari link https://github.com/xamox/pygame
2. Setelah itu membuka terminal python dengan menekan "ctrl+shift+p" dan mengetik terminal python, nanti akan ada pilihannya.
3. Setelah membuat file Dockerfile dengan mengetik "docker build -t (nama image) . "
4. Masukkan kode berikut ke dalam Dockerfile :

                FROM python:slim

                WORKDIR /docker-pygame

                RUN pip install pygame

                CMD [ "python", "examples/aliens.py"]

5. Pada file Dockerfile, klik kanan pada mouse dan build image dari file tersebut
6. Setelah itu pada terminal, input "docker run (nama image yang telah di build)"