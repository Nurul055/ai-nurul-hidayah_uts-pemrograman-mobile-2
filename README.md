# ai-nurul-hidayah_uts-pemrograman-mobile-2
Jelaskan perbedaan Cubit Bloc dalam arsitektur Flutter
Perbedaan Cubit dan Bloc: Perbedaan utama antara Cubit dan Bloc terletak pada cara mereka memproses perubahan state. Cubit adalah alat yang lebih ringan dan sederhana; ia mengubah state secara langsung hanya dengan memanggil fungsi dan kemudian emit() state baru. Sebaliknya, Bloc menggunakan konsep Events sebagai input untuk memicu perubahan state. Events diproses melalui mapEventToState atau on<Event> sebelum state baru di-emit. Bloc lebih baik untuk logika kompleks yang membutuhkan keterlacakan (traceability) tinggi, sedangkan Cubit cocok untuk logika sederhana dengan boilerplate yang minimal.

Mengapa penting untuk memisahkan antara model data, logika bisnis, dan UI dalam pengembangan aplikasi Flutter?
Pemisahan Arsitektur (Model, Logic, UI): Memisahkan Model (data), Logika Bisnis (Cubit/Bloc), dan UI (Widget) adalah prinsip arsitektur modular yang krusial. Pemisahan ini meningkatkan Testability karena logika dapat diuji tanpa me-render UI, meningkatkan Maintainability karena perubahan pada satu lapisan (misalnya, UI) tidak merusak yang lain (logika bisnis), dan mendorong Scalability yang lebih baik dalam tim besar.


Sebutkan dan jelaskan minimal tiga state yang mungkin digunakan dalam CertCubit beserta fungsinya.
Minimal Tiga State CartCubit: Tiga state minimal yang mungkin digunakan dalam CartCubit adalah CartInitial (keranjang kosong/baru dibuat), CartLoaded (berisi daftar List<CartItem> yang sedang aktif dan siap ditampilkan), dan CartError (mengindikasikan kegagalan, misalnya saat gagal memuat data keranjang dari storage). State CartLoaded sangat penting karena memicu pembaruan tampilan secara real-time setiap kali produk ditambahkan, dihapus, atau kuantitasnya diubah.


