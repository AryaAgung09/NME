# PT Nusantara Mineral Energi (NME) — Website Korporat

![Versi proyek](https://img.shields.io/badge/versi-0.1.0-blue)
![Next.js](https://img.shields.io/badge/Next.js-16.4.3-black)
![React](https://img.shields.io/badge/React-19.3.0-149ECA)
![Lisensi](https://img.shields.io/badge/lisensi-belum_ditetapkan-lightgrey)

Website korporat demonstrasi untuk PT Nusantara Mineral Energi (NME), dibuat sebagai pengalaman web berbahasa Indonesia dan Inggris. README ini ditujukan untuk developer, reviewer, dan pembaca portofolio yang ingin memahami fitur serta menjalankan project.

> **Catatan:** Ini adalah project demonstrasi. Informasi perusahaan, personel, proyek, angka, dan target operasional di dalamnya bersifat ilustratif dan bukan data terverifikasi untuk penggunaan bisnis.

## Fitur

- Halaman beranda dengan bagian profil, bisnis, proyek, keberlanjutan, investor, berita, dan karier.
- Halaman profil perusahaan, sejarah, dan tim.
- Lima halaman detail lini bisnis dan enam halaman detail proyek.
- Halaman hubungan investor, keberlanjutan, media/informasi, karier, dan kontak.
- Konten antarmuka Indonesia/Inggris melalui pemilih bahasa di sisi klien.
- Interaksi dan animasi menggunakan GSAP, Framer Motion, dan Lenis.
- Formulir kontak dengan validasi di browser dan API.

### Screenshot dan demo

- Screenshot: **TODO: tambahkan screenshot halaman utama dan halaman internal.**
- Demo langsung: **TODO: tambahkan URL demo jika tersedia.**

## Tech stack

| Area | Teknologi |
|---|---|
| Framework | Next.js 16.4.3 (App Router) |
| UI | React 19.3.0 |
| Bahasa | TypeScript |
| Styling | Tailwind CSS 4 dan CSS Modules |
| Animasi | GSAP, `@gsap/react`, Framer Motion, Lenis |
| Visualisasi peta | `d3-geo`, `react-simple-maps` |
| Komponen tambahan | Swiper, Lucide React, `react-countup` |
| Lint | ESLint 9 |
| Package manager | npm (lockfile v3) |

## Prasyarat

- Node.js **20.9.0 atau lebih baru** (batas minimum dari Next.js yang digunakan).
- npm.
- Database tidak diperlukan untuk menjalankan versi saat ini.
- Koneksi internet diperlukan untuk memuat gambar dan video yang di-host oleh layanan eksternal.

## Instalasi dan setup

```bash
git clone https://github.com/AryaAgung09/NME.git
cd NME
npm ci
```

Jalankan server pengembangan:

```bash
npm run dev
```

Buka [http://localhost:3000](http://localhost:3000).

## Konfigurasi environment

Saat ini project tidak memerlukan variabel environment dan tidak menyediakan file `.env.example`. Tidak ada database atau layanan email yang dikonfigurasi.

Jangan menambahkan kredensial ke source control. Jika integrasi layanan eksternal ditambahkan kemudian, dokumentasikan variabel yang dibutuhkan di sini dan sediakan `.env.example` tanpa nilai rahasia.

## Menjalankan dan memeriksa project

| Perintah | Fungsi |
|---|---|
| `npm run dev` | Menjalankan server pengembangan Next.js |
| `npm run lint` | Menjalankan ESLint |
| `npm run build` | Membuat build produksi |
| `npm run start` | Menjalankan build produksi yang sudah dibuat |

Untuk menjalankan versi produksi secara lokal:

```bash
npm run build
npm run start
```

Repository ini belum mengonfigurasi workflow CI, sehingga belum ada badge status build. `package.json` juga belum menyediakan script atau suite test otomatis; gunakan lint dan build untuk pemeriksaan dasar.

### Formulir kontak

Formulir mengirim `POST /api/kontak`. Endpoint memeriksa field wajib, format email, dan panjang pesan minimum, lalu mencatat metadata pengiriman ke console server. Endpoint **tidak** mengirim email atau menyimpan pesan ke database.

## Struktur folder

```text
src/
├── app/                 # Rute halaman dan API Next.js
│   └── api/kontak/      # Endpoint formulir kontak
├── components/
│   ├── company/         # Komponen halaman perusahaan
│   ├── home/            # Bagian-bagian halaman beranda
│   └── motion/          # Komponen animasi dan interaksi
└── data/                # Konten, media, dan terjemahan ID/EN
public/                  # Aset statis
```

Konten halaman dikelola dalam berkas TypeScript di `src/data/`; project ini tidak menggunakan CMS.

## Rute utama

| Rute | Isi |
|---|---|
| `/` | Beranda |
| `/tentang-kami` | Profil perusahaan |
| `/tentang-kami/sejarah-kami` | Sejarah |
| `/tentang-kami/tim-kami` | Tim |
| `/bisnis-kami` dan `/bisnis-kami/[slug]` | Ikhtisar dan detail lini bisnis |
| `/proyek` dan `/proyek/[slug]` | Portofolio dan detail proyek |
| `/hubungan-investor` | Hubungan investor |
| `/keberlanjutan` | Keberlanjutan |
| `/media-informasi` dan `/media-informasi/[slug]` | Media dan detail konten |
| `/karir` | Informasi karier |
| `/kontak` | Informasi dan formulir kontak |
| `POST /api/kontak` | Endpoint formulir kontak |

## Kontribusi

1. Buat fork atau branch untuk perubahan.
2. Pastikan perubahan sesuai dengan implementasi dan tidak memasukkan data rahasia.
3. Jalankan `npm run lint` dan `npm run build`.
4. Buka pull request dengan ringkasan perubahan dan hasil pemeriksaan.

## Lisensi

Belum ada file lisensi di repository ini. **TODO: tentukan lisensi project sebelum mengizinkan penggunaan atau distribusi ulang.** Aset eksternal memiliki ketentuan lisensi masing-masing; sumber dan keterangan aset tercantum di `src/data/media.ts`.

## Kontak dan kredit

- Repository: [AryaAgung09/NME](https://github.com/AryaAgung09/NME)
- Kontak maintainer: **TODO: tambahkan alamat atau kanal kontak yang ingin dipublikasikan.**
- Gambar dan video: sumber eksternal Pexels dan Unsplash; lihat komentar sumber pada `src/data/media.ts`.
