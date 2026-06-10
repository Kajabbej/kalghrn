# Eliminasi Gaussian

Eliminasi Gaussian adalah algoritma dalam aljabar linear untuk menyelesaikan sistem persamaan linear, menentukan pangkat matriks, atau mencari invers suatu matriks. Metode ini dinamai dari matematikawan Jerman, Carl Friedrich Gauss.

## Langkah-Langkah Eliminasi Gaussian

1. **Matriks Augmentasi**: Tuliskan sistem persamaan linear (SPL) dalam bentuk matriks augmented $[A|b]$.
2. **Eliminasi Maju (Forward Elimination)**: Mengubah matriks augmented menjadi bentuk eselon baris (segitiga atas) menggunakan Operasi Baris Elementer (OBE).
3. **Substitusi Balik (Back Substitution)**: Menyelesaikan nilai-nilai variabel dari baris paling bawah ke atas.

## Implementasi Python (NumPy)

Berikut adalah contoh implementasi kode Python untuk menyelesaikan SPL menggunakan Eliminasi Gaussian dengan partial pivoting.

```python
import numpy as np

def eliminasi_gaussian(A, b):
    # Gabungkan menjadi matriks augmented
    M = np.hstack([A, b.reshape(-1, 1)])
    n = len(b)
    
    # Eliminasi Maju dengan Partial Pivoting
    for i in range(n):
        # Cari pivot terbesar di kolom i
        pivot_row = np.argmax(abs(M[i:, i])) + i
        # Tukar baris jika diperlukan
        if pivot_row != i:
            M[[i, pivot_row]] = M[[pivot_row, i]]
            
        for j in range(i + 1, n):
            factor = M[j, i] / M[i, i]
            M[j, i:] -= factor * M[i, i:]
            
    # Substitusi Balik
    x = np.zeros(n)
    for i in range(n - 1, -1, -1):
        x[i] = (M[i, -1] - np.dot(M[i, i+1:n], x[i+1:n])) / M[i, i]
        
    return x
```
