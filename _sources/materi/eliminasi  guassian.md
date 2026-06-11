# Sistem Persamaan Linear
## Metode Eliminasi Gauss

---

### penjelasan

**Eliminasi Gauss** adalah metode sistematis untuk menyelesaikan Sistem Persamaan Linear (SPL) dengan cara mengubah matriks augmented menjadi bentuk **eselon baris (row echelon form)**, kemudian diselesaikan dengan **substitusi mundur (back substitution)**.

---

### contoh Soal

Tentukan nilai $x$, $y$, dan $z$ dari sistem persamaan berikut:

$$
\begin{cases}
2x + y - z = 8 \\
-3x - y + 2z = -11 \\
-2x + y + 2z = -3
\end{cases}
$$

---

###  Langkah 1 — Bentuk Matriks Augmented

Sistem persamaan di atas dapat dituliskan dalam bentuk matriks augmented $[A|b]$:

$$
\left[\begin{array}{ccc|c}
2 & 1 & -1 & 8 \\
-3 & -1 & 2 & -11 \\
-2 & 1 & 2 & -3
\end{array}\right]
$$

Matriks ini terdiri dari:
- **Kolom 1, 2, 3** → koefisien variabel $x$, $y$, $z$
- **Kolom 4** → nilai ruas kanan $b$

---

###  Langkah 2 — Forward Elimination (Eliminasi ke Depan)

Tujuan: membuat elemen **di bawah diagonal utama menjadi nol**.

---

#### Eliminasi Kolom $x$ (Pivot: Baris 1)

Pivot = $a_{11} = 2$

**Operasi baris:**

$$
R_2 \leftarrow R_2 + \frac{3}{2} R_1
$$

$$
R_2 = [-3 + \tfrac{3}{2}(2),\ -1 + \tfrac{3}{2}(1),\ 2 + \tfrac{3}{2}(-1)\ |\ -11 + \tfrac{3}{2}(8)]
$$

$$
R_2 = [0,\ \tfrac{1}{2},\ \tfrac{1}{2}\ |\ 1]
$$

$$
R_3 \leftarrow R_3 + \frac{2}{2} R_1 = R_3 + R_1
$$

$$
R_3 = [-2+2,\ 1+1,\ 2+(-1)\ |\ -3+8]
$$

$$
R_3 = [0,\ 2,\ 1\ |\ 5]
$$

**Hasil setelah eliminasi kolom $x$:**

$$
\left[\begin{array}{ccc|c}
2 & 1 & -1 & 8 \\
0 & \frac{1}{2} & \frac{1}{2} & 1 \\
0 & 2 & 1 & 5
\end{array}\right]
$$

---

#### Eliminasi Kolom $y$ (Pivot: Baris 2)

Pivot = $a_{22} = \dfrac{1}{2}$

**Operasi baris:**

$$
R_3 \leftarrow R_3 - \frac{2}{\frac{1}{2}} R_2 = R_3 - 4R_2
$$

$$
R_3 = [0-0,\ 2-4(\tfrac{1}{2}),\ 1-4(\tfrac{1}{2})\ |\ 5-4(1)]
$$

$$
R_3 = [0,\ 0,\ -1\ |\ 1]
$$

**Hasil setelah eliminasi kolom $y$ (bentuk eselon baris):**

$$
\left[\begin{array}{ccc|c}
2 & 1 & -1 & 8 \\
0 & \frac{1}{2} & \frac{1}{2} & 1 \\
0 & 0 & -1 & 1
\end{array}\right]
$$

---

###  Langkah 3 — Back Substitution (Substitusi Mundur)

Dimulai dari baris paling bawah ke atas.

---

####  Dari Baris 3 → cari $z$

$$
-z = 1
$$

$$
\boxed{z = -1}
$$

---

####  Dari Baris 2 → cari $y$

$$
\frac{1}{2}y + \frac{1}{2}z = 1
$$

$$
\frac{1}{2}y + \frac{1}{2}(-1) = 1
$$

$$
\frac{1}{2}y = 1 + \frac{1}{2} = \frac{3}{2}
$$

$$
\boxed{y = 3}
$$

---

####  Dari Baris 1 → cari $x$

$$
2x + y - z = 8
$$

$$
2x + 3 - (-1) = 8
$$

$$
2x + 4 = 8
$$

$$
2x = 4
$$

$$
\boxed{x = 2}
$$

---

###  Solusi SPL 3 Variabel

$$
\boxed{x = 2, \quad y = 3, \quad z = -1}
$$

Kita bisa periksa dengan mensubstitusikan ke ketiga persamaan asal. Persamaan pertama: $2(2) + 3 - (-1) = 8$ , persamaan kedua: $-3(2) - 3 + 2(-1) = -11$, persamaan ketiga: $-2(2) + 3 + 2(-1) = -3$. Semua nilai terpenuhi.

---

## SPL 4 Variabel — Eliminasi Gauss

Setelah memahami SPL 3 variabel, kita perluas ke **4 variabel** dengan cara yang sama. Semakin banyak variabel, semakin banyak langkah eliminasi — namun polanya tetap identik.

---

### contoh Soal

Tentukan nilai $w$, $x$, $y$, dan $z$ dari sistem berikut:

$$
\begin{cases}
w + x + y + z = 10 \\
2w + 3x + y - z = 14 \\
w - x + 3y + 2z = 9 \\
3w + x - y + 2z = 13
\end{cases}
$$

---

###  Langkah 1 — Bentuk Matriks Augmented

$$
\left[\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10 \\
2 & 3 & 1 & -1 & 14 \\
1 & -1 & 3 & 2 & 9 \\
3 & 1 & -1 & 2 & 13
\end{array}\right]
$$

Matriks ini terdiri dari:
- **Kolom 1, 2, 3, 4** → koefisien variabel $w$, $x$, $y$, $z$
- **Kolom 5** → nilai ruas kanan $b$

---

###  Langkah 2 — Forward Elimination

####  Eliminasi Kolom $w$ (Pivot: Baris 1)

Pivot = $a_{11} = 1$

$$R_2 \leftarrow R_2 - 2R_1$$

$$R_2 = [2-2(1),\ 3-2(1),\ 1-2(1),\ -1-2(1)\ |\ 14-2(10)]$$

$$R_2 = [0,\ 1,\ -1,\ -3\ |\ -6]$$

$$R_3 \leftarrow R_3 - R_1$$

$$R_3 = [1-1,\ -1-1,\ 3-1,\ 2-1\ |\ 9-10]$$

$$R_3 = [0,\ -2,\ 2,\ 1\ |\ -1]$$

$$R_4 \leftarrow R_4 - 3R_1$$

$$R_4 = [3-3,\ 1-3,\ -1-3,\ 2-3\ |\ 13-30]$$

$$R_4 = [0,\ -2,\ -4,\ -1\ |\ -17]$$

**Hasil setelah eliminasi kolom $w$:**

$$
\left[\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10 \\
0 & 1 & -1 & -3 & -6 \\
0 & -2 & 2 & 1 & -1 \\
0 & -2 & -4 & -1 & -17
\end{array}\right]
$$

---

####  Eliminasi Kolom $x$ (Pivot: Baris 2)

Pivot = $a_{22} = 1$

$$R_3 \leftarrow R_3 + 2R_2$$

$$R_3 = [0,\ -2+2,\ 2+2(-1),\ 1+2(-3)\ |\ -1+2(-6)]$$

$$R_3 = [0,\ 0,\ 0,\ -5\ |\ -13]$$

$$R_4 \leftarrow R_4 + 2R_2$$

$$R_4 = [0,\ -2+2,\ -4+2(-1),\ -1+2(-3)\ |\ -17+2(-6)]$$

$$R_4 = [0,\ 0,\ -6,\ -7\ |\ -29]$$

**Hasil setelah eliminasi kolom $x$:**

$$
\left[\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10 \\
0 & 1 & -1 & -3 & -6 \\
0 & 0 & 0 & -5 & -13 \\
0 & 0 & -6 & -7 & -29
\end{array}\right]
$$

---

####  Tukar Baris 3 dan Baris 4 (Partial Pivoting)

Karena $a_{33} = 0$, kita perlu tukar baris agar pivot tidak nol:

$$R_3 \leftrightarrow R_4$$

$$
\left[\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10 \\
0 & 1 & -1 & -3 & -6 \\
0 & 0 & -6 & -7 & -29 \\
0 & 0 & 0 & -5 & -13
\end{array}\right]
$$

Matriks sudah dalam **bentuk eselon baris** 

---

###  Langkah 3 — Back Substitution

####  Dari Baris 4 → cari $z$

$$-5z = -13$$

$$\boxed{z = \frac{13}{5} = 2{,}6}$$

---

####  Dari Baris 3 → cari $y$

$$-6y - 7z = -29$$

$$-6y - 7\left(\frac{13}{5}\right) = -29$$

$$-6y = -29 + \frac{91}{5} = \frac{-145 + 91}{5} = \frac{-54}{5}$$

$$\boxed{y = \frac{54}{30} = \frac{9}{5} = 1{,}8}$$

---

####  Dari Baris 2 → cari $x$

$$x - y - 3z = -6$$

$$x - \frac{9}{5} - 3\left(\frac{13}{5}\right) = -6$$

$$x - \frac{9}{5} - \frac{39}{5} = -6$$

$$x - \frac{48}{5} = -6$$

$$x = -6 + \frac{48}{5} = \frac{-30 + 48}{5} = \frac{18}{5}$$

$$\boxed{x = \frac{18}{5} = 3{,}6}$$

---

####  Dari Baris 1 → cari $w$

$$w + x + y + z = 10$$

$$w + \frac{18}{5} + \frac{9}{5} + \frac{13}{5} = 10$$

$$w + \frac{40}{5} = 10$$

$$w + 8 = 10$$

$$\boxed{w = 2}$$

---

###  Solusi SPL 4 Variabel

$$
\boxed{w = 2, \quad x = 3{,}6, \quad y = 1{,}8, \quad z = 2{,}6}$$

---


### 💡 Ringkasan Langkah Eliminasi Gauss

```{admonition} Algoritma Eliminasi Gauss
:class: tip

1. **Bentuk matriks augmented** $[A|b]$
2. **Forward Elimination** — ubah menjadi bentuk segitiga atas:
   - Untuk setiap kolom pivot $k$, eliminasi semua elemen di bawahnya
   - Faktor eliminasi: $m_{ik} = \dfrac{a_{ik}}{a_{kk}}$
   - Operasi: $R_i \leftarrow R_i - m_{ik} \cdot R_k$
3. **Back Substitution** — selesaikan dari baris terakhir ke atas:
   $$x_i = \frac{b_i - \sum_{j=i+1}^{n} a_{ij} x_j}{a_{ii}}$$
```