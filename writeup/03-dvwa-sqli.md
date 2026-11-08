# Temuan 3: DVWA - SQL Injection

| Item | Isi |
|---|---|
| Layanan | HTTP, port 80, aplikasi DVWA |
| Tingkat risiko | Tinggi |
| CVSS | ... |
| Kategori OWASP | A03: Injection |

## Persiapan
- Buka `http://IP_TARGET/dvwa` dari Kali
- Login (kredensial bawaan DVWA ada di dokumentasi resminya)
- Atur tingkat keamanan DVWA ke **Low** untuk latihan awal

## Eksploitasi

### 1. Konfirmasi kerentanan
(Catat input yang Anda coba pada kolom User ID dan respons aplikasi.)
Screenshot: `![sqli-1](../screenshots/03-sqli-konfirmasi.png)`

### 2. Ekstraksi data
(Catat payload yang dipakai dan data apa yang berhasil ditampilkan, misalnya daftar user.)
Screenshot: `![sqli-2](../screenshots/03-sqli-data.png)`

### 3. (Opsional) Otomasi dengan sqlmap
```
sqlmap -u "URL_DENGAN_PARAMETER" --cookie="COOKIE_SESI" --batch
```
Hanya jalankan pada DVWA di lab Anda sendiri.

## Penjelasan Teknis
(Dengan kata sendiri: bagaimana input pengguna bisa mengubah query SQL, dan kenapa itu berbahaya.)

## Dampak
(Contoh: pembacaan data database tanpa izin.)

## Rekomendasi Perbaikan
- Gunakan prepared statement / parameterized query
- Validasi dan sanitasi input
- Terapkan hak akses database minimum
- Pasang WAF sebagai lapisan tambahan

## Pelajaran
- ...
