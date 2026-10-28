# World BattleRoyale — Android 2D Turn-Based Strategy (v1.1)

Game strategi offline berbasis giliran dengan peta dunia vektor berdasarkan geometri negara Natural Earth.

## Fitur
- Peta vektor dunia dengan batas negara geografis (Equal Earth projection), bukan grid/hexagon.
- 177 unit negara/wilayah dari Natural Earth low-resolution dataset; bentuk garis pantai dan pulau mengikuti geometri sumber pada skala global.
- Bendera pemilik wilayah ditampilkan di atas peta; warna wilayah berubah sesuai pemilik setelah penaklukan.
- Zoom, geser, dan pilih negara di peta.
- Roulette attacker dan defender 5,2 detik yang menyorot negara yang sedang dilewati di peta.
- Defender dipilih dari tetangga darat yang masih independen; jika tidak ada, kandidat negara berjarak kurang dari 100 km dari geometri wilayah (berdasarkan titik geometri terdekat).
- Tiga dadu 6 sisi per negara, diputar satu per satu dengan animasi sekitar 0,8 detik.
- Skor = jumlah 3 dadu × multiplier populasi. Multiplier naik 0,1× tiap kelompok 10 juta penduduk, mulai 1,0× dan maksimum 1,5×. Hasil seri memicu lempar ulang.
- Pemenang mengambil semua unit wilayah yang dimiliki negara kalah; populasi wilayah yang dikuasai dijumlahkan untuk multiplier berikutnya.
- Log, simpan progres lokal, reset, dan kontrol giliran.
- Data peta disematkan di aplikasi sehingga peta/gameplay dasar dapat berjalan offline.

## Batasan data
Peta memakai Natural Earth low-resolution yang tersedia di lingkungan build (177 unit peta). Ini jauh lebih realistis daripada tile/hexagon, tetapi bukan peta 1:10m; negara mikro dan pulau kecil tertentu tidak terwakili dengan detail penuh. Geometri Natural Earth juga menggeneralisasi garis pantai dan menggunakan kebijakan batas de facto pada beberapa wilayah sengketa. Populasi pada dataset geografis merupakan estimasi historis, bukan angka real-time atau sumber statistik terbaru. Untuk rilis yang menargetkan seluruh negara berdaulat dan detail lebih tinggi, ganti dataset dengan Natural Earth 1:50m atau 1:10m dan perbarui data populasi dengan sumber resmi.

## Sumber data
Natural Earth, `naturalearth_lowres` country geometry (public domain). Peta diubah ke SVG path untuk rendering interaktif offline. Natural Earth: https://www.naturalearthdata.com/

## Build APK
Lingkungan ini tidak memiliki Android SDK/Gradle sehingga APK belum dikompilasi di sini. Gunakan GitHub Actions workflow `Build Android APK`, atau buka proyek di Android Studio (JDK 17 dan Android SDK 35) lalu jalankan `assembleDebug`. APK hasil build berada di `app/build/outputs/apk/debug/app-debug.apk`.
