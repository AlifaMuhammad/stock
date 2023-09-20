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

TUGAS 3

Dalam konteks Django, terdapat perbedaan antara form POST dan form GET. Berikut adalah perbedaan antara keduanya:
Form POST:
-Nilai variabel tidak ditampilkan di URL, sehingga user tidak dapat dengan mudah memasukkan nilai baru
-Lebih aman daripada form GET
-Tidak dibatasi panjang string
-Pengambilan variabel menggunakan request.POST.get

Form GET:
-Nilai variabel ditampilkan di URL, sehingga user dapat dengan mudah memasukkan nilai baru
-Kurang aman daripada form POST
-Dibatasi panjang string sampai 2047 karakter
-Pengambilan variabel menggunakan request.GET.get


XML, JSON, dan HTML adalah tiga format yang berbeda dalam konteks pengiriman data. Berikut adalah perbedaan utama antara ketiganya:
XML (Extensible Markup Language):
-Digunakan untuk merepresentasikan data dengan cara yang dapat dibaca mesin
-Digunakan untuk menyimpan dan mengangkut data dari satu aplikasi ke aplikasi lain melalui Internet
-Lebih kompleks dan lebih lambat daripada JSON
-Memiliki aturan yang ketat dalam penulisan tanda
-File XML diakhiri dengan ekstensi .xml

JSON (JavaScript Object Notation):
-Digunakan untuk menyimpan dan mengirimkan data dengan cara data diuraikan dan dikirimkan melalui internet
-Format pertukaran data terbuka yang dapat dibaca baik oleh manusia maupun mesin
-Bersifat independen dari setiap bahasa pemrograman dan merupakan output API umum dalam berbagai aplikasi
-Lebih ringan dan berukuran lebih kecil daripada XML
-Dapat menyimpan data dalam bentuk array dan menjadikan transfer data menjadi lebih mudah
-File JSON diakhiri dengan ekstensi .json

HTML (Hypertext Markup Language):
-Digunakan untuk membuat halaman web
-Lebih terbatas dalam hal struktur dan tidak dapat merepresentasikan data dengan cara yang dapat dibaca mesin
-Memiliki tanda standar yang harus digunakan semua orang
-Tidak dapat membuat tanda kustom

Dalam konteks pengiriman data, JSON lebih sering digunakan daripada XML karena lebih ringan, lebih cepat, dan lebih mudah dipahami oleh komputer
HTML, di sisi lain, digunakan untuk membuat halaman web dan tidak digunakan untuk pengiriman data antar aplikasi


JSON sering digunakan dalam pertukaran data antara aplikasi web modern karena beberapa alasan, di antaranya:
-Ringan dan responsif: JSON memiliki sintaks yang kecil dan ringan, sehingga lebih responsif terhadap request
Selain itu, JSON juga lebih ringan dan berukuran lebih kecil daripada format pertukaran data lainnya seperti XML
-Mudah dibaca dan dimengerti: JSON mudah dibaca dan ditulis oleh manusia, sehingga lebih mudah dimengerti oleh pengembang
Selain itu, JSON juga mudah dimengerti oleh mesin
-Mendukung array: JSON dapat menyimpan data dalam bentuk array, sehingga transfer data menjadi lebih mudah
-Mendukung API: JSON unggul dalam penanganan API baik untuk aplikasi berbasis web maupun mobile
-Mendukung banyak bahasa pemrograman: JSON bersifat independen dari setiap bahasa pemrograman dan merupakan output API umum dalam berbagai aplikasi

1.Mengatur Routing:
Buka berkas urls.py pada folder shopping_list dalam proyek Django.
Ubah pola URL dari main/ menjadi '' pada urlpatterns sehingga menjadi path('', include('main.urls')),.

2.Membuat Kerangka Tampilan (Views):
Buat folder templates pada root folder proyek.
Buat berkas HTML baru bernama base.html dalam folder templates dan isi dengan kode kerangka umum untuk halaman web. Ini akan menjadi template dasar untuk halaman web lainnya.

3.Menggunakan Template Dasar:
Ubah berkas main.html dalam folder templates/main (atau sesuai dengan struktur direktori) untuk meng-extend base.html.

4.Membuat Form Input Data:
Buat berkas forms.py dalam aplikasi main untuk mendefinisikan form input data barang.
Buat sebuah class ProductForm yang merupakan turunan dari ModelForm dan menentukan model yang akan digunakan serta field-field yang akan ditampilkan pada form.

5.Mengatur Fungsi Views:
Di berkas views.py aplikasi main, buat fungsi create_product untuk menangani pembuatan produk baru.
Di dalam fungsi ini, buat instance form ProductForm dari request POST, lakukan validasi form, dan simpan data produk jika form valid.

6.Menampilkan Data Produk pada HTML:
Di dalam fungsi show_main dalam views.py, ambil semua data produk dari model Product.
Kirim data tersebut ke template main.html untuk ditampilkan.

7.Mengatur URL Routing:
Di berkas urls.py aplikasi main, impor fungsi create_product yang telah dibuat sebelumnya.
Tambahkan path URL untuk mengakses fungsi tersebut.

8.Mengakses Data dalam Bentuk XML:
Buka views.py yang ada pada folder main dan tambahkan import HttpResponse dan Serializer pada bagian paling atas.
Buatlah sebuah fungsi yang menerima parameter request dengan nama show_xml dan buatlah sebuah variabel di dalam fungsi tersebut yang menyimpan hasil query dari seluruh data yang ada pada Product.
Tambahkan return function berupa HttpResponse yang berisi parameter data hasil query yang sudah diserialisasi menjadi XML dan parameter content_type="application/xml".

9.Mengakses Data dalam Bentuk JSON:
Buka views.py yang ada pada folder main dan buatlah sebuah fungsi baru yang menerima parameter request dengan nama show_json.
Tambahkan return function berupa HttpResponse yang berisi parameter data hasil query yang sudah diserialisasi menjadi JSON dan parameter content_type="application/json".

10.Mengakses Data Berdasarkan ID dalam Bentuk XML dan JSON:
Buka views.py yang ada pada folder main dan buatlah sebuah fungsi baru yang menerima parameter request dan id dengan nama show_xml_by_id dan show_json_by_id.
Buatlah sebuah variabel di dalam fungsi tersebut yang menyimpan hasil query dari data dengan id tertentu yang ada pada Product.
Tambahkan return function berupa HttpResponse yang berisi parameter data hasil query yang sudah diserialisasi menjadi JSON atau XML dan parameter content_type dengan value "application/xml" (untuk format XML) atau "application/json" (untuk format JSON).

11.Mengatur URL Routing:
Buka urls.py yang ada pada folder main dan impor fungsi-fungsi yang sudah kamu buat tadi.
Tambahkan path URL ke dalam urlpatterns untuk mengakses fungsi-fungsi yang sudah diimpor tadi.
urlpatterns = [
    path('', show_main, name='show_main'),
    path('create-product', create_product, name='create_product'),
    path('xml/', show_xml, name='show_xml'),
    path('json/', show_json, name='show_json'),
    path('xml/<int:id>/', show_xml_by_id, name='show_xml_by_id'),
    path('json/<int:id>/', show_json_by_id, name='show_json_by_id'),
    # ... tambahkan path lain sesuai kebutuhan ...
]

12.Menjalankan Aplikasi:
Jalankan proyek Django dengan perintah python manage.py runserver.


![JSON](image.png) 
![XML](image-1.png)
![JSON by id](image-2.png) 
![XML by id](image-3.png)
![HTML](image-5.png)