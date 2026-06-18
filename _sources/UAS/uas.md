# tugas UAS 
## mencari determinan dari matrix 4 x 4 menggunakan metode ekspansi baris 1


# Jawaban
**answer revisi**
::::{grid} 4
:::{grid-item}
![bagian](../images/Dekomposisi/revisi/revisi1.jpeg)
**Bagian 1** before 
:::
:::{grid-item}
![bagian](../images/Dekomposisi/revisi/revisi2.jpeg)
**Bagian 2** before
:::
:::{grid-item}
![bagian](../images/Dekomposisi/revisi/revisi3.jpeg)
**Bagian 3** after
:::
:::{grid-item}
![bagian](../images/Dekomposisi/revisi/revisi4.jpeg)
**Bagian 4** after
:::
::::

### Keterangan Revisi Tugas

*   **Bagian 1 & 2 (Sebelum Revisi):**
    Pada *flow* pengerjaan tugas determinan matriks $4 \times 4$ menggunakan metode ekspansi kofaktor baris pertama sebelumnya, ditemukan kesalahan (celah) perhitungan pada minor-minornya ($M_{11}, M_{12}, M_{13}, M_{14}$). Hasil perhitungan minor tersebut tidak akurat, sehingga menyebabkan akumulasi penjumlahan dengan tanda kofaktor ($+ - + -$) menjadi keliru. Oleh karena itu, dilakukan perbaikan menyeluruh pada tahap perhitungan minor.

*   **Bagian 3 & 4 (Setelah Revisi):**
    Proses revisi dilakukan dengan mengoreksi dan menghitung ulang seluruh elemen minor dan kofaktor secara teliti. Langkah penyelesaian di bawah ini ditulis ulang menggunakan matriks:
    $$ A = \begin{bmatrix} 1 & 3 & 4 & 5  \\ 7 & 6 & 1 & 2 \\ 2 & 3 & 1 & 4 \\ 5 & 3 & 2 & 1 \end{bmatrix} $$
    Perbaikan ini mengacu pada metode perhitungan determinan matriks $4 \times 4$ yang sistematis (mengikuti prinsip dasar ekspansi Laplace seperti pada panduan [YouTube referensi](https://youtu.be/mZ-QNk-U3bg?si=I7_rbiFxvj7sYduK)).

---
---
 
### Langkah Perhitungan Determinan Secara Matematis (LaTeX)
 
$$
A = \begin{bmatrix}
1 & 3 & 4 & 5 \\
7 & 6 & 1 & 2 \\
2 & 3 & 1 & 4 \\
5 & 3 & 2 & 1
\end{bmatrix}
$$
 
$$
\begin{aligned}
\det(A) &= 1 \begin{vmatrix} 6 & 1 & 2 \\ 3 & 1 & 4 \\ 3 & 2 & 1 \end{vmatrix}
- 3 \begin{vmatrix} 7 & 1 & 2 \\ 2 & 1 & 4 \\ 5 & 2 & 1 \end{vmatrix}
+ 4 \begin{vmatrix} 7 & 6 & 2 \\ 2 & 3 & 4 \\ 5 & 3 & 1 \end{vmatrix}
- 5 \begin{vmatrix} 7 & 6 & 1 \\ 2 & 3 & 1 \\ 5 & 3 & 2 \end{vmatrix} \\[10pt]
&= 1 \Big[ 6(1\cdot1-4\cdot2) - 1(3\cdot1-4\cdot3) + 2(3\cdot2-1\cdot3) \Big] \\
&\quad - 3 \Big[ 7(1\cdot1-4\cdot2) - 1(2\cdot1-4\cdot5) + 2(2\cdot2-1\cdot5) \Big] \\
&\quad + 4 \Big[ 7(3\cdot1-4\cdot3) - 6(2\cdot1-4\cdot5) + 2(2\cdot3-3\cdot5) \Big] \\
&\quad - 5 \Big[ 7(3\cdot2-1\cdot3) - 6(2\cdot2-1\cdot5) + 1(2\cdot3-3\cdot5) \Big] \\[10pt]
&= 1 \Big[ 6(-7) - 1(-9) + 2(3) \Big]
- 3 \Big[ 7(-7) - 1(-18) + 2(-1) \Big] \\
&\quad + 4 \Big[ 7(-9) - 6(-18) + 2(-9) \Big]
- 5 \Big[ 7(3) - 6(-1) + 1(-9) \Big] \\[10pt]
&= 1(-27) - 3(-33) + 4(27) - 5(18) \\[6pt]
&= -27 + 99 + 108 - 90 \\[6pt]
&= 72 + 108 - 90 \\[6pt]
&= 180 - 90 \\[6pt]
&= \boxed{\det(A) = 90}
\end{aligned}
$$