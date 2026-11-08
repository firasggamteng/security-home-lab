# Laporan Ringkasan Penetration Test

## Informasi Umum

| Item | Isi |
|---|---|
| Tanggal pengujian | ... |
| Penguji | (nama Anda) |
| Target | Metasploitable 2, IP ... |
| Lingkungan | Lab virtual terisolasi milik sendiri |
| Tools | Nmap, Metasploit Framework, (tambahkan) |

## Ringkasan Eksekutif
(Tulis 3-5 kalimat dalam bahasa awam: apa yang diuji, berapa temuan, seberapa serius, dan apa saran utamanya. Contoh: "Pengujian menemukan 3 kerentanan, 2 di antaranya berisiko kritis dan memungkinkan penyerang mengambil alih sistem sepenuhnya. Disarankan memperbarui layanan dan menonaktifkan port yang tidak diperlukan.")

## Tabel Temuan

| ID | Temuan | Layanan / Port | Risiko | CVSS | Status Eksploitasi | Writeup |
|---|---|---|---|---|---|---|
| F-01 | vsftpd 2.3.4 Backdoor | FTP / 21 | Kritis | ... | Berhasil | [01](writeups/01-vsftpd.md) |
| F-02 | Samba usermap_script | SMB / 139, 445 | Kritis | ... | Berhasil | [02](writeups/02-samba.md) |
| F-03 | SQL Injection pada DVWA | HTTP / 80 | Tinggi | ... | Berhasil | [03](writeups/03-dvwa-sqli.md) |

## Skala Risiko yang Dipakai
- **Kritis (CVSS 9.0-10.0):** pengambilalihan sistem tanpa autentikasi
- **Tinggi (7.0-8.9):** kebocoran data atau akses signifikan
- **Sedang (4.0-6.9):** dampak terbatas atau butuh kondisi tertentu
- **Rendah (0.1-3.9):** dampak kecil

## Rekomendasi Prioritas
1. (Contoh) Perbarui atau hapus layanan yang rentan
2. (Contoh) Tutup port yang tidak dipakai dengan firewall
3. (Contoh) Terapkan prinsip least privilege
4. (Contoh) Aktifkan logging dan pemantauan

## Pemetaan MITRE ATT&CK (opsional, nilai tambah)

| Teknik | ID ATT&CK | Dipakai pada |
|---|---|---|
| Active Scanning | T1595 | Recon Nmap |
| Exploit Public-Facing Application | T1190 | F-01, F-02, F-03 |

## Kesimpulan
(2-3 kalimat: apa yang berhasil, apa yang dipelajari, rencana berikutnya.)
