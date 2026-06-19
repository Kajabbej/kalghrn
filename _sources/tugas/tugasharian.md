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

# jawaban 

## soal 1
Hitung determinan dari matriks berikut:
$$A = \begin{bmatrix} 2 & 1 & 3 \\ 0 & 4 & 5 \\ 1 & 2 & 1 \end{bmatrix}$$

### Pendekatan Teoritis
Secara formal, determinan matriks $A \in \mathbb{R}^{3 \times 3}$ didefinisikan melalui rumus Leibniz:
$$\det(A) = \sum_{\sigma \in S_3} \operatorname{sgn}(\sigma) \prod_{i=1}^3 a_{i, \sigma(i)}$$
di mana $S_3$ adalah grup simetris dari permutasi berorder 3. Untuk komputasi praktis, kita menggunakan Teorema Ekspansi Laplace (ekspansi kofaktor) sepanjang baris atau kolom mana pun, serta Aturan Sarrus.

---

### Metode 1: Ekspansi Laplace (Kofaktor) sepanjang Kolom 1
Kita memilih kolom pertama ($j=1$) karena memiliki elemen nol ($a_{21} = 0$), yang menyederhanakan perhitungan:
$$\det(A) = \sum_{i=1}^3 (-1)^{i+1} a_{i1} M_{i1}$$
di mana $M_{i1}$ adalah minor matriks (determinan submatriks berukuran $2 \times 2$ setelah menghapus baris $i$ dan kolom 1).

Ekspansi secara eksplisit:
$$\det(A) = (-1)^{1+1} a_{11} M_{11} + (-1)^{2+1} a_{21} M_{21} + (-1)^{3+1} a_{31} M_{31}$$
$$\det(A) = (-1)^2 (2) \det\begin{bmatrix} 4 & 5 \\ 2 & 1 \end{bmatrix} + (-1)^3 (0) \det\begin{bmatrix} 1 & 3 \\ 2 & 1 \end{bmatrix} + (-1)^4 (1) \det\begin{bmatrix} 1 & 3 \\ 4 & 5 \end{bmatrix}$$

1. **Menghitung Minor $M_{11}$:**
   $$M_{11} = \det\begin{bmatrix} 4 & 5 \\ 2 & 1 \end{bmatrix} = (4 \cdot 1) - (5 \cdot 2) = 4 - 10 = -6$$
   Maka suku pertama:
   $$(-1)^2 (2) (-6) = 2 \cdot (-6) = -12$$

2. **Menghitung Minor $M_{21}$:**
   Karena pengalinya adalah $a_{21} = 0$, kontribusi suku ini adalah $0$.

3. **Menghitung Minor $M_{31}$:**
   $$M_{31} = \det\begin{bmatrix} 1 & 3 \\ 4 & 5 \end{bmatrix} = (1 \cdot 5) - (3 \cdot 4) = 5 - 12 = -7$$
   Maka suku ketiga:
   $$(-1)^4 (1) (-7) = 1 \cdot (-7) = -7$$

**Evaluasi Akhir Determinan:**
$$\det(A) = -12 + 0 + (-7) = -19$$

---

### Metode 2: Aturan Sarrus (Verifikasi Formal)
Kita memperluas matriks $A$ dengan menuliskan kembali dua kolom pertama di sebelah kanan:
$$\begin{matrix}
2 & 1 & 3 & | & 2 & 1 \\
0 & 4 & 5 & | & 0 & 4 \\
1 & 2 & 1 & | & 1 & 2
\end{matrix}$$

Jumlah perkalian diagonal utama (arah kiri-atas ke kanan-bawah):
$$D^+ = (2 \cdot 4 \cdot 1) + (1 \cdot 5 \cdot 1) + (3 \cdot 0 \cdot 2)$$
$$D^+ = 8 + 5 + 0 = 13$$

Jumlah perkalian diagonal sekunder (arah kiri-bawah ke kanan-atas):
$$D^- = (1 \cdot 4 \cdot 3) + (2 \cdot 5 \cdot 2) + (1 \cdot 0 \cdot 1)$$
$$D^- = 12 + 20 + 0 = 32$$

Maka determinannya adalah:
$$\det(A) = D^+ - D^- = 13 - 32 = -19$$
Kedua metode memberikan hasil yang konsisten secara matematis: $\det(A) = -19$.

---

## soal 2
Tentukan nilai determinan matriks:
$$B = \begin{bmatrix} 3 & 2 & 1 \\ 1 & 0 & 4 \\ 2 & 5 & 1 \end{bmatrix}$$

### Metode 1: Ekspansi Laplace sepanjang Baris 2
Baris kedua ($i=2$) dipilih karena memiliki satu elemen nol ($b_{22} = 0$). Formula ekspansi kofaktor:
$$\det(B) = \sum_{j=1}^3 (-1)^{2+j} b_{2j} M_{2j}$$
$$\det(B) = (-1)^{2+1} b_{21} M_{21} + (-1)^{2+2} b_{22} M_{22} + (-1)^{2+3} b_{23} M_{23}$$
$$\det(B) = (-1)^3 (1) \det\begin{bmatrix} 2 & 1 \\ 5 & 1 \end{bmatrix} + (-1)^4 (0) \det\begin{bmatrix} 3 & 1 \\ 2 & 1 \end{bmatrix} + (-1)^5 (4) \det\begin{bmatrix} 3 & 2 \\ 2 & 5 \end{bmatrix}$$

1. **Menghitung Minor $M_{21}$:**
   $$M_{21} = \det\begin{bmatrix} 2 & 1 \\ 5 & 1 \end{bmatrix} = (2 \cdot 1) - (1 \cdot 5) = 2 - 5 = -3$$
   Suku pertama:
   $$-1 \cdot (1) \cdot (-3) = 3$$

2. **Menghitung Minor $M_{22}$:**
   Suku kedua bernilai $0$ karena $b_{22} = 0$.

3. **Menghitung Minor $M_{23}$:**
   $$M_{23} = \det\begin{bmatrix} 3 & 2 \\ 2 & 5 \end{bmatrix} = (3 \cdot 5) - (2 \cdot 2) = 15 - 4 = 11$$
   Suku ketiga:
   $$-1 \cdot (4) \cdot (11) = -44$$

**Evaluasi Akhir Determinan:**
$$\det(B) = 3 + 0 + (-44) = -41$$

---

### Metode 2: Aturan Sarrus (Verifikasi Formal)
Matriks perluasan Sarrus untuk $B$:
$$\begin{matrix}
3 & 2 & 1 & | & 3 & 2 \\
1 & 0 & 4 & | & 1 & 0 \\
2 & 5 & 1 & | & 2 & 5
\end{matrix}$$

Jumlah perkalian diagonal utama:
$$D^+ = (3 \cdot 0 \cdot 1) + (2 \cdot 4 \cdot 2) + (1 \cdot 1 \cdot 5)$$
$$D^+ = 0 + 16 + 5 = 21$$

Jumlah perkalian diagonal sekunder:
$$D^- = (2 \cdot 0 \cdot 1) + (5 \cdot 4 \cdot 3) + (1 \cdot 1 \cdot 2)$$
$$D^- = 0 + 60 + 2 = 62$$

Maka determinannya adalah:
$$\det(B) = D^+ - D^- = 21 - 62 = -41$$
Hasil terbukti konsisten: $\det(B) = -41$.

---

## soal 3
Jika:
$$C = \begin{bmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 1 & 1 & 1 \end{bmatrix}$$
tentukan det C dan jelaskan matriks tersebut singular atau tidak.

### Analisis Struktural dan Teorema Ketergantungan Linier
Secara teoritis, jika baris-baris atau kolom-kolom dari sebuah matriks saling bergantung linier (linearly dependent), maka determinan dari matriks tersebut adalah nol ($\det = 0$).

Misalkan $R_1, R_2, R_3$ menyatakan baris-baris dari matriks $C$:
*   $R_1 = \begin{bmatrix} 1 & 2 & 3 \end{bmatrix}$
*   $R_2 = \begin{bmatrix} 2 & 4 & 6 \end{bmatrix}$
*   $R_3 = \begin{bmatrix} 1 & 1 & 1 \end{bmatrix}$

Perhatikan hubungan aljabar berikut:
$$R_2 = 2 \cdot R_1$$
Ini menunjukkan bahwa terdapat kombinasi linier non-trivial dari baris-baris tersebut yang menghasilkan vektor nol:
$$2 R_1 - R_2 + 0 R_3 = \mathbf{0}$$
Karena baris-baris tersebut dependen secara linier, berdasarkan teorema aljabar linier, $\det(C) = 0$.

---

### Pembuktian dengan Operasi Baris Elementer (OBE)
Operasi baris elementer yang menambahkan kelipatan dari suatu baris ke baris lainnya tidak mengubah nilai determinan. Kita terapkan operasi $R_2 \leftarrow R_2 - 2R_1$:
$$C' = \begin{bmatrix} 1 & 2 & 3 \\ 2 - 2(1) & 4 - 2(2) & 6 - 2(3) \\ 1 & 1 & 1 \end{bmatrix} = \begin{bmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 1 & 1 & 1 \end{bmatrix}$$
Karena matriks $C'$ memiliki baris yang seluruh elemennya adalah nol ($R_2 = \mathbf{0}$), maka nilai determinannya adalah:
$$\det(C) = \det(C') = 0$$

---

### Pembuktian dengan Ekspansi Laplace sepanjang Baris 3
$$\det(C) = 1 \cdot \det\begin{bmatrix} 2 & 3 \\ 4 & 6 \end{bmatrix} - 1 \cdot \det\begin{bmatrix} 1 & 3 \\ 2 & 6 \end{bmatrix} + 1 \cdot \det\begin{bmatrix} 1 & 2 \\ 2 & 4 \end{bmatrix}$$
$$\det(C) = 1 \cdot (2 \cdot 6 - 3 \cdot 4) - 1 \cdot (1 \cdot 6 - 3 \cdot 2) + 1 \cdot (1 \cdot 4 - 2 \cdot 2)$$
$$\det(C) = 1 \cdot (12 - 12) - 1 \cdot (6 - 6) + 1 \cdot (4 - 4)$$
$$\det(C) = 0 - 0 + 0 = 0$$

### Kesimpulan Singularitas
Sebuah matriks persegi $M \in \mathbb{R}^{n \times n}$ didefinisikan sebagai **matriks singular** jika dan hanya jika $\det(M) = 0$. 
Karena $\det(C) = 0$, maka matriks $C$ adalah **matriks singular**. Akibatnya, matriks $C$ tidak memiliki invers ($C^{-1}$ tidak terdefinisi) dan kernel dari $C$ berdimensi non-nol ($\dim(\ker(C)) \ge 1$).

---

## soal 4
Lakukan dekomposisi LU pada matriks:
$$A = \begin{bmatrix} 2 & 4 & 2 \\ 1 & 5 & 2 \\ 1 & 2 & 4 \end{bmatrix}$$
dengan bentuk:
$$A = LU$$
dimana L adalah matriks segitiga bawah dengan elemen diagonal utama bernilai 1 ($L_{ii}=1$), dan U adalah matriks segitiga atas.

### Formulasi Matematika
Dekomposisi LU setara dengan melakukan eliminasi Gauss pada $A$ untuk menghasilkan matriks segitiga atas $U$. Secara formal, ini diwakili oleh perkalian matriks-matriks elementer $E_k$:
$$E_p \dots E_2 E_1 A = U \implies A = (E_1^{-1} E_2^{-1} \dots E_p^{-1}) U \implies A = LU$$
di mana $L = \prod_{k} E_k^{-1}$ adalah matriks segitiga bawah.

---

### Langkah-langkah Eliminasi Gauss dan Konstruksi L

Matriks Awal:
$$A^{(0)} = \begin{bmatrix} 2 & 4 & 2 \\ 1 & 5 & 2 \\ 1 & 2 & 4 \end{bmatrix}$$

1.  **Mengeliminasi Kolom 1 (Baris 2 dan Baris 3):**
    *   **Baris 2:** Elemen pivot adalah $a_{11} = 2$. Elemen yang akan dieliminasi adalah $a_{21} = 1$.
        Faktor pengali (multiplier):
        $$m_{21} = \frac{a_{21}}{a_{11}} = \frac{1}{2} = 0.5$$
        Operasi Baris Elementer: $R_2 \leftarrow R_2 - 0.5 R_1$
        $$R_2 = \begin{bmatrix} 1 & 5 & 2 \end{bmatrix} - 0.5 \begin{bmatrix} 2 & 4 & 2 \end{bmatrix} = \begin{bmatrix} 0 & 3 & 1 \end{bmatrix}$$
    *   **Baris 3:** Elemen yang akan dieliminasi adalah $a_{31} = 1$.
        Faktor pengali:
        $$m_{31} = \frac{a_{31}}{a_{11}} = \frac{1}{2} = 0.5$$
        Operasi Baris Elementer: $R_3 \leftarrow R_3 - 0.5 R_1$
        $$R_3 = \begin{bmatrix} 1 & 2 & 4 \end{bmatrix} - 0.5 \begin{bmatrix} 2 & 4 & 2 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 3 \end{bmatrix}$$

    Matriks setelah tahap pertama:
    $$A^{(1)} = \begin{bmatrix} 2 & 4 & 2 \\ 0 & 3 & 1 \\ 0 & 0 & 3 \end{bmatrix}$$

2.  **Mengeliminasi Kolom 2 di bawah Diagonal:**
    Karena elemen pada posisi $(3,2)$ di $A^{(1)}$ sudah bernilai $0$, tidak diperlukan operasi baris.
    Faktor pengali:
    $$m_{32} = 0$$

---

### Hasil Akhir Dekomposisi

Matriks Segitiga Atas ($U$):
$$U = A^{(1)} = \begin{bmatrix} 2 & 4 & 2 \\ 0 & 3 & 1 \\ 0 & 0 & 3 \end{bmatrix}$$

Matriks Segitiga Bawah ($L$) terbentuk dari pengali $m_{ij}$ dengan diagonal utama bernilai 1:
$$L = \begin{bmatrix} 1 & 0 & 0 \\ m_{21} & 1 & 0 \\ m_{31} & m_{32} & 1 \end{bmatrix} = \begin{bmatrix} 1 & 0 & 0 \\ 0.5 & 1 & 0 \\ 0.5 & 0 & 1 \end{bmatrix}$$

---

### Verifikasi Perkalian $LU = A$
$$LU = \begin{bmatrix} 1 & 0 & 0 \\ 0.5 & 1 & 0 \\ 0.5 & 0 & 1 \end{bmatrix} \begin{bmatrix} 2 & 4 & 2 \\ 0 & 3 & 1 \\ 0 & 0 & 3 \end{bmatrix}$$
$$LU = \begin{bmatrix} 1(2) + 0 + 0 & 1(4) + 0 + 0 & 1(2) + 0 + 0 \\ 0.5(2) + 1(0) + 0 & 0.5(4) + 1(3) + 0 & 0.5(2) + 1(1) + 0 \\ 0.5(2) + 0 + 1(0) & 0.5(4) + 0 + 1(0) & 0.5(2) + 0 + 1(3) \end{bmatrix}$$
$$LU = \begin{bmatrix} 2 & 4 & 2 \\ 1 & 5 & 2 \\ 1 & 2 & 4 \end{bmatrix} = A \quad (\text{Valid terbukti secara matematis})$$

---

## soal 5
Tentukan matriks L dan U dari:
$$B = \begin{bmatrix} 1 & 2 & 1 \\ 2 & 5 & 3 \\ 4 & 10 & 8 \end{bmatrix}$$
menggunakan eliminasi Gauss.

### Langkah-langkah Eliminasi Gauss dan Pengumpulan Pengali

Matriks Awal:
$$B^{(0)} = \begin{bmatrix} 1 & 2 & 1 \\ 2 & 5 & 3 \\ 4 & 10 & 8 \end{bmatrix}$$

1.  **Tahap 1: Eliminasi Kolom 1**
    *   **Baris 2:** Elemen pivot $b_{11} = 1$, elemen target $b_{21} = 2$.
        Faktor pengali:
        $$m_{21} = \frac{b_{21}}{b_{11}} = \frac{2}{1} = 2$$
        Operasi baris: $R_2 \leftarrow R_2 - 2 R_1$
        $$R_2 = \begin{bmatrix} 2 & 5 & 3 \end{bmatrix} - 2 \begin{bmatrix} 1 & 2 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 1 & 1 \end{bmatrix}$$
    *   **Baris 3:** Elemen target $b_{31} = 4$.
        Faktor pengali:
        $$m_{31} = \frac{b_{31}}{b_{11}} = \frac{4}{1} = 4$$
        Operasi baris: $R_3 \leftarrow R_3 - 4 R_1$
        $$R_3 = \begin{bmatrix} 4 & 10 & 8 \end{bmatrix} - 4 \begin{bmatrix} 1 & 2 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 2 & 4 \end{bmatrix}$$

    Matriks setelah Tahap 1:
    $$B^{(1)} = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 1 \\ 0 & 2 & 4 \end{bmatrix}$$

2.  **Tahap 2: Eliminasi Kolom 2 di bawah diagonal**
    *   **Baris 3:** Elemen pivot baru $b'_{22} = 1$, elemen target $b'_{32} = 2$.
        Faktor pengali:
        $$m_{32} = \frac{b'_{32}}{b'_{22}} = \frac{2}{1} = 2$$
        Operasi baris: $R_3 \leftarrow R_3 - 2 R_2$
        $$R_3 = \begin{bmatrix} 0 & 2 & 4 \end{bmatrix} - 2 \begin{bmatrix} 0 & 1 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 2 \end{bmatrix}$$

    Matriks setelah Tahap 2:
    $$B^{(2)} = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 2 \end{bmatrix}$$

---

### Hasil Dekomposisi

Matriks Segitiga Atas ($U$):
$$U = B^{(2)} = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 2 \end{bmatrix}$$

Matriks Segitiga Bawah ($L$):
$$L = \begin{bmatrix} 1 & 0 & 0 \\ m_{21} & 1 & 0 \\ m_{31} & m_{32} & 1 \end{bmatrix} = \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 4 & 2 & 1 \end{bmatrix}$$

---

### Verifikasi Perkalian $LU = B$
$$LU = \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 4 & 2 & 1 \end{bmatrix} \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 2 \end{bmatrix}$$
$$LU = \begin{bmatrix} 1 & 2 & 1 \\ 2(1) + 0 & 2(2) + 1(1) + 0 & 2(1) + 1(1) + 0 \\ 4(1) + 0 + 0 & 4(2) + 2(1) + 0 & 4(1) + 2(1) + 1(2) \end{bmatrix}$$
$$LU = \begin{bmatrix} 1 & 2 & 1 \\ 2 & 5 & 3 \\ 4 & 10 & 8 \end{bmatrix} = B \quad (\text{Valid terbukti secara matematis})$$

---

## soal 6
Dekomposisikan matriks berikut menjadi LU:
$$C = \begin{bmatrix} 4 & 2 & 0 \\ 2 & 5 & 1 \\ 0 & 1 & 3 \end{bmatrix}$$

### Langkah-langkah Eliminasi Gauss dan Pengumpulan Pengali

Matriks Awal (Matriks Simetris Pita):
$$C^{(0)} = \begin{bmatrix} 4 & 2 & 0 \\ 2 & 5 & 1 \\ 0 & 1 & 3 \end{bmatrix}$$

1.  **Tahap 1: Eliminasi Kolom 1**
    *   **Baris 2:** Elemen pivot $c_{11} = 4$, elemen target $c_{21} = 2$.
        Faktor pengali:
        $$m_{21} = \frac{c_{21}}{c_{11}} = \frac{2}{4} = 0.5$$
        Operasi baris: $R_2 \leftarrow R_2 - 0.5 R_1$
        $$R_2 = \begin{bmatrix} 2 & 5 & 1 \end{bmatrix} - 0.5 \begin{bmatrix} 4 & 2 & 0 \end{bmatrix} = \begin{bmatrix} 0 & 4 & 1 \end{bmatrix}$$
    *   **Baris 3:** Elemen target $c_{31} = 0$.
        Faktor pengali:
        $$m_{31} = \frac{0}{4} = 0$$
        Operasi baris: $R_3 \leftarrow R_3 - 0 R_1 = \begin{bmatrix} 0 & 1 & 3 \end{bmatrix}$

    Matriks setelah Tahap 1:
    $$C^{(1)} = \begin{bmatrix} 4 & 2 & 0 \\ 0 & 4 & 1 \\ 0 & 1 & 3 \end{bmatrix}$$

2.  **Tahap 2: Eliminasi Kolom 2 di bawah diagonal**
    *   **Baris 3:** Elemen pivot baru $c'_{22} = 4$, elemen target $c'_{32} = 1$.
        Faktor pengali:
        $$m_{32} = \frac{c'_{32}}{c'_{22}} = \frac{1}{4} = 0.25$$
        Operasi baris: $R_3 \leftarrow R_3 - 0.25 R_2$
        $$R_3 = \begin{bmatrix} 0 & 1 & 3 \end{bmatrix} - 0.25 \begin{bmatrix} 0 & 4 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 2.75 \end{bmatrix}$$
        Catatan fraksional: $2.75 = \frac{11}{4}$.

    Matriks setelah Tahap 2:
    $$C^{(2)} = \begin{bmatrix} 4 & 2 & 0 \\ 0 & 4 & 1 \\ 0 & 0 & \frac{11}{4} \end{bmatrix}$$

---

### Hasil Dekomposisi

Matriks Segitiga Atas ($U$):
$$U = \begin{bmatrix} 4 & 2 & 0 \\ 0 & 4 & 1 \\ 0 & 0 & \frac{11}{4} \end{bmatrix}$$

Matriks Segitiga Bawah ($L$):
$$L = \begin{bmatrix} 1 & 0 & 0 \\ 0.5 & 1 & 0 \\ 0 & 0.25 & 1 \end{bmatrix} = \begin{bmatrix} 1 & 0 & 0 \\ \frac{1}{2} & 1 & 0 \\ 0 & \frac{1}{4} & 1 \end{bmatrix}$$

---

### Verifikasi Perkalian $LU = C$
$$LU = \begin{bmatrix} 1 & 0 & 0 \\ \frac{1}{2} & 1 & 0 \\ 0 & \frac{1}{4} & 1 \end{bmatrix} \begin{bmatrix} 4 & 2 & 0 \\ 0 & 4 & 1 \\ 0 & 0 & \frac{11}{4} \end{bmatrix}$$
$$LU = \begin{bmatrix} 4 & 2 & 0 \\ \frac{1}{2}(4) + 0 & \frac{1}{2}(2) + 4 & \frac{1}{2}(0) + 1 \\ 0 & \frac{1}{4}(4) & \frac{1}{4}(1) + \frac{11}{4} \end{bmatrix}$$
$$LU = \begin{bmatrix} 4 & 2 & 0 \\ 2 & 5 & 1 \\ 0 & 1 & 3 \end{bmatrix} = C \quad (\text{Valid terbukti secara matematis})$$

---

## soal 7
Tentukan invers dari matriks:
$$A = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 1 \\ 2 & 3 & 4 \end{bmatrix}$$
menggunakan metode Adjoin.

### Landasan Teori
Jika $A$ adalah matriks persegi tak-singular ($\det(A) \neq 0$), maka terdapat matriks invers unik $A^{-1}$ yang memenuhi $A A^{-1} = A^{-1} A = I_n$. Matriks invers dapat dihitung menggunakan metode Adjoin:
$$A^{-1} = \frac{1}{\det(A)} \operatorname{adj}(A)$$
di mana $\operatorname{adj}(A) = C^T$ adalah transpos dari matriks kofaktor $C$. Elemen kofaktor didefinisikan sebagai $C_{ij} = (-1)^{i+j} M_{ij}$.

---

### Langkah 1: Menghitung Determinan $A$
Menggunakan ekspansi kofaktor pada Kolom 1 (dari Soal 1, kita tahu $\det(A) = 3$):
$$\det(A) = 1 \cdot \det\begin{bmatrix} 1 & 1 \\ 3 & 4 \end{bmatrix} - 0 + 2 \cdot \det\begin{bmatrix} 2 & 1 \\ 1 & 1 \end{bmatrix}$$
$$\det(A) = 1(4 - 3) + 2(2 - 1) = 1(1) + 2(1) = 3$$
Karena $\det(A) = 3 \neq 0$, matriks invers $A^{-1}$ eksis (non-singular).

---

### Langkah 2: Menghitung Sembilan Elemen Kofaktor $C_{ij}$

*   **Baris 1:**
    *   $$C_{11} = (-1)^{1+1} \det\begin{bmatrix} 1 & 1 \\ 3 & 4 \end{bmatrix} = +(4 - 3) = 1$$
    *   $$C_{12} = (-1)^{1+2} \det\begin{bmatrix} 0 & 1 \\ 2 & 4 \end{bmatrix} = -(0 - 2) = 2$$
    *   $$C_{13} = (-1)^{1+3} \det\begin{bmatrix} 0 & 1 \\ 2 & 3 \end{bmatrix} = +(0 - 2) = -2$$

*   **Baris 2:**
    *   $$C_{21} = (-1)^{2+1} \det\begin{bmatrix} 2 & 1 \\ 3 & 4 \end{bmatrix} = -(8 - 3) = -5$$
    *   $$C_{22} = (-1)^{2+2} \det\begin{bmatrix} 1 & 1 \\ 2 & 4 \end{bmatrix} = +(4 - 2) = 2$$
    *   $$C_{23} = (-1)^{2+3} \det\begin{bmatrix} 1 & 2 \\ 2 & 3 \end{bmatrix} = -(3 - 4) = 1$$

*   **Baris 3:**
    *   $$C_{31} = (-1)^{3+1} \det\begin{bmatrix} 2 & 1 \\ 1 & 1 \end{bmatrix} = +(2 - 1) = 1$$
    *   $$C_{32} = (-1)^{3+2} \det\begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix} = -(1 - 0) = -1$$
    *   $$C_{33} = (-1)^{3+3} \det\begin{bmatrix} 1 & 2 \\ 0 & 1 \end{bmatrix} = +(1 - 0) = 1$$

Matriks Kofaktor ($C$):
$$C = \begin{bmatrix} 1 & 2 & -2 \\ -5 & 2 & 1 \\ 1 & -1 & 1 \end{bmatrix}$$

---

### Langkah 3: Menentukan Matriks Adjoin ($\operatorname{adj}(A)$)
Adjoin adalah transpos dari kofaktor:
$$\operatorname{adj}(A) = C^T = \begin{bmatrix} 1 & -5 & 1 \\ 2 & 2 & -1 \\ -2 & 1 & 1 \end{bmatrix}$$

---

### Langkah 4: Menghitung Invers Matriks $A^{-1}$
$$A^{-1} = \frac{1}{3} \begin{bmatrix} 1 & -5 & 1 \\ 2 & 2 & -1 \\ -2 & 1 & 1 \end{bmatrix} = \begin{bmatrix} \frac{1}{3} & -\frac{5}{3} & \frac{1}{3} \\ \frac{2}{3} & \frac{2}{3} & -\frac{1}{3} \\ -\frac{2}{3} & \frac{1}{3} & \frac{1}{3} \end{bmatrix}$$

---

### Verifikasi Formal $A A^{-1} = I_3$
$$A A^{-1} = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 1 \\ 2 & 3 & 4 \end{bmatrix} \begin{bmatrix} 1/3 & -5/3 & 1/3 \\ 2/3 & 2/3 & -1/3 \\ -2/3 & 1/3 & 1/3 \end{bmatrix}$$
*   Elemen $(1,1) = 1(\frac{1}{3}) + 2(\frac{2}{3}) + 1(-\frac{2}{3}) = \frac{1 + 4 - 2}{3} = 1$
*   Elemen $(1,2) = 1(-\frac{5}{3}) + 2(\frac{2}{3}) + 1(\frac{1}{3}) = \frac{-5 + 4 + 1}{3} = 0$
*   Elemen $(2,2) = 0 + 1(\frac{2}{3}) + 1(\frac{1}{3}) = 1$
*   Elemen $(3,3) = 2(\frac{1}{3}) + 3(-\frac{1}{3}) + 4(\frac{1}{3}) = \frac{2 - 3 + 4}{3} = 1$
Perkalian menghasilkan matriks identitas $I_3$. Pembuktian selesai.

---

## soal 8
Carilah invers matriks:
$$B = \begin{bmatrix} 2 & 1 & 0 \\ 1 & 2 & 1 \\ 0 & 1 & 2 \end{bmatrix}$$

### Langkah 1: Menghitung Determinan $B$
Menggunakan ekspansi Laplace pada baris 1:
$$\det(B) = 2 \cdot \det\begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix} - 1 \cdot \det\begin{bmatrix} 1 & 1 \\ 0 & 2 \end{bmatrix} + 0$$
$$\det(B) = 2(4 - 1) - 1(2 - 0) = 2(3) - 2 = 4$$
Karena $\det(B) = 4 \neq 0$, matriks invers eksis.

---

### Langkah 2: Menghitung Sembilan Elemen Kofaktor $C_{ij}$
Karena $B$ adalah matriks simetris ($B = B^T$), matriks kofaktornya juga akan bersifat simetris ($C = C^T$).

*   **Baris 1:**
    *   $$C_{11} = (-1)^{1+1} \det\begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix} = +(4 - 1) = 3$$
    *   $$C_{12} = (-1)^{1+2} \det\begin{bmatrix} 1 & 1 \\ 0 & 2 \end{bmatrix} = -(2 - 0) = -2$$
    *   $$C_{13} = (-1)^{1+3} \det\begin{bmatrix} 1 & 2 \\ 0 & 1 \end{bmatrix} = +(1 - 0) = 1$$

*   **Baris 2:**
    *   $$C_{21} = C_{12} = -2 \quad (\text{karena sifat simetris})$$
    *   $$C_{22} = (-1)^{2+2} \det\begin{bmatrix} 2 & 0 \\ 0 & 2 \end{bmatrix} = +(4 - 0) = 4$$
    *   $$C_{23} = (-1)^{2+3} \det\begin{bmatrix} 2 & 1 \\ 0 & 1 \end{bmatrix} = -(2 - 0) = -2$$

*   **Baris 3:**
    *   $$C_{31} = C_{13} = 1 \quad (\text{karena sifat simetris})$$
    *   $$C_{32} = C_{23} = -2 \quad (\text{karena sifat simetris})$$
    *   $$C_{33} = (-1)^{3+3} \det\begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix} = +(4 - 1) = 3$$

Matriks Kofaktor ($C$):
$$C = \begin{bmatrix} 3 & -2 & 1 \\ -2 & 4 & -2 \\ 1 & -2 & 3 \end{bmatrix}$$

---

### Langkah 3: Menentukan Matriks Adjoin ($\operatorname{adj}(B)$)
Karena $C$ simetris, maka $\operatorname{adj}(B) = C^T = C$:
$$\operatorname{adj}(B) = \begin{bmatrix} 3 & -2 & 1 \\ -2 & 4 & -2 \\ 1 & -2 & 3 \end{bmatrix}$$

---

### Langkah 4: Menghitung Invers Matriks $B^{-1}$
$$B^{-1} = \frac{1}{4} \begin{bmatrix} 3 & -2 & 1 \\ -2 & 4 & -2 \\ 1 & -2 & 3 \end{bmatrix} = \begin{bmatrix} \frac{3}{4} & -\frac{1}{2} & \frac{1}{4} \\ -\frac{1}{2} & 1 & -\frac{1}{2} \\ \frac{1}{4} & -\frac{1}{2} & \frac{3}{4} \end{bmatrix}$$

---

### Verifikasi Formal $B B^{-1} = I_3$
$$B B^{-1} = \begin{bmatrix} 2 & 1 & 0 \\ 1 & 2 & 1 \\ 0 & 1 & 2 \end{bmatrix} \begin{bmatrix} 0.75 & -0.5 & 0.25 \\ -0.5 & 1 & -0.5 \\ 0.25 & -0.5 & 0.75 \end{bmatrix}$$
*   Elemen $(1,1) = 2(0.75) + 1(-0.5) + 0 = 1.5 - 0.5 = 1$
*   Elemen $(1,2) = 2(-0.5) + 1(1) + 0 = -1 + 1 = 0$
*   Elemen $(2,2) = 1(-0.5) + 2(1) + 1(-0.5) = -0.5 + 2 - 0.5 = 1$
Perkalian terbukti menghasilkan $I_3$.

---

## soal 9
Diketahui:
$$C = \begin{bmatrix} 3 & 0 & 2 \\ 2 & 0 & -2 \\ 0 & 1 & 1 \end{bmatrix}$$
tentukan $C^{-1}$.

### Langkah 1: Menghitung Determinan $C$
Menggunakan ekspansi kofaktor sepanjang Kolom 2 yang memuat dua elemen nol:
$$\det(C) = \sum_{i=1}^3 (-1)^{i+2} c_{i2} M_{i2}$$
$$\det(C) = 0 + 0 + (-1)^{3+2} (1) \det\begin{bmatrix} 3 & 2 \\ 2 & -2 \end{bmatrix}$$
$$\det(C) = -1 \cdot (3(-2) - 2(2)) = -1 \cdot (-6 - 4) = 10$$
Karena $\det(C) = 10 \neq 0$, maka matriks invers terdefinisi.

---

### Langkah 2: Menghitung Sembilan Elemen Kofaktor $C_{ij}$

*   **Baris 1:**
    *   $$C_{11} = (-1)^{1+1} \det\begin{bmatrix} 0 & -2 \\ 1 & 1 \end{bmatrix} = +(0 - (-2)) = 2$$
    *   $$C_{12} = (-1)^{1+2} \det\begin{bmatrix} 2 & -2 \\ 0 & 1 \end{bmatrix} = -(2 - 0) = -2$$
    *   $$C_{13} = (-1)^{1+3} \det\begin{bmatrix} 2 & 0 \\ 0 & 1 \end{bmatrix} = +(2 - 0) = 2$$

*   **Baris 2:**
    *   $$C_{21} = (-1)^{2+1} \det\begin{bmatrix} 0 & 2 \\ 1 & 1 \end{bmatrix} = -(0 - 2) = 2$$
    *   $$C_{22} = (-1)^{2+2} \det\begin{bmatrix} 3 & 2 \\ 0 & 1 \end{bmatrix} = +(3 - 0) = 3$$
    *   $$C_{23} = (-1)^{2+3} \det\begin{bmatrix} 3 & 0 \\ 0 & 1 \end{bmatrix} = -(3 - 0) = -3$$

*   **Baris 3:**
    *   $$C_{31} = (-1)^{3+1} \det\begin{bmatrix} 0 & 2 \\ 0 & -2 \end{bmatrix} = +(0 - 0) = 0$$
    *   $$C_{32} = (-1)^{3+2} \det\begin{bmatrix} 3 & 2 \\ 2 & -2 \end{bmatrix} = -( -6 - 4) = 10$$
    *   $$C_{33} = (-1)^{3+3} \det\begin{bmatrix} 3 & 0 \\ 2 & 0 \end{bmatrix} = +(0 - 0) = 0$$

Matriks Kofaktor ($C_{cof}$):
$$C_{cof} = \begin{bmatrix} 2 & -2 & 2 \\ 2 & 3 & -3 \\ 0 & 10 & 0 \end{bmatrix}$$

---

### Langkah 3: Menentukan Matriks Adjoin ($\operatorname{adj}(C)$)
$$\operatorname{adj}(C) = (C_{cof})^T = \begin{bmatrix} 2 & 2 & 0 \\ -2 & 3 & 10 \\ 2 & -3 & 0 \end{bmatrix}$$

---

### Langkah 4: Menghitung Invers Matriks $C^{-1}$
$$C^{-1} = \frac{1}{10} \begin{bmatrix} 2 & 2 & 0 \\ -2 & 3 & 10 \\ 2 & -3 & 0 \end{bmatrix} = \begin{bmatrix} 0.2 & 0.2 & 0 \\ -0.2 & 0.3 & 1 \\ 0.2 & -0.3 & 0 \end{bmatrix} = \begin{bmatrix} \frac{1}{5} & \frac{1}{5} & 0 \\ -\frac{1}{5} & \frac{3}{10} & 1 \\ \frac{1}{5} & -\frac{3}{10} & 0 \end{bmatrix}$$

---

### Verifikasi Formal $C C^{-1} = I_3$
$$C C^{-1} = \begin{bmatrix} 3 & 0 & 2 \\ 2 & 0 & -2 \\ 0 & 1 & 1 \end{bmatrix} \begin{bmatrix} 0.2 & 0.2 & 0 \\ -0.2 & 0.3 & 1 \\ 0.2 & -0.3 & 0 \end{bmatrix}$$
*   Elemen $(1,1) = 3(0.2) + 0 + 2(0.2) = 0.6 + 0.4 = 1$
*   Elemen $(1,2) = 3(0.2) + 0 + 2(-0.3) = 0.6 - 0.6 = 0$
*   Elemen $(1,3) = 3(0) + 0(1) + 2(0) = 0$
*   Elemen $(2,1) = 2(0.2) + 0 - 2(0.2) = 0.4 - 0.4 = 0$
*   Elemen $(2,2) = 2(0.2) + 0 - 2(-0.3) = 0.4 + 0.6 = 1$
*   Elemen $(3,2) = 0(0.2) + 1(0.3) + 1(-0.3) = 0.3 - 0.3 = 0$
*   Elemen $(3,3) = 0(0) + 1(1) + 1(0) = 1$
Perkalian menghasilkan $I_3$. Pembuktian selesai secara sempurna.



