# Hash Table (Dictionary di Python)

---

## 📌 INFORMASI UMUM

* Pertemuan: 4
* Topik: Hash Table
* Durasi: 3 Jam

  * 60 menit konsep
  * 120 menit praktik
* Prasyarat:

  * Paham List
  * Paham Stack & Queue
  * Paham Looping & If

---

## 🎯 CAPAIAN PEMBELAJARAN

Mahasiswa mampu:

1. Menjelaskan konsep Hash Table
2. Memahami konsep key–value
3. Menggunakan Dictionary di Python
4. Melakukan pencarian data secara efisien
5. Mengimplementasikan kasus sederhana berbasis Hash Table

---

## 🔁 BAGIAN I – JEMBATAN DARI PERTEMUAN 3 (10 MENIT)

Tanya ke mahasiswa:

> Kalau kita punya list:

```python
data = ["Andi", "Budi", "Citra"]
```

Kalau kita ingin mencari “Citra”, bagaimana caranya?

Jawaban:

* Cek satu per satu
* Gunakan loop

Itu disebut **Linear Search**.

Masalahnya:

* Kalau datanya 1 juta?
* Harus cek satu per satu ❌

Masuk ke Hash Table.

---

## 📦 BAGIAN II – APA ITU HASH TABLE?

### 1️⃣ Definisi

Hash Table adalah:

> Struktur data yang menyimpan data dalam bentuk pasangan **key–value** dan memungkinkan pencarian sangat cepat.

---

### 2️⃣ Konsep Key–Value

Contoh:

| Key    | Value   |
| ------ | ------- |
| "nama" | "Budi"  |
| "umur" | 20      |
| "nim"  | "12345" |

Berbeda dengan list:

```python
["Budi", 20, "12345"]
```

List → pakai indeks
Hash table → pakai key

---

### 🧠 Analogi Sederhana

Kamus Bahasa:

* Kata = key
* Arti = value

Tidak perlu cek semua halaman.
Langsung ke huruf awal.

---

## 💻 BAGIAN III – HASH TABLE DI PYTHON (Dictionary)

Python sudah menyediakan Hash Table dalam bentuk **Dictionary**.

---

### 1️⃣ Membuat Dictionary

```python
mahasiswa = {
    "nama": "Andi",
    "nim": "2023001",
    "umur": 20
}

print(mahasiswa)
```

---

### 2️⃣ Mengakses Data

```python
print(mahasiswa["nama"])
print(mahasiswa["nim"])
```

Berbeda dengan list:

```python
list_data[0]
```

---

### 3️⃣ Menambah Data

```python
mahasiswa["jurusan"] = "Informatika"
```

---

### 4️⃣ Mengubah Data

```python
mahasiswa["umur"] = 21
```

---

### 5️⃣ Menghapus Data

```python
del mahasiswa["nim"]
```

---

## 🔁 BAGIAN IV – LOOPING PADA DICTIONARY

---

### 1️⃣ Loop Key

```python
for key in mahasiswa:
    print(key)
```

---

### 2️⃣ Loop Value

```python
for value in mahasiswa.values():
    print(value)
```

---

### 3️⃣ Loop Key & Value

```python
for key, value in mahasiswa.items():
    print(key, ":", value)
```

---

## ⚡ BAGIAN V – KEUNGGULAN HASH TABLE

Bandingkan:

### List (Linear Search)

```python
data = ["Andi", "Budi", "Citra"]

for nama in data:
    if nama == "Citra":
        print("Ditemukan")
```

### Dictionary

```python
data = {
    "Andi": 80,
    "Budi": 75,
    "Citra": 90
}

print(data["Citra"])
```

Tidak perlu loop.
Langsung akses berdasarkan key.

---

# 🧠 Konsep Hashing (Tanpa Terlalu Teknis)

Jelaskan sederhana:

* Key diubah menjadi angka (hash)
* Angka menentukan posisi penyimpanan
* Itulah kenapa pencarian cepat

Tidak perlu bahas collision detail dulu (kecuali kelas kuat).

---

## 🧪 BAGIAN VI – STUDI KASUS

---

### Kasus 1: Program Data Mahasiswa

```python
mahasiswa = {}

jumlah = int(input("Berapa data mahasiswa? "))

for i in range(jumlah):
    nim = input("Masukkan NIM: ")
    nama = input("Masukkan Nama: ")
    
    mahasiswa[nim] = nama

print("\nData Mahasiswa:")
for nim, nama in mahasiswa.items():
    print(nim, "-", nama)
```

---

### Kasus 2: Pengecekan Login Sederhana

```python
users = {
    "admin": "1234",
    "budi": "abcd"
}

username = input("Username: ")
password = input("Password: ")

if username in users and users[username] == password:
    print("Login berhasil")
else:
    print("Login gagal")
```

Konsep:

* Key existence
* Lookup cepat

---

## 🆚 PERBANDINGAN STRUKTUR DATA

| Struktur   | Akses  | Urutan Penting? |
| ---------- | ------ | --------------- |
| List       | Indeks | Ya              |
| Stack      | LIFO   | Ya              |
| Queue      | FIFO   | Ya              |
| Hash Table | Key    | Tidak           |

---

## 📝 LATIHAN DI KELAS

1️⃣ Buat program:

* Simpan 5 barang dan harganya
* Tampilkan harga berdasarkan nama barang

2️⃣ Buat program:

* Hitung jumlah kemunculan huruf dalam sebuah kata
  (contoh: “data” → d:1, a:2, t:1)

Contoh solusi dasar:

```python
kata = input("Masukkan kata: ")
frekuensi = {}

for huruf in kata:
    if huruf in frekuensi:
        frekuensi[huruf] += 1
    else:
        frekuensi[huruf] = 1

print(frekuensi)
```

Ini contoh klasik kekuatan Hash Table.

---

## 🏠 TUGAS RUMAH

1. Buat program kamus mini (Indonesia–Inggris).
2. Buat sistem inventaris sederhana berbasis dictionary.
3. Jelaskan perbedaan Array dan Hash Table.
