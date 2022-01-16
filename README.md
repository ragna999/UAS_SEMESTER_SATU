# UAS_SEMESTER_SATU
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <table border="1">
        <tr>
            <th> Nama</th>
            <th>NIM</th>
            <th>Kelas</th>
        </tr>
        <tr>
            <td>Erik maualan </td>
            <td>312110188</td>
            <td>TI.21.C1</td>
        </tr>
    </table>
</body>
</html>

- Berikut adalah isi dari file **daftar_nilai.py**

```python
from view.input_nilai import *

data = {}

Menambahkan data

def tambah_data():
global data
ulangi = 'y'
while ulangi =='y':
nama = input_nama()
nim = input_nim()
nilai_tugas = input_ntugas()
nilai_uts = input_nuts()
nilai_uas = input_nuas()
nilai_akhir = nakhir()
data[nama] = [nama, nim, nilai_tugas, nilai_uts, nilai_uas, nilai_akhir]
ulangi = (input('tambah data?(y/t) : '))

        if ulangi == 't':
            print('\nData berhasil di tambah!')
            return data

Mengubah data

def ubah_data():
nama = input("Masukan nama untuk mengubah data: ")
if nama in data.keys():
print("\nMau mengubah apa?")
sub_data = input("(Semua), (NIM), (Tugas), (UTS), (UAS) : ")
if sub_data.lower() == "semua":
print("==========================")
print("Ubah data {}.".format(nama))
print("==========================")
data[nama][1] = input("Ubah NIM:")
data[nama][2] = int(input("Ubah Nilai Tugas: "))
data[nama][3] = int(input("Ubah Nilai UTS: "))
data[nama][4] = int(input("Ubah Nilai UAS: "))
data[nama][5] = data[nama][2] *30/100 + data[nama][3]*35/100 + data[nama][4] \*35/100
print("\nBerhasil ubah data!")

        elif sub_data.lower() == "nim":
            data[nama][1] = input("\nNIM:")
            print('\nData berhasil di ubah!')
        elif sub_data.lower() == "tugas":
            data[nama][2] = int(input("\nNilai Tugas: "))
            data[nama][5] = data[nama][2] *30/100 + data[nama][3]*35/100 + data[nama][4] *35/100
            print('\nData berhasil di ubah!')
        elif sub_data.lower() == "uts":
            data[nama][3] = int(input("\nNilai UTS: "))
            data[nama][5] = data[nama][2] *30/100 + data[nama][3]*35/100 + data[nama][4] *35/100
            print('\nData berhasil di ubah!')
        elif sub_data.lower() == "uas":
            data[nama][4] = int(input("\nNilai UAS: "))
            data[nama][5] = data[nama][2] *30/100 + data[nama][3]*35/100 + data[nama][4] *35/100
            print('\nData berhasil di ubah!')
        else:
            print("\nMenu tidak ditemukan.")

    else:
        print("'{}' Tidak ditemukan.".format(nama))
       
 <img width="711" alt="2022-01-16" src="https://user-images.githubusercontent.com/92783916/149649559-e4533ccd-f7da-4213-adb5-114342b2ffda.png">
 <img width="712" alt="2022-01-16 (1)" src="https://user-images.githubusercontent.com/92783916/149649573-0b18cc39-1bec-4c18-9455-59d0d719a060.png">
<img width="722" alt="2022-01-16 (2)" src="https://user-images.githubusercontent.com/92783916/149649584-0189a13a-4687-499d-90c8-5ef7e8641668.png">

        

