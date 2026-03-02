# Analisis Kompleksitas Algoritma (Big-O Notation)

---

## 🎯 CAPAIAN PEMBELAJARAN

Setelah pertemuan ini mahasiswa mampu:

1. Menjelaskan pentingnya analisis algoritma
2. Memahami konsep kompleksitas waktu
3. Menentukan kompleksitas Big-O dari kode sederhana
4. Membandingkan efisiensi dua algoritma

---

## 1️⃣ Mengapa Perlu Analisis Algoritma?

Algoritma yang:

* ✔ Benar
* ✔ Berjalan
* ❌ Belum tentu efisien

Contoh:

Program A → 1 detik untuk 100 data
Program B → 1 detik untuk 1000 data

Mana lebih baik saat data 1 juta?

➡ Yang penting bukan waktu sekarang, tapi **pertumbuhan waktu saat data membesar**.

---

## 2️⃣ Kompleksitas Waktu vs Ruang

### Kompleksitas Waktu (Time Complexity)

Mengukur:

> Seberapa cepat waktu eksekusi bertambah ketika input (n) bertambah

### Kompleksitas Ruang (Space Complexity)

Mengukur:

> Seberapa banyak memori yang digunakan terhadap ukuran input

Pada pertemuan ini fokus ke **Time Complexity**

---

## 3️⃣ Konsep Dasar Big-O

Big-O adalah notasi matematika untuk menggambarkan:

> Batas atas pertumbuhan waktu algoritma

Ditulis sebagai:

O(1)
O(n)
O(n²)
O(log n)
dll.

Yang dianalisis:

* Operasi dominan
* Pertumbuhan
* Bukan angka konstanta

---

## 4️⃣ Tipe Kompleksitas Umum

| Kompleksitas | Nama         | Contoh                  |
| ------------ | ------------ | ----------------------- |
| O(1)         | Konstan      | Akses array             |
| O(log n)     | Logaritmik   | Binary search           |
| O(n)         | Linear       | Loop tunggal            |
| O(n log n)   | Linear log   | Merge sort              |
| O(n²)        | Kuadratik    | Nested loop             |
| O(2ⁿ)        | Eksponensial | Rekursi naive Fibonacci |

---

## 5️⃣ Contoh Implementasi dalam Python

---

### 🔹 O(1) – Konstan

```python
arr = [10, 20, 30]
print(arr[0])
```

Tidak peduli panjang array → tetap 1 operasi.

---

### 🔹 O(n) – Linear

```python
def print_all(arr):
    for item in arr:
        print(item)
```

Jika n = 1000 → loop 1000 kali
Jika n = 1.000.000 → loop 1.000.000 kali

---

### 🔹 O(n²) – Kuadratik

```python
def print_pairs(arr):
    for i in arr:
        for j in arr:
            print(i, j)
```

Jika n = 10 → 100 operasi
Jika n = 100 → 10.000 operasi

Pertumbuhan sangat cepat.

---

## 6️⃣ Cara Menghitung Big-O

### Langkah Analisis:

1. Hitung jumlah loop
2. Perhatikan nested loop
3. Abaikan konstanta
4. Ambil pertumbuhan terbesar

---

#### Contoh 1

```python
def example(n):
    for i in range(n):
        print(i)
    
    for j in range(n):
        print(j)
```

O(n) + O(n) = O(2n)

Hilangkan konstanta →
✅ O(n)

---

#### Contoh 2

```python
def example2(n):
    for i in range(n):
        for j in range(n):
            print(i, j)
```

O(n × n) =
✅ O(n²)

---

#### Contoh 3

```python
def example3(n):
    for i in range(n):
        print(i)
    
    for j in range(n*n):
        print(j)
```

O(n) + O(n²) =
Ambil yang terbesar →
✅ O(n²)

---

# 7️⃣ Kompleksitas Logaritmik – O(log n)

Contoh: Binary Search

```python
def binary_search(arr, target):
    low = 0
    high = len(arr) - 1
    
    while low <= high:
        mid = (low + high) // 2
        
        if arr[mid] == target:
            return True
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1
    
    return False
```

Kenapa O(log n)?

Karena:
Setiap iterasi → data dibagi dua.

Jika n = 1.000.000
Binary search hanya sekitar 20 langkah.

---

# 8️⃣ Perbandingan Linear vs Binary Search

| n         | Linear Search  | Binary Search |
| --------- | -------------- | ------------- |
| 10        | 10 langkah     | 4 langkah     |
| 100       | 100 langkah    | 7 langkah     |
| 1.000.000 | 1 juta langkah | ±20 langkah   |

---

# 9️⃣ Best Case, Average Case, Worst Case

Contoh Linear Search:

* Best case → data di awal → O(1)
* Worst case → data di akhir → O(n)

Dalam analisis Big-O → biasanya fokus ke **Worst Case**

---

# 🔟 Kompleksitas Umum yang Harus Diingat

Urutan dari paling cepat ke paling lambat:

O(1)
O(log n)
O(n)
O(n log n)
O(n²)
O(2ⁿ)
O(n!)

---

# 1️⃣1️⃣ Studi Kasus Diskusi

Jika:

* n = 1.000
* Algoritma A → O(n²)
* Algoritma B → O(n log n)

Mana lebih baik?

Hitung pendekatan:

A → 1.000.000
B → 1.000 × 10 = 10.000

Jauh berbeda.

---

## 1️⃣2️⃣ Latihan Analisis (Untuk Mahasiswa)

Tentukan kompleksitas berikut:

#### Soal 1

```python
for i in range(n):
    print(i)
```

---

#### Soal 2

```python
for i in range(n):
    for j in range(5):
        print(i, j)
```

---

#### Soal 3

```python
for i in range(n):
    for j in range(n):
        for k in range(n):
            print(i, j, k)
```

---

#### Soal 4

```python
i = n
while i > 1:
    i = i // 2
```

---

## 1️⃣3️⃣ Kesalahan Umum Mahasiswa

❌ Menghitung detail operasi satu per satu
❌ Tidak mengabaikan konstanta
❌ Tidak fokus pada pertumbuhan terbesar
❌ Mengira O(2n) berbeda jauh dari O(n)

---

## 📌 Mini Project Pertemuan 5

Buat program Python:

1. Generate list angka acak
2. Implementasi:

   * Linear Search
   * Binary Search
3. Bandingkan waktu eksekusi menggunakan `time` module

Diskusikan hasilnya.

---

## 🧠 Ringkasan Pertemuan 5

* Big-O mengukur pertumbuhan waktu
* Fokus pada worst case
* Abaikan konstanta
* Ambil pertumbuhan terbesar
* Efisiensi penting untuk data besar