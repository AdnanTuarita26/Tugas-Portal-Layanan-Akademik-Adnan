# Portal Layanan Akademik (Tugas Pertemuan 5)

Halaman web client responsif dan aksesibel, tanpa JavaScript.

- Nama: Adnan Fahri Jauhari Putra Tuarita
- NIM: 202451051
- Mata kuliah: Membangun Web, Universitas Pattimura

## Struktur
- `index.html`: header, nav, main (intro, 3 kartu layanan, form), footer
- `css/styles.css`: CSS mobile-first, Grid/Flexbox, focus ring terlihat
- `evidence/`: screenshot bukti DevTools

## Keputusan desain
- Mobile-first: satu kolom dulu, breakpoint 40em dan 64em dipasang saat konten mulai lapang.
- Elemen native lebih dulu (label, fieldset/legend, button), tanpa ARIA berlebihan.
- Ikon logo di header dekoratif (`aria-hidden="true"`), jadi tidak diberi teks alternatif.
- Skip link, focus ring emas, target sentuh minimal 44px.
- Font sistem, jadi tidak ada resource eksternal yang bisa gagal dimuat.

## Bukti pengujian DevTools (isi setelah kamu uji sendiri)
| Pemeriksaan | Hasil | File bukti |
|---|---|---|
| Responsive 360 px | Tidak ada horizontal scroll | evidence/01-360.png |
| Responsive 768 px | Kartu 2-3 kolom, terbaca | evidence/02-768.png |
| Responsive 1280 px | Form 2 kolom, terbaca | evidence/03-1280.png |
| Elements/Inspector | Landmark dan heading h1 > h2 > h3 benar | evidence/04-elements.png |
| Network (reload) | Semua resource status 200, tidak ada yang gagal | evidence/05-network.png |
| Accessibility tree | Label terhubung ke input, landmark terbaca | evidence/06-a11y.png |
| Keyboard (Tab) | Semua kontrol terjangkau, fokus terlihat | evidence/07-focus.png |
| Validasi email | Format salah ditolak browser | evidence/08-validasi.png |
