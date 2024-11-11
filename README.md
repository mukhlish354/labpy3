## latihan1 
````python
import random

n = int(input("Masukkan nilai N: "))

for i in range(1, n+1):
    a = random.uniform(0, 0.5)
    print(f"Data ke: {i} => {a}")
````
## Hasil
```
Masukkan nilai N: 5
Data ke: 1 => 0.48949809806221006
Data ke: 2 => 0.06325157008466487
Data ke: 3 => 0.1601108490800564
Data ke: 4 => 0.4305807343717917
Data ke: 5 => 0.1645386464841146
````
## Alur Algoritma
1. Program melakukan import library `random` untuk menggunakan fungsi bilangan acak

2. Program meminta user memasukkan nilai N sebagai jumlah bilangan yang akan digenerate
  - Input berupa bilangan bulat positif
  - Disimpan dalam variabel `n`

3. Program melakukan perulangan/loop sebanyak N kali:
  - Menggunakan fungsi `range(1, n+1)` agar loop mulai dari 1 sampai N
  - Di setiap loop:
    - Generate bilangan random antara 0-0.5 menggunakan `random.uniform()`
    - Tampilkan nomor data dan bilangan random yang dihasilkan
## Latihan 2
```
modal = 4500000000
laba_per_bulan = [0, 0, 1, 1, 5, 5, 5, 3]
total_laba = 0

for i, laba in enumerate(laba_per_bulan, start=1):
    laba_bulan = (laba / 100) * modal
    total_laba += laba_bulan    
    if i <= 2:
        print(f"Laba bulan ke-{i} sebesar: {int(laba_bulan)}")
    else:
        print(f"Laba bulan ke-{i} sebesar: {laba_bulan:.1f}")

print(f"Total laba adalah: {total_laba:.1f}")
```
## Hasil
```python
Laba bulan ke-1 sebesar: 0
Laba bulan ke-2 sebesar: 0
Laba bulan ke-3 sebesar: 45000000.0
Laba bulan ke-4 sebesar: 45000000.0
Laba bulan ke-5 sebesar: 225000000.0
Laba bulan ke-6 sebesar: 225000000.0
Laba bulan ke-7 sebesar: 225000000.0
Laba bulan ke-8 sebesar: 135000000.0
Total laba adalah: 900000000.0
```
## Alur Algoritma
1. Inisialisasi data awal:
  - Modal awal ditetapkan sebesar 100.000.000
  - Array/List `laba_per_bulan` berisi persentase laba tiap bulan [0, 0, 1, 1, 5, 5, 5, 3]
  - Variabel `total_laba` diinisialisasi dengan nilai 0

2. Melakukan perulangan/loop menggunakan for loop untuk setiap bulan:
  - Menggunakan `enumerate()` agar mendapatkan indeks(i) dan nilai(laba)
  - Parameter `start=1` membuat indeks dimulai dari 1
  - Di setiap perulangan/loop:
    - Hitung laba bulan = (persentase / 100) × modal
    - Tambahkan laba bulan ke total laba

3. Menampilkan hasil:
  - Untuk bulan 1-2: tampilkan dalam bilangan bulat
  - Untuk bulan 3-8: tampilkan dengan 1 angka desimal
  - Di akhir tampilkan total laba

## Latihan 3
```python
    saldo = 50000000

while True:
    print(f"Saldo saat ini {saldo}")
    print("1. Tarik Uang")
    print("2. Keluar")
    pilihan = input("Pilih menu (1/2): ")
    if pilihan == '1':
        nom_tarik = int(input("Masukkan Jumlah penarikan: "))
        if saldo > nom_tarik:
            saldo -= nom_tarik
        else:
            print("Saldo Anda Tidak Cukup")
    else:
        print("Terimakasih telah menggunakan ATM")
        break
```
## Hasil
```
Saldo saat ini 50000000
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 1
Masukkan Jumlah penarikan: 1500000
Saldo saat ini 48500000
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 2
Terimakasih telah menggunakan ATM
```
## Alur Algoritma

1. Inisialisasi data awal:
   - `saldo` ditetapkan sebesar 1,000,000 sebagai saldo awal.

2. Memasuki loop utama menggunakan `while True`:
   - Menampilkan saldo saat ini.
   - Menampilkan dua pilihan menu:
     - **1. Tarik Uang**
     - **2. Keluar**
   - Meminta input pengguna untuk memilih opsi.

3. Menangani pilihan pengguna:
   - **Jika pilihan adalah 1 (Tarik Uang)**:
     - Meminta pengguna memasukkan jumlah uang yang ingin ditarik.
     - Mengecek apakah saldo cukup untuk penarikan:
       - Jika saldo mencukupi, kurangi saldo sebesar jumlah yang dimasukkan.
       - Jika saldo tidak mencukupi, tampilkan pesan "Saldo Anda Tidak Cukup".
   - **Jika pilihan adalah 2 (Keluar)**:
     - Menampilkan pesan "Terimakasih telah menggunakan ATM" dan menghentikan loop menggunakan `break`.

4. Program berakhir setelah pengguna memilih untuk keluar.
