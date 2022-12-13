# PRAKTIKUM-8

NAMA    : NADYA KHAIRUNNISA

NIM     : 312210133

KELAS   : TI.22.A1

## DAFTAR ISI <br>
| No | Description | Link |
|-----|------|-----|
|1|Latihan|[Click Here](#latihan)|
|2|Praktikum8|[Click Here](#praktikum8)|
|3|Flowchart Praktikum8|[Click Here](#flowchart-praktikum-8)|

### Tugas Praktikum 8

Buat program sederhana dengan mengaplikasikan penggunaan class. Buatlah class untuk menampilkan daftar nilai mahasiswa, dengan ketentuan:

- Method tambah() untuk menambah data
- Method tampilkan() untuk menampilkan data
- Method hapus(nama) untuk menghapus data berdasarkan nama
- Method ubah(nama) untuk mengubah data berdasarkan nama
- Buat diagram class, flowchart dan penjelasan programnya pada README.md.
- Commit dan push repository ke github.

## Praktikum 8

Rumus 

        class mahasiswa:
            def __init__(self, nim, nama, tugas, uts, uas):
            self.nim = nim
            self.nama = nama
            self.tugas = tugas
            self.uts = uts
            self.uas = uas

        def tambah(self,nim,nama,tugas,uts,uas):
            data.nim.append(nim)
            data.nama.append(nama)
            data.tugas.append(tugas)
            data.uts.append(uts)
            data.uas.append(uas)

        def lihat(self):
            for i in range(len(data.nama)):
                print("|", i+1, "  |", end="")
                print('{0:<25}'.format(self.nama[i]), end="")
                print("|", self.nim[i], end="")
                print(" |", self.tugas[i], end="")
                print("    |", self.uts[i], end="")
                print("  |", self.uas[i], " | ", end="")
                print(f'{((self.tugas[i]*30/100) + (self.uts[i]*35/100) + (self.uas[i]*35/100)) :.2f}', " |")

        def ubah(self,nim,nama,tugas,uts,uas):
            self.nim[no] = nim
            self.nama[no] = nama
            self.tugas[no] = tugas
            self.uts[no] = uts
            self.uas[no] = uas

        def hapus(self):
            del self.nim[no]
            del self.nama[no]
            del self.tugas[no]
            del self.uts[no]
            del self.uas[no]

    data = mahasiswa([],[],[],[],[])

    while True:
        menu = input("\n[(L)ihat, (T)ambah, (U)bah, (H)apus, (K)eluar]:")
        if menu == "t" or menu == "T":
           print("\nTambah Data")
           data.tambah(
               input("Masukkan NIM : "),
               input("Masukkan Nama : "),
               int(input("Nilai Tugas : ")),
               int(input("Nilai UTS : ")),
               int(input("Nilai UAS : "))
               )
           print("\nData berhasil ditambahkan")

        elif menu == "l" or menu == "L":
            print("\nDaftar Nilai")
            print("==========================================================================")
            print("| No  |          Nama           |    NIM    | TUGAS | UTS | UAS |  AKHIR |")
            print("==========================================================================")
            if len(data.nama) != 0:
                data.lihat()
            else:
                print("                         TIDAK ADA DATA                               ")
            print("==========================================================================")

        elif menu == "u" or menu == "U":
            print("\nUbah Data")
            ubah = input("Masukkan Nama : ")
            if ubah in data.nama:
               no = data.nama.index(ubah)
               print("Masukkan Data Yang Baru : ")
               data.ubah(
                   input("NIM : "),
                   input("Nama : "),
                   int(input("Nilai Tugas : ")),
                   int(input("Nilai UTS : ")),
                   int(input("Nilai UAS : "))
                   )
            else:
                print(ubah, "tidak ada di dalam data")

        elif menu == "h" or menu == "H":
            print("\nHapus Data")
            hapus = input("Masukkan Nama : ")
            if hapus in data.nama:
                no = data.nama.index(hapus)
                data.hapus()
                print("Data", hapus, "Berhasil dihapus")
            else:
                print(hapus, "tidak ada di dalam data")

        elif menu == "k" or menu == "K":
            print("\nTerimakasih\n")
            break

        else:
            print("\nPerintah yang dimasukkan salah!\n")

## PROGRAM :
![PRAKTIKUM 8 1](https://user-images.githubusercontent.com/115801823/207297525-26eefcf9-f699-4dfc-b6f0-a0115ef8cec1.PNG)

![PRAKTIKUM 8 2](https://user-images.githubusercontent.com/115801823/207297591-6ee1e345-a7b8-4d1d-8e73-a4c5ad07332f.PNG)

![PRAKTIKUM 8 3](https://user-images.githubusercontent.com/115801823/207297668-dfc8a5d8-e1dd-4484-9c19-461a97ad25c0.PNG)

![PRAKTIKUM 8 4](https://user-images.githubusercontent.com/115801823/207297765-7775f61b-9974-4a06-97d7-879fdbdf08ae.PNG)

# Hasil Run & Penjelasan Program :

- Pertama kita mendeklarasikan sebuah class mahasiswa yang didalamnya terdapat atribut NIM, Nama, nilai tugas, nilai UTS dan nilai UAS. Jangan lupa, untuk mendeklarasikan sebuah class didalam OOP kita harus menggunakan def__init__ dan juga self.
        class mahasiswa:
            def __init__(self, nim, nama, tugas, uts, uas):
                self.nim = nim
                self.nama = nama
                self.tugas = tugas
                self.uts = uts
                self.uas = uas                
- Seperti biasa, deklarasikan satu dictionary kosong sebagai tempat menyimpan data-data yang sudah kita input. Ada 5 list kosong yang nantinya berisi NIM, Nama, nilai tugas, nilai UTS dan nilai UAS.
        data = mahasiswa([],[],[],[],[])  
- Kita akan buat beberapa method untuk menambahkan, menampilkan, menghapus, mengubah data mahasiswa. Pertama membuat method tambah(), method ini berfungsi untuk menambahkan data. Dalam method ini kita menggunakan append() supaya data yang terakhir ditambahkan ada di urutan list paling akhir.
        def tambah(self,nim,nama,tugas,uts,uas):
                data.nim.append(nim)
                data.nama.append(nama)
                data.tugas.append(tugas)
                data.uts.append(uts)
                data.uas.append(uas)
- Ini tampilan jika kita menginput method : Tambah()

![HASIL RUN TAMBAH DATA](https://user-images.githubusercontent.com/115801823/207298950-a269633e-5b6c-4a31-9d2c-6a2e0d29ec0b.PNG)

- Fungsi membuat method lihat() yaitu untuk menampilkan seluruh data yang sudah kita tambahkan tadi. Jika tidak ada data sama sekali, maka akan muncul tulisan TIDAK ADA DATA.
        def lihat(self):
                for i in range(len(data.nama)):
                    print("|", i+1, "  |", end="")
                    print('{0:<25}'.format(self.nama[i]), end="")
                    print("|", self.nim[i], end="")
                    print(" |", self.tugas[i], end="")
                    print("    |", self.uts[i], end="")
                    print("  |", self.uas[i], " | ", end="")
                    print(f'{((self.tugas[i]*30/100) + (self.uts[i]*35/100) + (self.uas[i]*35/100)) :.2f}', " |")
- Ini tampilan jika kita menginput method : Lihat()

![HASIL RUN LIHAT DATA](https://user-images.githubusercontent.com/115801823/207299422-8351f49c-61f1-4dc3-b8bb-b65633bc6a4e.PNG)

- Fungsi membuat method ubah() yaitu untuk mengubah data. jika method ini diinput, maka data Nama, NIM, nilai tugas, nilai UTS, nilai UAS index nomor - (no) akan diubah sesuai dengan inputan dari user. Index ke - (no) akan dicari secara otomatis sesuai dengan nama yang ingin diubah oleh user.
        def ubah(self,nim,nama,tugas,uts,uas):
                self.nim[no] = nim
                self.nama[no] = nama
                self.tugas[no] = tugas
                self.uts[no] = uts
                self.uas[no] = uas
- Ini tampilan jika kita menginput method : Ubah()

![HASIL RUN UBAH DATA](https://user-images.githubusercontent.com/115801823/207299760-36b47d9c-ed23-43bd-ac44-c8ca9180bacd.PNG)
               
- Terakhir kita membuat method hapus(), yang berfungsi untuk menghapus data berdasarkan nama. Kita bisa menggunakan del untuk menghapus datanya. Seperti sebelumnya, nomor index list yang akan dihapus disesuaikan dengan inputan dari user. Yaitu index nomor ke - (no).
        def hapus(self):
                del self.nim[no]
                del self.nama[no]
                del self.tugas[no]
                del self.uts[no]
                del self.uas[no]
- Ini tampilan jika kita menginput method : Hapus()

![HASIL RUN HAPUS DATA](https://user-images.githubusercontent.com/115801823/207301398-fe36b062-2a7f-4d8a-9639-ec715e050c9b.PNG)

## Diagram Class Praktikum 8

![WhatsApp Image 2022-12-13 at 08 09 44](https://user-images.githubusercontent.com/115801823/207301797-f2e361d3-bf75-4aa9-892c-c08e5a525506.jpg)

## Flowchart Praktikum 8

![WhatsApp Image 2022-12-13 at 09 27 39](https://user-images.githubusercontent.com/115801823/207301962-d902da3c-825c-401c-9158-b65b98169cfb.jpg)

## Sekian dan Terima Kasih
