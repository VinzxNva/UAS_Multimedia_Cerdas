Fungsi / Fitur : 
1. Berfungsi untuk Melakukan otomasi pemindahan berkas dan konversi format anotasi dari XML ke format YOLO
2. Mengidentifikasi status ruang parkir menjadi tiga kelas: free, not_free, dan partially_free
3. Menampilkan hasil deteksi secara langsung, yang mencakup bounding box dan label status pada gambar.
Instalasi :
1.menggunakan Google Colab untuk akses GPU yang optimal. Gunakan runtime T4
2.buat folder parkir dan dataset didalam folder content pada collab
3. pada folder parkir upload annotations.xml ini berisi data labeling dari foto yang sudah di format menggunakan CVAT atau juga bisa menggunakan roboflow.
Tambahkan folder didalm tabel parkir dengan nama images lalu tambahkan foto yang akan digunakan tadi
4. lalu jalankan kode ddari awal mulai dari !pip install ultralytics dan seterusnya
Cara Kerja :
1.krip melakukan iterasi pada folder sumber untuk membaca citra dan mengekstrak koordinat polygon dari file XML,
kemudian dikonversi menjadi format koordinat pusat dan dimensi agar bisa terbaca oleh YOLO.
2.Membuat file data.yaml yang berfungsi sebagai pemetaan direktori dataset dan kelas objek bagi model YOLO.
3.Model dilatih untuk mengenali pola visual ruang parkir dengan resolusi input 640x640 piksel.
4.Melakukan pengujian pada gambar dengan confidence threshold sebesar 0.25
Hasil :
1. Hasil akan bisa dilihat pada collab langsung jika sudah menjalankan semua kode dari awal
