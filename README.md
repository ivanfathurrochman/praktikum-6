# praktikum-6

# Latihan 1

Buat Dictionary daftar kontak

### Nama sebagai Key dan Nomor sebagai Value

telp = {}

telp['Ari'] = '081267888'

telp['Dina'] = '087677776'

### Tampilkan kontaknya Ari

print(telp['Ari'])

### Tambah kontak baru dengan nama Riko, nomor 087654544

telp['Riko'] = '087654544'

### Ubah kontak Dina dengan nomor baru 088999776

telp['Dina'] = '088999776'

### Tampilkan semua Nama

print(telp.keys())

### Tampilkan semua Nomor

print(telp.values())

### Tampilkan daftar Nama dan nomornya

print(telp.items())
![Untitled](https://user-images.githubusercontent.com/115911604/204180698-82607575-e2a9-4319-8464-48b280fa037e.png)


# Hapus kontak Dina.

telp.pop('Dina')

![image](https://user-images.githubusercontent.com/115911604/204180922-14841acb-e30d-46be-8d88-f10c07894ae9.png)

### Daftar Nilai Mahasiswa Menggunakan Dictionary
### Pertama kita membuat sebuah dictionary kosong yang nantinya akan diinputkan data ketika program dijalankan.
Data = {}

Lalu kita membuat kondisi perulangan dan sebuah keterangan untuk pilihan menu yang akan menjalankan program.

while True:

List = input("\n(T)ambah, (U)bah, (H)apus, (C)ari, (L)ihat, (K)eluar: ")

Membuat syntax untuk menambahkan data.

if List.lower() == 't':

print("Tambah Data")

nama = input("Nama           : ")

nim = int(input("NIM            : "))

tugas = int(input("Nilai Tugas    : "))

uts = int(input("Nilai UTS      : "))

uas = int(input("Nilai UAS      : "))

akhir = tugas*30/100 + uts*35/100 + uas*35/100

Data[nama] = nim, tugas, uts, uas, akhir

Disini apabila kita menginputkan 't' maka kita akan diminta untuk menginputkan beberapa data. Data yang kita inputkan akan masuk ke dictionary 'Data' yang telah dibuat 

tadi dengan data 'nama' sebagai keys dan sisanya
