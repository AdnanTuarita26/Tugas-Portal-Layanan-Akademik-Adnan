# Portal Layanan Akademik (Tugas Pertemuan 5)

Halaman web client responsif dan aksesibel untuk studi kasus Portal Layanan Akademik, dibuat tanpa JavaScript.

- Nama: Adnan Fahri Jauhari Putra Tuarita
- NIM: 202451051
- Mata kuliah: Membangun Web, Universitas Pattimura
- URL aplikasi: https://adnantuarita26.github.io/Tugas-Portal-Layanan-Akademik-Adnan/
- Repositori: https://github.com/AdnanTuarita26/Tugas-Portal-Layanan-Akademik-Adnan

## Struktur berkas
- `index.html`: header, nav, main (intro, 3 kartu layanan, form permohonan), footer
- `styles.css`: CSS mobile-first dengan Grid/Flexbox dan focus ring terlihat
- `uji-responsif.html`: halaman bantu untuk menampilkan situs pada lebar 360, 768, dan 1280 px
- Screenshot bukti pengujian

## Keputusan desain
- Mobile-first: dimulai dari satu kolom, breakpoint 40em dan 64em dipasang saat konten mulai lapang.
- Elemen native lebih dulu (label, fieldset/legend, button) sebelum ARIA.
- Logo di header bersifat dekoratif (`aria-hidden="true"`), jadi tidak diberi teks alternatif.
- Ada skip link, focus ring emas yang jelas, dan target sentuh minimal 44 px.
- Memakai font sistem, jadi tidak ada resource eksternal yang bisa gagal dimuat.

## Bukti pengujian
Pengujian dilakukan dari perangkat mobile karena tidak tersedia laptop. Alat yang dipakai: halaman uji bantu (`uji-responsif.html`) dan Lighthouse melalui PageSpeed Insights, bukan panel Browser DevTools di desktop.

| Pemeriksaan | Alat | Hasil | Bukti |
|---|---|---|---|
| Responsif 360 px | uji-responsif.html | Tidak ada horizontal scroll (lebar konten 360 px, viewport 360 px). Satu kolom, menu membungkus ke baris kedua, teks terbaca. | Screenshot_2026-10-29-15-25-46-117_com_android_chrome.jpg |
| Responsif 768 px | uji-responsif.html | Tidak ada horizontal scroll (lebar konten 768 px, viewport 768 px). Tiga kartu layanan berdampingan. | Screenshot_2026-10-29-15-25-46-117_com_android_chrome.jpg dan Screenshot_2026-10-29-15-25-51-641_com_android_chrome.jpg |
| Responsif 1280 px | uji-responsif.html | Tidak ada horizontal scroll (lebar konten 1280 px, viewport 1280 px). Tiga kartu berdampingan, form dua kolom, konten dibatasi lebar maksimum. | Screenshot_2026-10-29-15-25-51-641_com_android_chrome.jpg |
| Aksesibilitas (mobile) | PageSpeed Insights / Lighthouse | Skor 100/100 | Screenshot_2026-10-29-15-14-46-664_com_android_chrome.jpg |
| Aksesibilitas (desktop) | PageSpeed Insights / Lighthouse | Skor 100/100 | Screenshot_2026-10-29-15-16-08-310_com_android_chrome.jpg |

### Temuan dan perbaikan
- Setelah diunggah ke GitHub, `styles.css` berada satu folder dengan `index.html`, sehingga tautan stylesheet diubah dari `css/styles.css` menjadi `styles.css`. Tanpa perubahan itu, halaman tampil tanpa gaya.
- Lighthouse (mobile dan desktop) memberi skor 100 untuk Performa, Aksesibilitas, Praktik Terbaik, dan SEO.
- Insight performa mencatat pemblokiran render oleh `styles.css` (perkiraan hemat 140 md di mobile). Keputusan: CSS tetap dipisah sesuai ketentuan tugas, dan skor performa tetap 100.
- Insight cache efisien (hemat 2 KiB) berasal dari pengaturan server GitHub Pages, bukan dari kode halaman.
- Lighthouse menandai 10 item aksesibilitas untuk diperiksa manual (urutan tab, fokus keyboard, dan sejenisnya). Item itu tidak dihitung otomatis, jadi diperiksa secara manual (lihat Keterbatasan).

### Keterbatasan
- Pemeriksaan Elements, Network, dan accessibility tree pada Browser DevTools desktop belum dilakukan. Sebagai gantinya dipakai Lighthouse dan halaman uji bantu di atas.
- Uji keyboard (Tab) dan validasi email dilakukan manual pada halaman yang sudah dipublikasikan. (ISI hasil kalau sudah dicoba)
