# perintah-mysql
Menulis perintah database mysql command prompt
---------- PERINTAH DATABASE -----------

1. Menambah foreign key :
ALTER TABLE nama_tabel ADD FOREIGN KEY (nama_kolom) REFERENCES nama_tabel(nama_kolom) ON UPDATE CASCADE ON DELETE CASCADE;

2. Menambah field/kolom :
ALTER TABLE nama_tabel ADD nama_kolom typedata();

3. Mengubah nama field/kolom :
ALTER TABLE nama_tabel CHANGE nama_kolom_lama nama_kolom_baru typedata();

4. Menambah primary key :
ALTER TABLE nama_tabel ADD PRIMARY KEY (nama_kolom);

5.Menghapus primary key :
ALTER TABLE nama_tabel DROP PRIMARY KEY;

6. Mengubah nama sebuah table :
ALTER TABLE nama_tabel RENAME nama_tabel_baru



---------- PERINTAH DATABASE -----------

7. Perintah Membuat Index pada table:
CREATE INDEX nama_table ON nama_table(nama_kolom);
