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

### **Latihan Activity**
- *android:layout_width="match_parent"* : mengesuaikan konten di dalamnya
- *android:layout_height="wrap_content"* : menyesuaikan layar device
- *android:padding="16dp"* : padding. jarak dari isi konten ke latar belakangnya
- *android:margin="16dp"* : margin. jarak dari komponen ke komponen lain di luarnya
- sp : scale independent pixel. ukuran text
- dp : destiny indeoendent pixel. semua ukuran komponen selain text
