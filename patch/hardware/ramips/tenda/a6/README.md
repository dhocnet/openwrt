PETUNJUK: A6.dts
----------------
Salin A6.dts ke **<openwrt_root_dir>/target/linux/ramips/dts**
```
$ cp A6.dts <folder_root_openwrt>/target/linux/ramips/dts
```

CATATAN: A6-orig.patch
-----------------
File patch sudah cukup tua, lakukan copy-paste manual ke setiap file target untuk mendapatkan tingkat keberhasilan yang tinggi.

INFO SETELAH MELAKUKAN PATCH
----------------------------
Setelah file-file target berhasil ditambal dan pilihan Tenda A6 tidak juga terlihat, 
hapus semua isi direktori *tmp* dengan perintah:
```
<folder_root_openwrt>$ rm -rf tmp/*
```

Lalu jalankan lagi perintah:
```
<folder_root_openwrt>$ make menuconfig
```
UPDATE: A6-trunk.patch
----------------------
Terdapat perubahan struktur/ kontruksi dari file **<openwrt_root_dir>/target/linux/ramips/Makefile** dengan ditambahkannya file **<openwrt_root_dir>/target/linux/ramips/image/rt305x.mk** sebagai *profile* untuk masing-masing hardware.

Patch terbaru dapat dilihat pada file: [A6-trunk.patch](./A6-trunk.patch).
