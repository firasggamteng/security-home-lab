# Temuan 1: vsftpd 2.3.4 Backdoor

| Item | Isi |
|---|---|
| Layanan | FTP, port 21 |
| Versi | vsftpd 2.3.4 |
| Tingkat risiko | Kritis |
| CVSS | ... (cari di NVD) |
| Referensi | (isi nomor CVE dari hasil pencarian Anda) |

## Cara Menemukan
Ditemukan dari hasil `nmap -sV` pada [00-recon-nmap.md](00-recon-nmap.md). (Jelaskan versi yang terdeteksi.)

## Eksploitasi

### Dengan Metasploit
```
msfconsole
search vsftpd
use <nama modul>
set RHOSTS IP_TARGET
run
```
Hasil / screenshot: `![exploit](../screenshots/01-exploit.png)`

Bukti akses (contoh: output `whoami` dan `id`): `![bukti](../screenshots/01-whoami.png)`

### Secara manual (tantangan lanjutan, sangat disarankan)
(Pelajari cara kerja backdoor ini: bagaimana ia dipicu dan di port berapa shell terbuka. Coba ulangi tanpa Metasploit menggunakan `nc` atau `telnet`, lalu catat langkahnya di sini.)

## Penjelasan Teknis
(Dengan kata sendiri: kenapa versi ini rentan dan apa yang terjadi di balik layar.)

## Dampak
(Contoh: penyerang mendapatkan shell dengan hak akses tertinggi tanpa autentikasi.)

## Rekomendasi Perbaikan
- Perbarui vsftpd ke versi yang aman
- Batasi akses port 21 dengan firewall
- Gunakan SFTP sebagai pengganti FTP

## Pelajaran
- ...
