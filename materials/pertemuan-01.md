# Pengantar + Dasar Python

---

## 📌 INFORMASI UMUM

- Mata Kuliah: Struktur Data & Algoritma
- Pertemuan: 1
- Durasi: 3 Jam (1 Teori + 2 Praktik)
- Fokus: Mindset algoritmik & Python dasar

---

# 🎯 CAPAIAN PEMBELAJARAN

Setelah pertemuan ini mahasiswa mampu:

1. Memahami apa itu algoritma
2. Menjelaskan perbedaan algoritma dan program
3. Membuat algoritma sederhana
4. Menggunakan Python dasar (input, output, variabel, percabangan sederhana)

---

# 📚 BAGIAN I — KONSEP DASAR

---

## 1️⃣ Apa Itu Algoritma?

Definisi sederhana:

> Algoritma adalah langkah-langkah logis dan sistematis untuk menyelesaikan masalah.

### Contoh kehidupan sehari-hari

Algoritma membuat mie instan:

1. Rebus air
2. Masukkan mie
3. Tunggu 3 menit
4. Masukkan bumbu
5. Aduk
6. Sajikan

Ciri algoritma:

- Ada langkah jelas
- Ada awal & akhir
- Pasti berhenti

---

## 2️⃣ Apa Itu Program?

- **Algoritma** = rencana langkah
- **Program** = algoritma yang ditulis dalam bahasa pemrograman

Analogi:

> Algoritma = resep
> Program = masakan yang benar-benar dibuat

---

## 3️⃣ Kenapa Belajar Struktur Data?

Karena:

- Data harus disimpan
- Data harus diatur
- Data harus diproses

Contoh:

- Nilai mahasiswa
- Daftar belanja
- Data transaksi

---

# 💻 BAGIAN II — PYTHON DASAR 

---

## 1️⃣ Output (print)

```python
print("Halo Dunia")
print("Saya belajar Algoritma")
```

---

## 2️⃣ Variabel

```python
nama = "Budi"
umur = 20
tinggi = 170.5

print(nama)
print(umur)
```

Penjelasan:

- Variabel = tempat menyimpan data

---

## 3️⃣ Input dari User

```python
nama = input("Masukkan nama: ")
print("Halo", nama)
```

Input angka:

```python
umur = int(input("Masukkan umur: "))
print("Umur kamu:", umur)
```

---

## 4️⃣ Operasi Matematika

```python
a = 10
b = 5

print(a + b)
print(a - b)
print(a * b)
print(a / b)
```

---

# 🔀 BAGIAN III — PERCABANGAN (IF)

---

## Menentukan Genap atau Ganjil

```python
angka = int(input("Masukkan angka: "))

if angka % 2 == 0:
    print("Genap")
else:
    print("Ganjil")
```

Konsep penting:

- %
- if
- indentasi

---

# 🔁 BAGIAN IV — PERULANGAN DASAR (FOR)

---

## Menampilkan Angka 1–5

```python
for i in range(1, 6):
    print(i)
```

Penjelasan:

- range(1,6) artinya 1 sampai 5
- Perulangan membantu menghindari penulisan berulang

---

# 🧪 LATIHAN DI KELAS

### Latihan 1

Buat program:

- Input 2 angka
- Tampilkan hasil penjumlahan

---

### Latihan 2

Buat program:

- Input nilai
- Jika ≥ 75 → tampilkan “Lulus”
- Jika < 75 → tampilkan “Tidak Lulus”

---

### Latihan 3

Tampilkan angka 1 sampai 10 menggunakan for

---

# 🧠 MINI STUDI KASUS (15–20 MENIT)

## Menghitung Luas Persegi Panjang

Masalah:
Hitung luas jika diketahui panjang dan lebar

Algoritma:

1. Input panjang
2. Input lebar
3. Hitung luas = panjang × lebar
4. Tampilkan hasil

Implementasi:

```python
panjang = int(input("Masukkan panjang: "))
lebar = int(input("Masukkan lebar: "))

luas = panjang * lebar

print("Luas =", luas)
```

---

# 📝 TUGAS RUMAH

1. Buat program menghitung luas lingkaran
2. Buat program menentukan bilangan terbesar dari 2 angka
3. Buat program menampilkan angka ganjil dari 1–20

Format:
File Python (.py)

---
