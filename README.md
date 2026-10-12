# Mirama Food Mart — Static Website for Vercel

Website statis multi-halaman menggunakan HTML, CSS, dan JavaScript murni. Tidak memerlukan build command, Node package, database, atau backend untuk demo ini.

## Halaman
- Beranda — `/`
- Produk — `/produk`
- Makanan Khas Daerah — `/makanan-khas-daerah`
- Promo — `/promo`
- Tentang Kami — `/tentang-kami`
- Lokasi & Kontak — `/lokasi-kontak`
- Kredit Foto — `/kredit-foto`

## Fitur
- Responsive desktop, tablet, dan mobile
- Navigasi antarhalaman serta pencarian produk
- Filter kategori, filter makanan khas daerah, dan pengurutan harga
- Keranjang belanja sederhana dengan `localStorage`
- Tombol tanya pesanan via WhatsApp (tanpa nomor resmi, WhatsApp terbuka dengan pesan siap kirim dan pengguna memilih kontak)
- Link antarhalaman memakai path relatif (`produk.html`), sehingga bisa dibuka langsung, lewat Live Server, maupun di Vercel
- Embed pencarian Google Maps dan tautan ke Google Maps
- SEO title/description per halaman

## Deploy ke Vercel
1. Ekstrak ZIP ini.
2. Upload folder project ke repository GitHub.
3. Di Vercel pilih **Add New → Project**, lalu impor repository tadi.
4. Framework Preset pilih **Other** (atau Static Site jika tersedia).
5. Build Command dan Output Directory dapat dikosongkan/default karena file HTML ada di root project.
6. Klik **Deploy**.

Alternatif: dengan Vercel CLI terpasang, jalankan `vercel` dari folder proyek, ikuti prompt, lalu `vercel --prod` untuk production.

## Hal yang WAJIB diperbarui sebelum go-live
1. Buka `assets/js/app.js`, isi konstanta `WHATSAPP_NUMBER` dengan nomor WhatsApp bisnis dalam format internasional tanpa tanda `+`, spasi, atau tanda hubung (contoh format: `62812xxxxxxxx`).
2. Validasi alamat, jam buka, akun media sosial, dan informasi kontak resmi toko.
3. Ubah daftar produk di array `products` pada `assets/js/app.js` agar nama, foto, varian, harga, satuan, dan stok sesuai kondisi toko.
4. Kartu promo hanya konsep contoh—sesuaikan dengan promo resmi dan masa berlakunya.
5. Foto camilan khas Purwokerto/Banyumas disimpan di `assets/img/snacks/` dan berasal dari Wikimedia Commons (CC BY / CC BY-SA / CC0). Atribusi wajib tetap ditampilkan di halaman `kredit-foto.html`. Jika foto diganti dengan foto milik Mirama, perbarui juga halaman kredit tersebut.

## Catatan
- Keranjang tersimpan lokal pada browser pengunjung; tidak disinkronkan antar-perangkat dan bukan sistem order backend.
- Harga pada proyek ini adalah data contoh untuk demo UI, bukan daftar harga resmi Mirama Food Mart.
- Google Maps menggunakan URL pencarian lokasi. Pastikan pin yang tepat sebelum publikasi.
