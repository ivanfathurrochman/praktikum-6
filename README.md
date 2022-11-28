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

![gambar1](https://user-images.githubusercontent.com/115911604/204181178-b2492396-f841-4512-93cd-9d895cd6a4bc.png)


### Membuat syntax untuk mencari data

elif List.lower() == 'c':
        print("Cari Data")
        nama = input("Masukkan Nama : ")
        if nama in Data.keys():
            print("="*73)
            print("|                             Daftar Mahasiswa                          |")
            print("="*73)
            print("| Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*73)
            print("| {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                  .format(nama, nim, uts, uas, tugas, akhir))
            print("="*73)
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))
            
            
### Membuat syntax untuk melihat atau menampilkan data.

elif List.lower() == 'l':
        if Data.items():
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            i = 0
            for j in Data.items():
                i += 1
                print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                      .format(j[0][:13], j[1][0], j[1][1], j[1][2], j[1][3], j[1][4], no=i))
            print("=" * 78)
        else:
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            print("|                                TIDAK ADA DATA                              |")
            print("="*78)
            
            
           
### Apabila kita menginput 'l' maka sistem akan menampilkan data - data yang sudah kita masukkan. Jika kita belum memasukkan data maka outputnya menjadi "TIDAK ADA DATA".

![foto8](https://user-images.githubusercontent.com/115911604/204182244-228b9788-b2ee-4dde-bc2e-c01935d35763.png)

### Apabila kita menginput 'k' maka program akan langsung berhenti.
