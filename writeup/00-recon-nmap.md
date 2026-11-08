# 00 - Reconnaissance dengan Nmap

## Tujuan
Mengidentifikasi host aktif, port terbuka, dan versi layanan pada target.

## Lingkungan
- Penyerang: Kali Linux, IP ...
- Target: Metasploitable, IP ...

## Langkah

### 1. Pastikan target terjangkau
```
ping -c 3 IP_TARGET
```
Hasil / screenshot: `![ping](../screenshots/00-ping.png)`

### 2. Scan port dan versi layanan
```
nmap -sV -sC -p- IP_TARGET -oN nmap-full.txt
```
Penjelasan opsi:
- `-sV` : deteksi versi layanan
- `-sC` : jalankan script default
- `-p-` : scan semua 65535 port
- `-oN` : simpan hasil ke file

Hasil / screenshot: `![nmap](../screenshots/00-nmap.png)`

## Hasil

| Port | Layanan | Versi | Catatan |
|---|---|---|---|
| 21 | ftp | vsftpd 2.3.4 | (versi lama, cek kerentanan) |
| 22 | ssh | ... | |
| 80 | http | ... | |
| 139/445 | smb | Samba ... | |
| ... | ... | ... | |

## Analisis
(Tulis dengan kata sendiri: layanan mana yang paling mencurigakan dan kenapa. Cari versi layanan di Exploit-DB atau CVE database untuk menentukan target eksploitasi.)

## Pelajaran
- ...
