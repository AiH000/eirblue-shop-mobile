# eirblue_shop

Tugas 7

1. Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.
    Stateful Widget adalah widget yang state-nya dapat berubah berkali-kali setelah di-built. Contohnya, CheckBox, RadioButton, dan Form.
    Stateless Widget adalah widget yang state-nya tidak dapat diubah oleh user. Contohnya Text dan Icon. 
    Perbedaan dari keduanya, yaitu jika widget berubah ketika user berinteraksi dengan widget tersebut maka widget tersebut stateful widget, sedangkan jika tidak dapat berubah widget tersebut adalah stateless widget.

2. Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.
    Card: Sebagai container untuk menampilkan sejumlah informasi
    Icon: Menyediakan ikon yang tersedia langsung untuk tampilan aplikasi.
    Column: Menampilkan children dalam array vertikal
    Container: Sebagai parent widget yang dapat memiliki sejumlah child widget dan juga mengelola lebar, tinggi, padding, background color, dan sebagainya.
    Text: Menampilkan sebuah string
    Scaffold: Menyediakan API untuk menunjukkan drawers dan bottom sheets.
    AppBar: Fixed-height widget di bagian atas screen
    Theme: Untuk mendeskripsikan warna dan pilihan tipografi aplikasi
    Padding: Memperkecil layout constraint child
    Row: Menyebabkan child memenuhi ruang horizontal yang tersedia 
    SizedBox: Box dengan ukuran yang spesifik yang jika diberikan pada child, child akan dipaksa memiliki ukuran yang spesifik.
    Center: Membuat child berada di tengah dirinya
    GridView: Mengatur layout secara 2D
    MediaQuery: Menetapkan subtree di mana media queries diselesaikan berdasarkan data yang diberikan.
    SnackBar: Mengeluarkan display dalam waktu singkat pada bagian bawah layar.
    MaterialApp: Membungkus sejumlah widget yang biasa dibutuhkan untuk desain Material aplikasi.

3. Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.
    Method setState() berfungsi untuk memberitahu framework bahwa internal state dari suatu object telah berubah.
    Variabel yang dapat terdampak dari fungsi tersebut adalah State objects.

4. Jelaskan perbedaan antara const dengan final.
    Variabel const memiliki value yang harus diketahui saat compile time dan tidak dapat diubah ketika runtime.
    Variabel final memiliki value yang dapat di-assign ketika runtime, tetapi hanya dapat di-assign sekali, dan valuenya tidak dapat diubah.

5. Jelaskan bagaimana cara kamu mengimplementasikan checklist-checklist di atas.
    - Membuat sebuah program Flutter baru dengan tema E-Commerce yang sesuai dengan tugas-tugas sebelumnya.
        : Menjalankan command "flutter run eirblue_shop"
    - Membuat tiga tombol sederhana dengan ikon dan teks untuk:
        - Melihat daftar produk (Lihat Daftar Produk)
        - Menambah produk (Tambah Produk)
        - Logout (Logout)
        :   - Membentuk class ItemHomePage yang mengambil parameter String nama dan Icon icon
            - Menambahkan list item ItemHomePage dengan nama "Lihat Daftar Produk", "Tambah Produk", dan "Logout" dengan icon yang sesuai pada class MyHomePage
            - Membentuk class ItemCard yang menerima parameter item untuk menampilkan kartu dengan nama dan ikon sesuai item
            - Menambahkan item sebagai children dari GridView di MyHomePage dengan return sebagai ItemCard
    - Mengimplementasikan warna-warna yang berbeda untuk setiap tombol (Lihat Daftar Produk, Tambah Produk, dan Logout).
        : Menambahkan parameter color pada ItemHomePage yang selanjutnya dipakai sebagai color Material dengan Widget build() di class ItemCard
    - Memunculkan Snackbar dengan tulisan:
        - "Kamu telah menekan tombol Lihat Daftar Produk" ketika tombol Lihat Daftar Produk ditekan.
        - "Kamu telah menekan tombol Tambah Produk" ketika tombol Tambah Produk ditekan.
        - "Kamu telah menekan tombol Logout" ketika tombol Logout ditekan.
        : Tambahkan event handler onTap() pada class ItemCard yang akan menjalankan method showSnackBar(SnackBar(content: Text("Kamu telah menekan tombol ${item.name}!")))