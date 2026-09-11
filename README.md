# MinPro-DDP
Nama : Graceilla Tifunny Glory Hutagalung

NIM : 079

Kelas : B

<img width="948" height="1240" alt="Flowchart manajemen buku" src="https://github.com/user-attachments/assets/912b5fca-0339-4c89-b725-08b9bc8d3479" />

PENJELASAN ALUR FLOWCHART:

1. Awal program
   program dimulai dengan langsung menampilkan daftar pilihan tugas. Tujuannya supaya langsung tahu apa saja yang bisa dikerjakan. setelah memilih, program tidak langsung menjalankan perintah, tapi meengecek dulu apakah angka yang di masukkan itu benar-benar ada di daftar pilihan. kalau salah ketik atau masuk angka lain, program akan memberi tahu dan pengembalikan ke menu, jadi program tetap berjalan aman, tidak berhenti atau rusak. kalau pilihannya benar, baru bisa lanjut ke bagian yang diinginkan

2. Menu 1 : Tambah Buku
   Bagian ini berfungsi untuk memasukkan catatan baru. kita diminta untuk mengisi informasi yang dibutuhkan, lalu data itu langsung disimpan ke dalam daftar. sebelum kembali ke menu, program memberitahu kalau proses penyimpanan sudah berhasil, supaya kamu yakin data sudah masuk.

3. Menu 2 : Lihat Semua Buku
   Sebelum menampilkan apapun, program mengecek dulu apakh di dalam daftar sudah ada catatan atau masih kosong? Kalau belum ada, program akan kasih tahu supaya tidak bingung. Kalau sudah ada, semua data ditampilkan secara rapi dan berurutan. setelah selesai dilihat, otomatis kembali ke menu utama.

4. Menu 3 : Ubah Data Buku
   Di sini program mulai memastikan hal-hal penting, pertama apakah memang sudah ada data yang bisa di ubah? kalau belum ada, langsung kembali. kalau ada, akan diminta menyebutkan nomor urut buku yang ingin diperbaiki. Lalu dicek lagi apakah nomor yang udah diberikan itu benar-benar ada di daftar? Kalau salah nomor, langsung diberi tahu. kalau benar, baru kamu diminta mengisi data yang baru, data lama diganti dengan yang baru, lalu disimpan dan dikonfirmasi sudah berhasil.

5. Menu 4 : Hapus Buku
   Cara kerjanya mirip dengan ubah data, dicek dulu apakah ada catatan, lalu nomor yang diminta keberadaanya dipastikan. Kalau semuanya benar, data itu langsung dihapus dari daftar, lalu dikonfirkan. kalau nomornya salah atau belum ada data, program akan memberi tahu ada kembali ke menu.

6. Menu 5 : Keluar
   Kalau memilih ini, program tidak akan kembali lagi ke menu. program menutup semua proses, memberi pesan selesai, lalu berhenti berjalan sepenuhnya.

   Program ini dirancang supaya berulang terus, selesai satu slide, balik ke menu, siap dikerjakan lagi, sampai bisa memutuskan berhenti. semua langkahnya selalu ada pengecekkan dulu supaya tidak ada data yang salah masuk, tidak ada data yang salah masuk, tidak ada ubah atau hapus yang gagal, dan program tetap aman dipakai.

SCREENSHOT OUTPUT :

<img width="960" height="600" alt="Screenshot 2026-09-11 202037" src="https://github.com/user-attachments/assets/50277ac5-6639-43a4-84a7-fa71d57dea9b" />

<img width="960" height="600" alt="Screenshot 2026-09-11 202112" src="https://github.com/user-attachments/assets/a7070da9-8c23-4e16-aa54-1502eac23eff" />

<img width="960" height="600" alt="Screenshot 2026-09-11 202127" src="https://github.com/user-attachments/assets/fd38f77d-af70-437d-bb92-2f7317268836" />

<img width="960" height="600" alt="Screenshot 2026-09-11 202142" src="https://github.com/user-attachments/assets/40a3f171-c557-47a2-a039-ec9b20d19ef0" />

PENJELASAN CODE PROGRAM PYTHON :

1. Tempat Simpan Data
   daftar_buku = []
   Ini adalah tempat penyimpanan utama, berbentuk daftar kosong. nanti semua data buku yang sudah dimasukkan akan tersimpan di sini. bentuknya pakai "list" supaya bisa ditambah, dilihat, diubah, maupun dihapus isinya. setiap satu buku disimpan berpasangan (judul sama halamannya), pakai bentuk "tuple" agar datanya tetap utuh satu pasang.

2. Perulangan Menu
   while True:
   Bagian ini yang bikin program berjalan berulang-ulang terus. artinya "kerjakan apa yang ada di dalam sini, berulang tanpa berhenti, sampai ada perintah berhenti". jadi setiap selesai satu pekerjaan, menu akan muncul lagi secara otomatis, seperti di flowchart sampai pilih angka 5 untuk keluar.

3. Tampilan Dan Pilihan
   print("===== MENU DAFTAR BUKU =====")
   pilihan = input("Masukkan pilihan angka [1-5]:")
   Di sini program menampilkan semua pilihan yang bisa dikerjakan, lalu menunggu untuk mengetik angka. angka yang diketik disimpan sementara buat diperiksa selanjutnya.

4. Cek Pilihan Benar Atau Salah
   if pilihan not in ["1","2","3","4","5",]:
      print("Pilihan tidak ada! Coba lagi.")
      continue
   Bagian ini pengaman penting. program langsung mengecek apakah yang diketik itu salah satu dari angka 1-5 atau huruf, kalau salah program langsung kasih tahu, lalu continue artinya, langsung balik ke menu awal lagi, jangan lanjut ke bawah. jadi program tidak akan rusak atau berhenti, tetap aman.

5. Bagian Tambah Buku
   if pilihan == "1":
      nama = input("...")
      daftar_buku.append((nama, hal))
      print("Berhasil ditambahkan!")
   Jika pilih angka 1, program akan minta isi judul buku dan halaman buku. lalu data itu digabung jadin satu pasang (nama,halamman), dimasukkan ke dalam daftar pakai append artinya "tambahkan ke bagian paling belakang daftar". terus dikasih tahu sudah berhasil masuk.

6. Bagian Lihat Semua Buku
   elif pilihan == "2":
      if len(daftar_buku) == 0:
          print("Belum ada catatan buku.")
    else:
       for i, buku in enumerate(daftar_buku, start=1):
           print(f"{i}. Judul: {buku[0]} | Halaman: {buku[1]}")
   pertama dicek dulu "len" artinya jumlah isinya. kalau jumlah nol = kosong, kasih tahu belum ada data. kalau sudah ada, diproses satu-satu pakai "for" artinya ulangi untuk setiap isi yang ada di dalam daftar. "enumerate" fungsinya memberi nomor urut otomatis mulai dari 1, supaya tampilannya rapi. buku[0] itu judul, buku[1] itu angka halaman.

7. Bagian Ubah Data Buku
   elif pilihan == "3":
      if len(daftar_buku) == 0:
         print("Belum ada data buku.")
      else:
         nomor = int(input(".."))-1
         if 0 <= nomor < len(daftar_buku):
         daftar_buku[nomor] = (nama_baru, hal_baru)
          print("Berhasil diubah!")
       else:
          print("Nomor buku tidak ada!")
  bagian ini dicek dulu ada data atau tidak, kalau kosong langsung balik. kalau ada, makan akan diminta masukin nomor urut dan dikurangi 1 karena hitungan komputer mulai dari nol. terus dicek lagi apakah nomor itu masuk batas yang benar, kalau masuk data lama diganti langsung dengan yang baru di posisi nomor itu. kalau nomornya kebesaran atau kurang, langsung dikasih tahu tidak ada.

8. Bagian Hapus Buku
   elif pilihan == "4":
     if len(daftar_buku) == 0:
        print("Belum ada data buku.")
     else:
       nomor = int(input(".."))-1
       if 0 <= nomor < len(daftar_buku):
          daftar_buku.pop(nomor)
          print("Berhasil dihapus!")
     else:
          print("Nomor buku tidak ada!")
   Cara kerjanya mirip ubah data cek dulu ada isinya atau tidak, lalu pastikan nomornya benar. kalau semua sudah oke, pakai perintah "pop" artinya keluarkan dan hapus data yang ada di posisi nomor ini". setelah dihapus, daftar otomaatis merapikan nomor urutnya sendiri.

9. Bagian Keluar Dari Program
    elif pilihan == "5":
       print("Program selasai. Terima kasih!")
       break
   Bagian ini kalau pilih angka 5, tampil pesan penutup, lalu "break" artinya berhenti perulangan "while True" di atas, berhenti sepenuhnya. Program berakhir, tidak balik ke menu lagi.

Program ini bekerja dengan pola, simpan data sementara, tampilkan pilihan, cek dulu sebelum kerjakan, jalankan perintah, lalu ulangi lagi. semua perubahan data langsung tersimpan di dalam daftar, dan setiap langkah selalu ada pengecekkan supaya tidak terjadi kesalahan atau kerusakan pada program.
