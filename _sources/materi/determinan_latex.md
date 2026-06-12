# Determinan Matriks

Halaman ini membahas cara mencari determinan matriks.

---
# Mencari Determinan 2×2

Diketahui:

$$
\begin{vmatrix}
3 & 2 \\
1 & 4
\end{vmatrix}
$$

---

## Rumus Determinan 2×2

$\det(A)$

$= (a \times d) - (b \times c)$

---

## Identifikasi Elemen

$$
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$

=

$$
\begin{bmatrix}
3 & 2 \\
1 & 4
\end{bmatrix}
$$

Maka:

$a = 3$
$b = 2$
$c = 1$
$d = 4$

---

## Substitusi ke Rumus

$\det(A)$

$$ = (3 \times 4) - (2 \times 1) $$

$$ = 12 - 2 $$

$$ = 10 $$

---

# Jawaban Akhir

$\det(A)$ = 10

---

## Bentuk Ekspansi Baris 1

Baris pertama:

$$ [3 \quad 2] $$

Pola tanda:

+  -

Maka:

$\det(A)$

$$ = 3(4) - 2(1) $$

$$ = 12 - 2 $$

$$ = 10 $$

---

# Kesimpulan

Untuk matriks 2×2:

$$
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$

$\det(A)$

$= a(d) - b(c)$

$= ad - bc$

# Mencari Determinan 3×3 dengan Ekspansi Baris Pertama

Diketahui:

$$
\begin{vmatrix}
1 & 2 & 3 \\
0 & 4 & 5 \\
1 & 0 & 6
\end{vmatrix}
$$

---

## Langkah 1: Pilih Baris Pertama

Baris pertama:

$$ [1 \quad 2 \quad 3] $$

Pola tanda:

+  -  +

Maka:

$\det(A)$

= 1($M_{11}$) - 2($M_{12}$) + 3($M_{13}$)

---

## Langkah 2: Cari Minor $M_{11}$

Coret baris 1 dan kolom 1

$M_{11}$ =

$$
\begin{vmatrix}
4 & 5 \\
0 & 6
\end{vmatrix}
$$

$\det(M_{11})$

$$ = (4\times6) - (5\times0) $$

$$ = 24 $$

---

## Langkah 3: Cari Minor $M_{12}$

Coret baris 1 dan kolom 2

$M_{12}$ =

$$
\begin{vmatrix}
0 & 5 \\
1 & 6
\end{vmatrix}
$$

$\det(M_{12})$

$$ = (0\times6) - (5\times1) $$

$$ = -5 $$

---

## Langkah 4: Cari Minor $M_{13}$

Coret baris 1 dan kolom 3

$M_{13}$ =

$$
\begin{vmatrix}
0 & 4 \\
1 & 0
\end{vmatrix}
$$

$\det(M_{13})$

$$ = (0\times0) - (4\times1) $$

$$ = -4 $$

---

## Langkah 5: Substitusi ke Rumus

$\det(A)$

$$ = 1(24) - 2(-5) + 3(-4) $$

$$ = 24 + 10 - 12 $$

$$ = 22 $$

---

# Jawaban Akhir

$\det(A)$ = 22

---

# Pola yang Harus Diingat

Untuk ekspansi baris pertama matriks 3×3:

$\det(A)$

= a($M_{11}$) - b($M_{12}$) + c($M_{13}$)

Pola tanda:

+  -  +

Langkah:

1. Pilih baris.
2. Coret baris dan kolom elemen tersebut.
3. Hitung minor 2×2.
4. Kalikan dengan tanda (+ - +).
5. Jumlahkan semuanya.


# Mencari Determinan 4×4 dengan Ekspansi Baris Pertama

Diketahui:

|A| =

$$
\begin{vmatrix}
2 & 0 & 1 & 0 \\
3 & 1 & 2 & 4 \\
1 & 2 & 3 & 1 \\
0 & 1 & 2 & 3
\end{vmatrix}
$$

---

## Langkah 1: Pilih Baris Pertama

Baris pertama:

$$ [2 \quad 0 \quad 1 \quad 0] $$

Pola tanda:

+  -  +  -

Maka:

$\det(A)$

$$ = 2M_{11} - 0M_{12} + 1M_{13} - 0M_{14} $$

Karena ada nol:

= 2M11 + $M_{13}$

---

## Langkah 2: Cari Minor $M_{11}$

Coret baris 1 dan kolom 1

$M_{11}$ =

$$
\begin{vmatrix}
1 & 2 & 4 \\
2 & 3 & 1 \\
1 & 2 & 3
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (1 \times 3 \times 3) + (2 \times 1 \times 1) + (4 \times 2 \times 2) $$

$$ = 9 + 2 + 16 $$

$$ = 27 $$

Diagonal naik:

$$ (1 \times 3 \times 4) + (2 \times 1 \times 1) + (3 \times 2 \times 2) $$

$$ = 12 + 2 + 12 $$

$$ = 26 $$

$M_{11}$ = 27 - 26

$M_{11}$ = 1

---

## Langkah 3: Cari Minor $M_{13}$

Coret baris 1 dan kolom 3

$M_{13}$ =

$$
\begin{vmatrix}
3 & 1 & 4 \\
1 & 2 & 1 \\
0 & 1 & 3
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (3 \times 2 \times 3) + (1 \times 1 \times 0) + (4 \times 1 \times 1) $$

$$ = 18 + 0 + 4 $$

$$ = 22 $$

Diagonal naik:

$$ (0 \times 2 \times 4) + (1 \times 1 \times 3) + (3 \times 1 \times 1) $$

$$ = 0 + 3 + 3 $$

$$ = 6 $$

$M_{13}$ = 22 - 6

$M_{13}$ = 16

---

## Langkah 4: Substitusi ke Rumus

$\det(A)$

= 2($M_{11}$) + $M_{13}$

$$ = 2(1) + 16 $$

$$ = 2 + 16 $$

$$ = 18 $$

---

# Jawaban Akhir

$\det(A)$ = 18

# Mencari Determinan 4×4 dengan Ekspansi Baris Kedua

Diketahui:

$$
\begin{vmatrix}
2 & 1 & 0 & 3 \\
1 & 0 & 2 & 4 \\
3 & 1 & 2 & 1 \\
0 & 2 & 1 & 3
\end{vmatrix}
$$

---

## Langkah 1: Pilih Baris Kedua

Baris kedua:

$$ [1 \quad 0 \quad 2 \quad 4] $$

Pola tanda baris kedua:

-  +  -  +

Maka:

$\det(A)$

= -1($M_{21}$)
+0($M_{22}$)
-2($M_{23}$)
+4($M_{24}$)

Karena ada nol:

$\det(A)$

= -$M_{21}$ - 2M23 + 4M24

---

## Langkah 2: Cari Minor $M_{21}$

Coret baris 2 dan kolom 1

$M_{21}$ =

$$
\begin{vmatrix}
1 & 0 & 3 \\
1 & 2 & 1 \\
2 & 1 & 3
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (1 \times 2 \times 3) + (0 \times 1 \times 2) + (3 \times 1 \times 1) $$

$$ = 6 + 0 + 3 $$

$$ = 9 $$

Diagonal naik:

$$ (2 \times 2 \times 3) + (1 \times 1 \times 1) + (3 \times 1 \times 0) $$

$$ = 12 + 1 + 0 $$

$$ = 13 $$

$M_{21}$

$$ = 9 - 13 $$

$$ = -4 $$

---

## Langkah 3: Cari Minor $M_{23}$

Coret baris 2 dan kolom 3

$M_{23}$ =

$$
\begin{vmatrix}
2 & 1 & 3 \\
3 & 1 & 1 \\
0 & 2 & 3
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 1 \times 3) + (1 \times 1 \times 0) + (3 \times 3 \times 2) $$

$$ = 6 + 0 + 18 $$

$$ = 24 $$

Diagonal naik:

$$ (0 \times 1 \times 3) + (2 \times 1 \times 2) + (3 \times 3 \times 1) $$

$$ = 0 + 4 + 9 $$

$$ = 13 $$

$M_{23}$

$$ = 24 - 13 $$

$$ = 11 $$

---

## Langkah 4: Cari Minor $M_{24}$

Coret baris 2 dan kolom 4

$M_{24}$ =

$$
\begin{vmatrix}
2 & 1 & 0 \\
3 & 1 & 2 \\
0 & 2 & 1
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 1 \times 1) + (1 \times 2 \times 0) + (0 \times 3 \times 2) $$

$$ = 2 + 0 + 0 $$

$$ = 2 $$

Diagonal naik:

$$ (0 \times 1 \times 0) + (2 \times 2 \times 2) + (1 \times 3 \times 1) $$

$$ = 0 + 8 + 3 $$

$$ = 11 $$

$M_{24}$

$$ = 2 - 11 $$

$$ = -9 $$

---

## Langkah 5: Substitusi

$\det(A)$

$$ = -(-4) - 2(11) + 4(-9) $$

$$ = 4 - 22 - 36 $$

$$ = -54 $$

---

# Jawaban Akhir

$\det(A)$ = -54

---

# Pola Tanda yang Wajib Hafal

$$
\begin{bmatrix}
+ & - & + & - \\
- & + & - & + \\
+ & - & + & - \\
- & + & - & +
\end{bmatrix}
$$

Untuk ekspansi baris ke-2:

-  +  -  +

Untuk ekspansi baris ke-4:

-  +  -  +
# Mencari Determinan 4×4 dengan Ekspansi Baris Ketiga

Diketahui:

$$
\begin{vmatrix}
2 & 1 & 0 & 3 \\
1 & 0 & 2 & 4 \\
3 & 1 & 2 & 1 \\
0 & 2 & 1 & 3
\end{vmatrix}
$$

---

## Langkah 1: Pilih Baris Ketiga

Baris ketiga:

$$ [3 \quad 1 \quad 2 \quad 1] $$

Pola tanda baris ketiga:

+  -  +  -

Maka:

$\det(A)$

= 3($M_{31}$)
- 1($M_{32}$)
+ 2($M_{33}$)
- 1($M_{34}$)

---

## Langkah 2: Cari Minor $M_{31}$

Coret baris 3 dan kolom 1

$M_{31}$ =

$$
\begin{vmatrix}
1 & 0 & 3 \\
0 & 2 & 4 \\
2 & 1 & 3
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (1 \times 2 \times 3) + (0 \times 4 \times 2) + (3 \times 0 \times 1) $$

$$ = 6 + 0 + 0 $$

$$ = 6 $$

Diagonal naik:

$$ (2 \times 2 \times 3) + (1 \times 4 \times 1) + (3 \times 0 \times 0) $$

$$ = 12 + 4 + 0 $$

$$ = 16 $$

$M_{31}$

$$ = 6 - 16 $$

$$ = -10 $$

---

## Langkah 3: Cari Minor $M_{32}$

Coret baris 3 dan kolom 2

$M_{32}$ =

$$
\begin{vmatrix}
2 & 0 & 3 \\
1 & 2 & 4 \\
0 & 1 & 3
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 2 \times 3) + (0 \times 4 \times 0) + (3 \times 1 \times 1) $$

$$ = 12 + 0 + 3 $$

$$ = 15 $$

Diagonal naik:

$$ (0 \times 2 \times 3) + (1 \times 4 \times 2) + (3 \times 1 \times 0) $$

$$ = 0 + 8 + 0 $$

$$ = 8 $$

$M_{32}$

$$ = 15 - 8 $$

$$ = 7 $$

---

## Langkah 4: Cari Minor $M_{33}$

Coret baris 3 dan kolom 3

$M_{33}$ =

$$
\begin{vmatrix}
2 & 1 & 3 \\
1 & 0 & 4 \\
0 & 2 & 3
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 0 \times 3) + (1 \times 4 \times 0) + (3 \times 1 \times 2) $$

$$ = 0 + 0 + 6 $$

$$ = 6 $$

Diagonal naik:

$$ (0 \times 0 \times 3) + (2 \times 4 \times 2) + (3 \times 1 \times 1) $$

$$ = 0 + 16 + 3 $$

$$ = 19 $$

$M_{33}$

$$ = 6 - 19 $$

$$ = -13 $$

---

## Langkah 5: Cari Minor $M_{34}$

Coret baris 3 dan kolom 4

$M_{34}$ =

$$
\begin{vmatrix}
2 & 1 & 0 \\
1 & 0 & 2 \\
0 & 2 & 1
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 0 \times 1) + (1 \times 2 \times 0) + (0 \times 1 \times 2) $$

$$ = 0 $$

Diagonal naik:

$$ (0 \times 0 \times 0) + (2 \times 2 \times 2) + (1 \times 1 \times 1) $$

$$ = 0 + 8 + 1 $$

$$ = 9 $$

$M_{34}$

$$ = 0 - 9 $$

$$ = -9 $$

---

## Langkah 6: Substitusi

$\det(A)$

$$ = 3(-10) $$
- 1(7)
+ 2(-13)
- 1(-9)

$$ = -30 - 7 - 26 + 9 $$

$$ = -54 $$

---

# Jawaban Akhir

$\det(A)$ = -54

---

# Pola Tanda Kofaktor 4×4

$$
\begin{bmatrix}
+ & - & + & - \\
- & + & - & + \\
+ & - & + & - \\
- & + & - & +
\end{bmatrix}
$$

Baris ke-3 menggunakan:

+  -  +  -

# Mencari Determinan 4×4 dengan Ekspansi Baris Keempat

Diketahui:

$$
\begin{vmatrix}
2 & 1 & 0 & 3 \\
1 & 0 & 2 & 4 \\
3 & 1 & 2 & 1 \\
0 & 2 & 1 & 3
\end{vmatrix}
$$

---

## Langkah 1: Pilih Baris Keempat

Baris keempat:

$$ [0 \quad 2 \quad 1 \quad 3] $$

Pola tanda baris keempat:

-  +  -  +

Maka:

$\det(A)$

= -0($M_{41}$)
+2($M_{42}$)
-1($M_{43}$)
+3($M_{44}$)

Karena ada nol:

$\det(A)$

= 2($M_{42}$)
- $M_{43}$
+ 3($M_{44}$)

---

## Langkah 2: Cari Minor $M_{42}$

Coret baris 4 dan kolom 2

$M_{42}$ =

$$
\begin{vmatrix}
2 & 0 & 3 \\
1 & 2 & 4 \\
3 & 2 & 1
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 2 \times 1) + (0 \times 4 \times 3) + (3 \times 1 \times 2) $$

$$ = 4 + 0 + 6 $$

$$ = 10 $$

Diagonal naik:

$$ (3 \times 2 \times 3) + (2 \times 4 \times 2) + (1 \times 1 \times 0) $$

$$ = 18 + 16 + 0 $$

$$ = 34 $$

$M_{42}$

$$ = 10 - 34 $$

$$ = -24 $$

---

## Langkah 3: Cari Minor $M_{43}$

Coret baris 4 dan kolom 3

$M_{43}$ =

$$
\begin{vmatrix}
2 & 1 & 3 \\
1 & 0 & 4 \\
3 & 1 & 1
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 0 \times 1) + (1 \times 4 \times 3) + (3 \times 1 \times 1) $$

$$ = 0 + 12 + 3 $$

$$ = 15 $$

Diagonal naik:

$$ (3 \times 0 \times 3) + (1 \times 4 \times 2) + (1 \times 1 \times 1) $$

$$ = 0 + 8 + 1 $$

$$ = 9 $$

$M_{43}$

$$ = 15 - 9 $$

$$ = 6 $$

---

## Langkah 4: Cari Minor $M_{44}$

Coret baris 4 dan kolom 4

$M_{44}$ =

$$
\begin{vmatrix}
2 & 1 & 0 \\
1 & 0 & 2 \\
3 & 1 & 2
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 0 \times 2) + (1 \times 2 \times 3) + (0 \times 1 \times 1) $$

$$ = 0 + 6 + 0 $$

$$ = 6 $$

Diagonal naik:

$$ (3 \times 0 \times 0) + (1 \times 2 \times 2) + (2 \times 1 \times 1) $$

$$ = 0 + 4 + 2 $$

$$ = 6 $$

$M_{44}$

$$ = 6 - 6 $$

$$ = 0 $$

---

## Langkah 5: Substitusi

$\det(A)$

$$ = 2(-24) $$
- (6)
+ 3(0)

$$ = -48 - 6 + 0 $$

$$ = -54 $$

---

# Jawaban Akhir

$\det(A)$ = -54

---

# Pola Tanda Kofaktor 4×4

$$
\begin{bmatrix}
+ & - & + & - \\
- & + & - & + \\
+ & - & + & - \\
- & + & - & +
\end{bmatrix}
$$

Baris ke-4 menggunakan:

-  +  -  +

---

# Ringkasan Ekspansi Baris

Baris 1 → +  -  +  -

Baris 2 → -  +  -  +

Baris 3 → +  -  +  -

Baris 4 → -  +  -  +

Semua ekspansi menghasilkan determinan yang sama.

# ekpansi  perkolom 1-4
# Mencari Determinan 4×4 dengan Ekspansi Kolom Pertama

Diketahui:

$$
\begin{vmatrix}
2 & 1 & 0 & 3 \\
1 & 0 & 2 & 4 \\
3 & 1 & 2 & 1 \\
0 & 2 & 1 & 3
\end{vmatrix}
$$

---

## Langkah 1: Pilih Kolom Pertama

Kolom pertama:

$$
\begin{bmatrix}
2 \\
1 \\
3 \\
0
\end{bmatrix}
$$

Pola tanda kolom pertama:

+
-
+
-

Maka:

$\det(A)$

= 2($M_{11}$)
- 1($M_{21}$)
+ 3($M_{31}$)
- 0($M_{41}$)

Karena elemen terakhir nol:

$\det(A)$

= 2($M_{11}$)
- $M_{21}$
+ 3($M_{31}$)

---

## Langkah 2: Cari Minor $M_{11}$

Coret baris 1 dan kolom 1

$$
\begin{vmatrix}
0 & 2 & 4 \\
1 & 2 & 1 \\
2 & 1 & 3
\end{vmatrix}
$$

Hitung Sarrus:

Diagonal turun:

$$ (0 \times 2 \times 3)+(2 \times 1 \times 2)+(4 \times 1 \times 1) $$

$$ = 0+4+4 $$

$$ = 8 $$

Diagonal naik:

$$ (2 \times 2 \times 4)+(1 \times 1 \times 0)+(3 \times 1 \times 2) $$

$$ =16+0+6 $$

$$ =22 $$

$M_{11}$ = 8 - 22

$M_{11}$ = -14

---

## Langkah 3: Cari Minor $M_{21}$

Coret baris 2 dan kolom 1

$$
\begin{vmatrix}
1 & 0 & 3 \\
1 & 2 & 1 \\
2 & 1 & 3
\end{vmatrix}
$$

Hitung Sarrus:

Diagonal turun:

$$ (1 \times 2 \times 3)+(0 \times 1 \times 2)+(3 \times 1 \times 1) $$

$$ =6+0+3 $$

$$ =9 $$

Diagonal naik:

$$ (2 \times 2 \times 3)+(1 \times 1 \times 1)+(3 \times 1 \times 0) $$

$$ =12+1+0 $$

$$ =13 $$

$M_{21}$ = 9 - 13

$M_{21}$ = -4

---

## Langkah 4: Cari Minor $M_{31}$

Coret baris 3 dan kolom 1

$$
\begin{vmatrix}
1 & 0 & 3 \\
0 & 2 & 4 \\
2 & 1 & 3
\end{vmatrix}
$$

Hitung Sarrus:

Diagonal turun:

$$ (1 \times 2 \times 3)+(0 \times 4 \times 2)+(3 \times 0 \times 1) $$

$$ =6 $$

Diagonal naik:

$$ (2 \times 2 \times 3)+(1 \times 4 \times 1)+(3 \times 0 \times 0) $$

$$ =16 $$

$M_{31}$ = 6 - 16

$M_{31}$ = -10

---

## Langkah 5: Substitusi

$\det(A)$

$$ = 2(-14) $$
-(-4)
+3(-10)

$$ = -28 + 4 - 30 $$

$$ = -54 $$

---

# Jawaban Akhir

$\det(A)$ = -54

# Mencari Determinan 4×4 dengan Ekspansi Kolom Kedua

Diketahui:

$$
\begin{vmatrix}
2 & 1 & 0 & 3 \\
1 & 0 & 2 & 4 \\
3 & 1 & 2 & 1 \\
0 & 2 & 1 & 3
\end{vmatrix}
$$

---

## Langkah 1: Pilih Kolom Kedua

Kolom kedua:

$$
\begin{bmatrix}
1 \\
0 \\
1 \\
2
\end{bmatrix}
$$

Pola tanda kolom kedua:

-
+
-
+

Maka:

$\det(A)$

= -1($M_{12}$)
+0($M_{22}$)
-1($M_{32}$)
+2($M_{42}$)

Karena ada nol:

$\det(A)$

= -$M_{12}$ - $M_{32}$ + 2M42

---

## Langkah 2: Cari Minor $M_{12}$

Coret baris 1 dan kolom 2

$$
\begin{vmatrix}
1 & 2 & 4 \\
3 & 2 & 1 \\
0 & 1 & 3
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (1 \times 2 \times 3) + (2 \times 1 \times 0) + (4 \times 3 \times 1) $$

$$ = 6 + 0 + 12 $$

$$ = 18 $$

Diagonal naik:

$$ (0 \times 2 \times 4) + (1 \times 1 \times 1) + (3 \times 3 \times 2) $$

$$ = 0 + 1 + 18 $$

$$ = 19 $$

$M_{12}$

$$ = 18 - 19 $$

$$ = -1 $$

---

## Langkah 3: Cari Minor $M_{32}$

Coret baris 3 dan kolom 2

$$
\begin{vmatrix}
2 & 0 & 3 \\
1 & 2 & 4 \\
0 & 1 & 3
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 2 \times 3) + (0 \times 4 \times 0) + (3 \times 1 \times 1) $$

$$ = 12 + 0 + 3 $$

$$ = 15 $$

Diagonal naik:

$$ (0 \times 2 \times 3) + (1 \times 4 \times 2) + (3 \times 1 \times 0) $$

$$ = 0 + 8 + 0 $$

$$ = 8 $$

$M_{32}$

$$ = 15 - 8 $$

$$ = 7 $$

---

## Langkah 4: Cari Minor $M_{42}$

Coret baris 4 dan kolom 2

$$
\begin{vmatrix}
2 & 0 & 3 \\
1 & 2 & 4 \\
3 & 2 & 1
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 2 \times 1) + (0 \times 4 \times 3) + (3 \times 1 \times 2) $$

$$ = 4 + 0 + 6 $$

$$ = 10 $$

Diagonal naik:

$$ (3 \times 2 \times 3) + (2 \times 4 \times 2) + (1 \times 1 \times 0) $$

$$ = 18 + 16 + 0 $$

$$ = 34 $$

$M_{42}$

$$ = 10 - 34 $$

$$ = -24 $$

---

## Langkah 5: Substitusi

$\det(A)$

$$ = -(-1) - (7) + 2(-24) $$

$$ = 1 - 7 - 48 $$

$$ = -54 $$

---

# Jawaban Akhir

$\det(A)$ = -54

---

# Pola Tanda Kolom Kedua

Posisi:

(1,2) = -

(2,2) = +

(3,2) = -

(4,2) = +

Sehingga:

-  +  -  +

Semua ekspansi (baris atau kolom mana pun) harus menghasilkan nilai determinan yang sama.

# Mencari Determinan 4×4 dengan Ekspansi Kolom Ketiga

Diketahui:

$$
\begin{vmatrix}
2 & 1 & 0 & 3 \\
1 & 0 & 2 & 4 \\
3 & 1 & 2 & 1 \\
0 & 2 & 1 & 3
\end{vmatrix}
$$

---

## Langkah 1: Pilih Kolom Ketiga

Kolom ketiga:

$$
\begin{bmatrix}
0 \\
2 \\
2 \\
1
\end{bmatrix}
$$

Pola tanda kolom ketiga:

+
-
+
-

Maka:

$\det(A)$

= 0($M_{13}$)
-2($M_{23}$)
+2($M_{33}$)
-1($M_{43}$)

Karena ada nol:

$\det(A)$

= -2($M_{23}$)
+2($M_{33}$)
-$M_{43}$

---

## Langkah 2: Cari Minor $M_{23}$

Coret baris 2 dan kolom 3

$$
\begin{vmatrix}
2 & 1 & 3 \\
3 & 1 & 1 \\
0 & 2 & 3
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 1 \times 3) + (1 \times 1 \times 0) + (3 \times 3 \times 2) $$

$$ = 6 + 0 + 18 $$

$$ = 24 $$

Diagonal naik:

$$ (0 \times 1 \times 3) + (2 \times 1 \times 2) + (3 \times 3 \times 1) $$

$$ = 0 + 4 + 9 $$

$$ = 13 $$

$M_{23}$

$$ = 24 - 13 $$

$$ = 11 $$

---

## Langkah 3: Cari Minor $M_{33}$

Coret baris 3 dan kolom 3

$$
\begin{vmatrix}
2 & 1 & 3 \\
1 & 0 & 4 \\
0 & 2 & 3
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 0 \times 3) + (1 \times 4 \times 0) + (3 \times 1 \times 2) $$

$$ = 0 + 0 + 6 $$

$$ = 6 $$

Diagonal naik:

$$ (0 \times 0 \times 3) + (2 \times 4 \times 2) + (3 \times 1 \times 1) $$

$$ = 0 + 16 + 3 $$

$$ = 19 $$

$M_{33}$

$$ = 6 - 19 $$

$$ = -13 $$

---

## Langkah 4: Cari Minor $M_{43}$

Coret baris 4 dan kolom 3

$$
\begin{vmatrix}
2 & 1 & 3 \\
1 & 0 & 4 \\
3 & 1 & 1
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 0 \times 1) + (1 \times 4 \times 3) + (3 \times 1 \times 1) $$

$$ = 0 + 12 + 3 $$

$$ = 15 $$

Diagonal naik:

$$ (3 \times 0 \times 3) + (1 \times 4 \times 2) + (1 \times 1 \times 1) $$

$$ = 0 + 8 + 1 $$

$$ = 9 $$

$M_{43}$

$$ = 15 - 9 $$

$$ = 6 $$

---

## Langkah 5: Substitusi

$\det(A)$

$$ = -2(11) $$
+2(-13)
-6

$$ = -22 - 26 - 6 $$

$$ = -54 $$

---

# Jawaban Akhir

$\det(A)$ = -54

---

# Pola Tanda Kolom Ketiga

Posisi:

(1,3) = +

(2,3) = -

(3,3) = +

(4,3) = -

Sehingga:

+  -  +  -

Semua ekspansi baris maupun kolom harus menghasilkan determinan yang sama.

# Mencari Determinan 4×4 dengan Ekspansi Kolom Keempat

Diketahui:

$$
\begin{vmatrix}
2 & 1 & 0 & 3 \\
1 & 0 & 2 & 4 \\
3 & 1 & 2 & 1 \\
0 & 2 & 1 & 3
\end{vmatrix}
$$

---

## Langkah 1: Pilih Kolom Keempat

Kolom keempat:

$$
\begin{bmatrix}
3 \\
4 \\
1 \\
3
\end{bmatrix}
$$

Pola tanda kolom keempat:

-
+
-
+

Maka:

$\det(A)$

= -3($M_{14}$)
+4($M_{24}$)
-1($M_{34}$)
+3($M_{44}$)

---

## Langkah 2: Cari Minor $M_{14}$

Coret baris 1 dan kolom 4

$$
\begin{vmatrix}
1 & 0 & 2 \\
3 & 1 & 2 \\
0 & 2 & 1
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (1 \times 1 \times 1) + (0 \times 2 \times 0) + (2 \times 3 \times 2) $$

$$ = 1 + 0 + 12 $$

$$ = 13 $$

Diagonal naik:

$$ (0 \times 1 \times 2) + (2 \times 2 \times 1) + (1 \times 3 \times 0) $$

$$ = 0 + 4 + 0 $$

$$ = 4 $$

$M_{14}$

$$ = 13 - 4 $$

$$ = 9 $$

---

## Langkah 3: Cari Minor $M_{24}$

Coret baris 2 dan kolom 4

$$
\begin{vmatrix}
2 & 1 & 0 \\
3 & 1 & 2 \\
0 & 2 & 1
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 1 \times 1) + (1 \times 2 \times 0) + (0 \times 3 \times 2) $$

$$ = 2 + 0 + 0 $$

$$ = 2 $$

Diagonal naik:

$$ (0 \times 1 \times 0) + (2 \times 2 \times 2) + (1 \times 3 \times 1) $$

$$ = 0 + 8 + 3 $$

$$ = 11 $$

$M_{24}$

$$ = 2 - 11 $$

$$ = -9 $$

---

## Langkah 4: Cari Minor $M_{34}$

Coret baris 3 dan kolom 4

$$
\begin{vmatrix}
2 & 1 & 0 \\
1 & 0 & 2 \\
0 & 2 & 1
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 0 \times 1) + (1 \times 2 \times 0) + (0 \times 1 \times 2) $$

$$ = 0 $$

Diagonal naik:

$$ (0 \times 0 \times 0) + (2 \times 2 \times 2) + (1 \times 1 \times 1) $$

$$ = 0 + 8 + 1 $$

$$ = 9 $$

$M_{34}$

$$ = 0 - 9 $$

$$ = -9 $$

---

## Langkah 5: Cari Minor $M_{44}$

Coret baris 4 dan kolom 4

$$
\begin{vmatrix}
2 & 1 & 0 \\
1 & 0 & 2 \\
3 & 1 & 2
\end{vmatrix}
$$

Hitung dengan Sarrus:

Diagonal turun:

$$ (2 \times 0 \times 2) + (1 \times 2 \times 3) + (0 \times 1 \times 1) $$

$$ = 0 + 6 + 0 $$

$$ = 6 $$

Diagonal naik:

$$ (3 \times 0 \times 0) + (1 \times 2 \times 2) + (2 \times 1 \times 1) $$

$$ = 0 + 4 + 2 $$

$$ = 6 $$

$M_{44}$

$$ = 6 - 6 $$

$$ = 0 $$

---

## Langkah 6: Substitusi

$\det(A)$

$$ = -3(9) $$
+4(-9)
-1(-9)
+3(0)

$$ = -27 - 36 + 9 + 0 $$

$$ = -54 $$

---

# Jawaban Akhir

$\det(A)$ = -54

---

# Pola Tanda Kolom Keempat

Posisi:

(1,4) = -

(2,4) = +

(3,4) = -

(4,4) = +

Sehingga:

-  +  -  +

---

# Kesimpulan

Untuk matriks 4×4 ini:

- Ekspansi Baris 1 = -54
- Ekspansi Baris 2 = -54
- Ekspansi Baris 3 = -54
- Ekspansi Baris 4 = -54

- Ekspansi Kolom 1 = -54
- Ekspansi Kolom 2 = -54
- Ekspansi Kolom 3 = -54
- Ekspansi Kolom 4 = -54

Semua menghasilkan nilai determinan yang sama:

$\det(A)$ = -54