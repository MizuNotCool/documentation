---
judul: Kekekalan (ABRoot) - OS Vanila
deskripsi: Cari tahu cara menggunakan ABRoot.
---

# Kekekalan (`abroot`)

`abroot` adalah utilitas yang menyediakan kekekalan dan atomisitas lengkap dengan melakukan transaksi antara 2 partisi root (A⟺B), ini juga memungkinkan untuk transaksi sesuai permintaan melalui shell transaksional.

## Bagaimana itu bekerja

Sistem file Linux adalah struktur file hierarkis yang berisi root dan direktori lainnya. 
Root adalah direktori hierarki utama yang berisi semua partisi lain. 
Dalam sistem file yang tidak dapat diubah, partisi root hanya dapat dibaca, mencegah penginstalan paket penting, seperti driver di host.

`abroot` memungkinkan Anda menginstal modul kernel, driver, dan paket penting lainnya tanpa mengorbankan kekekalan sistem file. 

Ketika sebuah perintah dieksekusi di `abroot`, sebuah transaksi dimulai di shell transaksional di partisi root kedua. Jika transaksi berhasil, perubahan akan diterapkan menggunakan hamparan dan disinkronkan dengan root saat ini saat reboot. Jika transaksi gagal, tidak ada perubahan yang diterapkan (karena properti yang dikenal sebagai atomisitas). `abroot` juga memungkinkan transaksi on-demand menggunakan perintah `abroot shell`.

Instalasi Vanilla OS membuat partisi root dan boot untuk kedua status (20GB per partisi root) karena ini adalah persyaratan untuk `abroot`.

## Keadaan

`abroot` memiliki dua keadaan - sekarang dan masa depan. Saat Anda menginstal Vanilla OS untuk pertama kalinya, status saat ini adalah A. Saat Anda memulai ulang sistem, status secara otomatis beralih ke B. Saat Anda menginstal paket menggunakan `abroot`, paket tersebut akan diinstal di partisi root yang akan datang dan disinkronkan dengan partisi root saat ini setelah memulai ulang.

## Pembaruan

`abroot` memberi daya pada utilitas `vso` yang memungkinkan pembaruan otomatis pintar dan pemasangan pembaruan di latar belakang di partisi root di masa mendatang, sehingga menghemat waktu karena pembaruan offline selama reboot tidak diperlukan.

## Penamaan

Nama ABRoot merujuk pada dua partisi root yang bertransaksi A dan B (A⟺B).

## Pemakaian

- [Manpage](/docs/ABRoot/manpage)
