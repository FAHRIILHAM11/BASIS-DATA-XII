## 1. Gunakan perintah `DESC pegawai;` untuk mendapatkan struktur tabel.
**STRUKTUR "**
```SQL
CREATE TABLE pegawai (
-> NIP INT PRIMARY KEY,
-> NDep VARCHAR(255) NOT NULL,
-> NBlk VARCHAR(255),
-> JK ENUM('L', 'P') NOT NULL,
-> Alamat TEXT NOT NULL,
-> Telp VARCHAR(255) NOT NULL,
Jabatan ENUM('Manager', 'Supervisor', 'Staff'),
    Gaji BIGINT NOT NULL,
    NoCab VARCHAR(255) NOT NULL
);

```

**PENJELASAN :**


**HASIL :**
![[asset/Capture1.PNG]]
## 2. Gunakan perintah `SELECT * FROM pegawai;` untuk mendapatkan data.
**STRUKTUR "**
```SQL
INSERT INTO pegawai (NIP, NDep, NBlk, JK, Alamat, Telp, Jabatan, Gaji, NoCab) VALUES 
-> (10107, 'Emya', 'Salsalina', 'P', 'JL. Suci 78 Bandung', '022-555768', 'Manager', 5250000, 'C101'), 
-> (10246, 'Dian', 'Anggraini', 'P', 'JL. Mawar 5 Semarang', '024-555102', 'Supervisor', 2750000, 'C103'), 
-> (10324, 'Martin', 'Susanto', 'L', 'JL. Bima 51 Jakarta', '021-555785', 'Staff', 1750000, 'C102'), 
-> (10252, 'Antoni', 'Irawan', 'L', 'JL. A. Yani 15 Jakarta', '021-555888', 'Manager', 5750000, 'C102'), 
-> (10176, 'Diah', 'Wahyuni', 'P', 'JL. Maluku 56 Bandung', '022-555934', 'Supervisor', 2500000, 'C101'), 
-> (10314, 'Ayu', 'Rahmadani', 'P', 'JL. Malaka 342 Jakarta', '021-555098', 'Supervisor', 1950000, 'C102'), 
-> (10307, 'Erik', 'Adrian', 'L', 'JL. Manggis 5 Semarang', '024-555236', 'Manager', 6250000, 'C103'), 
-> (10415, 'Susan', 'Sumantri', 'P', 'JL. Pahlawan 24 Surabaya', '031-555120', '', 2650000, 'C104'), 
-> (10407, 'Rio', 'Gunawan', 'L', 'JL. Melati 356 Surabaya', '031-555231', 'Staff', 1725000, 'C104');
```

**PENJELASAN :**
- **`INSERT INTO pegawai`**:
    - Menunjukkan bahwa Anda akan menambahkan data ke tabel bernama `pegawai`.
    
- **`(NIP, NDep, NBlk, JK, Alamat, Telp, Jabatan, Gaji, NoCab)`**:
    - Ini adalah daftar kolom dalam tabel `pegawai` yang akan diisi dengan data. Kolom-kolom ini adalah:
        - `NIP` (Nomor Induk Pegawai)
        - `NDep` (Nama Depan)
        - `NBlk` (Nama Belakang)
        - `JK` (Jenis Kelamin)
        - `Alamat` (Alamat)
        - `Telp` (Telepon)
        - `Jabatan` (Jabatan)
        - `Gaji` (Gaji)
        - `NoCab` (Nomor Cabang)
        
- **`VALUES`**:
    - Menunjukkan data yang akan dimasukkan ke dalam tabel. Data untuk setiap baris harus sesuai dengan urutan kolom yang disebutkan sebelumnya.
    
- **Data yang Dimasukkan**:
    - Baris pertama:
        - NIP: `10107`
        - NDep: `'Emya'`
        - NBlk: `'Salsalina'`
        - JK: `'P'` (Perempuan)
        - Alamat: `'JL. Suci 78 Bandung'`
        - Telp: `'022-555768'`
        - Jabatan: `'Manager'`
        - Gaji: `5250000`
        - NoCab: `'C101'`
    - Baris kedua dan seterusnya mengikuti pola yang sama, dengan data yang berbeda.
    
- **Catatan**:
    - Pada baris `10415` untuk `Susan Sumantri`, kolom `Jabatan` tidak diisi (`''`), yang bisa menyebabkan masalah jika kolom `Jabatan` adalah `ENUM` dan tidak termasuk nilai kosong. Pastikan kolom `Jabatan` memiliki nilai yang valid.
    - Jika ada nilai kosong (`''`) dalam kolom `Jabatan`, Anda mungkin ingin memperbarui baris ini dengan jabatan yang sesuai, seperti `'Staff'`, atau menyesuaikan schema tabel untuk mengizinkan nilai kosong jika perlu.

**HASIL :**
![[asset/Capture2.PNG]]