# Tugas Determinan dan Invers Matriks

## A. Hitunglah determinan matriks berikut dengan menggunakan rumus ekspansi baris
$$ \sum_{k=1}^n (-1)^{i+k} a_{ik} M_{ik} $$
dengan $M_{ij}$ adalah minor dari matriks A dan
$$ M_{ij} = \det A_{ij}. $$

### **No 1.**
$$ A = \begin{bmatrix} -7 & -5 \\ 1 & 4 \end{bmatrix} $$

**Penyelesaian:**
Pilih ekspansi sepanjang baris ke-1 ($i = 1$):
*   Untuk $k = 1$: $a_{11} = -7$, Minor $M_{11} = \det([4]) = 4$.
*   Untuk $k = 2$: $a_{12} = -5$, Minor $M_{12} = \det([1]) = 1$.

Hitung determinannya:
$$ \det(A) = (-1)^{1+1} a_{11} M_{11} + (-1)^{1+2} a_{12} M_{12} $$
$$ \det(A) = (1)(-7)(4) + (-1)(-5)(1) = -28 + 5 = \mathbf{-23} $$

---

### **No 2.**
$$ A = \begin{bmatrix} 0 & 2 & -3 \\ 1 & -2 & -1 \\ 0 & 0 & 1 \end{bmatrix} $$

**Penyelesaian:**
Pilih ekspansi sepanjang baris ke-3 ($i = 3$) karena memiliki elemen nol terbanyak:
$$ \det(A) = (-1)^{3+1} a_{31} M_{31} + (-1)^{3+2} a_{32} M_{32} + (-1)^{3+3} a_{33} M_{33} $$
$$ \det(A) = 0 + 0 + (1)(1) M_{33} $$

Hitung minor $M_{33}$:
$$ M_{33} = \det\begin{bmatrix} 0 & 2 \\ 1 & -2 \end{bmatrix} = (0 \times -2) - (2 \times 1) = -2 $$

Maka determinan matriks:
$$ \det(A) = 1 \times (-2) = \mathbf{-2} $$

---

### **No 3.**
$$ A = \begin{bmatrix} 1 & -3 & 1 & 1 \\ -3 & 1 & 1 & 1 \\ 1 & 1 & -3 & 1 \\ 1 & 1 & 1 & -3 \end{bmatrix} $$

**Penyelesaian:**
Lakukan ekspansi kofaktor sepanjang baris ke-1 ($i = 1$):
$$ \det(A) = a_{11}C_{11} + a_{12}C_{12} + a_{13}C_{13} + a_{14}C_{14} $$
Dengan $a_{11} = 1, a_{12} = -3, a_{13} = 1, a_{14} = 1$.

1.  **Hitung kofaktor $C_{11}$**:
    $$ M_{11} = \det\begin{bmatrix} 1 & 1 & 1 \\ 1 & -3 & 1 \\ 1 & 1 & -3 \end{bmatrix} = 1(9-1) - 1(-3-1) + 1(1 - (-3)) = 8 + 4 + 4 = 16 $$
    $$ C_{11} = (-1)^{1+1} \cdot 16 = 16 $$
2.  **Hitung kofaktor $C_{12}$**:
    $$ M_{12} = \det\begin{bmatrix} -3 & 1 & 1 \\ 1 & -3 & 1 \\ 1 & 1 & -3 \end{bmatrix} = -3(9-1) - 1(-3-1) + 1(1 - (-3)) = -24 + 4 + 4 = -16 $$
    $$ C_{12} = (-1)^{1+2} \cdot (-16) = 16 $$
3.  **Hitung kofaktor $C_{13}$**:
    $$ M_{13} = \det\begin{bmatrix} -3 & 1 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & -3 \end{bmatrix} = -3(-3-1) - 1(-3-1) + 1(1-1) = 12 + 4 + 0 = 16 $$
    $$ C_{13} = (-1)^{1+3} \cdot 16 = 16 $$
4.  **Hitung kofaktor $C_{14}$**:
    $$ M_{14} = \det\begin{bmatrix} -3 & 1 & 1 \\ 1 & 1 & -3 \\ 1 & 1 & 1 \end{bmatrix} = -3(1 - (-3)) - 1(1 - (-3)) + 1(1-1) = -12 - 4 + 0 = -16 $$
    $$ C_{14} = (-1)^{1+4} \cdot (-16) = 16 $$

Gabungkan seluruh kofaktor:
$$ \det(A) = 1(16) + (-3)(16) + 1(16) + 1(16) = 16 - 48 + 16 + 16 = \mathbf{0} $$

---

## B. Gunakan rumus matriks adjoin untuk menghitung invers dari matriks berikut dengan rumus
$$ (\operatorname{adj} A)_{ij} = (-1)^{i+j} M_{ji} $$
dan rumus 
$$ A^{-1} = \frac{1}{\det A} \operatorname{adj} A. $$

### **No 4.**
$$ A = \begin{bmatrix} -7 & -5 \\ 1 & 4 \end{bmatrix} $$

**Penyelesaian:**
Dari No 1, kita tahu $\det(A) = -23$.
Hitung matriks kofaktor $C$:
*   $C_{11} = (-1)^{1+1}(4) = 4$
*   $C_{12} = (-1)^{1+2}(1) = -1$
*   $C_{21} = (-1)^{2+1}(-5) = 5$
*   $C_{22} = (-1)^{2+2}(-7) = -7$

Maka $C = \begin{bmatrix} 4 & -1 \\ 5 & -7 \end{bmatrix}$. 
Transpos kofaktor adalah adjoinnya:
$$ \operatorname{adj}(A) = C^T = \begin{bmatrix} 4 & 5 \\ -1 & -7 \end{bmatrix} $$

Hitung invers matriks:
$$ A^{-1} = \frac{1}{\det A} \operatorname{adj}(A) = -\frac{1}{23} \begin{bmatrix} 4 & 5 \\ -1 & -7 \end{bmatrix} = \mathbf{\begin{bmatrix} -\frac{4}{23} & -\frac{5}{23} \\ \frac{1}{23} & \frac{7}{23} \end{bmatrix}} $$

---

### **No 5.**
$$ A = \begin{bmatrix} 0 & 2 & -3 \\ 1 & -2 & -1 \\ 0 & 0 & 1 \end{bmatrix} $$

**Penyelesaian:**
Dari No 2, kita tahu $\det(A) = -2$.
Hitung masing-masing kofaktor $C_{ij}$:
*   $C_{11} = (-1)^{1+1} \det\begin{bmatrix} -2 & -1 \\ 0 & 1 \end{bmatrix} = -2$
*   $C_{12} = (-1)^{1+2} \det\begin{bmatrix} 1 & -1 \\ 0 & 1 \end{bmatrix} = -1$
*   $C_{13} = (-1)^{1+3} \det\begin{bmatrix} 1 & -2 \\ 0 & 0 \end{bmatrix} = 0$
*   $C_{21} = (-1)^{2+1} \det\begin{bmatrix} 2 & -3 \\ 0 & 1 \end{bmatrix} = -2$
*   $C_{22} = (-1)^{2+2} \det\begin{bmatrix} 0 & -3 \\ 0 & 1 \end{bmatrix} = 0$
*   $C_{23} = (-1)^{2+3} \det\begin{bmatrix} 0 & 2 \\ 0 & 0 \end{bmatrix} = 0$
*   $C_{31} = (-1)^{3+1} \det\begin{bmatrix} 2 & -3 \\ -2 & -1 \end{bmatrix} = -8$
*   $C_{32} = (-1)^{3+2} \det\begin{bmatrix} 0 & -3 \\ 1 & -1 \end{bmatrix} = -3$
*   $C_{33} = (-1)^{3+3} \det\begin{bmatrix} 0 & 2 \\ 1 & -2 \end{bmatrix} = -2$

Matriks Kofaktor $C = \begin{bmatrix} -2 & -1 & 0 \\ -2 & 0 & 0 \\ -8 & -3 & -2 \end{bmatrix}$.
Adjoin matriks $A$ adalah $C^T$:
$$ \operatorname{adj}(A) = \begin{bmatrix} -2 & -2 & -8 \\ -1 & 0 & -3 \\ 0 & 0 & -2 \end{bmatrix} $$

Hitung invers matriks:
$$ A^{-1} = \frac{1}{\det A} \operatorname{adj}(A) = -\frac{1}{2} \begin{bmatrix} -2 & -2 & -8 \\ -1 & 0 & -3 \\ 0 & 0 & -2 \end{bmatrix} = \mathbf{\begin{bmatrix} 1 & 1 & 4 \\ \frac{1}{2} & 0 & \frac{3}{2} \\ 0 & 0 & 1 \end{bmatrix}} $$

---

### **No 6.**
$$ A = \begin{bmatrix} 1 & -3 & 1 & 1 \\ -3 & 1 & 1 & 1 \\ 1 & 1 & -3 & 1 \\ 1 & 1 & 1 & -3 \end{bmatrix} $$

**Penyelesaian:**
Dari No 3, didapatkan $\det(A) = 0$.

Karena determinan matriks bernilai nol, matriks ini merupakan **matriks singular** yang baris/kolomnya saling bergantung secara linear. Oleh karena itu, matriks adjoin tidak dapat dibagi oleh determinan untuk menghasilkan matriks invers.

Kesimpulan:
$$ \mathbf{A^{-1} \text{ tidak terdefinisi (tidak ada invers untuk matriks singular)}} $$
