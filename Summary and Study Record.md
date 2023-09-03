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

## 3 September 2023 (51% - )

### **View and ViewGroup Theory**

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







