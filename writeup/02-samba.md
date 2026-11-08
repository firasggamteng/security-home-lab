# Temuan 2: Samba usermap_script

| Item | Isi |
|---|---|
| Layanan | SMB (Samba), port 139/445 |
| Versi | (isi dari hasil Nmap) |
| Tingkat risiko | Kritis |
| CVSS | ... (cari di NVD) |
| Referensi | (isi nomor CVE dari hasil pencarian Anda) |

## Cara Menemukan
(Jelaskan: versi Samba dari Nmap, lalu pencarian kerentanan di `searchsploit` atau Metasploit.)

```
searchsploit samba
```
Screenshot: `![searchsploit](../screenshots/02-searchsploit.png)`

## Eksploitasi

### Dengan Metasploit
```
msfconsole
search usermap_script
use <nama modul>
set RHOSTS IP_TARGET
run
```
Hasil / screenshot: `![exploit](../screenshots/02-exploit.png)`

Bukti akses: `![bukti](../screenshots/02-whoami.png)`

## Penjelasan Teknis
(Dengan kata sendiri: bagaimana opsi konfigurasi "username map script" dapat disalahgunakan.)

## Dampak
(Contoh: eksekusi perintah jarak jauh tanpa autentikasi.)

## Rekomendasi Perbaikan
- Perbarui Samba ke versi yang sudah ditambal
- Nonaktifkan opsi konfigurasi yang tidak diperlukan
- Batasi akses SMB hanya dari jaringan tepercaya

## Pelajaran
- ...
