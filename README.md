Membuat Proyek Django Baru:

Buka terminal dan jalankan perintah django-admin startproject nama_proyek untuk membuat proyek Django baru.
Membuat Aplikasi 'main':

Di dalam direktori proyek Django, jalankan perintah python manage.py startapp main untuk membuat aplikasi dengan nama 'main'.
Melakukan Routing pada Proyek:

Buka file urls.py di dalam proyek Django dan tambahkan path untuk mengarahkan ke aplikasi 'main'. Contoh: path('main/', include('main.urls')).
Membuat Model 'Item':

Buka file models.py di dalam aplikasi 'main' dan buat model 'Item' dengan atribut yang sesuai, seperti yang telah dijelaskan dalam checklist.
Membuat Fungsi pada views.py:

Buka file views.py di dalam aplikasi 'main' dan buat sebuah fungsi yang akan merender template HTML dengan informasi yang diminta.
Membuat Routing pada urls.py Aplikasi 'main':

Buka file urls.py di dalam aplikasi 'main' dan buat path untuk memetakan fungsi yang telah dibuat di views.py.
Deployment ke Adaptable

  +----------+         +----------------+       +-------------+
  | Client   |   --->  | urls.py (routing)| --->  | views.py    |
  | (Browser)|  Request|------------------|       | (Controller)|
  |          |         |    (URL Path)   |       |             |
  |          |         +----------------+       +-------------+
  |          |               |                        |
  |          |         +-----v------+                 |
  |          |         | models.py |                 |
  |          |   <---  | (Model)   |  <--------------+
  |          |   Response|-----------|
  +----------+          |   (Database)|
                        +------------+

urls.py digunakan untuk routing permintaan dari client ke views yang sesuai.
views.py berisi logika aplikasi, seperti memproses permintaan dan merender template HTML.
models.py adalah tempat di mana kita mendefinisikan model database yang digunakan oleh aplikasi. Model ini dapat diakses oleh views untuk mengambil atau menyimpan data.


Meskipun sangat disarankan untuk memakai virtual environment, kita masih dapat membuat aplikasi web berbasis Django tanpa menggunakan virtual environment. Namun, ini dapat menyebabkan masalah seperti konflik dependensi dan kesulitan dalam mengelola berbagai proyek. Oleh karena itu, sangat disarankan untuk menggunakan virtual environment untuk pengembangan aplikasi Python, terutama jika Anda bekerja pada proyek-proyek yang lebih besar atau memiliki dependensi yang kompleks. Virtual environment adalah alat yang kuat untuk menjaga lingkungan pengembangan agar tetap bersih, terisolasi, dan teratur.

MVC (Model-View-Controller):
Model: Mewakili data dan logika bisnis. Ini adalah komponen yang mengurus pengelolaan data dan berinteraksi dengan basis data.
View: Menampilkan data kepada pengguna. Tidak memiliki logika bisnis. Hanya menangani presentasi.
Controller: Menangani permintaan dari pengguna, memproses input, dan mengatur alur aplikasi. Ini adalah otak dari aplikasi yang menghubungkan Model dan View.

MVT (Model-View-Template):
Model: Mirip dengan MVC, mewakili data dan logika bisnis. Ini berinteraksi dengan basis data.
View: Menentukan bagaimana data ditampilkan kepada pengguna. Tidak memiliki logika bisnis. Mengambil data dari Model.
Template: Mengatur tampilan dan struktur halaman HTML. Ini adalah bagian yang merender data yang diberikan oleh View.

MVVM (Model-View-ViewModel):
Model: Mewakili data dan logika bisnis, sama seperti dalam MVC dan MVT.
View: Menampilkan data seperti dalam MVC dan MVT. Tidak memiliki logika bisnis.
ViewModel: Memisahkan logika tampilan dari tampilan itu sendiri. Ini adalah lapisan yang mengelola data yang akan ditampilkan dan berfungsi sebagai penghubung antara Model dan View. ViewModel mempersiapkan data yang akan ditampilkan oleh View.

Perbedaan utama antara ketiganya adalah bagaimana logika aplikasi dan tampilan dipisahkan dan bagaimana data mengalir antara komponen-komponen tersebut. MVC memiliki Controller, MVT menggunakan Template, sedangkan MVVM memiliki ViewModel. Django, sebuah kerangka kerja berbasis MVT, memisahkan tampilan dengan Template, sementara Model dan View bekerja lebih dekat bersama.