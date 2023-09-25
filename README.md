# Data Mining and Warehouse : EDA

**Kelompok 6**

1. Imam Chalish Rafidhul Haque
2. Rakha Dhifiargo Hariadi
3. Salma Ghaida
4. Themy Sabri Syuhada

# Explanatory Data Analysis

Pada tugas kali ini kami melakukan pre-processing data, transformasi data, mengubah tipe data, mengatasi data yang tidak masuk akal, dan
melakukan penghapusan pada kolom/atribut yang memiliki nilai redundan.

Kami menggunakan 2 dataset untuk EDA kali ini.

### Penjelasan Dataset Daftar Desa Berdasarkan Provider Telepon Seluler di Jawa Barat

Dataset ini berisi data daftar desa berdasarkan provider telepon seluler di Provinsi Jawa Barat periode tahun 2021.

Penjelasan mengenai variabel di dalam dataset ini:

- kode_provinsi: menyatakan kode Provinsi Jawa Barat sesuai ketentuan BPS merujuk pada aturan Peraturan Badan Pusat Statistik Nomor 3 Tahun 2019 dengan tipe data numerik.
- nama_provinsi: menyatakan lingkup data berasal dari wilayah Provinsi Jawa Barat sesuai ketentuan BPS merujuk pada aturan Peraturan Badan Pusat Statistik Nomor 3 Tahun 2019 dengan tipe data teks.
- kode_kabupaten_kota: menyatakan kode dari setiap kabupaten dan kota di Provinsi Jawa Barat sesuai ketentuan BPS merujuk pada aturan Peraturan Badan Pusat Statistik Nomor 3 Tahun 2019 dengan tipe data numerik.
- nama_kabupaten_kota: menyatakan lingkup data berasal dari setiap kabupaten dan kota di Provinsi Jawa Barat sesuai penamaan BPS merujuk pada aturan Peraturan Badan Pusat Statistik Nomor 3 Tahun 2019 dengan tipe data teks.
- bps_kode_kecamatan: menyatakan kode dari setiap kecamatan di Provinsi Jawa Barat sesuai ketentuan BPS merujuk pada aturan Peraturan Badan Pusat Statistik Nomor 3 Tahun 2019 dengan tipe data numerik.
- bps_nama_kecamatan: menyatakan lingkup data berasal dari setiap kecamatan di Provinsi Jawa Barat sesuai penamaan BPS merujuk pada aturan Peraturan Badan Pusat Statistik Nomor 3 Tahun 2019 dengan tipe data teks.
- bps_kode_desa_kelurahan: menyatakan kode dari setiap desa dan kelurahan di Provinsi Jawa Barat sesuai ketentuan BPS merujuk pada aturan Peraturan Badan Pusat Statistik Nomor 3 Tahun 2019 dengan tipe data numerik.
- bps_nama_desa_kelurahan: menyatakan lingkup data berasal dari setiap desa dan kelurahan di Provinsi Jawa Barat sesuai penamaan BPS merujuk pada aturan Peraturan Badan Pusat Statistik Nomor 3 Tahun 2019 dengan tipe data teks.
- kemendagri_kode_kecamatan: menyatakan kode dari setiap kecamatan di Provinsi Jawa Barat sesuai ketentuan Kementerian Dalam Negeri merujuk pada aturan Peraturan Menteri Dalam Negeri No. 137 tahun 2017 dengan tipe data numerik.
- kemendagri_nama_kecamatan: menyatakan lingkup data berasal dari setiap kecamatan di Provinsi Jawa Barat sesuai penamaan Kementerian Dalam Negeri merujuk pada aturan Peraturan Menteri Dalam Negeri No. 137 tahun 2017 dengan tipe data teks.
- kemendagri_kode_desa_kelurahan: menyatakan kode dari setiap desa dan kelurahan di Provinsi Jawa Barat sesuai ketentuan Kementerian Dalam Negeri merujuk pada aturan Peraturan Menteri Dalam Negeri No. 137 tahun 2017 dengan tipe data numerik.
- kemendagri_nama_desa_kelurahan: menyatakan lingkup data berasal dari setiap desa dan kelurahan di Provinsi Jawa Barat sesuai penamaan Kementerian Dalam Negeri merujuk pada aturan Peraturan Menteri Dalam Negeri No. 137 tahun 2017 dengan tipe data teks.
- status_sinyal: menyatakan kategori status sinyal dengan tipe data teks.
  - sinyal kuat: menyatakan status sinyal kuat.
  - sinyal lemah: menyatakan status sinyal kuat.
  - tidak ada sinyal: menyatakan status sinyal kuat.
- keberadaan_internet: menyatakan status keberadaan internet dengan tipe data teks.
  - ada: menyatakan adanya keberadaan internet di desa.
  - tidak ada: menyatakan tidak adanya keberadaan internet di desa.
- kepemilikan_internet: menyatakan status kepemilikan internet dengan tipe data teks.
  - ada: menyatakan adanya kepemilikan internet di desa.
  - tidak ada: menyatakan tidak adanya kepemilikan internet di desa.
- ketersediaan_tower_bts: menyatakan status ketersediaan tower bts dengan tipe data teks.
  - ada: menyatakan adanya ketersediaan tower bts di desa.
  - tidak ada: menyatakan tidak adanya ketersediaan tower bts di desa.
- jarak_tower_terdekat: menyatakan jarak tower terdekat dalam kilometer dengan tipe data numerik.
- keberadaan_telkomsel: menyatakan status keberadaan sinyal telkomsel di desa dengan tipe data teks.
  - ada: menyatakan adanya sinyal telkomsel di desa
  - tidak ada: menyatakan tidak adanya sinyal telkomsel di desa.
- keberadaan_indosat: menyatakan status keberadaan sinyal indosat di desa dengan tipe data teks.
  - ada: menyatakan adanya sinyal indosat di desa
  - tidak ada: menyatakan tidak adanya sinyal indosat di desa.
- keberadaan_xl_axiata: menyatakan status keberadaan sinyal xl axiata di desa dengan tipe data teks.
  - ada: menyatakan adanya sinyal xl axiata di desa
  - tidak ada: menyatakan tidak adanya sinyal xl axiata di desa.
- keberadaan_operator_lain: menyatakan status keberadaan sinyal operator lainnya di desa dengan tipe data teks.
  - ada: menyatakan adanya sinyal sinyal operator lainnya di desa
  - tidak ada: menyatakan tidak adanya sinyal sinyal operator lainnya di desa.
- operator_lainnya: menyatakan status keberadaan sinyal operator lainnya di desa diantaranya axis, three, smartfren, by.u, indihome, lainnya dengan tipe data teks.
- tahun: menyatakan tahun produksi data dengan tipe data numerik.

### Penjelasan Dataset Jumlah Kawasan Desa Digital Berdasarkan Kabupaten/Kota di Jawa Barat

Dataset ini berisi data jumlah kawasan desa digital berdasarkan kabupaten/kota di Provinsi Jawa Barat dari tahun 2021 s.d. 2022.

Desa digital adalah sebuah konsep pengembangan desa di Jawa Barat yang menggunakan teknologi informasi dan komunikasi. Tujuannya untuk mempercepat pertumbuhan ekonomi, meningkatkan kualitas hidup masyarakat, dan memperkuat pemerintahan desa informasi dan wilayah.

Penjelasan mengenai variabel di dalam dataset ini:

- kode_provinsi: menyatakan kode Provinsi Jawa Barat sesuai ketentuan BPS merujuk pada aturan Peraturan Badan Pusat Statistik Nomor 3 Tahun 2019 dengan tipe data numerik.
- nama_provinsi: menyatakan lingkup data berasal dari wilayah Provinsi Jawa Barat sesuai ketentuan BPS merujuk pada aturan Peraturan Badan Pusat Statistik Nomor 3 Tahun 2019 dengan tipe data teks.
- kode_kabupaten_kota: menyatakan kode dari setiap kabupaten dan kota di Provinsi Jawa Barat sesuai ketentuan BPS merujuk pada aturan Peraturan Badan Pusat Statistik Nomor 3 Tahun 2019 dengan tipe data numerik.
- nama_kabupaten_kota: menyatakan lingkup data berasal dari setiap kabupaten dan kota di Provinsi Jawa Barat sesuai penamaan BPS merujuk pada aturan Peraturan Badan Pusat Statistik Nomor 3 Tahun 2019 dengan tipe data teks.
- jumlah_desa: menyatakan jumlah kawasan desa digital dengan tipe data numerik.
- satuan: menyatakan satuan dari pengukuran jumlah kawasan desa digital dalam desa dengan tipe data teks.
- tahun: menyatakan tahun produksi data dengan tipe data numerik.
