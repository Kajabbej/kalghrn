# Determinan dan Invers Matriks

Pembahasan ini mencakup definisi formal determinan dan langkah penyelesaian Sistem Persamaan Linear (SPL) menggunakan matriks invers.

## 1. Definisi Determinan Matriks

Misalkan terdapat matriks persegi:
$$ A = [a_{ij}]_{n \times n} $$

### Kasus Dasar ($n = 1$)
Jika ukuran matriks adalah $1 \times 1$, maka determinannya adalah nilai elemen itu sendiri:
$$ \det(A) = a_{11} $$

### Kasus Rekursif ($n \geq 2$)
Untuk matriks berukuran $n \times n$ dengan $n \geq 2$, determinan didefinisikan secara rekursif melalui ekspansi kofaktor pada baris pertama:
$$ \det(A) = \sum_{j=1}^{n} (-1)^{1+j} \, a_{1j} \, \det(A_{1j}) $$

Keterangan:
- $A_{1j}$ adalah submatriks yang diperoleh dengan menghapus baris ke-1 dan kolom ke-$j$ dari matriks $A$.

## 2. Penyelesaian SPL 4x4 dengan Matriks Invers

Diberikan Sistem Persamaan Linear berikut:
$$
\begin{bmatrix} 
1 & 1 & 1 & 1 \\ 
2 & -1 & 1 & -1 \\ 
1 & 2 & -1 & 1 \\ 
3 & -1 & 2 & 1 
\end{bmatrix} 
\begin{bmatrix} 
x_1 \\ 
x_2 \\ 
x_3 \\ 
x_4 
\end{bmatrix} 
= 
\begin{bmatrix} 
10 \\ 
-1 \\ 
6 \\ 
11 
\end{bmatrix}
$$

Untuk mencari solusinya, kita dapat menggunakan persamaan matriks:
$$ AX = B \Rightarrow X = A^{-1}B $$

Metode yang digunakan untuk mencari matriks invers $A^{-1}$ adalah **Eliminasi Gauss-Jordan**.

### Langkah 1: Pembentukan Matriks Gabungan $[A|I]$
Sandingkan matriks $A$ dengan matriks identitas $4 \times 4$:
$$
\left[ 
\begin{array}{cccc|cccc} 
1 & 1 & 1 & 1 & 1 & 0 & 0 & 0 \\ 
2 & -1 & 1 & -1 & 0 & 1 & 0 & 0 \\ 
1 & 2 & -1 & 1 & 0 & 0 & 1 & 0 \\ 
3 & -1 & 2 & 1 & 0 & 0 & 0 & 1 
\end{array} 
\right]
$$

Lakukan Operasi Baris Elementer (OBE) pada kolom pertama untuk membuat nol elemen di bawah pivot utama:
- $R_2 - 2R_1 \rightarrow R_2$
- $R_3 - R_1 \rightarrow R_3$
- $R_4 - 3R_1 \rightarrow R_4$

Hasil sementara:
$$
\left[ 
\begin{array}{cccc|cccc} 
1 & 1 & 1 & 1 & 1 & 0 & 0 & 0 \\ 
0 & -3 & -1 & -3 & -2 & 1 & 0 & 0 \\ 
0 & 1 & -2 & 0 & -1 & 0 & 1 & 0 \\ 
0 & -4 & -1 & -2 & -3 & 0 & 0 & 1 
\end{array} 
\right]
$$

### Langkah 2: Matriks Invers Akhir ($A^{-1}$)
Setelah menyelesaikan seluruh tahapan eliminasi Gauss-Jordan hingga ruas kiri menjadi matriks identitas, diperoleh matriks invers:
$$
A^{-1} = \frac{1}{13} 
\begin{bmatrix} 
-3 & 3 & 4 & 2 \\ 
9 & 4 & 1 & -6 \\ 
11 & 2 & -6 & -3 \\ 
-4 & -9 & 1 & 7 
\end{bmatrix}
$$

### Langkah 3: Menghitung Nilai Variabel ($X = A^{-1}B$)
Kalikan setiap baris dari matriks $A^{-1}$ dengan kolom konstanta $B = [10, -1, 6, 11]^T$.

- **Mencari $x_1$**:
  $$ x_1 = \frac{1}{13} [(-3 \times 10) + (3 \times -1) + (4 \times 6) + (2 \times 11)] = \frac{13}{13} = 1 $$
- **Mencari $x_2$**:
  $$ x_2 = \frac{1}{13} [(9 \times 10) + (4 \times -1) + (1 \times 6) + (-6 \times 11)] = \frac{26}{13} = 2 $$
- **Mencari $x_3$**:
  $$ x_3 = \frac{1}{13} [(11 \times 10) + (2 \times -1) + (-6 \times 6) + (-3 \times 11)] = \frac{39}{13} = 3 $$
- **Mencari $x_4$**:
  $$ x_4 = \frac{1}{13} [(-4 \times 10) + (-9 \times -1) + (1 \times 6) + (7 \times 11)] = \frac{52}{13} = 4 $$

### Kesimpulan Akhir
Nilai variabel yang memenuhi sistem adalah:
$$
X = 
\begin{bmatrix} 
x_1 \\ 
x_2 \\ 
x_3 \\ 
x_4 
\end{bmatrix} 
= 
\begin{bmatrix} 
1 \\ 
2 \\ 
3 \\ 
4 
\end{bmatrix}
$$
