# modul6_php

1. Cookie
Pada dasarnya cookie merupakan mekanisme untuk meletakkan data pada remote
browser sehingga memudahkan penelusuran atau identifikasi user. Dapat juga dikatakan
bahwa cookie merupakan informasi dalam bentuk teks yang dipertukarkan oleh client
dan server, di mana pembuat cookie adalah pihak server.
   Session
Session memungkinkan client untuk menyimpan informasi pada server. Namun,
informasi session ini bersifat temporer, sehingga biasanya server akan menghapus session
ketika user telah meninggalkan website yang menggunakan session.
Tidak seperti cookie, session tersimpan di server, dengan demikian, client tidak memiliki
akses untuk mendapatkan informasi session.

2. Menghapus Cookie
Penghapusan cookie dilakukan dengan cara mengirimkan nama cookie sama tetapi
nilainya kosong. Untuk langkah yang lebih baik, tambahkan argumen opsional dengan nilai
waktu yang telah lewat.
    Menghapus session
    Untuk menghapus data session, Anda bisa menggunakan konstruksi bahasa unset() atau
fungsi session_destroy().

3. Menghapus cookie
<html>
<head>
<title>Hapus Cookie</title>
</head>
<body>
<?php
setcookie('nama_cookie', 'nilai_cookie');
if (isset($_COOKIE['nama_cookie'])) {
echo 'cookie di-set <br />';
// Menghapus cookie, dengan masa berlaku 1 jam yang lalu setcookie('nama_cookie',
'', time() - 1 * 3600);
echo 'cookie dihapus';
} else {
echo 'unset';
} ?>
<p>
Tekan Refresh (F5);
</body>
</html>
Menghapus session
<html>
<head>
<title>Hapus Session</title>
</head>
<body>
<?php
// Inisialisasi data session
session_start();
// Set session jika belum ada
if (isset($_SESSION['test'])) {
// Hapus session test

unset($_SESSION['test']);
echo 'session dihapus';
} else {
echo 'unset';
// Mencetak semua elemen session
print_r($_SESSION);
}
?>
<p>
Tekan Refresh (F5);
</body>
</html>

Latihan 1
![modul6_latihan1](https://user-images.githubusercontent.com/41880161/53564033-5f2ebb80-3b88-11e9-9913-966b4878c646.JPG)
Latihan 2
![modul6_latihan2](https://user-images.githubusercontent.com/41880161/53564041-60f87f00-3b88-11e9-9e8f-a04f925ec714.JPG)
Latihan 3
![modul6_latihan3](https://user-images.githubusercontent.com/41880161/53564040-60f87f00-3b88-11e9-98e3-1eab703b9c89.JPG)
Latihan 4
![modul6_latihan4](https://user-images.githubusercontent.com/41880161/53564039-605fe880-3b88-11e9-8d4a-77865991ea69.JPG)
Latihan 5
![modul6_latihan5](https://user-images.githubusercontent.com/41880161/53564038-605fe880-3b88-11e9-867d-8eed15281750.JPG)
Latihan 6
![modul6_latihan6](https://user-images.githubusercontent.com/41880161/53564037-605fe880-3b88-11e9-9f8a-d7332b3eda90.JPG)
Latihan 7
![modul6_latihan7](https://user-images.githubusercontent.com/41880161/53564036-5fc75200-3b88-11e9-98ac-232ed052e2fe.JPG)
Praktikum
![modul6_prak1](https://user-images.githubusercontent.com/41880161/53564035-5fc75200-3b88-11e9-8e6a-fd750ad08c18.JPG)
![modul6_prak2](https://user-images.githubusercontent.com/41880161/53564034-5fc75200-3b88-11e9-9af8-5b10e88a398c.JPG)
