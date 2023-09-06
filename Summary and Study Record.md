## 29 August 2023
### **Teory Activity**
- Pengertian: salah satu komponen android
- Fungsi: menampilkan user interface
- MainActivity: berkas yang mewarisi kelas activity untuk menampilkan layout dan mengelola interaksi
- Activity: terdapat beberapa activity dalam aplikasi dengan tugas yang berbeda-beda. Setiap activity harus terdaftar pada AndroidManifest.xml
- onCreate: activity dibuat
- onStart: activity dijalankan
- onResume: activity sedang berjalan
- onPause: beberapa activity yang tidak terlihat karena pop-up/dialog
- onStop: activity tidak terlihat sama sekali karena berpindah ke aplikasi lain
- onRestart: kembali ke activity sebelumnya
- onDestroyed: juga dipanggil ketika terjadi perubahan konfigurasi seperti orientasi layar, keyboard availability, dan perubahan bahasa
- onSaveInstanceState: dipanggil ketika berpindah ke activity lain untuk menyimpan informasi

## 31 August 2023
### **Latihan Activity**
- *android:layout_width="match_parent"* : mengesuaikan konten di dalamnya
- *android:layout_height="wrap_content"* : menyesuaikan layar device
- *android:padding="16dp"* : padding. jarak dari isi konten ke latar belakangnya
- *android:margin="16dp"* : margin. jarak dari komponen ke komponen lain di luarnya
- sp : scale independent pixel. ukuran text
- dp : destiny indeoendent pixel. semua ukuran komponen selain text

## 1 September 2023
### **Intent**
- Definition: A mechanism to do an action and comunication between apps component (activity, service, broadcast receiver)
- Penggunaan Umum Intent: Memindahkan activity to another activity, run service background, send broadcast object to apps
- Bentuk Intent: Explicit (move to another activity), Implicit (run another application fitur)

## 3 September 2023 (51% - 71%)
### **View and ViewGroup**
- View: Kumpulan komponen apk: button, text, image, checkbox, radio button, grid view, recyclear view (tampilan list)
- [ViewGroup](https://developer.android.com/develop/ui/views/layout/declaring-layout): Kumpulan view. Beberapa penempatan komponen View pada ViewGroup adalah sebagai berikut:
  - [LinearLayout](https://developer.android.com/develop/ui/views/layout/linear): komponen disusun secara vertical dan horizontal. Memiliki atribut weight.
  - [RelativeLayout](https://developer.android.com/develop/ui/views/layout/linear): ada yang relatif dengan komponen di dalamnya, ada yang relatif dengan parent layoutnya.
  -  [ConstraintLayout](https://developer.android.com/develop/ui/views/layout/constraint-layout):  memiliki banyak fitur untuk mengatur posisi komponen, diantaranya:
      - relative positioning: komponen dengan komponen
      - center positioning: memposisikan di tengah
      - guideline: garis pembantu yang tidak terlihat
      - barrier: posisi komponen mengikuti posisi komponen lainnya
      - chain: sekumpulan komponen diatur secara linear, diantaranya:
        - spread: setiap elemen menyebar
        - spread inside: setiap elemen menyebar dengan elemen paling ujungnya menempel pada batas ujungnya
        - weighted: beberapa konten disetel ke match constraint, maka mereka akan membagi ruang yang tersedia
        - packed: elemen akan menyatu dan dikemas bersama.
   - [FrameLayout](https://developer.android.com/reference/android/widget/FrameLayout.html): komponen saling menumpuk
   - [TableLayout](https://developer.android.com/guide/topics/ui/layout/grid.html): disusun secara baris dan kolom
   - [ScrollView](https://developer.android.com/reference/android/widget/ScrollView.html): komponen dapat digeser
- Mengganti icon apps: res -> new -> image asset
- Latihan Membuat LinearLayout, RelativeLayout, FrameLayout, dan TableLayout
- Inspector: Komponen untuk menganalisis tampilan. Caranya adalah Tools -> Layout Inspector

## 4 September 2023 (71% - 97%)
### **Style and Theme**
- Style: kumpulan properti (bold, warna, margin, dll) yang diimplementasi ke dalam komponen
- Theme: Style yang diterapkan untuk activity

### **Recyclear View**
- Merupakan kelas yang dari android yang di dalamnya terdapat beberapa jenis LayoutManager, yaitu LinearLayoutManager, GridLayoutManager, StaggeredGridLayoutManager (tampilan yang menyesuaikan tinggi setiap item).
- Adapter merupakan kelas untuk menghubungkan data resource dengan kode. Terdapat beberapa method di dalamnya:
  - onCreateViewHolder(): digunakan untuk membuat ViewHolder baru yang terhubung dengan layout item.
  - onBindViewHolder(): digunakan untuk menetapkan data source ke dalam ViewHolder sesuai dengan posisinya.
  - getItemCount(): digunakan untuk menetapkan ukuran dari jumlah data yang ingin ditampilkan.

### **Latihan Membuat Recyclear View**
1. Menambahkan <androidx.recyclerview.widget.RecyclerView ke dalam activity_main
2. Membuat item_row_hero dengan (<androidx.cardview.widget.CardView) pada layout resource file untuk membuat tampilan card berisi foto, nama, dan deskripsi.
3. Menambahkan resource string
4. Membuat data class bernama hero berisi variabel name dan description yang bertipe String dan photo bertipe Int yang di-parcelize
5. Membuat kelas ListHeroAdapter yang berisi method
   - onCreateViewHolder untuk mengambil layout xml dan mengubahnya menjadi kode
   - onBindViewHolder mengisi atau memperbarui data dalam daftar
   - getItemCount untuk menentukan berapa banyak elemen yang akan ditampilan dalam daftar
6. Membuah kelas ListViewHolder untuk mengakses elemen tampilan dalam method onBindViewHolder sehingga dapat menampilkan data yang sesuai
7. Membuat variabel private lateinit var rvHeroes yang diinisialisasikan pada fun onCreate
8. Memanggil method getListHeroes dan showRecyclerList pada onCreate
9. Membuat method getListHeroes dan mengambil data dari data class Hero dengan resource strings.xml
10. Membuat method showRecyclerList untuk mengadaptasi (adapter) RecyclearView
11. Menambahkan holder.itemView.setOnClickListener pada method onBindViewHolder yang berada pada kelas ListHeroAdapter untuk menentukan tindakan ketika salah satu item diklik
12. Membuat interface OnItemClickCallback pada method onBindViewHolder yang berisi fungsi onItemClicked
13. membuat method showSelectedHero yang berisi kode untuk menampilkan Toast yang memiliki 3 buah parameter yaitu context, text, dan juga durasi toast.
14. Membuat Android Resource Directory baru bernama menu berisi menu_main.xml yang di dalamnya terdapat dua buah item yang bernama Grid dan juga List
15. Mengimplementasi menu_main.xml pada fungsi onCreateOptionsMenu dengan objek menuInflater dan method inflate untuk mengkonversi xml
16. Membuat fungsi berisi pencabangan ketika menu List dan Grid diklik

### **Latihan Implementasi Library Glide**
1. Tambahkan dependencies implementation("com.github.bumptech.glide:glide:4.15.0") pada build.gradle lalu klik sync
2. Ubah data_photo pada strings.xml menjadi  <item>https://upload.wikimedia.org/wikipedia/commons/8/87/Ahmad_Dahlan.jpg</item> artinya mengambil gambar dari internet untuk ditampilkan pada ImageView
3. Ubah tipe data pada data class Hero properti photo dari Int menjadi String
4. Ubah method getListHeroes pada MainActivity, dataPhoto menjadi getStringArray
5. Ubah kode holder.imgPhoto pada method onBindViewHolder menjadi Glide.with holder untuk menampilkan foto dari URL pada ImageView yang sesuai
6. Aktifkan permission <uses-permission android:name="android.permission.INTERNET" /> pada Manifest -> AndroidManifest.xml untuk mengambil data dari internet  

### **View Binding**
- Merupakan fitur untuk binding (menghubungkan elemen ke dalam aplikasi) sebuah properti ke elemen view

### **Exam**
- Manakah yang bukan opsi untuk menambahkan aksi onClick pada RecyclerView? 
Langsung memanggil fungsi setOnItemClickListener dari RecyclerView.

## 5 September 2023 (97% - 100%)

### **Final Exam**

Membuat aplikasi Kdrama Sinopsis dengan 3 activity, dan parcelable untuk mengirim data secara keseluruhan






