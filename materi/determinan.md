# Determinan Matriks

Halaman ini membahas cara mencari determinan matriks.

---

## Menghitung Determinan

Misalkan kita punya matriks persegi $A$:
$$ A = [a_{ij}]_{n \times n} $$

### Matriks $1 \times 1$
Jika ukuran matriks hanya $1 \times 1$, determinannya adalah nilai elemen itu sendiri:
$$ \det(A) = a_{11} $$

### Matriks $n \times n$ ($n \geq 2$)
Untuk matriks berukuran $2 \times 2$ atau lebih besar, kita gunakan metode ekspansi kofaktor pada baris pertama:
$$ \det(A) = \sum_{j=1}^{n} (-1)^{1+j} \, a_{1j} \, \det(A_{1j}) $$

*Catatan: $A_{1j}$ adalah matriks sisa setelah kita menghapus baris ke-1 dan kolom ke-$j$ dari matriks $A$.*
