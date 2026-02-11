# 🧠 **MODUL PERTEMUAN 1 - STRUKTUR DATA & ALGORITMA**

## **INFORMASI UMUM**
- **Mata Kuliah**: Struktur Data & Algoritma
- **Pertemuan**: 1 (Pertama)
- **Topik**: Pengantar + Dasar Python untuk Algoritma
- **Alokasi Waktu**: 3 Jam (1 Jam Teori + 2 Jam Praktik)
- **Format**: Hybrid (Teori + Hands-on Coding)

---

## 🎯 **CAPAIAN PEMBELAJARAN PERTEMUAN**

Setelah mengikuti pertemuan ini, mahasiswa mampu:
1. **Memahami** konsep dasar algoritma dan struktur data
2. **Menerapkan** sintaks Python dasar untuk pemecahan masalah
3. **Membangun** pola pikir algoritmik melalui studi kasus sederhana
4. **Mengimplementasikan** fungsi, perulangan, dan struktur data list

---

## 📚 **BAGIAN I: KONSEP DASAR (60 MENIT)**

### **A. APA ITU ALGORITMA?**
**Definisi Formal**: 
> Urutan langkah-langkah logis yang terdefinisi dengan baik untuk menyelesaikan suatu masalah dalam jumlah waktu terbatas.

**Karakteristik Algoritma yang Baik**:
1. **Input**: Memiliki 0 atau lebih masukan
2. **Output**: Menghasilkan minimal 1 keluaran
3. **Definiteness**: Setiap langkah jelas/tidak ambigu
4. **Finiteness**: Berakhir setelah sejumlah langkah terbatas
5. **Effectiveness**: Setiap langkah dapat dikerjakan dalam waktu terbatas

**Contoh Analogi**: Resep Masakan
```python
# Algoritma membuat kopi
1. Siapkan gelas
2. Masukkan 1 sendok kopi
3. Tuang air panas 150ml
4. Tambahkan 2 sendok gula
5. Aduk hingga rata
6. Kopi siap disajikan
```

### **B. APA ITU STRUKTUR DATA?**
**Definisi**: 
> Cara menyimpan, mengatur, dan mengelola data dalam komputer sehingga data dapat digunakan secara efisien.

**Jenis-Jenis Dasar**:
1. **Linear**: Array, List, Stack, Queue
2. **Non-Linear**: Tree, Graph
3. **Primitif**: Integer, Float, Boolean, Character

**Analogi**: 
- **List** → Daftar belanjaan
- **Dictionary** → Kamus bahasa
- **Set** → Kumpulan nomor unik

### **C. HUBUNGAN SIMBIOSIS**
```
Masalah → Algoritma → Struktur Data → Solusi
```
**Contoh**: Mencari buku di perpustakaan
- **Masalah**: Cari buku "Struktur Data"
- **Algoritma**: Binary Search
- **Struktur Data**: Array buku terurut alfabet
- **Solusi**: Posisi buku ditemukan

### **D. MENGAPA PYTHON UNTUK SDA?**
**Keunggulan**:
1. **Sintaks sederhana** → fokus pada logika, bukan syntax
2. **High-level** → abstraksi lebih tinggi
3. **Multi-paradigma** → OOP, fungsional, prosedural
4. **Komunitas besar** → library lengkap
5. **Industri relevan** → digunakan di FAANG, startup, riset

---

## 💻 **BAGIAN II: PYTHON CRASH COURSE**

### **A. VARIABEL & TIPE DATA**
```python
# Tipe data primitif
nama = "Budi"          # String
umur = 20              # Integer
tinggi = 175.5         # Float
lulus = True           # Boolean

# Tipe data koleksi
list_nilai = [85, 90, 78]      # List (mutable)
tuple_koordinat = (3, 4)       # Tuple (immutable)
set_unik = {1, 2, 3, 3, 2}     # Set (unique) → {1, 2, 3}
dict_mahasiswa = {             # Dictionary
    "nama": "Budi",
    "nim": "12345"
}
```

### **B. PERCABANGAN (IF-ELIF-ELSE)**
```python
def kategori_nilai(nilai):
    if nilai >= 85:
        return "A"
    elif nilai >= 70:
        return "B"
    elif nilai >= 60:
        return "C"
    else:
        return "D"
```

### **C. PERULANGAN**
```python
# For loop dengan range
for i in range(5):            # 0, 1, 2, 3, 4
    print(i)

# For loop dengan list
buah = ["apel", "jeruk", "mangga"]
for b in buah:
    print(b)

# While loop
counter = 0
while counter < 3:
    print("Iterasi:", counter)
    counter += 1
```

### **D. FUNGSI**
```python
# Fungsi tanpa return
def sapa(nama):
    print(f"Halo, {nama}!")

# Fungsi dengan return
def tambah(a, b):
    return a + b

# Fungsi dengan default parameter
def pangkat(angka, eksponen=2):
    return angka ** eksponen
```

### **E. LIST & OPERASI DASAR**
```python
# Inisialisasi
angka = [10, 20, 30, 40, 50]

# Akses elemen
print(angka[0])     # 10 (indeks dimulai dari 0)
print(angka[-1])    # 50 (indeks negatif dari belakang)

# Modifikasi
angka.append(60)    # Tambah di akhir
angka.insert(2, 25) # Sisipkan di indeks 2
angka.remove(30)    # Hapus nilai 30

# Slicing
print(angka[1:4])   # [20, 25, 40]
print(angka[:3])    # [10, 20, 25]
print(angka[3:])    # [40, 50, 60]
```

### **F. REKURSI (PENGENALAN)**
```python
def hitung_mundur(n):
    if n <= 0:
        print("Selesai!")
    else:
        print(n)
        hitung_mundur(n-1)  # Memanggil diri sendiri
        
# Jalankan
hitung_mundur(5)
```

---

## 🧪 **BAGIAN III: STUDI KASUS ALGORITMIK**

### **KASUS 1: REVERSE STRING**
**Masalah**: Membalik urutan karakter dalam string

```python
def reverse_string(teks):
    """
    Mengembalikan string yang dibalik
    
    Args:
        teks (str): String input
    
    Returns:
        str: String yang sudah dibalik
    """
    hasil = ""
    for karakter in teks:
        hasil = karakter + hasil  # Menambahkan di depan
    return hasil

# Analisis Algoritma:
# 1. Inisialisasi variabel hasil
# 2. Loop melalui setiap karakter
# 3. Gabungkan karakter di depan string hasil
# 4. Kembalikan hasil
```

**Latihan**: Coba implementasi dengan slicing
```python
def reverse_string_slice(teks):
    return teks[::-1]
```

### **KASUS 2: MENGHITUNG HURUF VOKAL**
```python
def hitung_vokal(kalimat):
    """
    Menghitung jumlah huruf vokal dalam kalimat
    
    Args:
        kalimat (str): Input kalimat
    
    Returns:
        int: Jumlah huruf vokal
    """
    vokal = "aiueoAIUEO"
    counter = 0
    
    for huruf in kalimat:
        if huruf in vokal:
            counter += 1
    
    return counter

# Contoh eksekusi
print(hitung_vokal("Struktur Data"))  # Output: 4
```

### **KASUS 3: DERET FIBONACCI ITERATIF**
```python
def fibonacci_iteratif(n):
    """
    Menghasilkan n bilangan Fibonacci pertama
    
    Args:
        n (int): Jumlah bilangan Fibonacci
    
    Returns:
        list: Deret Fibonacci
    """
    if n <= 0:
        return []
    elif n == 1:
        return [0]
    
    deret = [0, 1]
    
    for i in range(2, n):
        berikutnya = deret[-1] + deret[-2]
        deret.append(berikutnya)
    
    return deret

# Pola: 0, 1, 1, 2, 3, 5, 8, 13, ...
# Setiap bilangan adalah jumlah dua bilangan sebelumnya
```

### **KASUS 4: PENCARIAN ELEMEN DALAM LIST**
```python
def cari_elemen(list_data, target):
    """
    Mencari elemen dalam list (linear search)
    
    Args:
        list_data (list): List yang akan dicari
        target: Elemen yang dicari
    
    Returns:
        int: Indeks elemen, atau -1 jika tidak ditemukan
    """
    for i in range(len(list_data)):
        if list_data[i] == target:
            return i
    return -1  # Tidak ditemukan

# Contoh penggunaan
data = [10, 20, 30, 40, 50]
print(cari_elemen(data, 30))  # Output: 2
print(cari_elemen(data, 99))  # Output: -1
```

---

## 📝 **BAGIAN IV: LATIHAN MANDIRI**

### **SOAL LATIHAN**
1. **Luas Lingkaran**
   ```python
   def luas_lingkaran(jari_jari):
       # Lengkapi kode ini
       pass
   ```

2. **Nilai Maksimum**
   ```python
   def nilai_maksimum(list_angka):
       # Lengkapi kode ini
       pass
   ```

3. **Fibonacci Rekursif**
   ```python
   def fibonacci_rekursif(n):
       # Lengkapi kode ini
       pass
   ```

4. **Palindrome Checker**
   ```python
   def is_palindrome(kata):
       # Mengembalikan True jika kata palindrome
       pass
   ```

### **SOLUSI CONTOH**
```python
# Soal 1: Luas Lingkaran
import math

def luas_lingkaran(r):
    return math.pi * r * r

# Soal 2: Nilai Maksimum
def nilai_maksimum(angka):
    if not angka:  # Jika list kosong
        return None
    
    maks = angka[0]
    for nilai in angka:
        if nilai > maks:
            maks = nilai
    return maks
```

---

## 📊 **RUBRIK PENILAIAN**

| **Aspek** | **Bobot** | **Kriteria** |
|-----------|-----------|--------------|
| **Kebenaran Logika** | 40% | Algoritma menyelesaikan masalah dengan benar |
| **Kelengkapan Fungsi** | 30% | Semua fungsi terimplementasi dengan parameter dan return yang tepat |
| **Keterbacaan Kode** | 20% | Nama variabel bermakna, komentar jelas, struktur rapi |
| **Efisiensi** | 10% | Menggunakan struktur data dan perulangan yang tepat |

---

## 🚀 **TUGAS RUMAH (INDIVIDUAL)**

### **Bagian A: Teori**
1. Jelaskan perbedaan antara algoritma dan program!
2. Sebutkan 3 contoh algoritma dalam kehidupan sehari-hari!
3. Mengapa Python cocok untuk pembelajaran struktur data?

### **Bagian B: Praktik**
Buat program Python yang berisi:
1. Fungsi untuk menghitung faktorial (iteratif dan rekursif)
2. Fungsi untuk mengurutkan list kecil (3-5 elemen) secara manual
3. Program utama yang memanggil semua fungsi dengan contoh data

### **Format Pengumpulan**:
- Nama file: `Pertemuan1_NIM_Nama.py`
- Dikumpulkan melalui LMS sebelum pertemuan berikutnya

---

## 📖 **REFERENSI LANJUTAN**

1. **Buku**:
   - "Python for Everybody" by Charles Severance
   - "Problem Solving with Algorithms and Data Structures using Python" by Miller & Ranum

2. **Online Resources**:
   - W3Schools Python Tutorial
   - GeeksforGeeks Data Structures
   - Programiz Python Programming

3. **Tools**:
   - Python Tutor (pythontutor.com) untuk visualisasi eksekusi
   - Replit untuk coding online

---

## 🎯 **MAIN REFERENCE**

1. https://www.geeksforgeeks.org/dsa/dsa-tutorial-learn-data-structures-and-algorithms
2. https://www.w3schools.com/dsa/dsa_intro.php

---

**"The best way to learn data structures is to implement them from scratch."** - Unknown