# 📝 To-Do List Project Jupyter Book

Daftar tugas untuk pengembangan dan pemeliharaan buku interaktif **Aljabar Linear dan SPL**.

## 📌 Prioritas Utama
- [ ] **Perbaikan Warning Build**
  - [ ] Perbaiki warning referensi judul pada `intro1.md`
  - [ ] Cari solusi atau konfigurasi alternatif untuk *lexer* `geogebra` di Sphinx agar tidak memicu warning saat build.
- [ ] **Penyelarasan & Uji Coba Halaman Biodata**
  - [ ] Pastikan halaman biodata (`biodata/biodata.md`) ter-render dengan sempurna di HTML hasil build.
  - [ ] Periksa kecocokan foto profile dan link yang ada di halaman biodata.

## ⚙️ Alur Kerja Rutin (Maintenance)
- [ ] **Build Ulang Buku**
  - Jalankan perintah build lokal untuk mengecek kesalahan:
    ```bash
    jupyter-book build --all .
    ```
- [ ] **Deploy Perubahan ke GitHub Pages**
  - Jalankan perintah deploy ke branch `gh-pages`:
    ```bash
    ghp-import -n -p -f _build/html
    ```

## 📚 Pengembangan Konten (Materi & Tugas)
- [ ] Lengkapi pembahasan soal-soal latihan pada akhir bab di `intro.md`.
- [ ] Tambahkan interaktivitas baru pada sel SageMath untuk visualisasi matriks 4x4.
- [ ] Sempurnakan penjelasan dekomposisi matriks QR Gram-Schmidt dengan langkah-langkah yang lebih detail.
