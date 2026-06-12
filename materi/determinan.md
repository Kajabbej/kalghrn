# Determinan Matriks

Halaman ini membahas konsep determinan matriks persegi dari ukuran $2 \times 2$, $3 \times 3$, hingga $4 \times 4$, lengkap dengan metode ekspansi kofaktor (baris/kolom) dan metode Sarrus.

---

## 1. Determinan Matriks $2 \times 2$

Misalkan kita memiliki matriks persegi $A$ berukuran $2 \times 2$:
$$
A = \begin{bmatrix} 
3 & 2 \\ 
1 & 4 
\end{bmatrix}
$$

### Rumus Determinan
Determinan dari matriks $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$ didefinisikan sebagai:
$$
\det(A) = \begin{vmatrix} 
a & b \\ 
c & d 
\end{vmatrix} = ad - bc
$$

### Contoh Perhitungan
Dari matriks $A$ di atas, kita dapat mengidentifikasi elemen-elemennya:
* $a = 3$
* $b = 2$
* $c = 1$
* $d = 4$

Substitusi ke dalam rumus:
$$
\det(A) = (3 \times 4) - (2 \times 1) = 12 - 2 = 10
$$

---

## 2. Determinan Matriks $3 \times 3$ dengan Ekspansi Kofaktor

Metode ekspansi kofaktor digunakan untuk menghitung determinan matriks berukuran $3 \times 3$ atau lebih besar dengan cara mereduksi ukurannya menjadi minor-minor matriks $2 \times 2$.

Pola tanda kofaktor untuk matriks $3 \times 3$ adalah:
$$
\begin{bmatrix} 
+ & - & + \\ 
- & + & - \\ 
+ & - & + 
\end{bmatrix}
$$

### Contoh Perhitungan (Ekspansi Baris Pertama)
**Diketahui:**
$$
A = \begin{bmatrix} 
1 & 2 & 3 \\ 
0 & 4 & 5 \\ 
1 & 0 & 6 
\end{bmatrix}
$$

Kita akan menggunakan ekspansi sepanjang **baris pertama** yaitu $[1, 2, 3]$ dengan pola tanda $[+, -, +]$:
$$
\det(A) = 1 \cdot M_{11} - 2 \cdot M_{12} + 3 \cdot M_{13}
$$

#### Langkah 1: Hitung Minor $M_{11}$ (Coret Baris 1 & Kolom 1)
$$
M_{11} = \begin{vmatrix} 4 & 5 \\ 0 & 6 \end{vmatrix} = (4 \times 6) - (5 \times 0) = 24
$$

#### Langkah 2: Hitung Minor $M_{12}$ (Coret Baris 1 & Kolom 2)
$$
M_{12} = \begin{vmatrix} 0 & 5 \\ 1 & 6 \end{vmatrix} = (0 \times 6) - (5 \times 1) = -5
$$

#### Langkah 3: Hitung Minor $M_{13}$ (Coret Baris 1 & Kolom 3)
$$
M_{13} = \begin{vmatrix} 0 & 4 \\ 1 & 0 \end{vmatrix} = (0 \times 0) - (4 \times 1) = -4
$$

#### Langkah 4: Substitusi dan Hasil Akhir
$$
\det(A) = 1(24) - 2(-5) + 3(-4) = 24 + 10 - 12 = 22
$$

---

## 3. Determinan Matriks $4 \times 4$ (Ekspansi Baris Pertama)

Untuk matriks $4 \times 4$, ekspansi kofaktor akan mereduksinya menjadi beberapa minor $3 \times 3$.

Pola tanda kofaktor untuk matriks $4 \times 4$ adalah:
$$
\begin{bmatrix} 
+ & - & + & - \\ 
- & + & - & + \\ 
+ & - & + & - \\ 
- & + & - & + 
\end{bmatrix}
$$

### Contoh Perhitungan
**Diketahui:**
$$
A = \begin{bmatrix} 
2 & 0 & 1 & 0 \\ 
3 & 1 & 2 & 4 \\ 
1 & 2 & 3 & 1 \\ 
0 & 1 & 2 & 3 
\end{bmatrix}
$$

Kita pilih **baris pertama** $[2, 0, 1, 0]$ dengan pola tanda $[+, -, +, -]$:
$$
\det(A) = 2 \cdot M_{11} - 0 \cdot M_{12} + 1 \cdot M_{13} - 0 \cdot M_{14} = 2 \cdot M_{11} + M_{13}
$$

#### Langkah 1: Hitung Minor $M_{11}$ (Coret Baris 1 & Kolom 1)
$$
M_{11} = \begin{vmatrix} 
1 & 2 & 4 \\ 
2 & 3 & 1 \\ 
1 & 2 & 3 
\end{vmatrix}
$$
Hitung menggunakan metode **Sarrus**:
* Diagonal turun: $(1\times3\times3) + (2\times1\times1) + (4\times2\times2) = 9 + 2 + 16 = 27$
* Diagonal naik: $(1\times3\times4) + (2\times1\times1) + (3\times2\times2) = 12 + 2 + 12 = 26$
$$
M_{11} = 27 - 26 = 1
$$

#### Langkah 2: Hitung Minor $M_{13}$ (Coret Baris 1 & Kolom 3)
$$
M_{13} = \begin{vmatrix} 
3 & 1 & 4 \\ 
1 & 2 & 1 \\ 
0 & 1 & 3 
\end{vmatrix}
$$
Hitung menggunakan metode **Sarrus**:
* Diagonal turun: $(3\times2\times3) + (1\times1\times0) + (4\times1\times1) = 18 + 0 + 4 = 22$
* Diagonal naik: $(0\times2\times4) + (1\times1\times3) + (3\times1\times1) = 0 + 3 + 3 = 6$
$$
M_{13} = 22 - 6 = 16
$$

#### Langkah 3: Hasil Akhir
$$
\det(A) = 2(1) + 16 = 18
$$

---

## 4. Eksplorasi Ekspansi Baris & Kolom Lainnya (Matriks $4 \times 4$)

Teorema Laplace menjamin bahwa kita akan mendapatkan nilai determinan yang sama tidak peduli baris atau kolom mana yang kita pilih untuk ekspansi. 

Mari kita buktikan menggunakan matriks $B$ berikut:
$$
B = \begin{bmatrix} 
2 & 1 & 0 & 3 \\ 
1 & 0 & 2 & 4 \\ 
3 & 1 & 2 & 1 \\ 
0 & 2 & 1 & 3 
\end{bmatrix}
$$

Berikut adalah rincian perhitungan ekspansi kofaktor untuk seluruh baris dan kolom (klik untuk membukanya):

<details>
<summary><b>Ekspansi Baris Kedua (Hasil: -54)</b></summary>

Baris kedua: $[1, 0, 2, 4]$ dengan tanda $[-, +, -, +]$:
$$
\det(B) = -1 \cdot M_{21} + 0 \cdot M_{22} - 2 \cdot M_{23} + 4 \cdot M_{24} = -M_{21} - 2M_{23} + 4M_{24}
$$

*   **Hitung Minor $M_{21}$** (Coret Baris 2 & Kolom 1):
    $$
    M_{21} = \begin{vmatrix} 1 & 0 & 3 \\ 1 & 2 & 1 \\ 2 & 1 & 3 \end{vmatrix} = (6 + 0 + 3) - (12 + 1 + 0) = 9 - 13 = -4
    $$
*   **Hitung Minor $M_{23}$** (Coret Baris 2 & Kolom 3):
    $$
    M_{23} = \begin{vmatrix} 2 & 1 & 3 \\ 3 & 1 & 1 \\ 0 & 2 & 3 \end{vmatrix} = (6 + 0 + 18) - (0 + 4 + 9) = 24 - 13 = 11
    $$
*   **Hitung Minor $M_{24}$** (Coret Baris 2 & Kolom 4):
    $$
    M_{24} = \begin{vmatrix} 2 & 1 & 0 \\ 3 & 1 & 2 \\ 0 & 2 & 1 \end{vmatrix} = (2 + 0 + 0) - (0 + 8 + 3) = 2 - 11 = -9
    $$

**Substitusi:**
$$
\det(B) = -(-4) - 2(11) + 4(-9) = 4 - 22 - 36 = -54
$$
</details>

<details>
<summary><b>Ekspansi Baris Ketiga (Hasil: -54)</b></summary>

Baris ketiga: $[3, 1, 2, 1]$ dengan tanda $[+, -, +, -]$:
$$
\det(B) = 3 \cdot M_{31} - 1 \cdot M_{32} + 2 \cdot M_{33} - 1 \cdot M_{34}
$$

*   **Hitung Minor $M_{31}$**:
    $$
    M_{31} = \begin{vmatrix} 1 & 0 & 3 \\ 0 & 2 & 4 \\ 2 & 1 & 3 \end{vmatrix} = (6 + 0 + 0) - (12 + 4 + 0) = 6 - 16 = -10
    $$
*   **Hitung Minor $M_{32}$**:
    $$
    M_{32} = \begin{vmatrix} 2 & 0 & 3 \\ 1 & 2 & 4 \\ 0 & 1 & 3 \end{vmatrix} = (12 + 0 + 3) - (0 + 8 + 0) = 15 - 8 = 7
    $$
*   **Hitung Minor $M_{33}$**:
    $$
    M_{33} = \begin{vmatrix} 2 & 1 & 3 \\ 1 & 0 & 4 \\ 0 & 2 & 3 \end{vmatrix} = (0 + 0 + 6) - (0 + 16 + 3) = 6 - 19 = -13
    $$
*   **Hitung Minor $M_{34}$**:
    $$
    M_{34} = \begin{vmatrix} 2 & 1 & 0 \\ 1 & 0 & 2 \\ 0 & 2 & 1 \end{vmatrix} = 0 - (0 + 8 + 1) = -9
    $$

**Substitusi:**
$$
\det(B) = 3(-10) - 1(7) + 2(-13) - 1(-9) = -30 - 7 - 26 + 9 = -54
$$
</details>

<details>
<summary><b>Ekspansi Baris Keempat (Hasil: -54)</b></summary>

Baris keempat: $[0, 2, 1, 3]$ dengan tanda $[-, +, -, +]$:
$$
\det(B) = -0 \cdot M_{41} + 2 \cdot M_{42} - 1 \cdot M_{43} + 3 \cdot M_{44} = 2 \cdot M_{42} - M_{43} + 3 \cdot M_{44}
$$

*   **Hitung Minor $M_{42}$**:
    $$
    M_{42} = \begin{vmatrix} 2 & 0 & 3 \\ 1 & 2 & 4 \\ 3 & 2 & 1 \end{vmatrix} = (4 + 0 + 6) - (18 + 16 + 0) = 10 - 34 = -24
    $$
*   **Hitung Minor $M_{43}$**:
    $$
    M_{43} = \begin{vmatrix} 2 & 1 & 3 \\ 1 & 0 & 4 \\ 3 & 1 & 1 \end{vmatrix} = (0 + 12 + 3) - (0 + 8 + 1) = 15 - 9 = 6
    $$
*   **Hitung Minor $M_{44}$**:
    $$
    M_{44} = \begin{vmatrix} 2 & 1 & 0 \\ 1 & 0 & 2 \\ 3 & 1 & 2 \end{vmatrix} = (0 + 6 + 0) - (0 + 4 + 2) = 6 - 6 = 0
    $$

**Substitusi:**
$$
\det(B) = 2(-24) - 6 + 3(0) = -48 - 6 = -54
$$
</details>

<details>
<summary><b>Ekspansi Kolom Pertama (Hasil: -54)</b></summary>

Kolom pertama: $[2, 1, 3, 0]^T$ dengan tanda $[+, -, +, -]$:
$$
\det(B) = 2 \cdot M_{11} - 1 \cdot M_{21} + 3 \cdot M_{31} - 0 = 2 \cdot M_{11} - M_{21} + 3 \cdot M_{31}
$$

*   **Hitung Minor $M_{11}$**:
    $$
    M_{11} = \begin{vmatrix} 0 & 2 & 4 \\ 1 & 2 & 1 \\ 2 & 1 & 3 \end{vmatrix} = (0 + 4 + 4) - (16 + 0 + 6) = 8 - 22 = -14
    $$
*   **Minor $M_{21}$** (Sudah dihitung di bagian Baris 2): $-4$
*   **Minor $M_{31}$** (Sudah dihitung di bagian Baris 3): $-10$

**Substitusi:**
$$
\det(B) = 2(-14) - (-4) + 3(-10) = -28 + 4 - 30 = -54
$$
</details>

<details>
<summary><b>Ekspansi Kolom Kedua (Hasil: -54)</b></summary>

Kolom kedua: $[1, 0, 1, 2]^T$ dengan tanda $[-, +, -, +]$:
$$
\det(B) = -1 \cdot M_{12} + 0 - 1 \cdot M_{32} + 2 \cdot M_{42} = -M_{12} - M_{32} + 2 \cdot M_{42}
$$

*   **Hitung Minor $M_{12}$**:
    $$
    M_{12} = \begin{vmatrix} 1 & 2 & 4 \\ 3 & 2 & 1 \\ 0 & 1 & 3 \end{vmatrix} = (6 + 0 + 12) - (0 + 1 + 18) = 18 - 19 = -1
    $$
*   **Minor $M_{32}$** (Sudah dihitung di bagian Baris 3): $7$
*   **Minor $M_{42}$** (Sudah dihitung di bagian Baris 4): $-24$

**Substitusi:**
$$
\det(B) = -(-1) - 7 + 2(-24) = 1 - 7 - 48 = -54
$$
</details>

<details>
<summary><b>Ekspansi Kolom Ketiga (Hasil: -54)</b></summary>

Kolom ketiga: $[0, 2, 2, 1]^T$ dengan tanda $[+, -, +, -]$:
$$
\det(B) = 0 - 2 \cdot M_{23} + 2 \cdot M_{33} - 1 \cdot M_{43} = -2 \cdot M_{23} + 2 \cdot M_{33} - M_{43}
$$

*   **Minor $M_{23}$** (Sudah dihitung di bagian Baris 2): $11$
*   **Minor $M_{33}$** (Sudah dihitung di bagian Baris 3): $-13$
*   **Minor $M_{43}$** (Sudah dihitung di bagian Baris 4): $6$

**Substitusi:**
$$
\det(B) = -2(11) + 2(-13) - 6 = -22 - 26 - 6 = -54
$$
</details>

<details>
<summary><b>Ekspansi Kolom Keempat (Hasil: -54)</b></summary>

Kolom keempat: $[3, 4, 1, 3]^T$ dengan tanda $[-, +, -, +]$:
$$
\det(B) = -3 \cdot M_{14} + 4 \cdot M_{24} - 1 \cdot M_{34} + 3 \cdot M_{44}
$$

*   **Hitung Minor $M_{14}$**:
    $$
    M_{14} = \begin{vmatrix} 1 & 0 & 2 \\ 3 & 1 & 2 \\ 0 & 2 & 1 \end{vmatrix} = (1 + 0 + 12) - (0 + 4 + 0) = 13 - 4 = 9
    $$
*   **Minor $M_{24}$** (Sudah dihitung di bagian Baris 2): $-9$
*   **Minor $M_{34}$** (Sudah dihitung di bagian Baris 3): $-9$
*   **Minor $M_{44}$** (Sudah dihitung di bagian Baris 4): $0$

**Substitusi:**
$$
\det(B) = -3(9) + 4(-9) - (-9) + 3(0) = -27 - 36 + 9 = -54
$$
</details>

---

## Kesimpulan

Berdasarkan hasil perhitungan di atas, semua metode ekspansi baris dan kolom menghasilkan determinan yang konsisten:
$$
\det(B) = -54
$$
Hal ini membuktikan keabsahan Teorema Laplace untuk penentuan determinan matriks berukuran tinggi menggunakan baris atau kolom manapun yang paling memudahkan perhitungan (biasanya yang memiliki banyak elemen bernilai $0$).