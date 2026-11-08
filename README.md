# Security Home Lab: Mini Penetration Test Metasploitable

Proyek pembelajaran cybersecurity: penetration test terhadap mesin virtual **Metasploitable** di lingkungan lab terisolasi milik sendiri, lengkap dengan dokumentasi dan laporan temuan.

> **Catatan etika:** Semua pengujian dilakukan hanya pada VM di laptop saya sendiri, dalam jaringan terisolasi. Jangan gunakan teknik ini pada sistem tanpa izin tertulis.

## Tujuan

 
## Tools
-VirtualBox
-kali Linux (Penyerang)
-metasploitable (target)

- Mempelajari alur penetration test: recon -> enumerasi -> eksploitasi -> pelaporan
- Melatih dokumentasi teknis dan penulisan laporan temuan
- Menjadi fondasi untuk pengembangan lab berikutnya (Wazuh, pfSense, Active Directory)

## Lingkungan Lab

| Komponen | Detail |
|---|---|
| Hypervisor | VirtualBox (versi: ...) |
| Mesin penyerang | Kali Linux (versi: ...), IP: ... |
| Mesin target | Metasploitable (versi: 2), IP: ... |
| Jaringan | Host-Only / NAT Network (pilih salah satu), subnet: ... |

Topologi:

![Topologi lab](docs/topologi.png)

## Ruang Lingkup
- **Target:** satu VM Metasploitable (IP: ...)
- **Dalam lingkup:** scanning, enumerasi, eksploitasi layanan yang rentan
- **Di luar lingkup:** semua sistem selain VM lab ini

## Metodologi
1. Reconnaissance (Nmap)
2. Enumerasi layanan
3. Eksploitasi
4. Dokumentasi bukti
5. Rekomendasi perbaikan

## Daftar Writeup

| No | Judul | Status |
|---|---|---|
| 00 | [Reconnaissance dengan Nmap](writeups/00-recon-nmap.md) | [ ] |
| 01 | [vsftpd 2.3.4 Backdoor](writeups/01-vsftpd.md) | [ ] |
| 02 | [Samba usermap_script](writeups/02-samba.md) | [ ] |
| 03 | [DVWA: SQL Injection](writeups/03-dvwa-sqli.md) | [ ] |

Ringkasan semua temuan: [laporan-ringkasan.md](laporan-ringkasan.md)


