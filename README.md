# Sawi mobile 

> **Sawi mobile** adalah sebuah aplikasi mobile untuk membeli sayur-sayuran
### Daftar Tugas:
- **[Tugas 7](#tugas-7)**<br>

# Tugas 7
## **_Stateless_ dan _stateful widget_**
Stateless dan Stateful Widget adalah dua jenis widget yang umum digunakan dalam pengembangan aplikasi Flutter. Berikut adalah perbedaan utama antara Stateless dan Stateful Widget:

StatelessWidget:
- Tidak memiliki data yang dapat berubah (immutable).
- Digunakan untuk bagian tampilan yang tidak perlu berubah seiring waktu.
- Setiap kali ada perubahan yang memengaruhi widget ini, Anda perlu membuat widget baru.
- Contoh penggunaan: menampilkan teks statis, ikon, gambar, dan sebagainya.

StatefulWidget:
- Memiliki state (keadaan) yang dapat berubah selama siklus hidup widget.
- Digunakan untuk bagian tampilan yang perlu berubah seiring waktu atau merespons perubahan data.
- Stateful widget dapat memperbarui tampilan ketika ada perubahan dalam state atau data yang mereka kelola.
- Contoh penggunaan: formulir input, daftar item yang dapat diperbarui, aplikasi dengan banyak halaman yang dapat berubah, dan sebagainya.

Penggunaan StatelessWidget dan StatefulWidget dalam tugas ini menggambarkan konsep dasar Flutter di mana Anda menggunakan StatelessWidget untuk elemen tampilan yang tetap (seperti item daftar belanja) dan StatefulWidget ketika Anda perlu merespons perubahan data atau interaksi pengguna (seperti menampilkan umpan balik saat tombol diklik).

## **_Widget_ yang digunakan**
1. **MyHomePage**: Ini adalah widget utama yang merupakan halaman beranda dari aplikasi. Ini adalah widget Stateless (tidak memiliki keadaan internal) yang akan menggambarkan tampilan beranda aplikasi.

2. **Scaffold**: Ini adalah kerangka utama yang digunakan untuk menyusun berbagai elemen tampilan seperti AppBar dan body dalam satu tampilan. Ini memberikan kerangka umum untuk halaman.

3. **AppBar**: Widget ini digunakan untuk membuat bagian atas pada aplikasi yang berisi judul aplikasi dan tata letaknya.

4. **SingleChildScrollView**: Widget ini digunakan sebagai pembungkus untuk memungkinkan kontennya dapat discroll. Ini berguna ketika konten dalam halaman terlalu panjang untuk muat pada layar.

5. **Padding**: Widget ini digunakan untuk menambahkan jarak (padding) di sekitar widget-child yang ada di dalamnya.

6. **Column**: Widget ini digunakan untuk menampilkan widget-child secara vertikal. 

7. **Text**: Ini digunakan untuk menampilkan teks dalam aplikasi.

8. **GridView.count**: Ini adalah widget yang digunakan untuk menampilkan grid dengan jumlah kolom tetap. Dalam hal ini, grid ini digunakan untuk menampilkan daftar item toko.

9. **ShopCard**: Custom widget. Ini digunakan untuk menampilkan setiap item toko dalam bentuk card. Widget ini memiliki ikon dan teks, serta memberikan umpan balik saat ditekan.

10. **Material**: Ini adalah widget yang memberikan latar belakang berwarna pada setiap ShopCard.

11. **InkWell**: Ini adalah widget yang digunakan untuk membuat area yang responsif terhadap sentuhan. Ini digunakan untuk menangani interaksi saat pengguna mengklik ShopCard.

12. **Icon**: Ini digunakan untuk menampilkan ikon di dalam ShopCard.

13. **SnackBar**: Widget yang menampilkan pesan sementara yang muncul di bagian bawah layar ketika item di klik.

## **Implementasi Aplikasi**
**Membuat sebuah program Flutter baru dengan tema inventory seperti tugas-tugas sebelumnya.**
Generate proyek flutter baru dengan command flutter create sawimobile

 **Membuat tiga tombol sederhana dengan ikon dan teks untuk:
 Melihat daftar item (Lihat Item)
 Menambah item (Tambah Item)
 Logout (Logout)**
 Seperti pada tutorial menambahkan 3 tombol, edit menu.dart dan menambahkan kode
 final List<ShopItem> items = [
    ShopItem("Lihat Produk", Icons.checklist),
    ShopItem("Tambah Produk", Icons.add_shopping_cart),
    ShopItem("Logout", Icons.logout),
];

 **Memunculkan Snackbar dengan tulisan:
 "Kamu telah menekan tombol Lihat Item" ketika tombol Lihat Item ditekan.
 "Kamu telah menekan tombol Tambah Item" ketika tombol Tambah Item ditekan.
 "Kamu telah menekan tombol Logout" ketika tombol Logout ditekan.**
 Mengedit menu.dart pada bagian widgetbuild
  onTap: () {
          // Memunculkan SnackBar ketika diklik
          ScaffoldMessenger.of(context)
            ..hideCurrentSnackBar()
            ..showSnackBar(SnackBar(
                content: Text("Kamu telah menekan tombol ${item.name}!")));
        },
saat diclick maka akan ada message sesuai tombol yang ditekan

# Tugas 8

1. **Perbedaan antara `Navigator.push()` dan `Navigator.pushReplacement()`:**
   - `Navigator.push()`: Digunakan untuk menambahkan rute baru ke tumpukan navigasi. Ini menambahkan rute baru di atas rute saat ini, sehingga pengguna dapat kembali ke rute sebelumnya.
   
     ```dart
     Navigator.push(
       context,
       MaterialPageRoute(builder: (context) => ShopFormPage()),
     );
     ```
   
   - `Navigator.pushReplacement()`: Digunakan untuk menggantikan rute saat ini dengan rute baru. Ini berguna ketika Anda ingin mengganti tampilan saat ini dengan tampilan baru dan menghapus tampilan saat ini dari tumpukan.

     ```dart
     Navigator.pushReplacement(
       context,
       MaterialPageRoute(builder: (context) => NewPage()),
     );
     ```

2. **Layout Widgets pada Flutter dan Konteks Penggunaannya:**
   - `Container`: Widget ini digunakan untuk mengelompokkan dan mengatur widget lain. Kontainer dapat menentukan batasan ukuran, padding, dan dekorasi.
   - `Column` dan `Row`: Digunakan untuk menata widget secara vertikal (Column) atau horizontal (Row).
   - `ListView`: Digunakan untuk menampilkan daftar item secara berurutan, bisa scroll jika item melebihi ruang yang tersedia.
   - `Stack`: Digunakan untuk menumpuk widget di atas satu sama lain. Widget dalam tumpukan ditempatkan relatif terhadap satu sama lain.
   - `GridView`: Mengatur widget dalam bentuk grid atau matriks.

3. **Elemen Input pada Form dan Penggunaannya:**
   - `TextField`: Untuk input teks dari pengguna.
   - `Checkbox`: Untuk memungkinkan pengguna memilih opsi dengan kotak centang.
   - `RadioButton`: Untuk memungkinkan pengguna memilih satu opsi dari beberapa opsi.
   - `DropdownButton`: Untuk membuat dropdown menu dengan opsi pilihan.
   - `DatePicker`: Untuk memungkinkan pengguna memilih tanggal.

   Pilihan ini digunakan untuk mengumpulkan informasi yang diperlukan untuk formulir, seperti nama, alamat, tanggal, dan opsi-opsi pilihan.

4. **Penerapan Clean Architecture pada Aplikasi Flutter:**
   - **Domain Layer**: Berisi aturan bisnis dan logika aplikasi. Tidak bergantung pada lapisan lain dan hanya berisi kode yang dapat digunakan di berbagai platform.
   - **Data Layer**: Menyediakan implementasi konkrit dari abstraksi yang didefinisikan di lapisan domain. Berkomunikasi dengan sumber data eksternal seperti database atau API.
   - **Presentation Layer**: Menangani UI dan interaksi pengguna. Menggunakan kode dari lapisan domain dan data untuk mempresentasikan informasi kepada pengguna.

   Pemisahan ini memudahkan pengujian, pemeliharaan, dan penggantian komponen tanpa mempengaruhi yang lain. Clean architecture juga mendukung prinsip Dependency Inversion, di mana lapisan yang lebih tinggi tidak bergantung pada lapisan yang lebih rendah, tetapi sebaliknya.

5. **Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial)**
  
1. Membuat Halaman Formulir Tambah Item Baru
1.1. Buat Halaman Baru
Buat widget Flutter baru untuk halaman formulir tambah item. Anda dapat menggunakan StatefulWidget untuk mengelola status formulir.

1.2. Tambahkan Elemen Input
Gunakan elemen input seperti TextFormField untuk name, amount, dan description sesuai dengan model aplikasi Django yang Anda buat.

1.3. Tambahkan Tombol Save
Tambahkan tombol ElevatedButton atau TextButton untuk menyimpan data formulir.

1.4. Validasi Elemen Input
Implementasikan validasi untuk memastikan bahwa setiap elemen input tidak boleh kosong dan sesuai dengan tipe data yang diharapkan.

1.5. Tampilkan Pop-up
Setelah menekan tombol Save, tampilkan pop-up dengan informasi yang diisi pada formulir menggunakan showDialog.

2. Membuat Drawer
2.1. Implementasikan Drawer
Buat widget Flutter untuk Drawer yang minimal memiliki dua opsi: "Halaman Utama" dan "Tambah Item". Anda dapat menggunakan ListView di dalam Drawer untuk menampilkan opsi tersebut.

2.2. Arahkan Pengguna
Implementasikan navigasi menggunakan Navigator.push dan Navigator.pushReplacement sesuai dengan instruksi pada checklist. Arahkan pengguna ke halaman utama atau halaman formulir tambah item sesuai dengan opsi yang dipilih di Drawer.


# Tugas 9

### Pengambilan Data JSON tanpa Membuat Model:

Ya, kita dapat melakukan pengambilan data JSON tanpa membuat model terlebih dahulu. Ini sering disebut sebagai "parsing dinamis" di Flutter, di mana kita mengakses nilai dalam map JSON secara langsung tanpa menggunakan model.

Contoh sederhana pengambilan data JSON tanpa model:

```dart
import 'dart:convert';

void main() {
  String jsonData = '{"name": "John", "age": 30}';
  Map<String, dynamic> userMap = json.decode(jsonData);

  print('Name: ${userMap['name']}');
  print('Age: ${userMap['age']}');
}
```

### Penggunaan CookieRequest:

`CookieRequest` adalah bagian dari pustaka `pbp_django_auth` yang mungkin kita gunakan untuk melakukan permintaan HTTP di Flutter. Menggunakan instance `CookieRequest` memungkinkan aplikasi untuk menyimpan dan mengelola cookie, yang penting untuk menyimpan informasi otentikasi antara permintaan HTTP. Instance `CookieRequest` dibagikan ke semua komponen agar mereka dapat berinteraksi dengan server Django dan menjaga keadaan otentikasi.

### Mekanisme Pengambilan Data dari JSON hingga Ditampilkan pada Flutter:

1. **Pengambilan Data JSON:**
   - Menggunakan metode seperti `http.get` atau `http.post` untuk mengambil data JSON dari server.

2. **Pemrosesan Data JSON:**
   - Menggunakan `json.decode` untuk mengubah string JSON menjadi objek Dart (map atau list).

3. **Penyimpanan Data:**
   - Menyimpan data dalam variabel atau struktur data yang sesuai.

4. **Tampilan di Flutter:**
   - Menggunakan widget seperti `ListView`, `GridView`, atau widget lainnya untuk menampilkan data JSON dalam antarmuka pengguna Flutter.

### Mekanisme Autentikasi dari Input Data Akun pada Flutter ke Django:

1. **Input Data Akun di Flutter:**
   - Pengguna memasukkan informasi akun seperti nama pengguna dan kata sandi melalui antarmuka pengguna Flutter.

2. **Permintaan Autentikasi ke Django:**
   - Menggunakan `CookieRequest` atau pustaka http untuk mengirim permintaan autentikasi ke server Django.

3. **Proses Autentikasi di Django:**
   - Django memeriksa informasi otentikasi dan memberikan respons sesuai.

4. **Tampilan Menu di Flutter:**
   - Jika autentikasi berhasil, Flutter menavigasi ke halaman menu atau menampilkan menu sesuai dengan respons dari Django.

### Widget yang Digunakan pada Tugas:

1. **`ShopFormPage`:**
   - Widget utama yang menangani formulir penambahan item toko.

2. **`LeftDrawer`:**
   - Widget yang menyajikan drawer (menu sisi kiri) pada aplikasi.

3. **`MyHomePage`:**
   - Widget utama halaman beranda aplikasi.

4. **`Item`:**
   - Model untuk merepresentasikan item toko.

5. **`SnackBar`:**
   - Widget untuk menampilkan pesan sementara di bagian bawah layar.

6. **`ElevatedButton`:**
   - Tombol yang meningkatkan (elevated) untuk menekan saat menyimpan data.

7. **`Form`:**
   - Widget yang membungkus elemen-elemen formulir di dalamnya.

8. **`TextFormField`:**
   - Widget untuk input teks dalam formulir.

### Deployment Proyek Django:

Pastikan proyek Django telah di-*deploy* di server atau platform yang dipilih. Pastikan server berjalan, basis data terhubung, dan endpoint-endpoint dapat diakses dari internet.

### Membuat Halaman Login pada Proyek Flutter:

1. **Tambahkan Dependensi:**
   - Pastikan dependensi seperti `http` dan `shared_preferences` sudah ditambahkan.

2. **Buat Form Login:**
   - Buat halaman atau widget untuk form login dengan elemen input seperti nama pengguna dan kata sandi.

3. **Kirim Permintaan Autentikasi ke Django:**
   - Gunakan `http.post` untuk mengirim permintaan autentikasi ke endpoint Django.

4. **Kelola Respons dan Penyimpanan Token:**
   - Kelola respons dari Django, terutama token otentikasi. Simpan token ini di `shared_preferences`.

### Integrasi Sistem Autentikasi Django dengan Proyek Flutter:

1. **Gunakan Token pada Permintaan Selanjutnya:**
   - Tambahkan token otentikasi pada header setiap permintaan HTTP ke Django setelah login.

2. **Kelola Sesi Otentikasi:**
   - Pastikan untuk menyimpan dan mengelola sesi otentikasi.

### Membuat Model Kustom Sesuai dengan Proyek Aplikasi Django:

1. **Buat Model Flutter:**
   - Buat model Flutter yang sesuai dengan model Django. Pastikan atribut dan tipe data cocok.

2. **Gunakan Model dalam Aplikasi Flutter:**
   - Gunakan model Flutter ini untuk merepresentasikan data di aplikasi Flutter.

### Membuat Halaman Daftar Semua Item:

1. **Gunakan FutureBuilder:**
   - Gunakan `FutureBuilder` untuk mengambil dan menampilkan daftar item dari endpoint JSON di Django.

2. **Tampilkan Informasi yang Dibutuhkan:**
   - Tampilkan nama, amount, dan description dari masing-masing item di halaman ini.

### Membuat Halaman Detail untuk Setiap Item:

1. **Navigasi dari Halaman Daftar Item:**
   - Tambahkan navigasi agar pengguna dapat menekan salah satu item di halaman daftar dan diarahkan ke halaman detail.

2. **Gunakan FutureBuilder untuk Detail Item:**
   - Gunakan `FutureBuilder` lagi untuk mengambil detail item dari endpoint JSON di Django.

3. **Tampilkan Seluruh Atribut Model Item:**
   - Tampilkan seluruh atribut pada model item di halaman detail.

4. **Tambahkan Tombol Kembali:**
   - Tambahkan tombol atau ikon untuk kembali ke halaman daftar item.
