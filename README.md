# perintah-mysql
Menulis perintah database mysql command prompt
---------- PERINTAH DATABASE -----------

1. Menambah foreign key :<br>
ALTER TABLE nama_tabel ADD FOREIGN KEY (nama_kolom) REFERENCES nama_tabel(nama_kolom) ON UPDATE CASCADE ON DELETE CASCADE;<br>

2. Menambah field/kolom :<br>
ALTER TABLE nama_tabel ADD nama_kolom typedata();<br>

3. Mengubah nama field/kolom :<br>
ALTER TABLE nama_tabel CHANGE nama_kolom_lama nama_kolom_baru typedata();<br>

4. Menambah primary key :<br>
ALTER TABLE nama_tabel ADD PRIMARY KEY (nama_kolom);<br>

5. Menghapus primary key :<br>
ALTER TABLE nama_tabel DROP PRIMARY KEY;<br>

6. Mengubah nama sebuah table :<br>
ALTER TABLE nama_tabel RENAME nama_tabel_baru;<br>

7. Menambah kolom baru setelah kolom lain :<br>
ALTER TABLE nama_tabel ADD COLUMN nama_kolom_baru typedata() AFTER nama_kolom_lain; <br>


<br><br><br>



---------- PERINTAH DATABASE -----------

1. Perintah Membuat Index pada sebuah table:<br>
CREATE INDEX nama_table ON nama_table(nama_kolom); <br>
atau <br> CREATE INDEX nama_table ON nama_table(nama_kolom1, nama_kolom2) USING BTREE;<br>

2. Menampilkan jumlah data (COUNT) dengan kondisi tertentu : <br>
SELECT COUNT(*) AS sebagai FROM nama_table WHERE nama_kolom='kondisi';<br>

3. Perintah JOIN, menggabungkan 2 tabel :<br>
SELECT nama_kolom1, nama_kolom2 FROM nama_tabel1 JOIN nama_tabel2 USING(nama_kolom);<br>

4. Perintah JOIN, menggabungkan 2 tabel dengan kondisi (cocok untuk komentar) :<br>
SELECT nama_kolom1, nama_kolom2 from nama_tabel1 JOIN nama_tabel2 USING (nama_kolom) WHERE nama_kolom='kondisi';<br>

5. Perintah JOIN, menggabungkan 3 tabel : <br>
SELECT nama_kolom_tampil1, nama_kolom_tampil2,dst FROM nama_table1 JOIN nama_table2 USING(kondisi) JOIN nama_table3 USING(kondisi);<br>

6. Perintah JOIN, menggabungkan table apabila nama kolom yang sama : <br>
SELECT nama_kolom1, nama_tabel1.nama_kolom_yang_sama FROM nama_table1 JOIN nama_table2 USING(kondisi);<br> 

7. Perintah LIKE menampilkan 2 kondisi dengan gabungan AND dan OR : <br>
SELECT * FROM nama_table WHERE (nama_kolom1='kondisi') AND (nama_kolom2 LIKE = '%kondisi%' OR nama_kolom3 LIKE = '%kondisi%');<br>

8. Perintah INSERT memasukan data pada dua tabel foreign key bernilai auto_increment dengan LAST_INSERT_ID(): <br>
START TRANSACTION; INSERT INTO tabel1 (tabel1kolom1_AI, tabel1kolom2) VALUES('', 'tabel1kolom2'); INSERT INTO tabel2 (tabel2kolom1, tabel2kolom2) VALUES(LAST_INSERT_ID(),'tabel2kolom2'); COMMIT;<br>

9. Perintah ALTER TABLE reset nilai auto_increment pada sebuah tabel: <br>
ALTER TABLE nama_tabel AUTO_INCREMENT = 1;<br>
