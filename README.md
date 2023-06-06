# EnigmaGroup_JC_DS_FT_JKT_19_FinalProject

# Dashboard
Google Looker Studio: [https://lookerstudio.google.com/reporting/bfba7d0c-8be5-492c-8188-f57d1bdc3952](https://lookerstudio.google.com/reporting/bfba7d0c-8be5-492c-8188-f57d1bdc3952)

# Business Problem Understanding

### Context
Berdasarkan Undang-Undang Nomor 10 Tahun 1998 tentang Perbankan, **bank** adalah badan usaha yang menghimpun dana dari masyarakat dalam bentuk simpanan dan menyalurkannya kepada masyarakat dalam bentuk kredit dan atau bentuk-bentuk lainnya dalam rangka meningkatkan taraf hidup masysarakat. Bank berperan dalam menghimpun dana, menyalurkan dana, dan memberikan jasa-jasa bank lain. Bank menyediakan berbagai produk untuk nasabahnya seperti rekening giro, tabungan, deposito, kredit, kartu kredit, asuransi, layanan perbankan elektronik, investasi dan manajemen kekayaan. Seperti bank pada umumnya, bank di Amerika menyediakan deposito, kredit, layanan pembayaran (kartu debit dan kartu kredit), perencanaan keuangan, investasi, dan manajemen kekayaan.

Salah satu produk di dunia perbankan adalah kartu kredit.  Kartu kredit adalah produk pembayaran untuk nasabah dan transaksi bisnis. Berdasarkan **[Trading Economics](https://id.tradingeconomics.com/united-states/credit-card-accounts)** jumlah akun kartu kredit di Amerika Serikat mengalami kenaikan pada tahun 2023. Hampir setiap penduduk di Amerika dari berbagai golongan mendapatkan tawaran pembuatan kartu kredit melalui telepon atau *email* setiap minggunya. Nasabah kartu kredit dan bank akan memdapatkan keuntungan apabila sang nasabah sering melakukan transaksi menggunakan kartu kredit dan tetap menyimpan kartu kreditnya dalam jangka waktu yang lama. Selain itu, pihak bank akan mendapatkan keuntungan besar.

Bank Bangtut adalah suatu bank di Amerika. Bank Bangtut hanya memiliki satu program produk kartu kredit saja. Bank bangtut ingin menambah keuntungan bank lebih besar melalui produk kartu kredit dengan cara melakukan segmentasi atau menganalisa nasabah kartu kredit. Segmentasi nasabah kartu kredit dapat dilakukan dengan cara mengelompokkan para nasabah berdasarkan profil dan kebiasaan dari masing-masing nasabah agar Bank Bangtut menyusun strategi bisnis yang lebih efektif dan optimal, dan juga dapat memberikan *treatment* yang tepat untuk masing-masing nasabah kartu kredit.


### Problem Statement
Setiap bank memiliki produk kartu kredit sehingga satu tantangan dari Bank Bangtut adalah mempertahankan nasabah kartu kredit agar tetap menggunakan kartu kredit dari Bank Bangtut. Berdasarkan dari **[FPSC](https://www.fpsc.com/the_cost_of_customer_churn.pdf)** *cost* mendapatkan nasabah baru **lima kali** lebih besar dibandingkan mempertahankan yang sudah ada. Dengan mengetahui hal tersebut, itu menjadi tantangan tersendiri untuk bank Bangtut. Selama ini belum ada *treatment* yang diberikan kepada nasabah secara spesifik melihat profil-profil nasabah. Oleh sebab itu, masih ada permasalah untuk memberikan *treatment* ke masing-masing nasabah agar mereka tetap berlangganan kartu kredit di bank Bangtut dan sering bertransaksi menggunakan kartu kreditnya.

Kami sebagai tim data bekerja sama dengan tim *marketing* hendak melakukan sebuah strategi pemasaran dan *campaign* dalam bisnis dengan tujuan untuk mengelompokkan semua nasabah kartu kredit menjadi beberapa kelompok berdasarkan profil dan kebiasaan yang sama. Tujuannya adalah *treatment* atau strategi pemasaran yang diberikan kepada para nasabah tepat sesuai dengan target dan meminimalkan *cost* (*cost effectivity*) sehingga para nasabah akan sering menggunakan kartu kreditnya dan tetap berlangganan kartu kredit di Bank Bangtut.


### Goals
Berdasarkan dari permasalahan di atas, tujuan kami yaitu dapat menjabarkan karakteristik nasabah kartu kredit saat ini dan selanjutnya akan kami kelompokkan berdasarkan riwayat transaksi kartu kreditnya. Kami juga akan memberikan saran untuk tim *marketing* mengenai strategi pemasaran atau *tretment* yang tepat untuk diberikan ke masing-masing nasabah sehingga mereka tetap menggunakan kartu kredit bank Bangtut dan meningkatkan transaksi. Akhirnya, bank akan mendapatkan profit.

### Analytic Approach
Karena yang akan dilakukan adalah segmentasi nasabah maka metode yang digunakan adalah ***clustering*** dengan mencari pola atau kebiasaan yang serupa dari setiap nasabah kartu kredit.


### Metric Evaluation
Karena metode yang digunakan adalah *clustering* maka metrik evaluasi yang diguanakan adalah:

* ***Silhouette Coefficient*** (mengukur seberapa baik sample dengan kelompoknya sendiri dibandingkan kelompok lain)
* ***Elbow Method*** (menemukan jumlah kelompok optimal pada data)

# Data Understanding  

Dataset berasal dari [***Kaggle***](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata/discussion/169386) adalah dataset riwayat transaksi **nasabah** kartu kredit yang **aktif** melakukan transaksi selama **6 bulan terakhir** atau ***subscribe*** kartu kreditnya **6- 12 bulan**. 
* Dataset berisi **8950** riwayat transaksi pembelian dan pembayaran dengan diwakili **18 fitur** dari masing-masing nasabah kartu kredit selama 6 bulan.
* **Setiap baris** dari dataset merepresentasikan **riwayat transaksi satu nasabah** kartu kredit.

![Untitled](https://github.com/PurwadhikaDev/EnigmaGroup_JC_DS_FT_JKT_19_FinalProject/assets/113419733/0bc74d4c-a61a-48ac-851c-7c9d8a16850b)

# K-Means Clustering
Pada bagian ini akan dilakukan pengelompokkan dengan model K-Means pada dataset lalu akan divisualisasikan dengan metode PCA. Pembagian terbaik yang didapat yaitu dataset dibagi menjadi **4 *cluster***

![Untitled2](https://github.com/PurwadhikaDev/EnigmaGroup_JC_DS_FT_JKT_19_FinalProject/assets/113419733/ce08bb2c-07aa-4a8e-92a4-08d155c30adb)

# Conclusion

1. Kita telah mempelajari KPI kartu kredit dan menganalisa karakteristik setiap nasabah kartu kredit bank Bangtut berdasarkan KPI.
2. Untuk menganalisa, kita menggunakan komparasi ***shillouette score*** dan ***elbow method*** dalam pembagian *cluster* karena metode ***shillouette score*** dapat membagi secara **objektif** dan metode ***elbow method*** dapat membagi secara **subjektif**.
3. Berdasarkan hasil ***shillouette score*** dan ***elbow method***, ada kesamaan yaitu membagi dataset menjadi **4**, **5**, dan **6** kelompok.
4. Setelah dikelompokkan dengan metode **K-Means** dan divisualisasikan dengan metode **PCA**, didapat pembagian dataset terbaik menjadi **4 kelompok**.
5. Selanjutnya, masing-masing kelompok dianalisa berdasarkan pendekatan KPI yang berhubungan dengan fitur:
    * PURCHASES termasuk ONEOFF_PURCHASES dan INSTALLMENTS_PURCHASES
    * CASH_ADVANCE
    * PAYMENT_MINPAYMENT yang berhubungan dengan PAYMENT dan MINIMUM_PAYMENT
    * LIMIT_USE yang berhubungan dengan BALANCE dan CREDIT_LIMIT
    * TENURE
    * PRC_FULL_PAYMENT
6. Kita dapat merekomendasikan strategi kepada tim *marketing* secara *clustering* dan umum  

# Recommendation  

Secara pembagian *cluster*, kita dapat memberikan rekomendasi yang sesuai untuk nasabah-nasabah kartu kredit bank Bangtut:
1. **Cluster 0**: Nasabah di kelompok ini sudah menggunakan kartu kredit secara aktif dan memiliki kesadaran untuk membayar tagihan setiap bulannya dengan jumlah yang melebihi batas minimum. Treatment yang cocok untuk kelompok ini adalah memberikan insentif tambahan seperti reward points atau cashback khusus untuk setiap transaksi yang dilakukan. Hal ini dapat mendorong nasabah untuk lebih sering menggunakan kartu kredit dalam berbagai transaksi sehari-hari dan meningkatkan jumlah transaksi secara keseluruhan.

2. **Cluster 1**: Nasabah di kelompok ini cenderung memiliki gaya hidup yang lebih hemat. Untuk meningkatkan jumlah transaksi, treatment yang dapat diberikan adalah mengembangkan program diskon khusus atau penawaran eksklusif untuk produk atau layanan yang sesuai dengan kebutuhan dan minat nasabah di kelompok ini. Selain itu, tim marketing dapat memberikan informasi dan edukasi tentang manfaat penggunaan kartu kredit dalam mengatur keuangan secara bijak, sehingga nasabah merasa lebih percaya diri untuk melakukan transaksi yang sesuai dengan kemampuan keuangan mereka.

3. **Cluster 2**: Nasabah di kelompok ini sudah sering berbelanja dengan jumlah besar, tetapi cenderung membayar hanya batas minimum. Treatment yang sesuai adalah mengembangkan program cicilan dengan bunga rendah atau tanpa bunga untuk transaksi besar yang dilakukan oleh nasabah di kelompok ini. Hal ini akan memberikan insentif kepada nasabah untuk melakukan pembayaran yang lebih besar dan memperpanjang waktu cicilan dengan suku bunga yang lebih menguntungkan.

4. **Cluster 3**: Nasabah di kelompok ini sudah membayar tagihan dengan jumlah yang lebih besar daripada pembayaran minimum yang ditetapkan. Treatment yang cocok untuk kelompok ini adalah mengembangkan program reward yang lebih menarik, seperti level keanggotaan eksklusif, akses ke promo khusus, atau penawaran khusus yang hanya tersedia untuk nasabah di kelompok ini. Hal ini dapat mempertahankan loyalitas nasabah dan mendorong mereka untuk terus menggunakan kartu kredit Bank Bangtut.

Selain treatment yang spesifik untuk setiap kelompok, tim marketing juga dapat melakukan komunikasi proaktif dengan nasabah melalui email, pesan teks, atau media sosial untuk memberikan informasi tentang penawaran, promo, atau program baru yang dapat meningkatkan minat dan keterlibatan nasabah dalam menggunakan kartu kredit mereka.  

Secara umum kita dapat memberikan rekomendasi:
1. Tim *marketing* dapat mempertimbangkan penawaran yang mengakomodasi kedua preferensi pembayaran ini, seperti program cicilan dengan bunga rendah atau penawaran diskon khusus untuk pembayaran langsung untuk nasabah-nasabah dengan tipe pembelian dengan cicilan dan tanpa cicilan
2. Tim *marketing* dapat menawarkan program cicilan yang lebih fleksibel dan menguntungkan seperti penawaran tenor cicilan yang lebih lama atau diskon bunga untuk pembayaran secara berkala untuk nasabah-nasabah dengan tipe pembelian dengan cicilan saja
3. Tim *marketing* dapat menawarkan program promosi khusus atau *cashback* untuk nasabah yang melakukan pembelian pertama mereka dengan kartu kredit agar nasabah-nasabah yang tidak melakukan pembelian aktif bertransaksi
4. Tim *marketing* dapat menawarkan insentif seperti diskon khusus atau cashback untuk pembayaran langsung, atau memberikan program reward yang lebih menguntungkan bagi nasabah yang sering melakukan pembelian dengan cara ini untuk nasabah-nasabah dengan tipe pembelian tanpa cicilan saja
5. Tim *marketing* dapat menawarkan *reward*, insentif, *cashback*, *reward points*, diskon eksklusif agar nasabah merasa puas dan menjadi lebih loyal
6. Tim *marketing* dapat memberikan pendapingan seperti menyediakan akses ke alat pengelolaan anggaran atau memberikan tips dan panduan penghematan untuk nasabah yang memiliki nilai kredit sangat buruk atau sangat tidak baik
7. Tim *marketing* dapat memberikan penghargaan atau insentif seperti penawaran suku bunga yang lebih rendah, *reward*, dan meningkatkan limit untuk nasabah-nasabah yang melakukan pembayaran lebih dari batas minimum pembayaran
8. Tim *marketing* dapat memberikan layanan tambahan seperti konsultasi keuangan atau rekomendasi untuk mengoptimalkan pengelolaan kartu kredit untuk nasabah-nasabah yang melakukan pembayaran tagihan kurang dari batas minimum pembayaran
9. Tim *marketing* dapat memberikan pengingat pembayaran melalui pesan teks atau email yang disertai dengan insentif seperti diskon atau reward points tambahan jika nasabah membayar tagihan secara penuh untuk nasabah yang tidak pernah membayarkan tagihan secara penuh
10. Tim *marketing* dapat menghargai dan memberikan penghargaan seperti penawaran khusus atau keuntungan tambahan kepada nasabah yang konsisten melakukan pembayaran tagihan secara penuh setiap bulannya
11. Tim *marketing* dapat menawarkan program khusus seperti peningkatan limit kartu kredit, akses ke fitur dan layanan eksklusif, atau pemberian poin reward yang lebih besar seperti penawaran dengan bunga rendah atau program promosi eksklusif. Selain itu, tim marketing dapat melibatkan nasabah dalam program loyalitas yang memungkinkan mereka mengumpulkan poin dan menukarkannya dengan hadiah atau diskon di mitra bank Bangtut kepada nasabah-nasabah yang sudah berlangganan kartu kredit di bank Bangtut selama 1 tahun atau lebih
12. Tim *marketing* dapat menawarkan *reward* yang menarik, penawaran khusus, atau diskon spesial untuk nasabah-nasabah kartu kredit baru
