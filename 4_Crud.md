## Create Read Update Delete
Berikut ini kita akan membuat CRUD  menggunakan MODUL GII seperti pada template basic, yang pernah kita pelajari..

### step
* Membuat Desain Database baru
* membuat tabel user menggunakan `migrate` seperti pada materi `3`
* membuat CRUD menggunakan GII

### Deasain database
Buatlah desain database seperti gambar dibawah ini menggunakan `work brench`.
jika kalian tidak memiliki aplikasi `work brench` silakan download [disini](https://dev.mysql.com/downloads/workbench/) <br>
berikut ini adalah gambar desain database yang akan dibuat

![desain](asset/cek.png)

Berikut ini link download desain yang sudah saya siapkan, *hmmm... zaman milenial... (jika kalian  malas desain database) [disini](https://drive.google.com/file/d/1mdP6Z12ttIufC5GUaaR7wPg4marWnyQr/view?usp=sharing)

lalu generate kedalam `phpmyadmin`, berikut tampilanya 

![phpmyadmin](asset/phpmyadmin.PNG)

### table user
Membuat tabel user seperti yang dilakukan di materi `2`dan jangan lupa sesuaikan databasenya dengan database sekarang, di sett di bagian `main-local.php`
sehingga menghasilkan seperti ini

![migrate](asset/php2.PNG)

### CRUD menggunkan GII
Yang pertama akses url GII `frontend` berikut urlnya `http://localhost/advanced/frontend/web/index.php?r=gii` 

* Model Generator

![gii_front](asset/gii_frond.PNG)

klik button `start` untuk modul generator, berikut tampilannya

![generator](asset/generator.PNG)

setelah ini inputkan `table name` yang akan di gerate menggunakan genarator lalu klik `preview`

![table_name](asset/table.PNG)

klik button review sehingga menghasilkan seperti berikut

![review](asset/review.PNG)

lalu generate sehingga menghasilkan seperti berikut

![hasil_preview](asset/hasil_preview.PNG)

* CRUD Generator

inputkan model dan controller seperti di gambar dibawah ini

![crud_generator](asset/crud_generator.PNG)

lalu tekan button `preview` seperti gambar berikut

![priview_crud](asset/preview_generator.PNG)

hasil generator crud

![pre](asset/hasil_generator_crud.PNG)

* Hasil

 Berikut hasilnya dengan mengakses url: `http://localhost/advanced/frontend/web/index.php?r=area`

![view](asset/view_frontend.PNG)

<b>NOTE:</b> lakukan langkah seperti diatas di setiap tabel lalu buat juga model untuk bagian `backend`