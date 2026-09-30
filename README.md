# Praktikum 2 - HTML Lanjutan (Lab2Web)

Repositori ini memuat implementasi materi praktikum pemrograman web mengenai HTML lanjutan, meliputi pembuatan tabel terstruktur, form interaktif dengan validasi dasar, penggunaan elemen semantik dokumen, integrasi multimedia audio dan video, serta proyek mini pembuatan halaman biodata mahasiswa.

> ℹ️ **Catatan Dokumentasi Tangkapan Layar (Screenshots)**:
> 
> Seluruh bukti tangkapan layar (*screenshot*) hasil tampilan dan eksekusi program pada peramban (*browser*) untuk setiap tahapan latihan dan proyek mini telah disusun secara rinci di dalam **berkas laporan praktikum** yang diserahkan secara terpisah melalui tautan Google Drive (pada sistem e-learning / ecampus).

## Struktur Berkas

```
Lab2Web/
├── media/
│   ├── audio.mp3
│   └── video.mp4
├── biodata.html
├── index.html
├── semantic.html
└── README.md
```

* **`index.html`**: Halaman utama yang memuat latihan tabel data, form registrasi, radio button, checkbox, select, textarea, validasi form, dan multimedia.
* **`semantic.html`**: Implementasi struktur tata letak dokumen menggunakan elemen semantik HTML5 (header, nav, main, section, article, aside, footer).
* **`biodata.html`**: Halaman proyek mini yang menggabungkan seluruh konsep (tabel biodata, form input tervalidasi, semantic layout, dan multimedia).
* **`media/`**: Direktori penyimpanan aset audio dan video pendukung.

---

## Penjelasan Langkah-Langkah Praktikum

### 1. Membuat Tabel Data Mahasiswa
* **Penjelasan**: Membuat tabel data dasar menggunakan elemen `<table>`, `<tr>` (baris), `<th>` (kepala kolom), dan `<td>` (sel data). Atribut `border="1"` disematkan untuk menampilkan garis pemisah antar-sel secara visual. Pada bagian ini diisi data mahasiswa (NIM, Nama, Program Studi).


### 2. Mengembangkan Tabel dengan `thead`, `tbody`, dan `tfoot`
* **Penjelasan**: Menyusun hierarki tabel semantik dengan mengelompokkan data ke dalam bagian kepala (`<thead>`), isi data (`<tbody>`), dan ringkasan kaki tabel (`<tfoot>`). Ditambahkan elemen `<caption>` sebagai judul/keterangan tabel, serta atribut `colspan="2"` pada sel baris footer untuk menggabungkan dua kolom secara horizontal pada nilai rata-rata.


### 3. Membuat Form Registrasi Mahasiswa
* **Penjelasan**: Mengimplementasikan kontainer `<form>` yang memuat berbagai jenis elemen input interaktif satu baris, seperti teks nama (`type="text"`), alamat surel (`type="email"`), kata sandi tersensor (`type="password"`), dan pemilih kalender tanggal lahir (`type="date"`). Form dilengkapi tombol eksekusi bertipe `submit` serta tombol pembersih form bertipe `reset`.
  

### 4. Menambahkan Radio Button dan Checkbox
* **Penjelasan**: 
  * **Radio Button** (`type="radio"`): Diterapkan pada pemilihan jenis kelamin dengan atribut `name="jk"` yang seragam, sehingga peramban memastikan pengguna hanya dapat memilih satu opsi mutlak (Laki-laki atau Perempuan).
  * **Checkbox** (`type="checkbox"`): Diterapkan pada pemilihan keahlian teknis (*skill*), memberikan fleksibilitas bagi pengguna untuk memilih satu, beberapa, atau tidak sama sekali dari opsi yang tersedia (HTML, CSS, JavaScript).
  

### 5. Input Dropdown (`select`) dan Kotak Teks Multibaris (`textarea`)
* **Penjelasan**: Memanfaatkan elemen `<select>` beserta elemen anaknya `<option>` untuk membatasi pilihan Program Studi melalui menu dropdown yang ringkas. Selain itu, digunakan elemen `<textarea>` dengan atribut dimensi `rows="5"` dan `cols="40"` guna mengakomodasi pengisian alamat domisili yang memerlukan input teks multibaris (*multiline*).
  

### 6. Validasi Form Dasar HTML5
* **Penjelasan**: Menerapkan validasi formulir langsung dari sisi peramban (*native client-side validation*) tanpa JavaScript:
  * Atribut `required` pada kolom nama, email, dan umur untuk mencegah form dikirim dalam keadaan kosong.
  * Atribut `minlength="3"` pada nama untuk memastikan panjang karakter minimal terpenuhi.
  * Atribut `min="17"` dan `max="60"` pada input umur bertipe numerik untuk membatasi rentang usia yang diizinkan.
  

### 7. Membuat Struktur Tata Letak Semantic HTML (`semantic.html`)
* **Penjelasan**: Membangun arsitektur dokumen portal mahasiswa menggunakan elemen semantik HTML5 murni: `<header>` (identitas/judul portal), `<nav>` (kumpulan tautan navigasi), `<main>` (area muatan inti), `<section>` dan `<article>` (pembagian materi tematik), `<aside>` (informasi sampingan/pelengkap), serta `<footer>` (catatan hak cipta).
  

### 8. Integrasi Berkas Multimedia (Audio & Video)
* **Penjelasan**: Menyematkan pemutar media lokal ke dalam dokumen HTML:
  * Tag `<audio controls>` untuk memutar berkas audio dari folder `media/audio.mp3`.
  * Tag `<video controls width="480">` untuk memutar berkas rekaman video dari folder `media/video.mp4` dengan lebar 480 piksel.
  * Atribut `controls` disematkan agar kontrol pemutar bawaan peramban (play/pause, volume, timeline durasi) dapat diakses pengguna.
  


---

## 🌟 Proyek Mini: Halaman Biodata Mahasiswa (`biodata.html`)

* **Penjelasan**: Menggabungkan seluruh konsep materi yang dipelajari pada latihan 1 sampai 8 ke dalam satu berkas terpadu `biodata.html`:
  1. **Semantic Layout**: Tata letak dokumen diatur menggunakan `<header>`, `<nav>`, `<main>`, `<section>`, dan `<footer>`.
  2. **Navigasi Internal**: Menu navigasi memanfaatkan tautan jangkar (*anchor links*) `#biodata` dan `#form` untuk berpindah area konten di halaman yang sama secara instan.
  3. **Tabel Profil**: Memuat data ringkasan identitas mahasiswa (NIM, Nama, Program Studi) menggunakan struktur tabel.
  4. **Formulir Interaktif & Validasi**: Form entri biodata yang dilengkapi kolom nama, email, program studi (dropdown), dan alamat (textarea) dengan validasi `required`.
  5. **Multimedia**: Menghadirkan elemen audio/video pendukung pada halaman.
  
