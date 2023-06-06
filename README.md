# EnigmaGroup_JC_DS_FT_JKT_19_FinalProject

# Dashboard
Google Looker Studio: [https://lookerstudio.google.com/reporting/bfba7d0c-8be5-492c-8188-f57d1bdc3952](https://lookerstudio.google.com/reporting/bfba7d0c-8be5-492c-8188-f57d1bdc3952)

# 1. Business Problem Understanding

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
