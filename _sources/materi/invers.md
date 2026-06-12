# Invers Matriks

Halaman ini membahas cara menyelesaikan Sistem Persamaan Linear (SPL) menggunakan matriks invers.

---

## Menyelesaikan SPL $4 \times 4$ dengan Invers

Diberikan SPL dalam bentuk matriks:
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
\end{bmatrix} = \begin{bmatrix} 
10 \\ 
-1 \\ 
6 \\ 
11 
\end{bmatrix}
$$

Solusi SPL ini dicari menggunakan rumus:
$$ AX = B \Rightarrow X = A^{-1}B $$

Kita akan mencari matriks invers $A^{-1}$ dengan metode **Eliminasi Gauss-Jordan**.

### Langkah 1: Buat Matriks Gabungan $[A|I]$
Gabungkan matriks $A$ dengan matriks identitas $4 \times 4$:
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

Lakukan OBE pada kolom pertama untuk membuat nol angka di bawah pivot baris pertama:
*   $R_2 - 2R_1 \rightarrow R_2$
*   $R_3 - R_1 \rightarrow R_3$
*   $R_4 - 3R_1 \rightarrow R_4$

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

### Langkah 2: Hasil Akhir Invers ($A^{-1}$)
Selesaikan OBE Gauss-Jordan sampai ruas kiri menjadi matriks identitas. Hasil di ruas kanan adalah matriks invers kita:
$$
A^{-1} = \frac{1}{13} 
\begin{bmatrix} 
-3 & 3 & 4 & 2 \\ 
9 & 4 & 1 & -6 \\ 
11 & 2 & -6 & -3 \\ 
-4 & -9 & 1 & 7 
\end{bmatrix}
$$

### Langkah 3: Hitung Nilai Variabel ($X = A^{-1}B$)
Kalikan matriks $A^{-1}$ dengan kolom konstanta $B = [10, -1, 6, 11]^T$.

*   **Hitung $x_1$**:
    $$ x_1 = \frac{1}{13} [(-3 \times 10) + (3 \times -1) + (4 \times 6) + (2 \times 11)] = \frac{13}{13} = 1 $$
*   **Hitung $x_2$**:
    $$ x_2 = \frac{1}{13} [(9 \times 10) + (4 \times -1) + (1 \times 6) + (-6 \times 11)] = \frac{26}{13} = 2 $$
*   **Hitung $x_3$**:
    $$ x_3 = \frac{1}{13} [(11 \times 10) + (2 \times -1) + (-6 \times 6) + (-3 \times 11)] = \frac{39}{13} = 3 $$
*   **Hitung $x_4$**:
    $$ x_4 = \frac{1}{13} [(-4 \times 10) + (-9 \times -1) + (1 \times 6) + (7 \times 11)] = \frac{52}{13} = 4 $$

### Solusi Akhir
Nilai variabel yang memenuhi sistem adalah:
$$
X = 
\begin{bmatrix} 
x_1 \\ 
x_2 \\ 
x_3 \\ 
x_4 
\end{bmatrix} = \begin{bmatrix} 
1 \\ 
2 \\ 
3 \\ 
4 
\end{bmatrix}
$$
