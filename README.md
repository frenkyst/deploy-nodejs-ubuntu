# Deploy Nodejs Ubuntu

### Node.js

__NodeJs__ adalah runtime untuk lingkungan JavaScript di luar peramban web yang dibangun di atas mesin JavaScript V8.

1. Pertama-tama kita harus meng-install terlebih engine-nya dahulu. Untuk instalasi kalian bisa menggunakan beberapa perintah dibawah ini.

        curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash

![image](https://user-images.githubusercontent.com/40049149/186486060-c664f708-098f-4c7f-838c-0bf90e8aa789.png)

   keterangan : disini kita menggunakan __nvm__

__nvm__ merupakan singkatan dari __Node Version Manager__. __nvm__ adalah sebuah program yang akan membantu kita untuk menggunakan lebih dari satu versi Nodejs di dalam satu komputer.

        exec bash
keterangan : Jika nvm belum terdeteksi gunakan perintah di atas ini

        nvm install 16

![image](https://user-images.githubusercontent.com/40049149/186486963-e6fef845-4d27-4c93-a81d-c17aa3d4d0d7.png)

keterangan : perintah di atas berguna untuk menginstall __node.js__ dengan __versi 16__. Jika kalian ingin menggunakan __node.js__ dengan __version 14__, maka Jalankan perintah __nvm install 14__.

        nvm use 16

![image](https://user-images.githubusercontent.com/40049149/186487996-63f59394-86d3-4a42-b6f2-ae56bea13937.png)

keterangan : Untuk menggunakan node.js dengan versi 16

Jika tahapan di atas sudah kalian lakukan, maka kalian sudah berhasil untuk melakukan instalasi __node.js__. Untuk melakukan pengecekan kalian bisa menggunakan perintah di bawah ini.

        node -v
        npm -v

![image](https://user-images.githubusercontent.com/40049149/186488155-eac87e01-31b4-4207-88a2-312fdc9eaa0a.png)

2. Selanjutnya kita akan menjalankan perintah npm init gunanya untuk mengisiasi project, Hasil dari kalian menjalankan perintah akan membuat file baru dengan nama __package.json__, __package.json__ ini berisikan isi informasi dari aplikasi yang akan kalian buat.

        npm init -y

![image](https://user-images.githubusercontent.com/40049149/186488401-3c11fbc3-ef74-4bf5-986f-51fb71c842a0.png)

3. Selanjutnya kita akan menginstall __Express JS__. __Express JS__ adalah framework dari NodeJS yang dirancang secara fleksibel dan sederhana untuk membantu tahap pengembangan aplikasi back end. Menginstall __express js__ dapat dilakukan menggunakan __NPM__ dengan perintah berikut:

        npm install express --save

![image](https://user-images.githubusercontent.com/40049149/186488740-d1283a94-7053-49fc-9754-6c6d4857aba1.png)

4. Jika sudah buat file dengan nama __index.js__, lalu masukan script dibawah ini

        nano index.js
        
   Copy code dibawah ini

   __index.js__
   
        const express = require("express");
        const app = express();
        const port = 3000;

        app.get("/", (req, res) => {
          res.send("Hello World!");
        });

        app.listen(port, () => {
          console.log(`Example app listening on port ${port}`);
        });

![image](https://user-images.githubusercontent.com/40049149/186490187-c8323004-6250-4e40-9d0a-91e5db4f44b6.png)

5. Jika sudah sekarang kita akan coba untuk menjalankan aplikasi sederhana yang sudah kita buat. Untuk menjalankan dapat menggunakan perintah berikut ini.

        node index.js

![image](https://user-images.githubusercontent.com/40049149/186490392-47f35da2-76bb-4e09-95b6-bd134116f26b.png)


   Keterangan : untuk keluar bisa menggunakan CTRL + C

Sekarang coba akses web browser kalian setelah itu kalian coba akses dengan localhost:3000 atau dengan ip server:3000

![image](https://user-images.githubusercontent.com/40049149/186490995-f91216ad-6e59-4324-ad61-fc9b26a84638.png)












