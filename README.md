# LabPyUAS

*Nama   :Maulana Malik Ibrahim*

*Nim    :312410185*

*Kelas  :24.A.2*

*Matkul :Bahasa Pemrograman*

**Project Python: Sistem Kasir Sederha**

    #Program Kasir Sederhana
    def tampilkan_menu():
        print("=== Menu Kasir ===")
        print("1. Tambah Item")
        print("2. Tampilkan Struk")
        print("3. Keluar")
        
    def tambah_item(keranjang):
        nama_item = input("Masukkan nama item: ")
        harga_item = float(input("Masukkan harga item: "))
        jumlah_item = int(input("Masukkan jumlah item: "))
     #Menambahkan item ke dalam keranjang
     keranjang[nama_item] = {
           'harga': harga_item,
           'jumlah': jumlah_item
       }
      print(f"Item '{nama_item}' berhasil ditambahkan ke keranjang.")
      
     def tampilkan_struk(keranjang):
         print("\n=== Struk Pembayaran ===")
         total = 0
         for item, detail in keranjang.items():
              subtotal = detail['harga'] * detail['jumlah']
              total += subtotal
              print(f"{item} - Harga: {detail['harga']} x Jumlah: {detail['jumlah']} = Subtotal: {subtotal}")

               
         print(f"\nTotal Pembayaran: {total}")
         print("========================")

     def main():
        keranjang = {}
        while True:
           tampilkan_menu()
           pilihan = input("Pilih menu (1/2/3): ")

            if pilihan == '1':
               tambah_item(keranjang)
            elif pilihan == '2':
               tampilkan_struk(keranjang)
            elif pilihan == '3':
               print("Terima kasih! Sampai jumpa.")
               break
            else:
               print("Pilihan tidak valid! Silakan coba lagi.")

    if __name__ == "__main__":
      main()

**Berikut ini adalah Penjelasannya**
1. **Fungsi** `tampilkan_menu():`
  - Menampilkan menu pilihan kepada pengguna. Pengguna dapat memilih untuk menambah item, menampilkan struk, atau keluar dari program.
2. **Fungsi** `tambah_item(keranjang):`
  - Meminta pengguna untuk memasukkan nama item, harga, dan jumlah item.
  - Menyimpan informasi item dalam dictionary `keranjang`, di mana nama item adalah kunci dan detail (harga dan jumlah) adalah nilai.
3. **Fungsi** `tampilkan_struk(keranjang):`
  - Menghitung total harga dari semua item dalam keranjang.
  - Menampilkan setiap item beserta harga, jumlah, dan subtotal.
  - Menampilkan total pembayaran di akhir.
4. **Fungsi** `main():`
 - Menginisialisasi keranjang sebagai dictionary kosong.
 - Menggunakan loop `while` untuk terus menampilkan menu hingga pengguna memilih untuk keluar.
 - Memanggil fungsi yang sesuai berdasarkan pilihan pengguna.

**Hasil Dari Code Diatas**
Setelah menjalankan program, pengguna dapat:

 - Menambahkan item ke dalam keranjang belanja dengan memasukkan nama, harga, dan jumlah.
 - Melihat struk pembayaran yang menunjukkan semua item yang dibeli, subtotal untuk setiap item, dan total pembayaran.
 - Keluar dari program dengan memilih opsi yang sesuai.
