---
judul: Dokumentasi Vanilla OS
description: Cari tahu cara menggunakan Vanilla OS dan semua alat serta pengaturannya.
---

# Vanilla OS

Rasakan pengalaman Vanilla GNOME di Ubuntu dengan sedikit bumbu.

**Halaman ini adalah dokumentasi resmi untuk komponen Vanilla OS.**\
Lihat [**Handbook**](https://handbook.vanillaos.org) untuk panduan dan tutorial yang ditulis pengguna.

## FAQ

Jawaban atas pertanyaan yang paling sering ditanyakan tentang Vanilla OS.

- **Mengapa Distribusi baru?**\
  Vanilla OS muncul dari kebutuhan akan distribusi Linux berbasis Ubuntu 
  yang akan menyediakan vanilla GNOME tanpa perubahan apa pun pada pengalaman pengguna.  
  Kemudian, cakupannya diperluas untuk bereksperimen dengan beberapa alat dan 
  teknologi, seperti ABRoot dan Apx (subsistem 
  berbasis Distrobox).

- **Apakah ini menggunakan OSTree?**\
  Tidak. Vanilla OS mencapai kekekalan melalui [`ABRoot` (https://github.com/Vanilla-OS/ABRoot) [sebelumnya dicapai melalui `almost`]. Penggunaan OSTree mungkin akan dipertimbangkan di masa mendatang.

  Kami menulis utilitas `almost` untuk Kekekalan Sesuai Permintaan berdasarkan
  atribut kekekalan file. Pendekatan ini bekerja pada semua skema partisi/sistem file.
  
  Kami memperkenalkan utilitas baru [ABRoot](https://github.com/Vanilla-OS/ABRoot) menggantikan utilitas `almost` untuk menyediakan kekekalan dan atomisitas penuh, dengan bertransaksi antara 2 partisi akar (A⟺B). Ini juga memungkinkan transaksi berdasarkan permintaan melalui shell transaksional.
  
- **Rilis Bergulir?**\
  Tidak. Vanilla OS adalah rilis titik dan mengikuti siklus rilis Ubuntu.

## Panduan Pengguna

- **[Instalasi](https://handbook.vanillaos.org/2022/11/05/installation.html)**
- **[Penyiapan Pertama](https://handbook.vanillaos.org/2022/11/18/first-setup.html)**
- **[Pembaruan](https://handbook.vanillaos.org/2022/12/10/updates.html)**
- **[Panduan lainnya](https://handbook.vanillaos.org/)**

## Dokumen Komponen Inti

- **[Apx](/docs/apx)**\
  adalah manajer paket berbasis kontainer yang memungkinkan penginstalan paket dari distribusi lain di lingkungan sandbox.

- **[ABRoot](/docs/ABRoot)**\
  adalah utilitas yang memungkinkan transaksi atomik penuh antara 2 partisi root (A⟺B).

- **[VSO](/docs/vso)**\
  adalah utilitas yang memungkinkan Anda melakukan tugas pemeliharaan pada instalasi Vanilla OS Anda.

- ~~**[Almost](/docs/almost)**~~\
  ~~memungkinkan Anda untuk membuat sistem Anda tidak dapat diubah hanya dengan mengaktifkan atribut i dari file.~~

## Berkontribusi

- **[Packaging](/docs/packaging)**\
  aplikasi untuk vanilla OS memerlukan beberapa pertimbangan dan panduan untuk diikuti.
