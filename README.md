# pratikum6 - sub rutin/funsi

```python
while True:
    print("[(L)ihat, (T)ambah, (U)bah, (H)apus, (K)eluar]")
    pilihan = input("Pilih menu: ").lower()

    if pilihan == 'l':
        tampilkan_data()
    elif pilihan == 't':
        tambah_data()
    elif pilihan == 'h':
        hapus_data()    
    elif pilihan == 'u':
        ubah_data()
    elif pilihan == 'k':
        print("Keluar dari program...")
        break
    else:
        print("Pilihan tidak valid, silakan pilih menu yang tersedia.")
```
Menu input agar kita bisa `tampilkan_data`, `hapus_data`,`ubah_data`,dan `tambah_data`

```python
def tambah_data():
    nama = input("Nama: ")
    nim = input("NIM: ")
    tugas = float(input("Nilai Tugas: "))
    uts = float(input("Nilai UTS: "))
    uas = float(input("Nilai UAS: "))
    data_mahasiswa[nama] = {'nim': nim, 'tugas': tugas, 'uts': uts, 'uas': uas}
```
`def` adalah sebuah function
- nama: masukkan nama
- nim: masukan nim
- tugas: masukkan nilai tugas
- uts: masukkan nilai uts
- uas: masukkan nilai uas

dengan tugas 30% uts 35% dan uas 35%
```python
nilai_akhir = (data['tugas'] * 0.3) + (data['uts'] * 0.35) + (data['uas'] * 0.35)
```

```python
def hapus_data():
    nama = input("Masukkan Nama: ")
    if nama in data_mahasiswa:
        del data_mahasiswa[nama]
        print("Data berhasil dihapus!")
    else:
        print("Data dengan Nama tersebut tidak ditemukan!")
```
untuk menghapus data mahasiswa

```python
def ubah_data():
    nama= input("Masukkan Nama: ")
    if nama in data_mahasiswa:
        print("Masukkan data baru:")
        data_mahasiswa[nama]['nim'] = input("Masukkan NIM: ")
        data_mahasiswa[nama]['tugas'] = float(input("Nilai Tugas: "))
        data_mahasiswa[nama]['uts'] = float(input("Nilai UTS: "))
        data_mahasiswa[nama]['uas'] = float(input("Nilai UAS: "))
        print("Data berhasil diubah!")
    else:
        print("Data dengan Nama tersebut tidak ditemukan!")
```
untuk mengubah data 

### flowchat
![foto](https://github.com/FajarMhr24/flochart/blob/b427a7b3f1e98dc51c1ca3858c30489fa54f1d00/Screenshot%202024-12-01%20000125.png)

### output
![foto](https://github.com/FajarMhr24/foto/blob/e5a8ddb705b33ee790d58fdcfc0ba2dd90404584/Screenshot%202024-11-30%20233807.png)
