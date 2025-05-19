# Advprog Module 10 Tutorial Part 2 - Broadcast Chat
Hadyan Fachri\
2306245030\
Advprog A

# Reflection
![alt text](image.png)

Dari gambar di atas, setelah menjalankan satu server dan tiga client, dapat disimpulkan bahwa client hanya dapat berjalan jika server sudah dijalankan terlebih dahulu, karena client perlu terhubung ke endpoint WebSocket yang disediakan oleh server. Ketika salah satu client mengirimkan pesan, pesan tersebut akan diterima oleh server, lalu server akan membroadcast pesan tersebut ke semua client yang sedang terhubung, termasuk client pengirim jika masih aktif. 

Hal ini dimungkinkan karena setiap client yang berhasil terhubung akan otomatis menjadi subscriber pada channel broadcast yang dikelola oleh server. Meskipun server tidak menyimpan daftar client secara eksplisit, pesan yang dikirim melalui channel akan diterima oleh semua client yang masih terhubung. Dengan demikian, server berperan sebagai perantara yang menerima pesan dari client dan menyebarkannya kembali ke semua client lainnya.