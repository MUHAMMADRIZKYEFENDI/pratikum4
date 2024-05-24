# pratikum4
# table pegawai 
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






# table hewan
```
-- Create the table 'hewan'
CREATE TABLE hewan (
    id VARCHAR(5) PRIMARY KEY,
    name VARCHAR(50),
    owner VARCHAR(50),
    species VARCHAR(50),
    sex CHAR(1)
);

-- Insert data into the 'hewan' table
INSERT INTO hewan (id, name, owner, species, sex) VALUES
('p1', 'Puffball', 'Diane', 'Hamster', 'f'),
('p2', 'Claws', 'Gwen', 'cat', 'm'),
('p3', 'Fluffy', 'Haro 1d', 'cat', 'f'),
('p4', 'Buffy', 'Haro 1d', 'dog', 'f'),
('p5', 'Fang', 'Benny', 'dog', 'm'),
('p6', 'Bowser', 'Diane', 'dog', 'm'),
('p7', 'Chirpy', 'Gwen', 'bird', 'f'),
('p8', 'Whistler', 'Gwen', 'bird', NULL),
('p9', 'Slim', 'Benny', 'snake', 'm');
````
![Screenshot (89)](https://github.com/MUHAMMADRIZKYEFENDI/pratikum4/assets/168548623/e55a8120-a2b4-4890-8838-71af222eebe6)


# 1. Tampilkan jumlah hewan yang dimiliki setiap owner.
```
SELECT owner, COUNT(*) AS jumlah_hewan
FROM hewan
GROUP BY owner;
```
![Screenshot (90)](https://github.com/MUHAMMADRIZKYEFENDI/pratikum4/assets/168548623/094c7dc6-120d-4503-afec-b78abd654d39)

# 2. Tampilkan jumlah hewan berdasarkan spesies
```
SELECT species, COUNT(*) AS jumlah_hewan
FROM hewan
GROUP BY species;

```
![Screenshot (91)](https://github.com/MUHAMMADRIZKYEFENDI/pratikum4/assets/168548623/8164c7eb-665d-4928-b179-9f79829c98fd)
# 3. Tampilkan jumlah hewan berdasarkan jenis kelamin
```
SELECT sex, COUNT(*) AS jumlah_hewan
FROM hewan
GROUP BY sex;
```
# 4. Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin
```
SELECT species, sex, COUNT(*) AS jumlah_hewan
FROM hewan
GROUP BY species, sex;
```
# 5. Tampilkan jumlah hewan berdasarkan spesis (cat dan dog saja) dan jenis kelamin
```
SELECT species, sex, COUNT(*) AS jumlah_hewan
FROM hewan
WHERE species IN ('cat', 'dog')
GROUP BY species, sex;
```
# 6. Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui saja
```
SELECT sex, COUNT(*) AS jumlah_hewan
FROM hewan
WHERE sex IS NOT NULL
GROUP BY sex;
```
