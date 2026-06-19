# Determinan Matriks | Dekomposisi Matriks | Invers Matriks

# Soal Determinan Matriks 3x3

## Soal 1
Hitung determinan dari matriks berikut:
$$A = \begin{bmatrix} 2 & 1 & 3 \\ 0 & 4 & 5 \\ 1 & 2 & 1 \end{bmatrix}$$

## Soal 2
Tentukan nilai determinan matriks:
$$B = \begin{bmatrix} 3 & 2 & 1 \\ 1 & 0 & 4 \\ 2 & 5 & 1 \end{bmatrix}$$

## Soal 3
Jika:
$$C = \begin{bmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 1 & 1 & 1 \end{bmatrix}$$
Tentukan $\det(C)$ dan jelaskan matriks tersebut singular atau tidak.

---

# Soal Dekomposisi Matriks (LU Decomposition)

## Soal 4
Lakukan dekomposisi $LU$ pada matriks:
$$A = \begin{bmatrix} 2 & 4 & 2 \\ 1 & 5 & 2 \\ 1 & 2 & 4 \end{bmatrix}$$
dengan bentuk:
$$A = LU$$
di mana $L$ adalah matriks segitiga bawah dan $U$ adalah matriks segitiga atas.

## Soal 5
Tentukan matriks $L$ dan $U$ dari:
$$B = \begin{bmatrix} 1 & 2 & 1 \\ 2 & 5 & 3 \\ 4 & 10 & 8 \end{bmatrix}$$
menggunakan eliminasi Gauss.

## Soal 6
Dekomposisikan matriks berikut menjadi $LU$:
$$C = \begin{bmatrix} 4 & 2 & 0 \\ 2 & 5 & 1 \\ 0 & 1 & 3 \end{bmatrix}$$

---

# Soal Invers Matriks 3x3

## Soal 7
Tentukan invers dari matriks:
$$A = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 1 \\ 2 & 3 & 4 \end{bmatrix}$$
menggunakan metode adjoin atau eliminasi Gauss-Jordan.

## Soal 8
Carilah invers matriks:
$$B = \begin{bmatrix} 2 & 1 & 0 \\ 1 & 2 & 1 \\ 0 & 1 & 2 \end{bmatrix}$$

## Soal 9
Diketahui:
$$C = \begin{bmatrix} 3 & 0 & 2 \\ 2 & 0 & -2 \\ 0 & 1 & 1 \end{bmatrix}$$
Tentukan $C^{-1}$.

# # jawaban 

## Soal 1
$$A = \begin{bmatrix} 2 & 1 & 3 \\ 0 & 4 & 5 \\ 1 & 2 & 1 \end{bmatrix}$$

### Metode 1: Ekspansi Laplace (Kolom 1)
$$\det(A) = a_{11} C_{11} + a_{21} C_{21} + a_{31} C_{31}$$
$$\det(A) = 2 \cdot (-1)^{1+1} \det\begin{bmatrix} 4 & 5 \\ 2 & 1 \end{bmatrix} + 0 \cdot (-1)^{2+1} \det\begin{bmatrix} 1 & 3 \\ 2 & 1 \end{bmatrix} + 1 \cdot (-1)^{3+1} \det\begin{bmatrix} 1 & 3 \\ 4 & 5 \end{bmatrix}$$
$$\det(A) = 2 \cdot (1)(4 \cdot 1 - 5 \cdot 2) + 0 + 1 \cdot (1)(1 \cdot 5 - 3 \cdot 4)$$
$$\det(A) = 2 \cdot (4 - 10) + 1 \cdot (5 - 12)$$
$$\det(A) = 2 \cdot (-6) + 1 \cdot (-7)$$
$$\det(A) = -12 - 7 = -19$$

### Metode 2: Aturan Sarrus
$$\begin{matrix}
2 & 1 & 3 & | & 2 & 1 \\
0 & 4 & 5 & | & 0 & 4 \\
1 & 2 & 1 & | & 1 & 2
\end{matrix}$$

$$\det(A) = (2 \cdot 4 \cdot 1 + 1 \cdot 5 \cdot 1 + 3 \cdot 0 \cdot 2) - (1 \cdot 4 \cdot 3 + 2 \cdot 5 \cdot 2 + 1 \cdot 0 \cdot 1)$$
$$\det(A) = (8 + 5 + 0) - (12 + 20 + 0)$$
$$\det(A) = 13 - 32 = -19$$

---

## Soal 2
$$B = \begin{bmatrix} 3 & 2 & 1 \\ 1 & 0 & 4 \\ 2 & 5 & 1 \end{bmatrix}$$

### Metode 1: Ekspansi Laplace (Baris 2)
$$\det(B) = b_{21} C_{21} + b_{22} C_{22} + b_{23} C_{23}$$
$$\det(B) = 1 \cdot (-1)^{2+1} \det\begin{bmatrix} 2 & 1 \\ 5 & 1 \end{bmatrix} + 0 \cdot (-1)^{2+2} \det\begin{bmatrix} 3 & 1 \\ 2 & 1 \end{bmatrix} + 4 \cdot (-1)^{2+3} \det\begin{bmatrix} 3 & 2 \\ 2 & 5 \end{bmatrix}$$
$$\det(B) = 1 \cdot (-1)(2 \cdot 1 - 1 \cdot 5) + 0 + 4 \cdot (-1)(3 \cdot 5 - 2 \cdot 2)$$
$$\det(B) = -1 \cdot (2 - 5) - 4 \cdot (15 - 4)$$
$$\det(B) = -1 \cdot (-3) - 4 \cdot (11)$$
$$\det(B) = 3 - 44 = -41$$

### Metode 2: Aturan Sarrus
$$\begin{matrix}
3 & 2 & 1 & | & 3 & 2 \\
1 & 0 & 4 & | & 1 & 0 \\
2 & 5 & 1 & | & 2 & 5
\end{matrix}$$

$$\det(B) = (3 \cdot 0 \cdot 1 + 2 \cdot 4 \cdot 2 + 1 \cdot 1 \cdot 5) - (2 \cdot 0 \cdot 1 + 5 \cdot 4 \cdot 3 + 1 \cdot 1 \cdot 2)$$
$$\det(B) = (0 + 16 + 5) - (0 + 60 + 2)$$
$$\det(B) = 21 - 62 = -41$$

---

## Soal 3
$$C = \begin{bmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 1 & 1 & 1 \end{bmatrix}$$

### Analisis Ketergantungan Linier
Perhatikan bahwa Baris 2 ($R_2$) adalah 2 kali Baris 1 ($R_1$):
$$R_2 = 2R_1 \implies \begin{bmatrix} 2 & 4 & 6 \end{bmatrix} = 2 \begin{bmatrix} 1 & 2 & 3 \end{bmatrix}$$
Karena terdapat baris yang dependen secara linier, maka:
$$\det(C) = 0$$

### Verifikasi dengan Ekspansi Laplace (Baris 3)
$$\det(C) = 1 \cdot (-1)^{3+1} \det\begin{bmatrix} 2 & 3 \\ 4 & 6 \end{bmatrix} + 1 \cdot (-1)^{3+2} \det\begin{bmatrix} 1 & 3 \\ 2 & 6 \end{bmatrix} + 1 \cdot (-1)^{3+3} \det\begin{bmatrix} 1 & 2 \\ 2 & 4 \end{bmatrix}$$
$$\det(C) = 1 \cdot (1)(2 \cdot 6 - 3 \cdot 4) - 1 \cdot (1 \cdot 6 - 3 \cdot 2) + 1 \cdot (1)(1 \cdot 4 - 2 \cdot 2)$$
$$\det(C) = 1 \cdot (12 - 12) - 1 \cdot (6 - 6) + 1 \cdot (4 - 4)$$
$$\det(C) = 0 - 0 + 0 = 0$$

### Kesimpulan
Karena $\det(C) = 0$, matriks $C$ adalah **matriks singular** (tidak memiliki invers).

---

## Soal 4
$$A = \begin{bmatrix} 2 & 4 & 2 \\ 1 & 5 & 2 \\ 1 & 2 & 4 \end{bmatrix}$$

Dekomposisi dalam bentuk $A = LU$:

1. **Eliminasi Baris 2 (Kolom 1):**
   Multiplier: $m_{21} = \frac{a_{21}}{a_{11}} = \frac{1}{2} = 0.5$
   $$R_2 \leftarrow R_2 - 0.5 R_1 \implies \begin{bmatrix} 1 & 5 & 2 \end{bmatrix} - 0.5 \begin{bmatrix} 2 & 4 & 2 \end{bmatrix} = \begin{bmatrix} 0 & 3 & 1 \end{bmatrix}$$

2. **Eliminasi Baris 3 (Kolom 1):**
   Multiplier: $m_{31} = \frac{a_{31}}{a_{11}} = \frac{1}{2} = 0.5$
   $$R_3 \leftarrow R_3 - 0.5 R_1 \implies \begin{bmatrix} 1 & 2 & 4 \end{bmatrix} - 0.5 \begin{bmatrix} 2 & 4 & 2 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 3 \end{bmatrix}$$

3. **Eliminasi Baris 3 (Kolom 2):**
   Karena elemen posisi $(3,2)$ sudah bernilai $0$, multiplier $m_{32} = 0$.

### Hasil Matriks L dan U:
$$L = \begin{bmatrix} 1 & 0 & 0 \\ 0.5 & 1 & 0 \\ 0.5 & 0 & 1 \end{bmatrix}$$
$$U = \begin{bmatrix} 2 & 4 & 2 \\ 0 & 3 & 1 \\ 0 & 0 & 3 \end{bmatrix}$$

### Verifikasi perkalian:
$$LU = \begin{bmatrix} 1 & 0 & 0 \\ 0.5 & 1 & 0 \\ 0.5 & 0 & 1 \end{bmatrix} \begin{bmatrix} 2 & 4 & 2 \\ 0 & 3 & 1 \\ 0 & 0 & 3 \end{bmatrix} = \begin{bmatrix} 2 & 4 & 2 \\ 1 & 5 & 2 \\ 1 & 2 & 4 \end{bmatrix} = A$$

---

## Soal 5
$$B = \begin{bmatrix} 1 & 2 & 1 \\ 2 & 5 & 3 \\ 4 & 10 & 8 \end{bmatrix}$$

Dekomposisi dalam bentuk $B = LU$:

1. **Eliminasi Baris 2 (Kolom 1):**
   Multiplier: $m_{21} = \frac{b_{21}}{b_{11}} = \frac{2}{1} = 2$
   $$R_2 \leftarrow R_2 - 2 R_1 \implies \begin{bmatrix} 2 & 5 & 3 \end{bmatrix} - 2 \begin{bmatrix} 1 & 2 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 1 & 1 \end{bmatrix}$$

2. **Eliminasi Baris 3 (Kolom 1):**
   Multiplier: $m_{31} = \frac{b_{31}}{b_{11}} = \frac{4}{1} = 4$
   $$R_3 \leftarrow R_3 - 4 R_1 \implies \begin{bmatrix} 4 & 10 & 8 \end{bmatrix} - 4 \begin{bmatrix} 1 & 2 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 2 & 4 \end{bmatrix}$$

3. **Eliminasi Baris 3 (Kolom 2):**
   Multiplier: $m_{32} = \frac{b'_{32}}{b'_{22}} = \frac{2}{1} = 2$
   $$R_3 \leftarrow R_3 - 2 R_2 \implies \begin{bmatrix} 0 & 2 & 4 \end{bmatrix} - 2 \begin{bmatrix} 0 & 1 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 2 \end{bmatrix}$$

### Hasil Matriks L dan U:
$$L = \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 4 & 2 & 1 \end{bmatrix}$$
$$U = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 2 \end{bmatrix}$$

### Verifikasi perkalian:
$$LU = \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 4 & 2 & 1 \end{bmatrix} \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 2 \end{bmatrix} = \begin{bmatrix} 1 & 2 & 1 \\ 2 & 5 & 3 \\ 4 & 10 & 8 \end{bmatrix} = B$$

---

## Soal 6
$$C = \begin{bmatrix} 4 & 2 & 0 \\ 2 & 5 & 1 \\ 0 & 1 & 3 \end{bmatrix}$$

Dekomposisi dalam bentuk $C = LU$:

1. **Eliminasi Baris 2 (Kolom 1):**
   Multiplier: $m_{21} = \frac{c_{21}}{c_{11}} = \frac{2}{4} = 0.5$
   $$R_2 \leftarrow R_2 - 0.5 R_1 \implies \begin{bmatrix} 2 & 5 & 1 \end{bmatrix} - 0.5 \begin{bmatrix} 4 & 2 & 0 \end{bmatrix} = \begin{bmatrix} 0 & 4 & 1 \end{bmatrix}$$

2. **Eliminasi Baris 3 (Kolom 1):**
   Multiplier: $m_{31} = \frac{c_{31}}{c_{11}} = \frac{0}{4} = 0$
   $$R_3 \leftarrow R_3 - 0 R_1 = \begin{bmatrix} 0 & 1 & 3 \end{bmatrix}$$

3. **Eliminasi Baris 3 (Kolom 2):**
   Multiplier: $m_{32} = \frac{c'_{32}}{c'_{22}} = \frac{1}{4} = 0.25$
   $$R_3 \leftarrow R_3 - 0.25 R_2 \implies \begin{bmatrix} 0 & 1 & 3 \end{bmatrix} - 0.25 \begin{bmatrix} 0 & 4 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 2.75 \end{bmatrix}$$
   Catatan: $2.75 = \frac{11}{4}$

### Hasil Matriks L dan U:
$$L = \begin{bmatrix} 1 & 0 & 0 \\ 0.5 & 1 & 0 \\ 0 & 0.25 & 1 \end{bmatrix} = \begin{bmatrix} 1 & 0 & 0 \\ \frac{1}{2} & 1 & 0 \\ 0 & \frac{1}{4} & 1 \end{bmatrix}$$
$$U = \begin{bmatrix} 4 & 2 & 0 \\ 0 & 4 & 1 \\ 0 & 0 & \frac{11}{4} \end{bmatrix}$$

### Verifikasi perkalian:
$$LU = \begin{bmatrix} 1 & 0 & 0 \\ \frac{1}{2} & 1 & 0 \\ 0 & \frac{1}{4} & 1 \end{bmatrix} \begin{bmatrix} 4 & 2 & 0 \\ 0 & 4 & 1 \\ 0 & 0 & \frac{11}{4} \end{bmatrix} = \begin{bmatrix} 4 & 2 & 0 \\ 2 & 5 & 1 \\ 0 & 1 & 3 \end{bmatrix} = C$$

---

# Soal Invers Matriks 3x3

## Soal 7
$$A = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 1 \\ 2 & 3 & 4 \end{bmatrix}$$

Metode Adjoin: $A^{-1} = \frac{1}{\det(A)} \operatorname{adj}(A)$

### 1. Menghitung Determinan $A$
$$\det(A) = 1 \cdot \det\begin{bmatrix} 1 & 1 \\ 3 & 4 \end{bmatrix} - 0 + 2 \cdot \det\begin{bmatrix} 2 & 1 \\ 1 & 1 \end{bmatrix}$$
$$\det(A) = 1 \cdot (4 - 3) + 2 \cdot (2 - 1) = 1 \cdot (1) + 2 \cdot (1) = 3$$

### 2. Menghitung Matriks Kofaktor $C_{ij} = (-1)^{i+j} M_{ij}$
*   $C_{11} = +(4 - 3) = 1$
*   $C_{12} = -(0 - 2) = 2$
*   $C_{13} = +(0 - 2) = -2$
*   $C_{21} = -(8 - 3) = -5$
*   $C_{22} = +(4 - 2) = 2$
*   $C_{23} = -(3 - 4) = 1$
*   $C_{31} = +(2 - 1) = 1$
*   $C_{32} = -(1 - 0) = -1$
*   $C_{33} = +(1 - 0) = 1$

$$C = \begin{bmatrix} 1 & 2 & -2 \\ -5 & 2 & 1 \\ 1 & -1 & 1 \end{bmatrix}$$

### 3. Matriks Adjoin ($\operatorname{adj}(A) = C^T$)
$$\operatorname{adj}(A) = \begin{bmatrix} 1 & -5 & 1 \\ 2 & 2 & -1 \\ -2 & 1 & 1 \end{bmatrix}$$

### 4. Matriks Invers $A^{-1}$
$$A^{-1} = \frac{1}{3} \begin{bmatrix} 1 & -5 & 1 \\ 2 & 2 & -1 \\ -2 & 1 & 1 \end{bmatrix} = \begin{bmatrix} \frac{1}{3} & -\frac{5}{3} & \frac{1}{3} \\ \frac{2}{3} & \frac{2}{3} & -\frac{1}{3} \\ -\frac{2}{3} & \frac{1}{3} & \frac{1}{3} \end{bmatrix}$$

### 5. Verifikasi
$$A A^{-1} = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 1 \\ 2 & 3 & 4 \end{bmatrix} \begin{bmatrix} 1/3 & -5/3 & 1/3 \\ 2/3 & 2/3 & -1/3 \\ -2/3 & 1/3 & 1/3 \end{bmatrix} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$$

---

## Soal 8
$$B = \begin{bmatrix} 2 & 1 & 0 \\ 1 & 2 & 1 \\ 0 & 1 & 2 \end{bmatrix}$$

Metode Adjoin: $B^{-1} = \frac{1}{\det(B)} \operatorname{adj}(B)$

### 1. Menghitung Determinan $B$
$$\det(B) = 2 \cdot \det\begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix} - 1 \cdot \det\begin{bmatrix} 1 & 1 \\ 0 & 2 \end{bmatrix} + 0$$
$$\det(B) = 2 \cdot (4 - 1) - 1 \cdot (2 - 0) = 2(3) - 2 = 4$$

### 2. Menghitung Matriks Kofaktor $C_{ij}$ (Sifat Simetris: $C_{ij} = C_{ji}$)
*   $C_{11} = +(4 - 1) = 3$
*   $C_{12} = -(2 - 0) = -2$
*   $C_{13} = +(1 - 0) = 1$
*   $C_{21} = -2$
*   $C_{22} = +(4 - 0) = 4$
*   $C_{23} = -(2 - 0) = -2$
*   $C_{31} = 1$
*   $C_{32} = -2$
*   $C_{33} = +(4 - 1) = 3$

$$C = \begin{bmatrix} 3 & -2 & 1 \\ -2 & 4 & -2 \\ 1 & -2 & 3 \end{bmatrix}$$

### 3. Matriks Adjoin ($\operatorname{adj}(B) = C^T$)
$$\operatorname{adj}(B) = \begin{bmatrix} 3 & -2 & 1 \\ -2 & 4 & -2 \\ 1 & -2 & 3 \end{bmatrix}$$

### 4. Matriks Invers $B^{-1}$
$$B^{-1} = \frac{1}{4} \begin{bmatrix} 3 & -2 & 1 \\ -2 & 4 & -2 \\ 1 & -2 & 3 \end{bmatrix} = \begin{bmatrix} \frac{3}{4} & -\frac{1}{2} & \frac{1}{4} \\ -\frac{1}{2} & 1 & -\frac{1}{2} \\ \frac{1}{4} & -\frac{1}{2} & \frac{3}{4} \end{bmatrix}$$

### 5. Verifikasi
$$B B^{-1} = \begin{bmatrix} 2 & 1 & 0 \\ 1 & 2 & 1 \\ 0 & 1 & 2 \end{bmatrix} \begin{bmatrix} 0.75 & -0.5 & 0.25 \\ -0.5 & 1 & -0.5 \\ 0.25 & -0.5 & 0.75 \end{bmatrix} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$$

---

## Soal 9
$$C = \begin{bmatrix} 3 & 0 & 2 \\ 2 & 0 & -2 \\ 0 & 1 & 1 \end{bmatrix}$$

Metode Adjoin: $C^{-1} = \frac{1}{\det(C)} \operatorname{adj}(C)$

### 1. Menghitung Determinan $C$ (Ekspansi Kolom 2)
$$\det(C) = 1 \cdot (-1)^{3+2} \det\begin{bmatrix} 3 & 2 \\ 2 & -2 \end{bmatrix} = -1 \cdot (3(-2) - 2(2)) = -1 \cdot (-6 - 4) = 10$$

### 2. Menghitung Matriks Kofaktor $C_{ij}$
*   $C_{11} = +(0 - (-2)) = 2$
*   $C_{12} = -(2 - 0) = -2$
*   $C_{13} = +(2 - 0) = 2$
*   $C_{21} = -(0 - 2) = 2$
*   $C_{22} = +(3 - 0) = 3$
*   $C_{23} = -(3 - 0) = -3$
*   $C_{31} = +(0 - 0) = 0$
*   $C_{32} = -(-6 - 4) = 10$
*   $C_{33} = +(0 - 0) = 0$

$$C_{cof} = \begin{bmatrix} 2 & -2 & 2 \\ 2 & 3 & -3 \\ 0 & 10 & 0 \end{bmatrix}$$

### 3. Matriks Adjoin ($\operatorname{adj}(C) = (C_{cof})^T$)
$$\operatorname{adj}(C) = \begin{bmatrix} 2 & 2 & 0 \\ -2 & 3 & 10 \\ 2 & -3 & 0 \end{bmatrix}$$

### 4. Matriks Invers $C^{-1}$
$$C^{-1} = \frac{1}{10} \begin{bmatrix} 2 & 2 & 0 \\ -2 & 3 & 10 \\ 2 & -3 & 0 \end{bmatrix} = \begin{bmatrix} \frac{1}{5} & \frac{1}{5} & 0 \\ -\frac{1}{5} & \frac{3}{10} & 1 \\ \frac{1}{5} & -\frac{3}{10} & 0 \end{bmatrix}$$

### 5. Verifikasi
$$C C^{-1} = \begin{bmatrix} 3 & 0 & 2 \\ 2 & 0 & -2 \\ 0 & 1 & 1 \end{bmatrix} \begin{bmatrix} 0.2 & 0.2 & 0 \\ -0.2 & 0.3 & 1 \\ 0.2 & -0.3 & 0 \end{bmatrix} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$$




