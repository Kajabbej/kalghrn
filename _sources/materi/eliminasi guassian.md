# Metode Eliminasi Gauss

Metode Eliminasi Gauss adalah metode penyelesaian Sistem Persamaan Linier (SPL) dengan menggunakan operasi baris elementer pada matriks augmentasi hingga diperoleh bentuk matriks segitiga atas (upper triangular matrix). Setelah matriks berada pada bentuk tersebut, nilai variabel dapat ditentukan melalui proses substitusi balik (*back substitution*).

Tujuan utama Eliminasi Gauss adalah mengubah matriks augmentasi menjadi **bentuk eselon baris (row echelon form)**, yaitu bentuk matriks yang memenuhi kondisi:
1. Semua baris nol berada di bagian bawah matriks.
2. Elemen pertama yang tidak nol pada setiap baris (pivot) berada di sebelah kanan pivot pada baris sebelumnya.
3. Semua elemen di bawah pivot bernilai nol.

---

## Operasi Baris Elementer (OBE)

Dalam Eliminasi Gauss digunakan tiga operasi dasar, yaitu:
1. **Pertukaran Baris**: Menukar posisi dua baris.
   $$ B_i \leftrightarrow B_j $$
2. **Perkalian Baris**: Mengalikan suatu baris dengan konstanta bukan nol.
   $$ B_i \rightarrow kB_i $$ (dengan $k \neq 0$)
3. **Penjumlahan Baris**: Menambahkan kelipatan suatu baris ke baris lainnya.
   $$ B_i \rightarrow B_i + kB_j $$

---

## Pembahasan Contoh Soal

### 1. SPL Tiga Variabel

Diketahui sistem persamaan berikut:
$$
\begin{cases}
2x + y - z = 8 \\
-3x - y + 2z = -11 \\
-2x + y + 2z = -3
\end{cases}
$$

#### Langkah 1: Matriks Augmented
$$
\left[
\begin{array}{ccc|c}
2 & 1 & -1 & 8 \\
-3 & -1 & 2 & -11 \\
-2 & 1 & 2 & -3
\end{array}
\right]
$$

#### Langkah 2: Eliminasi Kolom Pertama
Lakukan operasi:
$$ R_2 = R_2 + \frac{3}{2}R_1 $$
$$ R_3 = R_3 + R_1 $$

Hasilnya:
$$
\left[
\begin{array}{ccc|c}
2 & 1 & -1 & 8 \\
0 & 0.5 & 0.5 & 1 \\
0 & 2 & 1 & 5
\end{array}
\right]
$$

#### Langkah 3: Eliminasi Kolom Kedua
Lakukan operasi:
$$ R_3 = R_3 - 4R_2 $$

Hasilnya:
$$
\left[
\begin{array}{ccc|c}
2 & 1 & -1 & 8 \\
0 & 0.5 & 0.5 & 1 \\
0 & 0 & -1 & 1
\end{array}
\right]
$$

Matriks di atas sudah berada dalam bentuk eselon baris.

#### Langkah 4: Substitusi Balik
- Dari baris ke-3:
  $$ -z = 1 \Rightarrow z = -1 $$
- Dari baris ke-2:
  $$ 0.5y + 0.5(-1) = 1 \Rightarrow 0.5y = 1.5 \Rightarrow y = 3 $$
- Dari baris ke-1:
  $$ 2x + (3) - (-1) = 8 \Rightarrow 2x + 4 = 8 \Rightarrow 2x = 4 \Rightarrow x = 2 $$

#### Solusi Akhir
$$ x = 2, \quad y = 3, \quad z = -1 $$

---

### 2. SPL Empat Variabel

Diketahui sistem persamaan berikut:
$$
\begin{cases}
x + y + z + w = 10 \\
2x - y + z + w = 5 \\
3x + y - z + w = 12 \\
x + 2y + 3z - w = 7
\end{cases}
$$

#### Langkah 1: Matriks Augmented
$$
\left[
\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10 \\
2 & -1 & 1 & 1 & 5 \\
3 & 1 & -1 & 1 & 12 \\
1 & 2 & 3 & -1 & 7
\end{array}
\right]
$$

#### Langkah 2: Eliminasi Kolom Pertama
Lakukan operasi:
$$ R_2 = R_2 - 2R_1 $$
$$ R_3 = R_3 - 3R_1 $$
$$ R_4 = R_4 - R_1 $$

Hasilnya:
$$
\left[
\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10 \\
0 & -3 & -1 & -1 & -15 \\
0 & -2 & -4 & -2 & -18 \\
0 & 1 & 2 & -2 & -3
\end{array}
\right]
$$

#### Langkah 3: Eliminasi Kolom Kedua dan Ketiga
Setelah melakukan OBE lanjutan, diperoleh matriks eselon:
$$
\left[
\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10 \\
0 & -3 & -1 & -1 & -15 \\
0 & 0 & -10/3 & -4/3 & -8 \\
0 & 0 & 0 & -3 & -12
\end{array}
\right]
$$

#### Langkah 4: Substitusi Balik
- Dari baris ke-4:
  $$ -3w = -12 \Rightarrow w = 4 $$
- Dari baris ke-3:
  $$ -\frac{10}{3}z - \frac{4}{3}(4) = -8 \Rightarrow z = 3 $$
- Dari baris ke-2:
  $$ -3y - (3) - (4) = -15 \Rightarrow y = 2 $$
- Dari baris ke-1:
  $$ x + 2 + 3 + 4 = 10 \Rightarrow x = 1 $$

#### Solusi Akhir
$$ x = 1, \quad y = 2, \quad z = 3, \quad w = 4 $$
