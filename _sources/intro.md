![Logo](images/Logo.jpg)
# 1.1 Sistem Persamaan Linear

Tidak dapat dipungkiri bahwa menghitung dan mempelajari solusi persamaan, serta *sistem persamaan*, memegang peranan yang sangat penting dalam matematika. Namun, perlu kami tegaskan bahwa bukan hanya itu yang dilakukan oleh para matematikawan!

Dalam bab ini, kita akan membangun teori yang hampir lengkap mengenai jenis persamaan matematika yang paling sederhana, yaitu: *persamaan linear*.

Pembahasan ini akan menjadi pengantar (walaupun sedikit tidak langsung) menuju studi **Aljabar Linear**. Mengapa? Karena di balik cara kita mendeskripsikan solusi sistem linear, sebenarnya tersembunyi konsep-konsep dasar ruang vektor seperti *subruang*, *rentang (span)*, dan *kebebasan linear*.

Selain itu, kita juga akan mempelajari salah satu alat hitung paling penting dalam aljabar linear: **Eliminasi Gaussian**.

### 1.1.1 Sistem Persamaan Linear

**Definisi 1.1.1. Persamaan Linear.** Sebuah *ekspresi linear* dalam $n$ variabel yang tidak diketahui (atau peubah) $x_1, x_2, \dots x_n$ adalah sebuah ekspresi yang berbentuk
$$ a_1x_1 + a_2x_2 + \dots + a_nx_n, $$
dengan $a_1, a_2, \dots, a_n$ adalah bilangan real tetap.

Sebuah *persamaan linear* dalam variabel yang tidak diketahui $x_1, x_2, \dots, x_n$ adalah sebuah persamaan yang dapat disederhanakan, hanya menggunakan penjumlahan dan pengurangan, menjadi sebuah persamaan yang berbentuk
$$ a_1x_1 + a_2x_2 + \dots a_nx_n = b, \tag{1.1.1} $$
yang kita sebut sebagai **bentuk baku**-nya. Sebuah persamaan dalam variabel yang tidak diketahui $x_1, x_2, \dots, x_n$ disebut *nonlinear* jika persamaan tersebut tidak dapat disederhanakan menjadi bentuk (1.1.1) hanya menggunakan penjumlahan dan pengurangan.

Diberikan sebuah persamaan linear dengan bentuk baku (1.1.1), persamaan tersebut disebut *homogen* jika $b = 0$, dan *tak-homogen* jika $b \neq 0$.
### Contoh 1.1.2. Persamaan linear dan nonlinear.

1.  Perhatikan $\sqrt{3}x + \sin(5) = 2z - e^4y$. Ini adalah persamaan linear dalam variabel yang tidak diketahui $x, y, z$. Bentuk bakunya adalah $\sqrt{3}x + e^4y - 2z = -\sin(5)$. Karena ruas kanannya bukan nol (nonzero), kita lihat bahwa persamaan tersebut adalah **tak-homogen** (nonhomogeneous).

    > 💡 **Penjelasan:** Meskipun ada $\sin(5)$ dan $e^4$, itu hanyalah angka tetap (konstanta), bukan variabel yang dipangkatkan atau dikalikan. Jadi, persamaannya tetap linear. Karena hasilnya tidak sama dengan 0, maka disebut tak-homogen.

2.  Persamaan $x^2 + y^2 = 1$ adalah persamaan *nonlinear* dalam variabel yang tidak diketahui $x$ dan $y$.

    > 💡 **Penjelasan:** Ada pangkat 2 ($x^2$ dan $y^2$), sehingga grafiknya akan melengkung (lingkaran), bukan garis lurus.

---

### Definisi 1.1.3. Sistem persamaan linear.
 
Sebuah **sistem persamaan linear** (atau *sistem linear*) adalah sekumpulan persamaan linear.

Sebuah sistem linear **homogen** adalah sekumpulan persamaan linear homogen.

Ketika menampilkan sistem yang terdiri dari $m$ persamaan dengan $n$ variabel yang tidak diketahui $x_1, x_2, \dots x_n$, kita biasanya menulis setiap persamaan dalam bentuk baku dan menyusun suku-suku yang bersesuaian dari setiap persamaan ke dalam kolom-kolom:

$$
\begin{aligned}
a_{11}x_1 \quad + \quad a_{12}x_2 \quad + \dots + \quad a_{1n}x_n \quad &= \quad b_1 \\
a_{21}x_1 \quad + \quad a_{22}x_2 \quad + \dots + \quad a_{2n}x_n \quad &= \quad b_2 \\
\vdots \qquad \qquad \vdots \qquad \qquad & \qquad \vdots \\
a_{m1}x_1 \quad + \quad a_{m2}x_2 \quad + \dots + \quad a_{mn}x_n \quad &= \quad b_m
\end{aligned}
$$

Sebuah sistem homogen dengan demikian biasanya ditulis sebagai:

$$ a_{11}x_1 \quad + \quad a_{12}x_2 \quad + \dots + \quad a_{1n}x_n \quad = \quad 0 $$

*(Catatan: Untuk sistem homogen, semua nilai $b$ di ruas kanan adalah 0)*
Sebuah sistem homogen dengan demikian biasanya ditulis sebagai:

$$
\begin{aligned}
a_{11}x_1 \quad + \quad a_{12}x_2 \quad + \dots + \quad a_{1n}x_n \quad &= \quad 0 \\
a_{21}x_1 \quad + \quad a_{22}x_2 \quad + \dots + \quad a_{2n}x_n \quad &= \quad 0 \\
\vdots \qquad \qquad \vdots \qquad \qquad & \qquad \vdots \\
a_{m1}x_1 \quad + \quad a_{m2}x_2 \quad + \dots + \quad a_{mn}x_n \quad &= \quad 0
\end{aligned}
$$

---

**Catatan 1.1.4.** Anda akan ingin terbiasa dengan *double-indexing* (pengindeksan ganda) yang digunakan untuk menampilkan sistem linear secepat mungkin. Berikut adalah cara yang baik untuk mengorientasikan diri Anda:

- Huruf $i$ yang muncul di $a_{ij}$ dan $b_i$ menunjukkan baris ke-$i$ dalam sistem yang ditampilkan, atau secara ekuivalen, persamaan ke-$i$.

- Huruf $j$ yang muncul di $a_{ij}$ menunjukkan kolom ke-$j$ dalam sistem yang ditampilkan, yang terkait dengan variabel ke-$j$, untuk $1 \leq j \leq n$.

> 💡 **Penjelasan Sederhana:**
> - **Indeks pertama ($i$)** = nomor baris/persamaan (vertikal)
> - **Indeks kedua ($j$)** = nomor kolom/variabel (horizontal)
> - Contoh: $a_{23}$ berarti koefisien di baris 2, kolom 3 (koefisien untuk variabel ke-3 di persamaan ke-2)

---

### 🎨 **Visualisasi GeoGebra (Direkomendasikan)**

**Mengapa butuh GeoGebra:** Untuk memahami konsep double-indexing dan bagaimana koefisien tersusun dalam matriks.

**Perintah yang diketik:**
```geogebra
# Buat matriks koefisien untuk visualisasi
A = {{1, 2, 3}, {4, 5, 6}}

# Tampilkan sebagai sistem persamaan
x + 2y + 3z = 0
4x + 5y + 6z = 0

# Atau gunakan spreadsheet view untuk lihat indeks
```

**Yang diamati:** 
- Posisi $a_{ij}$ dalam matriks
- Hubungan antara indeks dan posisi koefisien

---

**Definisi 1.1.5. Solusi untuk sistem linear.** Sebuah *solusi untuk persamaan linear*

$$ a_1x_1 + a_2x_2 + \cdots a_nx_n = b $$

adalah sebuah $n$-tuple $(s_1, s_2, \dots, s_n)$ dari bilangan real di mana penugasan variabel $x_1 = s_1, x_2 = s_2, \dots, x_n = s_n$ membuat persamaan tersebut benar. Kita katakan $(s_1, \dots, s_n)$ **menyelesaikan persamaan** dalam kasus ini.

*Sebuah solusi untuk sistem persamaan linear*

> 💡 **Penjelasan Sederhana:**
> - **$n$-tuple** = kumpulan $n$ bilangan (contoh: untuk 3 variabel, solusinya adalah triple $(s_1, s_2, s_3)$)
> - **Menyelesaikan persamaan** = ketika kita substitusi nilai-nilai tersebut ke persamaan, hasilnya benar (ruas kiri = ruas kanan)
> - Contoh: Untuk $2x + 3y = 8$, solusi $(1, 2)$ berarti $x=1, y=2$, dan $2(1) + 3(2) = 2 + 6 = 8$ ✓

---

### 🎨 **Visualisasi GeoGebra (Sangat Direkomendasikan)**

**Mengapa butuh GeoGebra:** Untuk memvisualisasikan konsep solusi dan bagaimana $n$-tuple bekerja dalam sistem persamaan.

**Perintah yang diketik:**
```geogebra
# Contoh persamaan linear 2 variabel
2x + 3y = 8

# Plot garisnya

# Tambahkan titik solusi
A = (1, 2)

# Verifikasi: titik A harus terletak pada garis

# Untuk sistem persamaan:
x + y = 5
2x - y = 1

# Cari titik potong (solusi sistem)
Intersect(x + y = 5, 2x - y = 1)

# Hasilnya akan menunjukkan solusi sebagai titik (x, y)
```

**Yang diamati:**
- Titik solusi terletak pada garis/persamaan
- Untuk sistem: titik potong adalah solusi yang menyelesaikan SEMUA persamaan sekaligus
- Jika titik tidak pada garis, maka bukan solusi

---

### 📊 Definisi Matriks di GeoGebra

**Perintah GeoGebra:**
```geogebra
A = {{1, 2, 3}, {4, 5, 6}}
```

---

#### 🔍 Penjelasan Struktur:

| Sintaks | Arti |
|---------|------|
| `A =` | Nama matriks yang akan dibuat |
| `{{...}, {...}}` | Kurung ganda: luar untuk matriks, dalam untuk setiap baris |
| `{1, 2, 3}` | Baris ke-1 dari matriks |
| `{4, 5, 6}` | Baris ke-2 dari matriks |

---

#### 📐 Representasi Matematika:

Matriks $A$ yang terbentuk:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix}
$$

- **Ukuran**: $2 \times 3$ (2 baris, 3 kolom)
- **Elemen $a_{ij}$**:
  - $a_{11} = 1$, $a_{12} = 2$, $a_{13} = 3$
  - $a_{21} = 4$, $a_{22} = 5$, $a_{23} = 6$

<iframe src="https://www.geogebra.org/calculator/gz9xyxsf?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

```python
# Ini contoh jika Anda ingin menyelesaikan persamaan di VS Code pakai Python
# Butuh install library: pip install sympy

from sympy import symbols, Eq, solve

# 1. Definisi variabel
x, y = symbols('x y')

# 2. Buat persamaan
# Eq(kiri, kanan) berarti "kiri = kanan"
eq1 = Eq(2*x + 3*y, 6)
eq2 = Eq(x - y, 1)

# 3. Selesaikan sistem persamaan
# solve((persamaan1, persamaan2), (variabel1, variabel2))
solusi = solve((eq1, eq2), (x, y))

# 4. Tampilkan hasil
print(solusi)
```

<iframe src="https://www.geogebra.org/calculator/gjt3qt27?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>


# PENYELESAIAN SISTEM PERSAMAAN LINEAR
## Menggunakan Metode Eliminasi Gaussian

---

# BAB I  
## PENDAHULUAN

### 1.1 Latar Belakang

Sistem Persamaan Linear (SPL) adalah kumpulan beberapa persamaan linear yang memiliki variabel yang sama dan diselesaikan secara bersamaan. Salah satu metode yang sistematis untuk menyelesaikan SPL adalah **Eliminasi Gaussian**, yaitu metode yang menggunakan Operasi Baris Elementer (OBE) untuk mengubah matriks menjadi bentuk segitiga atas, kemudian dilakukan substitusi balik.

### 1.2 Tujuan

1. Memahami konsep SPL.
2. Memahami langkah Eliminasi Gaussian.
3. Menyelesaikan SPL 3 dan 4 variabel secara sistematis.

---

# BAB II  
## LANDASAN TEORI

### 2.1 Bentuk Umum SPL

Bentuk umum SPL dalam bentuk matriks:

$$
Ax = b
$$

dengan:

$$
A \in \mathbb{R}^{m \times n}, \quad
x \in \mathbb{R}^{n}, \quad
b \in \mathbb{R}^{m}
$$

### 2.2 Operasi Baris Elementer (OBE)

Dalam Eliminasi Gaussian diperbolehkan:

1. Menukar dua baris
2. Mengalikan baris dengan konstanta ≠ 0
3. Menambahkan kelipatan suatu baris ke baris lain

---

# BAB III  
## PEMBAHASAN

---

# 3.1 SPL Tiga Variabel

Diketahui:

$$
\begin{cases}
2x + y - z = 8 \\
-3x - y + 2z = -11 \\
-2x + y + 2z = -3
\end{cases}
$$

---

### Langkah 1: Matriks Augmented

$$
\left[
\begin{array}{ccc|c}
2 & 1 & -1 & 8 \\
-3 & -1 & 2 & -11 \\
-2 & 1 & 2 & -3
\end{array}
\right]
$$

---

### Langkah 2: Eliminasi Kolom Pertama

$$
R_2 = R_2 + \frac{3}{2}R_1
$$

$$
R_3 = R_3 + R_1
$$

Hasil:

$$
\left[
\begin{array}{ccc|c}
2 & 1 & -1 & 8 \\
0 & 0.5 & 0.5 & 1 \\
0 & 2 & 1 & 5
\end{array}
\right]
$$

---

### Langkah 3: Eliminasi Kolom Kedua

$$
R_3 = R_3 - 4R_2
$$

$$
\left[
\begin{array}{ccc|c}
2 & 1 & -1 & 8 \\
0 & 0.5 & 0.5 & 1 \\
0 & 0 & -1 & 1
\end{array}
\right]
$$

Sudah berbentuk eselon baris.

---

### Substitusi Balik

Baris 3:

$$
-z = 1 \Rightarrow z = -1
$$

Baris 2:

$$
0.5y + 0.5(-1) = 1
$$

$$
0.5y = 1.5 \Rightarrow y = 3
$$

Baris 1:

$$
2x + 3 - (-1) = 8
$$

$$
x = 2
$$

---

### Solusi SPL 3 Variabel

$$
x = 2, \quad y = 3, \quad z = -1
$$

---

# 3.2 SPL Empat Variabel

Diketahui:

$$
\begin{cases}
x + y + z + w = 10 \\
2x - y + z + w = 5 \\
3x + y - z + w = 12 \\
x + 2y + 3z - w = 7
\end{cases}
$$

---

### Matriks Augmented

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

---

### Eliminasi Kolom Pertama

$$
R_2 = R_2 - 2R_1
$$

$$
R_3 = R_3 - 3R_1
$$

$$
R_4 = R_4 - R_1
$$

Hasil:

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

---

### Eliminasi Kolom Kedua dan Ketiga

Setelah dilakukan OBE lanjutan diperoleh bentuk eselon:

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

---

### Substitusi Balik

Baris 4:

$$
-3w = -12 \Rightarrow w = 4
$$

Baris 3:

$$
z = 3
$$

Baris 2:

$$
y = 2
$$

Baris 1:

$$
x = 1
$$

---

### Solusi SPL 4 Variabel

$$
x = 1, \quad y = 2, \quad z = 3, \quad w = 4
$$

---

# BAB IV  
## KESIMPULAN

1. Eliminasi Gaussian menyelesaikan SPL dengan membentuk matriks eselon baris.
2. Setelah bentuk segitiga atas diperoleh, solusi dicari dengan substitusi balik.
3. Kedua contoh memiliki solusi tunggal.
<script src="https://sagecell.sagemath.org/static/embedded_sagecell.js"></script>
<script>
sagecell.makeSagecell({inputLocation: '.sage'});
</script>

<div class="sage">
A = matrix([[1, 1, 1, 6],[2, -1, 1, 3],[1, 2, -1, 3]])
A.add_multiple_of_row(1, 0, -2)
A.add_multiple_of_row(2, 0, -1)
print (A)

</div>
