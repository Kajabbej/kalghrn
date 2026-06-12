# Determinan Matriks

Halaman ini membahas cara mencari determinan matriks persegi untuk ukuran $2 \times 2$, $3 \times 3$, dan $4 \times 4$.

---

## Mencari Determinan $2 \times 2$

**Diketahui:**
$$
A = \begin{bmatrix}
3 & 2 \\
1 & 4
\end{bmatrix}
$$

### Rumus Determinan $2 \times 2$
$$
\det(A) = ad - bc
$$

### Identifikasi Elemen
$$
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
=
\begin{bmatrix}
3 & 2 \\
1 & 4
\end{bmatrix}
$$

Maka didapatkan nilai elemen:
* $a = 3$
* $b = 2$
* $c = 1$
* $d = 4$

### Substitusi ke Rumus
$$
\det(A) = (3 \times 4) - (2 \times 1) = 12 - 2 = 10
$$

**Jawaban Akhir:**
$$
\det(A) = 10
$$

---

### Bentuk Ekspansi Baris Pertama ($2 \times 2$)
Baris pertama: $[3, 2]$ dengan pola tanda $[+, -]$:
$$
\det(A) = 3(4) - 2(1) = 12 - 2 = 10
$$

### Kesimpulan ($2 \times 2$)
Untuk matriks berukuran $2 \times 2$:
$$
\det \begin{bmatrix} a & b \\ c & d \end{bmatrix} = ad - bc
$$

---

## Mencari Determinan $3 \times 3$ dengan Ekspansi Baris Pertama

**Diketahui:**
$$
A = \begin{bmatrix}
1 & 2 & 3 \\
0 & 4 & 5 \\
1 & 0 & 6
\end{bmatrix}
$$

### Langkah 1: Pilih Baris Pertama
Baris pertama: $[1, 2, 3]$ dengan pola tanda $[+, -, +]$:
$$
\det(A) = 1(M_{11}) - 2(M_{12}) + 3(M_{13})
$$

### Langkah 2: Cari Minor $M_{11}$
Coret baris 1 dan kolom 1:
$$
M_{11} = \begin{vmatrix}
4 & 5 \\
0 & 6
\end{vmatrix}
$$
$$
\det(M_{11}) = (4 \times 6) - (5 \times 0) = 24
$$

### Langkah 3: Cari Minor $M_{12}$
Coret baris 1 dan kolom 2:
$$
M_{12} = \begin{vmatrix}
0 & 5 \\
1 & 6
\end{vmatrix}
$$
$$
\det(M_{12}) = (0 \times 6) - (5 \times 1) = -5
$$

### Langkah 4: Cari Minor $M_{13}$
Coret baris 1 dan kolom 3:
$$
M_{13} = \begin{vmatrix}
0 & 4 \\
1 & 0
\end{vmatrix}
$$
$$
\det(M_{13}) = (0 \times 0) - (4 \times 1) = -4
$$

### Langkah 5: Substitusi ke Rumus
$$
\det(A) = 1(24) - 2(-5) + 3(-4) = 24 + 10 - 12 = 22
$$

**Jawaban Akhir:**
$$
\det(A) = 22
$$

---

### Pola yang Harus Diingat ($3 \times 3$)
Untuk ekspansi baris pertama matriks $3 \times 3$:
$$
\det(A) = a(M_{11}) - b(M_{12}) + c(M_{13})
$$
Pola tanda:
$$
\begin{bmatrix}
+ & - & + \\
- & + & - \\
+ & - & +
\end{bmatrix}
$$

Langkah-langkah perhitungan:
1. Pilih baris atau kolom yang diinginkan.
2. Coret baris dan kolom yang bersesuaian dengan elemen tersebut.
3. Hitung minor matriks $2 \times 2$ yang tersisa.
4. Kalikan minor dengan elemen pembentuk dan tandanya.
5. Jumlahkan seluruh hasil kali kofaktor untuk mendapatkan determinan akhir.

---

## Mencari Determinan $4 \times 4$ dengan Ekspansi Baris Pertama

**Diketahui:**
$$
A = \begin{bmatrix}
2 & 0 & 1 & 0 \\
3 & 1 & 2 & 4 \\
1 & 2 & 3 & 1 \\
0 & 1 & 2 & 3
\end{bmatrix}
$$

### Langkah 1: Pilih Baris Pertama
Baris pertama: $[2, 0, 1, 0]$ dengan pola tanda $[+, -, +, -]$:
$$
\det(A) = 2M_{11} - 0M_{12} + 1M_{13} - 0M_{14}
$$
Karena terdapat elemen nol:
$$
\det(A) = 2M_{11} + M_{13}
$$

### Langkah 2: Cari Minor $M_{11}$
Coret baris 1 dan kolom 1:
$$
M_{11} = \begin{vmatrix}
1 & 2 & 4 \\
2 & 3 & 1 \\
1 & 2 & 3
\end{vmatrix}
$$
Hitung menggunakan metode Sarrus:
* Diagonal turun: $(1 \times 3 \times 3) + (2 \times 1 \times 1) + (4 \times 2 \times 2) = 9 + 2 + 16 = 27$
* Diagonal naik: $(1 \times 3 \times 4) + (2 \times 1 \times 1) + (3 \times 2 \times 2) = 12 + 2 + 12 = 26$
$$
M_{11} = 27 - 26 = 1
$$

### Langkah 3: Cari Minor $M_{13}$
Coret baris 1 dan kolom 3:
$$
M_{13} = \begin{vmatrix}
3 & 1 & 4 \\
1 & 2 & 1 \\
0 & 1 & 3
\end{vmatrix}
$$
Hitung menggunakan metode Sarrus:
* Diagonal turun: $(3 \times 2 \times 3) + (1 \times 1 \times 0) + (4 \times 1 \times 1) = 18 + 0 + 4 = 22$
* Diagonal naik: $(0 \times 2 \times 4) + (1 \times 1 \times 3) + (3 \times 1 \times 1) = 0 + 3 + 3 = 6$
$$
M_{13} = 22 - 6 = 16
$$

### Langkah 4: Substitusi ke Rumus
$$
\det(A) = 2(1) + 16 = 2 + 16 = 18
$$

**Jawaban Akhir:**
$$
\det(A) = 18
$$

---

## Eksplorasi Ekspansi Baris & Kolom Lainnya ($4 \times 4$)

Teorema Laplace menyatakan bahwa perhitungan determinan dengan ekspansi kofaktor pada baris atau kolom manapun akan menghasilkan nilai yang sama. Untuk membuktikannya, kita gunakan matriks berikut:
$$
B = \begin{bmatrix}
2 & 1 & 0 & 3 \\
1 & 0 & 2 & 4 \\
3 & 1 & 2 & 1 \\
0 & 2 & 1 & 3
\end{bmatrix}
$$

Pola tanda kofaktor $4 \times 4$ yang wajib diingat:
$$
\begin{bmatrix}
+ & - & + & - \\
- & + & - & + \\
+ & - & + & - \\
- & + & - & +
\end{bmatrix}
$$

Berikut rincian perhitungan langkah demi langkah untuk setiap ekspansi baris dan kolom (klik untuk memperluas):

<details>
<summary><b>Ekspansi Baris Kedua (Hasil: -54)</b></summary>

Baris kedua: $[1, 0, 2, 4]$ dengan pola tanda $[-, +, -, +]$:
$$
\det(B) = -1(M_{21}) + 0(M_{22}) - 2(M_{23}) + 4(M_{24})
$$
Karena ada nol:
$$
\det(B) = -M_{21} - 2M_{23} + 4M_{24}
$$

* **Cari Minor $M_{21}$** (Coret baris 2 dan kolom 1):
$$
M_{21} = \begin{vmatrix}
1 & 0 & 3 \\
1 & 2 & 1 \\
2 & 1 & 3
\end{vmatrix}
$$
  * Diagonal turun: $(1\times2\times3) + (0\times1\times2) + (3\times1\times1) = 6 + 0 + 3 = 9$
  * Diagonal naik: $(2\times2\times3) + (1\times1\times1) + (3\times1\times0) = 12 + 1 + 0 = 13$
$$
M_{21} = 9 - 13 = -4
$$

* **Cari Minor $M_{23}$** (Coret baris 2 dan kolom 3):
$$
M_{23} = \begin{vmatrix}
2 & 1 & 3 \\
3 & 1 & 1 \\
0 & 2 & 3
\end{vmatrix}
$$
  * Diagonal turun: $(2\times1\times3) + (1\times1\times0) + (3\times3\times2) = 6 + 0 + 18 = 24$
  * Diagonal naik: $(0\times1\times3) + (2\times1\times2) + (3\times3\times1) = 0 + 4 + 9 = 13$
$$
M_{23} = 24 - 13 = 11
$$

* **Cari Minor $M_{24}$** (Coret baris 2 dan kolom 4):
$$
M_{24} = \begin{vmatrix}
2 & 1 & 0 \\
3 & 1 & 2 \\
0 & 2 & 1
\end{vmatrix}
$$
  * Diagonal turun: $(2\times1\times1) + (1\times2\times0) + (0\times3\times2) = 2 + 0 + 0 = 2$
  * Diagonal naik: $(0\times1\times0) + (2\times2\times2) + (1\times3\times1) = 0 + 8 + 3 = 11$
$$
M_{24} = 2 - 11 = -9
$$

**Substitusi ke Rumus:**
$$
\det(B) = -(-4) - 2(11) + 4(-9) = 4 - 22 - 36 = -54
$$
</details>

<details>
<summary><b>Ekspansi Baris Ketiga (Hasil: -54)</b></summary>

Baris ketiga: $[3, 1, 2, 1]$ dengan pola tanda $[+, -, +, -]$:
$$
\det(B) = 3(M_{31}) - 1(M_{32}) + 2(M_{33}) - 1(M_{34})
$$

* **Cari Minor $M_{31}$** (Coret baris 3 dan kolom 1):
$$
M_{31} = \begin{vmatrix}
1 & 0 & 3 \\
0 & 2 & 4 \\
2 & 1 & 3
\end{vmatrix}
$$
  * Diagonal turun: $(1\times2\times3) + (0\times4\times2) + (3\times0\times1) = 6 + 0 + 0 = 6$
  * Diagonal naik: $(2\times2\times3) + (1\times4\times1) + (3\times0\times0) = 12 + 4 + 0 = 16$
$$
M_{31} = 6 - 16 = -10
$$

* **Cari Minor $M_{32}$** (Coret baris 3 dan kolom 2):
$$
M_{32} = \begin{vmatrix}
2 & 0 & 3 \\
1 & 2 & 4 \\
0 & 1 & 3
\end{vmatrix}
$$
  * Diagonal turun: $(2\times2\times3) + (0\times4\times0) + (3\times1\times1) = 12 + 0 + 3 = 15$
  * Diagonal naik: $(0\times2\times3) + (1\times4\times2) + (3\times1\times0) = 0 + 8 + 0 = 8$
$$
M_{32} = 15 - 8 = 7
$$

* **Cari Minor $M_{33}$** (Coret baris 3 dan kolom 3):
$$
M_{33} = \begin{vmatrix}
2 & 1 & 3 \\
1 & 0 & 4 \\
0 & 2 & 3
\end{vmatrix}
$$
  * Diagonal turun: $(2\times0\times3) + (1\times4\times0) + (3\times1\times2) = 0 + 0 + 6 = 6$
  * Diagonal naik: $(0\times0\times3) + (2\times4\times2) + (3\times1\times1) = 0 + 16 + 3 = 19$
$$
M_{33} = 6 - 19 = -13
$$

* **Cari Minor $M_{34}$** (Coret baris 3 dan kolom 4):
$$
M_{34} = \begin{vmatrix}
2 & 1 & 0 \\
1 & 0 & 2 \\
0 & 2 & 1
\end{vmatrix}
$$
  * Diagonal turun: $(2\times0\times1) + (1\times2\times0) + (0\times1\times2) = 0$
  * Diagonal naik: $(0\times0\times0) + (2\times2\times2) + (1\times1\times1) = 0 + 8 + 1 = 9$
$$
M_{34} = 0 - 9 = -9
$$

**Substitusi ke Rumus:**
$$
\det(B) = 3(-10) - 1(7) + 2(-13) - 1(-9) = -30 - 7 - 26 + 9 = -54
$$
</details>

<details>
<summary><b>Ekspansi Baris Keempat (Hasil: -54)</b></summary>

Baris keempat: $[0, 2, 1, 3]$ dengan pola tanda $[-, +, -, +]$:
$$
\det(B) = -0(M_{41}) + 2(M_{42}) - 1(M_{43}) + 3(M_{44})
$$
Karena ada nol:
$$
\det(B) = 2(M_{42}) - M_{43} + 3(M_{44})
$$

* **Cari Minor $M_{42}$** (Coret baris 4 dan kolom 2):
$$
M_{42} = \begin{vmatrix}
2 & 0 & 3 \\
1 & 2 & 4 \\
3 & 2 & 1
\end{vmatrix}
$$
  * Diagonal turun: $(2\times2\times1) + (0\times4\times3) + (3\times1\times2) = 4 + 0 + 6 = 10$
  * Diagonal naik: $(3\times2\times3) + (2\times4\times2) + (1\times1\times0) = 18 + 16 + 0 = 34$
$$
M_{42} = 10 - 34 = -24
$$

* **Cari Minor $M_{43}$** (Coret baris 4 dan kolom 3):
$$
M_{43} = \begin{vmatrix}
2 & 1 & 3 \\
1 & 0 & 4 \\
3 & 1 & 1
\end{vmatrix}
$$
  * Diagonal turun: $(2\times0\times1) + (1\times4\times3) + (3\times1\times1) = 0 + 12 + 3 = 15$
  * Diagonal naik: $(3\times0\times3) + (1\times4\times2) + (1\times1\times1) = 0 + 8 + 1 = 9$
$$
M_{43} = 15 - 9 = 6
$$

* **Cari Minor $M_{44}$** (Coret baris 4 dan kolom 4):
$$
M_{44} = \begin{vmatrix}
2 & 1 & 0 \\
1 & 0 & 2 \\
3 & 1 & 2
\end{vmatrix}
$$
  * Diagonal turun: $(2\times0\times2) + (1\times2\times3) + (0\times1\times1) = 0 + 6 + 0 = 6$
  * Diagonal naik: $(3\times0\times0) + (1\times2\times2) + (2\times1\times1) = 0 + 4 + 2 = 6$
$$
M_{44} = 6 - 6 = 0
$$

**Substitusi ke Rumus:**
$$
\det(B) = 2(-24) - (6) + 3(0) = -48 - 6 + 0 = -54
$$
</details>

<details>
<summary><b>Ekspansi Kolom Pertama (Hasil: -54)</b></summary>

Kolom pertama: $[2, 1, 3, 0]^T$ dengan pola tanda $[+, -, +, -]$:
$$
\det(B) = 2(M_{11}) - 1(M_{21}) + 3(M_{31}) - 0(M_{41})
$$
Karena elemen terakhir nol:
$$
\det(B) = 2(M_{11}) - M_{21} + 3(M_{31})
$$

* **Cari Minor $M_{11}$** (Coret baris 1 dan kolom 1):
$$
M_{11} = \begin{vmatrix}
0 & 2 & 4 \\
1 & 2 & 1 \\
2 & 1 & 3
\end{vmatrix}
$$
  * Diagonal turun: $(0\times2\times3)+(2\times1\times2)+(4\times1\times1) = 0 + 4 + 4 = 8$
  * Diagonal naik: $(2\times2\times4)+(1\times1\times0)+(3\times1\times2) = 16 + 0 + 6 = 22$
$$
M_{11} = 8 - 22 = -14
$$

* **Cari Minor $M_{21}$** (Sudah dihitung di bagian Baris 2): $-4$

* **Cari Minor $M_{31}$** (Sudah dihitung di bagian Baris 3): $-10$

**Substitusi ke Rumus:**
$$
\det(B) = 2(-14) - (-4) + 3(-10) = -28 + 4 - 30 = -54
$$
</details>

<details>
<summary><b>Ekspansi Kolom Kedua (Hasil: -54)</b></summary>

Kolom kedua: $[1, 0, 1, 2]^T$ dengan pola tanda $[-, +, -, +]$:
$$
\det(B) = -1(M_{12}) + 0(M_{22}) - 1(M_{32}) + 2(M_{42})
$$
Karena ada nol:
$$
\det(B) = -M_{12} - M_{32} + 2M_{42}
$$

* **Cari Minor $M_{12}$** (Coret baris 1 dan kolom 2):
$$
M_{12} = \begin{vmatrix}
1 & 2 & 4 \\
3 & 2 & 1 \\
0 & 1 & 3
\end{vmatrix}
$$
  * Diagonal turun: $(1\times2\times3) + (2\times1\times0) + (4\times3\times1) = 6 + 0 + 12 = 18$
  * Diagonal naik: $(0\times2\times4) + (1\times1\times1) + (3\times3\times2) = 0 + 1 + 18 = 19$
$$
M_{12} = 18 - 19 = -1
$$

* **Cari Minor $M_{32}$** (Sudah dihitung di bagian Baris 3): $7$

* **Cari Minor $M_{42}$** (Sudah dihitung di bagian Baris 4): $-24$

**Substitusi ke Rumus:**
$$
\det(B) = -(-1) - (7) + 2(-24) = 1 - 7 - 48 = -54
$$
</details>

<details>
<summary><b>Ekspansi Kolom Ketiga (Hasil: -54)</b></summary>

Kolom ketiga: $[0, 2, 2, 1]^T$ dengan pola tanda $[+, -, +, -]$:
$$
\det(B) = 0(M_{13}) - 2(M_{23}) + 2(M_{33}) - 1(M_{43})
$$
Karena ada nol:
$$
\det(B) = -2(M_{23}) + 2(M_{33}) - M_{43}
$$

* **Cari Minor $M_{23}$** (Sudah dihitung di bagian Baris 2): $11$

* **Cari Minor $M_{33}$** (Sudah dihitung di bagian Baris 3): $-13$

* **Cari Minor $M_{43}$** (Sudah dihitung di bagian Baris 4): $6$

**Substitusi ke Rumus:**
$$
\det(B) = -2(11) + 2(-13) - 6 = -22 - 26 - 6 = -54
$$
</details>

<details>
<summary><b>Ekspansi Kolom Keempat (Hasil: -54)</b></summary>

Kolom keempat: $[3, 4, 1, 3]^T$ dengan pola tanda $[-, +, -, +]$:
$$
\det(B) = -3(M_{14}) + 4(M_{24}) - 1(M_{34}) + 3(M_{44})
$$

* **Cari Minor $M_{14}$** (Coret baris 1 dan kolom 4):
$$
M_{14} = \begin{vmatrix}
1 & 0 & 2 \\
3 & 1 & 2 \\
0 & 2 & 1
\end{vmatrix}
$$
  * Diagonal turun: $(1\times1\times1) + (0\times2\times0) + (2\times3\times2) = 1 + 0 + 12 = 13$
  * Diagonal naik: $(0\times1\times2) + (2\times2\times1) + (1\times3\times0) = 0 + 4 + 0 = 4$
$$
M_{14} = 13 - 4 = 9
$$

* **Cari Minor $M_{24}$** (Sudah dihitung di bagian Baris 2): $-9$

* **Cari Minor $M_{34}$** (Sudah dihitung di bagian Baris 3): $-9$

* **Cari Minor $M_{44}$** (Sudah dihitung di bagian Baris 4): $0$

**Substitusi ke Rumus:**
$$
\det(B) = -3(9) + 4(-9) - (-9) + 3(0) = -27 - 36 + 9 + 0 = -54
$$
</details>

---

## Kesimpulan

Untuk matriks $4 \times 4$ ini, kita dapat melihat bahwa seluruh metode ekspansi menghasilkan determinan yang konsisten:
* Ekspansi Baris 1 = $-54$
* Ekspansi Baris 2 = $-54$
* Ekspansi Baris 3 = $-54$
* Ekspansi Baris 4 = $-54$
* Ekspansi Kolom 1 = $-54$
* Ekspansi Kolom 2 = $-54$
* Ekspansi Kolom 3 = $-54$
* Ekspansi Kolom 4 = $-54$

$$
\det(B) = -54
$$

Seluruh perhitungan membuktikan keabsahan Teorema Laplace untuk penentuan determinan matriks menggunakan baris atau kolom manapun.