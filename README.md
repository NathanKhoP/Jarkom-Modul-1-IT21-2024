# Jarkom-Modul-1-IT21-2024

|Nama  | NRP |
|--|--|
| Nathan Kho Pancras | 5027221002 |
| Muhammad Andrean Rizq Prasetio | 5027221052 |

## Challenges

- [Jarkom-Modul-1-IT21-2024](#jarkom-modul-1-it21-2024)
  - [Challenges](#challenges)
    - [Advance Sanity Check](#advance-sanity-check)
    - [Illegal Breakthrough](#illegal-breakthrough)
    - [Packets Barrage](#packets-barrage)
    - [FTP Login](#ftp-login)
    - [Surprise](#surprise)
    - [Corporate Branch](#corporate-branch)
    - [Malicious Code](#malicious-code)
    - [Pegawai Negeri Sebelah](#pegawai-negeri-sebelah)
    - [EZ](#ez)
    - [Rizzset](#rizzset)
    - [Gajah Terbang (Server Recon)](#gajah-terbang-server-recon)
    - [Gajah Terbang (Attacker Recon)](#gajah-terbang-attacker-recon)
    - [innerRCE](#innerrce)
    - [Baby Hengker](#baby-hengker)
    - [Adult Hengker](#adult-hengker)

### Advance Sanity Check

Yang sederhana dulu aja. (file: sanity.pcapng)

**Q1** - Apa username pengirim?

Follow > TCP Stream > eq 3

![](assets/sanity1.png)

**Q2** - Apa nama file yang dikirim?

tcp.stream.eq 4

![](assets/sanity2.png)

**Q3** - Ikuti petunjuk untuk mendapatkan pesan rahasia

Peraturan Soal Shift > cGVud29yZA== > penword

**`FLAG: JarkomIT{8uK4n_S4n1ty_b1a5A_vtvGNBv8TummwrvZPtLD4XFJTSu5BpwjTk21DruKc4us7bO67NBvgIKK}`**

### Illegal Breakthrough

Seorang full-stack developer bernama kevin sedang membuat sebuah web yang memiliki login page. Tetapi karena ia hanya digaji rendah, ia lupa untuk mengamankan web yang ia buat. Bantulah kevin untuk tracing dari jejak yang ditinggalkan oleh attacker. (file: break.pcapng)

**Q1** - Apa IP address dari korban?

![](assets/break1.png)

Korban = destination : 172.21.88.207

**Q2** - Apa port yang digunakan sebagai webserver?

1917

**Q3** - Dimana endpoint yang terdapat login?

![](assets/break2.png)

/ww1.php

**Q4** - Tools apa yang digunakan oleh attacker?

Fuzz Faster U Fool v2.1.0-dev -> package name: ffuf-v2.1.0-dev

**Q5** - Apa kredensial yang berhasil digunakan oleh attacker untuk login?

Follow > HTTP Stream > eq 1917

![alt text](assets/break3.png)

**`FLAG: JarkomIT{d34th_fr0m_th3_sky_yvEQH6jxmPAqZRbqNI0ooaGhEH1sScGTtiMPWm6vWuesQ6C74PZwWW1}`**

### Packets Barrage

Setelah membantu kevin untuk tracing attacker, sekarang bantu lagi kevin untuk mencari apa yang dilakukan oleh attacker.
File sama seperti Illegal Breakthrough.

**Q1** - Apa IP address dari attacker?

![](assets/break1.png)

Attacker = source : 172.21.80.1

**Q2** - Berapa total attempt dari bruteforce attacker?

Dikarenakan sudah menemukan un/pw di tcp.stream eq 1917, dan semua packet di HTTP stream: POST ke /ww1.php maka total attempt = 1917

**Q3** - Apa nama file yang didownload oleh attacker setelah berhasil login?

tcp.stream eq 1918 > Albatros.txt

![alt text](assets/break4.png)

**Q4** - Apa isi dari file yang disisipkan oleh attacker?

Der Rote Kampfflieger

**`FLAG: JarkomIT{th3_fly1ng_c1rcus_0f_w4r_2VpANzt61cHPI1bVJFbehI7a65StGbt2VsQwE2gMiKLkrxQEvtfL2ACE}`**

### FTP Login

Seseorang menemukan sebuah celah dalam sebuah server. Ia mencoba untuk melakukan brute force login dan ia berhasil masuk. Lakukan pemeriksaan untuk melihat apa yang dilakukan oleh orang tersebut! (file: ftplogin.pcapng)

**Q1** - 

**Q2** - 

**Q3** - 

### Surprise

Setelah mengetahui apa yang diketahui pada challenge sebelumnya, sekarang lakukan analisis untuk mengetahui apa yang sebenarnya terjadi.
File sama seperti FTP Login.

**Q1** - 

**Q2** - 

**Q3** - 

### Corporate Branch

Sebuah perusahaan IT support mendapatkan serangan oleh orang tidak dikenal. Bantulah perusahaan tersebut untuk melacak jejak yang ditinggalkan oleh attacker. (file: breach.pcapng)

**Q1** - 

**Q2** - 

**Q3** - 

### Malicious Code

Ternyata sang attacker dengan sengaja meninggalkan sesuatu untuk dibaca oleh kamu. Lihat pesan apa yang ditinggalkan attacker.
File sama seperti Corporate Breach.

**Q1** - 

**Q2** - 

**Q3** - 

### Pegawai Negeri Sebelah

Kamu seorang data analisis diminta untuk memastikan ulang data-data dari beberapa pegawai (file: rahasia.pcap)

**Q1** - 

**Q2** - 

**Q3** - 

### EZ

Aku sedang mencoba bikin chat service tapi kayanya pesannya bisa di sniffing deh? coba temukan pesannya. (file: ez.pcapng)

**Q1** - 

**Q2** - 

**Q3** - 

### Rizzset

Aku sedang bereksperimen dengan suatu tools, kamu juga bisa menggunakannya untuk menjawab soal ini (file: riset.pcapng)

**Q1** - 

**Q2** - 

**Q3** - 

### Gajah Terbang (Server Recon)

Pada perusahaan PT. +1000 Aura telah terjadi insiden yang besar, dimana seorang hengker berhasil masuk ke sistem database perusahaan tersebut, dan melakukan manipulasi sistem database mereka. Anda sebagai profesional Cyber Security Analyst ditugaskan untuk melakukan investigasi melalui log network yang berhasil tercapture! (file: gajahterbang.pcapng)

**Q1** - 

**Q2** - 

**Q3** - 

### Gajah Terbang (Attacker Recon)

Setelah berhasil menginvestigasi server yang berjalan, kamu diharuskan untuk mencari identitas dan mencari jejak apa saja yang telah dilakukan oleh penyerang! Kamu jago, pasti bisa let’s go temukan tersangkanya!!!
File sama seperti Gajah Terbang.

**Q1** - 

**Q2** - 

**Q3** - 

### innerRCE

omg, SIEM mendeteksi adanya serangan hacker yang berhasil mengupload webshell. sebagai analyst yang jago, kamu diharuskan membuat laporan insiden tersebut (file: innerRCE.pcapng)

**Q1** - 

**Q2** - 

**Q3** - 

### Baby Hengker

Pada suatu hari, ada seorang mahasiswa yang menyusup kedalam lab. mahasiswa tersebut menyalakan salah satu komputer yang ada dan mulai mengetikkan sesuatu?!?!?! bantulah mas aji menganalisa apa yang dilakukan oleh mahasiswa tersebut. (file: innerchild.pcap)

**Q1** - 

**Q2** - 

**Q3** - 

### Adult Hengker

Setelah sang mahasiswa tau passwordnya, dia akhirnya bisa masuk ke komputer dan menuliskan sesuatu di ms paint, apakah kamu tau dia menulis apa? (file: innerchild2.pcap)

**Q1** - 

**Q2** - 

**Q3** - 