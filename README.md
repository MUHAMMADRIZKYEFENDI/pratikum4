# pratikum4
```
-- Create the table 'pegawai'
CREATE TABLE pegawai (
    idpegawai VARCHAR(5) PRIMARY KEY,
    nama_depan VARCHAR(50),
    nama_belakang VARCHAR(50),
    email VARCHAR(100),
    telepon VARCHAR(20),
    tgl_kontrak DATE,
    id_job VARCHAR(5),
    gaji INT,
    tunjangan INT
);

-- Insert data into the 'pegawai' table
INSERT INTO pegawai (idpegawai, nama_depan, nama_belakang, email, telepon, tgl_kontrak, id_job, gaji, tunjangan) VALUES
('E001', 'Ferry', 'gustiawan', 'ferry@yahoo.com', '07117059004', '2005-09-01', 'L0001', 2000000, 500000),
('E002', 'aris', 'ganiardi', 'aris@yahoo.com', '081312345678', '2006-09-01', 'L0002', 2000000, 200000),
('E003', 'faiz', 'ahnad', 'faiz@gmail.com', '081367384322', '2006-10-01', 'L0003', 1500000, NULL),
('E004', 'emna', 'bunton', 'enna@gmail.com', '081363484342', '2006-10-01', 'L0004', 1500000, 9),
('E005', 'mike', 'scoff', 'mike@plasa.com', '08163454555', '2007-09-01', 'L0005', 1250000, 9),
('E006', 'lincoln', 'burrows', 'linc@yahoo.com', '08527388432', '2008-09-01', 'L0006', 1750000, NULL);
````
![1](https://github.com/MUHAMMADRIZKYEFENDI/pratikum4/assets/168548623/4eebb0b3-8a2b-4bc1-b6b2-235b47c0b9f5)

# 1. Tampilkan pegawai yang gajinya bukan 2.000.000 dan 1.250.000!

```
SELECT * FROM pegawai
WHERE gaji NOT IN (2000000, 1250000);

```
![1 1](https://github.com/MUHAMMADRIZKYEFENDI/pratikum4/assets/168548623/54bb5512-a556-4f09-bf8d-a10deea5a681)

# 2. Tampilkan pegawai yang tunjangannya NULL!
```
SELECT * FROM pegawai
WHERE tunjangan IS NULL;

```
![1 2](https://github.com/MUHAMMADRIZKYEFENDI/pratikum4/assets/168548623/81fe5164-aebd-46ea-86f8-6b036ccb0103)


# 3. Tampilkan pegawai yang tunjangannya tidak NULL!
```
SELECT * FROM pegawai
WHERE tunjangan IS NOT NULL;

```

![1 4](https://github.com/MUHAMMADRIZKYEFENDI/pratikum4/assets/168548623/427d5b92-5709-41de-8e30-dd480df46891)


# 4. Tampilkan/hitung jumlah baris/record tabel pegawai!
```
SELECT COUNT(*) AS jumlah_pegawai FROM pegawai;
```
![Screenshot (84)](https://github.com/MUHAMMADRIZKYEFENDI/pratikum4/assets/168548623/502e701f-da31-4c95-8d4e-82164612f3e1)



# 5. Tampilkan/hitung jumlah total gaji di tabel pegawai!

```
SELECT SUM(gaji) AS total_gaji FROM pegawai;
```

![Screenshot (85)](https://github.com/MUHAMMADRIZKYEFENDI/pratikum4/assets/168548623/6aaa7ae9-41d3-4862-8596-4edcc6d7bf94)

# 6. Tampilkan/hitung rata-rata gaji pegawai!
```
SELECT AVG(gaji) AS rata_rata_gaji FROM pegawai;
```
![Screenshot (86)](https://github.com/MUHAMMADRIZKYEFENDI/pratikum4/assets/168548623/0d8110ca-0f3a-4532-96bb-2a435396ac98)
# 7. Tampilkan gaji terkecil:
```
SELECT MIN(gaji) AS gaji_terkecil FROM pegawai;
````
![Screenshot (87)](https://github.com/MUHAMMADRIZKYEFENDI/pratikum4/assets/168548623/bd009ea9-42aa-47fe-bf7b-40847b600a61)



# 8. Tampilkan gaji terbesar!
```
SELECT MAX(gaji) AS gaji_terbesar FROM pegawai;
```
![Screenshot (88)](https://github.com/MUHAMMADRIZKYEFENDI/pratikum4/assets/168548623/5165d745-3920-4bed-b197-838d460c3460)
