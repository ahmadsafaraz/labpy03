1. Latihan 1

Hasil dari latihan 1

![Cuplikan layar 2024-11-07 101329](https://github.com/user-attachments/assets/6441d167-50ed-4daa-88c7-6c7db448f918)


Code

    import random

    # Meminta pengguna memasukkan nilai n
    n = int(input("Masukkan nilai N: "))

    # Looping untuk menghasilkan n bilangan acak
    for i in range(1, n + 1):
    # Menghasilkan bilangan acak antara 1 dan 5
    bilangan_acak = random.uniform(1, 5)

    # Menampilkan data ke-i dan nilai bilangan acak
    print(f"data ke: {i} => {bilangan_acak}")

    print("Selesai")

1. Import Modul random: o Baris pertama import random digunakan untuk mengimpor modul random yang
menyediakan berbagai fungsi untuk menghasilkan bilangan acak.

2. Meminta Input Pengguna: o Program meminta pengguna untuk memasukkan nilai n, yang merupakan jumlah bilangan acak yang ingin dihasilkan. Nilai n ini akan digunakan sebagai batas atas dalam perulangan.

3. Perulangan untuk Menghasilkan Bilangan Acak: o Menggunakan for i in range(1, n+1):, program melakukan perulangan sebanyak n kali. Dalam setiap iterasi:  random.uniform(1, 5) digunakan untuk menghasilkan bilangan acak dengan titik desimal (float) antara 1 (inklusif) dan 5 (inklusif).  Bilangan acak yang dihasilkan disimpan dalam variabel bilangan_acak.

4. Menampilkan Hasil: o Setiap bilangan acak yang dihasilkan akan ditampilkan bersama dengan nomor urutannya menggunakan format f"data ke: {i} => {bilangan_acak}". o Setelah semua bilangan acak dihasilkan dan ditampilkan, program akan mencetak pesan "Selesai" untuk mengindikasikan bahwa proses telah selesai. Penjelasan Fungsi random.uniform(a, b): • Fungsi ini menghasilkan bilangan acak dengan distribusi seragam (uniform) dalam rentang antara a (inklusif) dan b (inklusif). • Dalam contoh ini, a adalah 1 dan b adalah 5, sehingga bilangan acak yang dihasilkan akan berada di antara 1.0 dan 5.0.

LATIHAN 2

Hasil dari latihan 2

![Cuplikan layar 2024-11-07 104945](https://github.com/user-attachments/assets/eadd807b-a7d3-468f-b36c-4a720b56b1cd)

code 2

    # Inisialisasi modal awal dan total laba
    modal_awal = 100000000  # 100 juta
    laba = 0
    total_laba = 0

    # Loop untuk bulan 1 sampai 8
    for bulan in range(1, 9):
    # Menentukan laba berdasarkan bulan
    if bulan in [1, 2]:  # Bulan 1 dan 2, belum mendapatkan laba
        laba = 0
    elif bulan in [3, 4]:  # Bulan 3 dan 4, laba 1% dari modal
        laba = modal_awal * 0.01
    elif bulan in [5, 6, 7]:  # Bulan 5, 6, dan 7, laba 5% dari modal
        laba = modal_awal * 0.05
    elif bulan == 8:  # Bulan 8, laba turun menjadi 3% dari modal
        laba = modal_awal * 0.03
    
    # Menampilkan laba per bulan
    print(f"Laba bulan ke-{bulan} sebesar: {laba}")
    
    # Menambahkan laba ke total laba
    total_laba += laba

    # Menampilkan total laba selama 8 bulan
    print(f"Total laba selama 8 bulan adalah: {total_laba}")

penjelasan latihan 2

1. modal_awal diatur ke 100 juta.
2. Kode menggunakan loop for untuk mengulang dari bulan 1 hingga bulan 8.
3. Dalam setiap iterasi, laba per bulan dihitung berdasarkan persentase laba sesuai bulan:
    Bulan 1 dan 2 belum mendapatkan laba (laba = 0).
    Bulan 3 dan 4 memiliki laba sebesar 1% dari modal.
    Bulan 5, 6, dan 7 memiliki laba sebesar 5% dari modal.
    Bulan 8 mengalami penurunan laba menjadi 3% dari modal.
4. Laba bulanan ditambahkan ke total_laba.
5. Setelah loop selesai, total laba selama 8 bulan ditampilkan.


LATIHAN 3

Hasil dari Latihan 3

![image](https://github.com/user-attachments/assets/11d6fb2e-e173-4b73-a359-9767add7f206)

code

    def atm():
      saldo = 1000000

      while True:
    print("Saldo saat ini: Rp", saldo)
    print("1. Tarik Uang")
    print("2. Keluar")
    pilihan = int(input("Pilih menu (1/2): "))

    if pilihan == 1:
      jumlah_tarik = int(input("Masukkan jumlah penarikan: "))
      if jumlah_tarik <= saldo:
        saldo -= jumlah_tarik
        print("Penarikan berhasil!")
      else:
        print("Saldo tidak mencukupi!")
    elif pilihan == 2:
      print("Terima kasih telah menggunakan ATM!")
      break
    else:
      print("Pilihan tidak valid!")

    atm()

penjelasan code 3

1. Definisi Fungsi atm(): o Program dimulai dengan mendefinisikan fungsi atm(), untuk menjalankan seluruh logika program ATM.

2. Inisialisasi Saldo: o Di dalam fungsi atm(), variabel saldo diinisialisasi dengan nilai 1000000. Ini mewakili saldo awal di rekening pengguna.

3. Perulangan Utama: o while True: memulai sebuah perulangan tak terbatas. Perulangan ini akan terus berjalan hingga pengguna memilih untuk keluar dari program. o Di dalam perulangan, program akan terus menampilkan menu pilihan kepada pengguna.

4. Menampilkan Menu: o Program menampilkan saldo saat ini dan dua pilihan:
Tarik Uang/Keluar

5. Meminta Input Pengguna: o Pengguna diminta untuk memilih salah satu opsi dengan memasukkan angka 1 atau 2. Pilihan pengguna disimpan dalam variabel pilihan.

6. Percabangan Kondisi: o Pilihan 1 (Tarik Uang): Pengguna diminta untuk memasukkan jumlah uang yang ingin ditarik. Jumlah penarikan diperiksa apakah lebih kecil atau sama dengan saldo yang ada. Jika saldo mencukupi, maka saldo akan dikurangi dengan jumlah penarikan dan menampilkan pesan "Penarikan berhasil!". Jika saldo tidak mencukupi, maka akan ditampilkan pesan "Saldo tidak mencukupi!". o Pilihan 2 (Keluar): Perulangan akan dihentikan dengan perintah break. o Pilihan Tidak Valid: Jika pengguna memasukkan pilihan selain 1 atau 2, maka akan ditampilkan pesan "Pilihan tidak valid!".

7. Panggilan Fungsi: o Di akhir program, fungsi atm() dipanggil untuk memulai eksekusi program. Algoritma dalam Bentuk Langkah-langkah Sederhana:

    Mulai program.

    Inisialisasi saldo dengan nilai tertentu.

    Tampilkan menu pilihan kepada pengguna.

    Minta pengguna memilih opsi.

    Jika pengguna memilih "Tarik Uang": o Minta pengguna memasukkan jumlah yang ingin ditarik.
