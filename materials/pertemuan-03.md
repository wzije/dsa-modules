# Stack & Queue

---

## 📌 INFORMASI UMUM

- Pertemuan: 3
- Topik: Stack & Queue
- Durasi: 3 Jam
  - 60 menit konsep
  - 120 menit praktik

- Prasyarat: Mahasiswa sudah paham List (Array) & Loop

---

## 🎯 CAPAIAN PEMBELAJARAN

Mahasiswa mampu:

1. Menjelaskan konsep Stack dan Queue
2. Membedakan LIFO dan FIFO
3. Mengimplementasikan Stack menggunakan List
4. Mengimplementasikan Queue menggunakan List
5. Menyelesaikan kasus sederhana menggunakan Stack & Queue

---

## 🔁 BAGIAN I – REVIEW

Tanya:

- Apa itu Array?
- Apa fungsi append()?
- Apa fungsi pop()?

Lalu tampilkan:

```python
data = []

data.append(10)
data.append(20)
data.append(30)

print(data)
```

Lalu:

```python
data.pop()
print(data)
```

Masuk ke konsep Stack.

---

## 📦 BAGIAN II – STACK

## 1️⃣ Definisi

Stack adalah struktur data dengan prinsip:

> LIFO (Last In First Out)

Yang terakhir masuk → keluar duluan.

---

### 2️⃣ Analogi

- Tumpukan piring
- Tumpukan buku
- Undo di aplikasi

---

### 3️⃣ Operasi Dasar Stack

| Operasi | Fungsi                   |
| ------- | ------------------------ |
| push    | Menambah elemen          |
| pop     | Menghapus elemen teratas |
| peek    | Melihat elemen teratas   |
| isEmpty | Cek apakah kosong        |

---

### 4️⃣ Implementasi Stack di Python

Karena Python tidak punya Stack bawaan, kita pakai List.

#### Push

```python
stack = []

stack.append("A")
stack.append("B")
stack.append("C")

print(stack)
```

---

#### Pop

```python
stack.pop()
print(stack)
```

---

#### Peek

```python
print(stack[-1])
```

---

#### Cek Kosong

```python
if len(stack) == 0:
    print("Stack kosong")
```

---

## 🧪 STUDI KASUS STACK

### Kasus 1: Membalik Kata

Stack sangat cocok untuk reverse.

```python
kata = input("Masukkan kata: ")
stack = []

for huruf in kata:
    stack.append(huruf)

hasil = ""

while len(stack) > 0:
    hasil += stack.pop()

print("Hasil:", hasil)
```

Penjelasan:
Karakter terakhir keluar duluan → otomatis terbalik.

---

## 🚶 BAGIAN III – QUEUE

### 1️⃣ Definisi

Queue adalah struktur data dengan prinsip:

> FIFO (First In First Out)

Yang pertama masuk → keluar duluan.

---

### 2️⃣ Analogi

- Antrian bank
- Antrian tiket
- Printer queue

---

### 3️⃣ Operasi Dasar Queue

| Operasi | Fungsi                 |
| ------- | ---------------------- |
| enqueue | Menambah elemen        |
| dequeue | Menghapus elemen depan |
| front   | Melihat elemen depan   |
| isEmpty | Cek kosong             |

---

### 4️⃣ Implementasi Queue dengan List

#### Enqueue

```python
queue = []

queue.append("A")
queue.append("B")
queue.append("C")

print(queue)
```

---

#### Dequeue

```python
queue.pop(0)
print(queue)
```

Penjelasan:

- pop(0) menghapus elemen pertama

---

#### Melihat Elemen Depan

```python
print(queue[0])
```

---

## ⚠️ Catatan Akademik Penting

Jelaskan ke mahasiswa:

> Queue dengan pop(0) kurang efisien karena semua elemen bergeser.

Tapi belum bahas kompleksitas detail.
Itu bisa masuk saat analisis waktu nanti.

Kalau mau sedikit lebih benar secara teknis, bisa perkenalkan:

```python
from collections import deque

queue = deque()
queue.append("A")
queue.append("B")

queue.popleft()
```

Tapi ini opsional.

---

## 🧪 STUDI KASUS QUEUE

### Simulasi Antrian

```python
queue = []

# orang datang
queue.append("Andi")
queue.append("Budi")
queue.append("Citra")

print("Antrian:", queue)

# orang dilayani
queue.pop(0)

print("Setelah dilayani:", queue)
```

---

## 🆚 PERBANDINGAN STACK vs QUEUE

| Stack           | Queue             |
| --------------- | ----------------- |
| LIFO            | FIFO              |
| push / pop      | enqueue / dequeue |
| Akses dari atas | Akses dari depan  |

---

## 🧠 VISUALISASI SEDERHANA

Stack:

```
   C  ← keluar dulu
   B
   A
```

Queue:

```
A → keluar dulu
B
C
```

---

## 📝 LATIHAN KELAS

1️⃣ Buat program:

- Input 5 angka
- Masukkan ke stack
- Keluarkan semua satu per satu

2️⃣ Buat simulasi antrian kasir:

- Tambah pelanggan
- Layani 1 pelanggan

---

## 🏠 TUGAS RUMAH

1. Buat program pengecekan tanda kurung seimbang menggunakan Stack (versi sederhana).
2. Buat simulasi antrian rumah sakit dengan Queue.
3. Jelaskan perbedaan Stack dan Queue dengan contoh kehidupan nyata.

---
