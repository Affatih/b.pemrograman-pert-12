 # program daftar nilai mahasiswa dengan fitur
 Method tambah() untuk menambah data
 Method tampilkan() untuk menampilkan data
 Method hapus(nama) untuk menghapus data berdasarkan nama
 Method ubah(nama) untuk mengubah data berdasarkan nama




## input
```
class DaftarMahasiswa:
    def __init__(self):
        self.data_mahasiswa = []

    def tambah(self):
        """Menambah data mahasiswa baru."""
        nama = input("Masukkan nama mahasiswa: ")
        nilai = float(input("Masukkan nilai mahasiswa: "))
        self.data_mahasiswa.append({"nama": nama, "nilai": nilai})
        print("Data mahasiswa berhasil ditambahkan.")

    def tampilkan(self):
        """Menampilkan semua data mahasiswa."""
        if not self.data_mahasiswa:
            print("Data mahasiswa masih kosong.")
        else:
            print("Daftar Nilai Mahasiswa:")
            print("--------------------------")
            for mahasiswa in self.data_mahasiswa:
                print(f"Nama: {mahasiswa['nama']}, Nilai: {mahasiswa['nilai']}")
                print("--------------------------")

    def hapus(self, nama):
        """Menghapus data mahasiswa berdasarkan nama."""
        for i, mahasiswa in enumerate(self.data_mahasiswa):
            if mahasiswa['nama'].lower() == nama.lower():
                del self.data_mahasiswa[i]
                print(f"Data mahasiswa dengan nama {nama} berhasil dihapus.")
                return
        print(f"Data mahasiswa dengan nama {nama} tidak ditemukan.")

    def ubah(self, nama):
        """Mengubah data mahasiswa berdasarkan nama."""
        for mahasiswa in self.data_mahasiswa:
            if mahasiswa['nama'].lower() == nama.lower():
                nilai_baru = float(input("Masukkan nilai baru: "))
                mahasiswa['nilai'] = nilai_baru
                print(f"Data mahasiswa dengan nama {nama} berhasil diubah.")
                return
        print(f"Data mahasiswa dengan nama {nama} tidak ditemukan.")

# Inisialisasi objek DaftarMahasiswa
daftar_mahasiswa = DaftarMahasiswa()

# Menu program
while True:
    print("\nMenu:")
    print("1. Tambah data mahasiswa")
    print("2. Tampilkan data mahasiswa")
    print("3. Hapus data mahasiswa")
    print("4. Ubah data mahasiswa")
    print("5. Keluar")
    pilihan = input("Pilih menu (1/2/3/4/5): ")

    if pilihan == '1':
        daftar_mahasiswa.tambah()
    elif pilihan == '2':
        daftar_mahasiswa.tampilkan()
    elif pilihan == '3':
        nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
        daftar_mahasiswa.hapus(nama)
    elif pilihan == '4':
        nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
        daftar_mahasiswa.ubah(nama)
    elif pilihan == '5':
        print("Terima kasih! Program selesai.")
        break
    else:
        print("Pilihan tidak valid.")
```

 ## OUTPUT

 ```
Menu:
1. Tambah data mahasiswa
2. Tampilkan data mahasiswa
3. Hapus data mahasiswa
4. Ubah data mahasiswa
5. Keluar
Pilih menu (1/2/3/4/5): 1
Masukkan nama mahasiswa: Fatih
Masukkan nilai mahasiswa: 90
Data mahasiswa berhasil ditambahkan.

Menu:
1. Tambah data mahasiswa
2. Tampilkan data mahasiswa
3. Hapus data mahasiswa
4. Ubah data mahasiswa
5. Keluar
Pilih menu (1/2/3/4/5): 2
Daftar Nilai Mahasiswa:
--------------------------
Nama: Fatih, Nilai: 90.0

Menu:
1. Tambah data mahasiswa
2. Tampilkan data mahasiswa
3. Hapus data mahasiswa
4. Ubah data mahasiswa
5. Keluar
Pilih menu (1/2/3/4/5): 2
Daftar Nilai Mahasiswa:
2. Tampilkan data mahasiswa
3. Hapus data mahasiswa
4. Ubah data mahasiswa
5. Keluar
Pilih menu (1/2/3/4/5): 2
Daftar Nilai Mahasiswa:
Pilih menu (1/2/3/4/5): 2
Daftar Nilai Mahasiswa:
Daftar Nilai Mahasiswa:
--------------------------
Nama: Fatih, Nilai: 90.0
--------------------------

Menu:
1. Tambah data mahasiswa
2. Tampilkan data mahasiswa
Nama: Fatih, Nilai: 90.0
--------------------------

Menu:
1. Tambah data mahasiswa
2. Tampilkan data mahasiswa
3. Hapus data mahasiswa
4. Ubah data mahasiswa
3. Hapus data mahasiswa
4. Ubah data mahasiswa
5. Keluar
5. Keluar
Pilih menu (1/2/3/4/5):
```

![flowchart1](https://github.com/user-attachments/assets/1c32e361-9422-4f1c-979a-43ffae2a8e4a)

![flowchart2](https://github.com/user-attachments/assets/700de01f-3cc6-4d8e-a7b9-b398088d4403)
