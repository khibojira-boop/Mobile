import 'dart:io';

void main() {
  // daftar menu (nama dan harga)
  List<List<dynamic>> menu = [
    ['Nasi Padang', 25000],
    ['Sate Ayam', 20000],
    ['Bakso', 15000],
    ['Soto Ayam', 18000],
    ['Nasi Uduk', 12000],
    ['Es Teh Manis', 5000],
    ['Jus Alpukat', 12000],
    ['Es Campur', 10000],
    ['Air Mineral', 4000],
    ['Kopi Hitam', 8000],
  ];

  // list untuk menyimpan pesanan
  List<List<dynamic>> pesanan = [];

  print("=== Selamat Datang di Warung Nusantara ===");

  while (true) {
    num totalHarga = 0;

    // pelanggan memilih menu berulang sampai tekan 0
    while (true) {
      print("\n--- Daftar Menu ---");
      for (var i = 0; i < menu.length; i++) {
        print("${i + 1}. ${menu[i][0]} - Rp${menu[i][1]}");
      }
      print("0. Selesai memilih");

      stdout.write("Pilih nomor menu: ");
      String? input = stdin.readLineSync();

      if (input == '0') break;

      int? pilih = int.tryParse(input ?? "");
      if (pilih != null && pilih >= 1 && pilih <= menu.length) {
        pesanan.add(menu[pilih - 1]);
        print(">> ${menu[pilih - 1][0]} berhasil ditambahkan!");
      } else {
        print("Nomor menu tidak valid!");
      }
    }

    // tampilkan rincian pesanan
    print("\n=== Rincian Pesanan ===");
    for (var item in pesanan) {
      print("- ${item[0]} (Rp${item[1]})");
      totalHarga += item[1];
    }
    print("Jumlah item: ${pesanan.length}");
    print("Total harga: Rp$totalHarga");
    print("========================");

    // tanya apakah mau pesan lagi
    stdout.write("Apakah ingin memilih menu lagi? (1 = Ya, 2 = Tidak): ");
    String? ulang = stdin.readLineSync();

    if (ulang == '2') {
      print("Terima kasih sudah berkunjung!");
      break;
    }
  }
}
