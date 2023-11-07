# Sawi mobile 🧴🌬️✨🌸

> **Sawi mobile** adalah sebuah aplikasi mobile untuk membeli sayur-sayuran
### Daftar Tugas:
- **[Tugas 7](#tugas-7)**<br>

# Tugas 7
## **_Stateless_ dan _stateful widget_**
Stateless dan Stateful Widget adalah dua jenis widget yang umum digunakan dalam pengembangan aplikasi Flutter. Berikut adalah perbedaan utama antara Stateless dan Stateful Widget:

Stateless Widget:
- Widget yang di-build hanya dengan konfigurasi yang telah diinisiasi sejak awal.
- Widget yang tidak akan pernah berubah.
- Digunakan untuk membuat komponen yang statis dan tidak berubah.
- Tidak memiliki state internal yang dapat berubah seiring waktu.
- Tidak dapat menggunakan fungsi setState().

Stateful Widget:
- Widget yang dapat berubah dinamis.
- Digunakan untuk membuat komponen yang dapat berinteraksi atau merespons perubahan.
- Memiliki state internal yang dapat berubah seiring waktu.
- Dapat menggunakan fungsi setState() untuk memberitahu framework bahwa ada object yang berubah pada State, kemudian akan melakukan build ulang pada Widget tersebut.

Kesimpulannya, Stateless Widget digunakan untuk membuat komponen yang statis dan tidak berubah, sedangkan Stateful Widget digunakan untuk membuat komponen yang dapat berinteraksi atau merespons perubahan. Stateless Widget tidak memiliki state internal yang dapat berubah, sedangkan Stateful Widget memiliki state internal yang dapat berubah seiring waktu dan dapat menggunakan fungsi setState() untuk memberitahu framework bahwa ada object yang berubah pada State, kemudian akan melakukan build ulang pada Widget tersebut.

<img width="969" alt="SJURB" src="https://github.com/yhogaa/FragranceGate/assets/113284837/f76d4c23-398d-412e-a3bf-974c11e8f03a">

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
