# Array (List) & String dalam Python

## 🎯 Capaian Pembelajaran

Mahasiswa mampu:

1. Memahami konsep array sebagai struktur data linear
2. Mengimplementasikan array menggunakan list di Python
3. Mengolah data dalam array dengan algoritma sederhana
4. Memahami string sebagai array karakter
5. Melakukan manipulasi string dasar

---

# 📌 BAGIAN I – KONSEP ARRAY

## 1️⃣ Apa Itu Array?

Array adalah:

> Struktur data linear yang menyimpan sekumpulan elemen dengan tipe sama dan diakses menggunakan indeks.

Ciri:

* Berurutan
* Menggunakan indeks
* Elemen bertipe sama (konsep teoritis)

---

## 2️⃣ Array di Python

Di Python, array direpresentasikan dengan **List**:

```python
nilai = [80, 75, 90, 85]
```

Penegasan penting ke mahasiswa:

> Secara teori: ini disebut Array
> Secara Python: ini adalah List (dynamic array)

---

# 📌 BAGIAN II – OPERASI DASAR ARRAY

## 1️⃣ Akses Elemen

```python
print(nilai[0])
print(nilai[2])
```

## 2️⃣ Update Elemen

```python
nilai[1] = 88
```

## 3️⃣ Panjang Array

```python
print(len(nilai))
```

## 4️⃣ Traversal (Menelusuri Array)

```python
for n in nilai:
    print(n)
```

---

# 📌 BAGIAN III – ALGORITMA PADA ARRAY

Ini bagian penting supaya tidak cuma syntax.

## 1️⃣ Menjumlahkan Semua Elemen

```python
total = 0
for n in nilai:
    total += n
print(total)
```

## 2️⃣ Mencari Nilai Maksimum

```python
maks = nilai[0]

for n in nilai:
    if n > maks:
        maks = n

print("Nilai maksimum:", maks)
```

## 3️⃣ Mencari Elemen (Linear Search – Preview Pertemuan 3)

```python
target = 90
posisi = -1

for i in range(len(nilai)):
    if nilai[i] == target:
        posisi = i
        break

print("Posisi:", posisi)
```

Jangan bahas kompleksitas dulu. Cukup logika.

---

# 📌 BAGIAN IV – STRING SEBAGAI ARRAY KARAKTER

Masuk ke String.

## 1️⃣ Apa Itu String?

String adalah:

> Kumpulan karakter yang disimpan secara berurutan.

Contoh:

```python
nama = "Algoritma"
```

---

## 2️⃣ Akses Karakter

```python
print(nama[0])
print(nama[3])
```

Tekankan:
String punya indeks seperti array.

---

## 3️⃣ Traversal String

```python
for huruf in nama:
    print(huruf)
```

---

## 4️⃣ Studi Kasus: Hitung Huruf Vokal

```python
kata = input("Masukkan kata: ")
vokal = "aiueoAIUEO"
jumlah = 0

for huruf in kata:
    if huruf in vokal:
        jumlah += 1

print("Jumlah vokal:", jumlah)
```

Ini bagus untuk melatih logika.

---

# 📌 BAGIAN V – Mini Studi Kasus Integratif

### Kasus: Input 5 Nilai Mahasiswa

* Simpan dalam array
* Tampilkan semua
* Tampilkan nilai tertinggi
* Hitung rata-rata