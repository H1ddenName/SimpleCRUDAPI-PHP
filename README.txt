Cara menjalankan aplikasi
1. Jalankan Mysql dan Apache pada XAMPP
2. Import project ke htdocs dan 
3. Buat database pada mysql dengan nama database 'db_crud_api'
4. Jalankan semua Query CREATE TABLE
5. Akses aplikasi menggunakan postman inputkan http://localhost/api/insert.php
6. Tambahkan salah satu Postingan.


Berikut Merupakan List Table yang dibuat.
Database_name = db_crud_api
TABLE :
- category
- posts
- user

--Berikut merupakan Query CREATE TABLE (Jalankan Satu Persatu)--

CREATE TABLE user (
id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
username VARCHAR(30) NOT NULL,
password VARCHAR(200) NOT NULL,
email VARCHAR(50),
reg_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
)

CREATE TABLE category (
id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(30) NOT NULL,
reg_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
)

CREATE TABLE posts (
id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
title VARCHAR(100) NOT NULL,
description VARCHAR(500) NOT NULL,
category_id VARCHAR(50),
reg_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
)


---Contoh Menabhkan Record Pada Table Category---
INSERT INTO category (id, name) VALUES (default, 'Computer Network Security');

---Contoh Menabhkan Record Pada Table Post---
INSERT INTO posts (id, title, description, category_id) VALUES (default, 'Information Security', 'Keamanan informasi adalah perlindungan terhadap segala jenis sumber daya informasi dari penyalahgunaan pihak yang tak berwenang mengelolanya.', 1);