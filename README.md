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
ALTER TABLE nama_tabel RENAME nama_tabel_baru;

7. Menambah kolom baru setelah kolom lain :
ALTER TABLE nama_tabel ADD COLUMN nama_kolom_baru typedata() AFTER nama_kolom_lain; 



---------- PERINTAH DATABASE -----------

7. Perintah Membuat Index pada sebuah table:
CREATE INDEX nama_table ON nama_table(nama_kolom); <br>
atau <br> CREATE INDEX nama_table ON nama_table(nama_kolom1, nama_kolom2) USING BTREE;

8. Menampilkan jumlah data (COUNT) dengan kondisi tertentu : <br>

SELECT COUNT(*) AS sebagai FROM nama_table WHERE nama_kolom='kondisi';

9. Perintah JOIN, menggabungkan 2 tabel :<br>
SELECT nama_kolom1, nama_kolom2 FROM nama_tabel1 JOIN nama_tabel2 USING(nama_kolom);<br>

10. Perintah JOIN, menggabungkan 2 tabel dengan kondisi (cocok untuk komentar) :<br>
SELECT nama_kolom1, nama_kolom2 from nama_tabel1 JOIN nama_tabel2 USING (nama_kolom) WHERE nama_kolom='kondisi';<br>

11. Perintah JOIN, menggabungkan 3 tabel : <br>
SELECT nama_kolom_tampil1, nama_kolom_tampil2,dst FROM nama_table1 JOIN nama_table2 USING(kondisi) JOIN nama_table3 USING(kondisi);
