**Deskripsi Proyek**

Penelitian ini melakukan analisis topic modeling pada data percakapan publik di platform Twitter (X) yang berkaitan dengan demonstrasi DPR RI dan polemik RUU Pilkada pada Agustus 2025. Tujuan penelitian adalah untuk mengidentifikasi struktur topik yang muncul dalam data teks tidak terstruktur menggunakan metode Latent Dirichlet Allocation (LDA). Hasil analisis digunakan untuk memberikan gambaran mengenai isu-isu utama yang dibicarakan oleh masyarakat dalam diskursus publik di media sosial.

**Dataset**

Dataset yang digunakan dalam penelitian ini berjudul “DPR Demonstration Sentiment Dataset August 2025”. Data diperoleh melalui proses crawling dari platform Twitter menggunakan kata kunci “dpr” dengan bantuan tools Tweet-Harvest yang dikembangkan oleh Helmi Satria.
Jumlah data awal sebanyak 5.204 tweet, kemudian setelah proses preprocessing diperoleh 4.791 tweet yang digunakan dalam analisis. Dataset terdiri dari dua variabel utama yaitu tanggal publikasi (date) dan isi teks tweet (text). Seluruh data menggunakan bahasa Indonesia.

**Metodologi**

- _Preprocessing Data_

Tahapan preprocessing dilakukan untuk membersihkan dan mempersiapkan data teks agar dapat digunakan dalam pemodelan topik. Tahapan yang dilakukan meliputi:
1. Filtering bahasa Indonesia
2. Case folding
3. Cleaning (penghapusan URL, mention, hashtag, angka, dan tanda baca)
4. Tokenization
5. Normalisasi kata
6. Penghapusan stopword
7. Stemming menggunakan Sastrawi
   
- _ Pemodelan Topik_

Pemodelan topik dilakukan menggunakan metode Latent Dirichlet Allocation (LDA). Model ini merupakan pendekatan probabilistik dalam unsupervised learning yang mengasumsikan bahwa setiap dokumen merupakan kombinasi dari beberapa topik, dan setiap topik terdiri dari distribusi kata tertentu.
Representasi data menggunakan Bag of Words. Estimasi parameter dilakukan menggunakan pendekatan Gibbs Sampling atau Variational Inference. Hasil model berupa distribusi topik pada setiap dokumen dan distribusi kata pada setiap topik.

- _Evaluasi Model_

Evaluasi dilakukan menggunakan coherence score untuk mengukur tingkat keterkaitan antar kata dalam suatu topik. Model dengan nilai coherence tertinggi dipilih sebagai model terbaik karena menghasilkan topik yang lebih koheren dan mudah diinterpretasikan.

- _Hasil_

Model terbaik diperoleh dengan jumlah empat topik. Keempat topik tersebut merepresentasikan:
- Aksi demonstrasi dan kerusuhan
- Isu hubungan masyarakat dan pemerintah
- Isu ekonomi politik seperti pajak, gaji, dan tunjangan
- Dinamika partai politik dan kelembagaan
Selain itu, dilakukan visualisasi menggunakan intertopic distance map dan word cloud untuk memperkuat interpretasi hasil pemodelan.

**Struktur Repository**

Repository ini terdiri dari beberapa direktori utama sebagai berikut:

notebook: berisi kode analisis topic modeling

README.md: dokumentasi penelitian

**Perangkat yang Digunakan**

Analisis dilakukan menggunakan bahasa pemrograman Python dengan beberapa library utama yaitu Pandas, NLTK, Sastrawi, Gensim, Scikit-learn, dan Matplotlib.

**Penulis**

Miguel
Program Studi Statistika, Universitas Indonesia
Email: miguel@ui.ac.id

**Tautan Repository**

https://github.com/migueltjhang56-oss/Topic-Modelling
