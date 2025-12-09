# Prediksi Kemenangan VCT 2024
![](https://cmsassets.rgpub.io/sanity/images/dsfx7636/news/2f9c08f0f5b47f688edc8becde8fdd7e7e91bcb2-854x484.png?auto=format&fit=crop&q=80&h=319&w=567&crop=center)

## Project Overview:

Proyek data science ini bertujuan untuk menganalisis statistik performa pemain dalam turnamen Valorant Champions Tour (VCT) 2024 untuk memprediksi apakah sebuah tim akan memenangkan pertandingan atau tidak. Data yang digunakan mencakup metrik performa seperti Average Combat Score (ACS), Rating, Kill/Death Ratio, First Kill, Damage per Round, dan statistik lain yang mempengaruhi hasil akhir pertandingan.
Dengan memahami variabel kunci yang berperan dalam kemenangan tim, analisis ini diharapkan dapat membantu organisasi esports melakukan evaluasi performa, menentukan strategi, dan meningkatkan peluang kemenangan.

## Data Dictionary:

| Variabel    | Deskripsi                                                   |
| ----------- | ----------------------------------------------------------- |
| Team        | Nama tim                                                    |
| Opponent    | Tim lawan                                                   |
| Map         | Peta yang dimainkan                                         |
| Result      | Hasil pertandingan (Win/Lose)                               |
| Rating      | Performansi keseluruhan pemain (0–3)                        |
| ACS         | Average Combat Score                                        |
| KDR         | Kill/Death Ratio                                            |
| ADR         | Average Damage per Round                                    |
| KAST        | Persentase kontribusi pemain (Kill, Assist, Survive, Trade) |
| KPR         | Kill per Round                                              |
| APR         | Assist per Round                                            |
| FKPR        | First Kill per Round                                        |
| FDPR        | First Death per Round                                       |
| HS%         | Persentase headshot                                         |
| CL          | Total clutch berhasil                                       |
| CL%         | Persentase clutch success                                   |
| KMax        | Kill terbanyak dalam satu map                               |
| Total K/D/A | Total kills, deaths, assists                                |
| Role        | Peran pemain (Duelist, Initiator, Controller, Sentinel)     |


## Conclusion:

Dari analisis dan evaluasi model, beberapa temuan utama adalah:

Model klasifikasi terbukti efektif dalam memprediksi kemenangan tim berdasarkan performa individu. Baik SVM maupun Random Forest menunjukkan performa kuat ketika target didefinisikan menggunakan median ACS sebagai pembeda antara Win/Loss.

Support Vector Machine (RBF Kernel) mampu menangkap hubungan non-linear antar fitur. Model ini mencapai:

Recall Win: 88.89%

Recall Loss: 77.61%

AUC: 0.92
Hasil ini menunjukkan kemampuan SVM dalam membedakan dua kelas prediksi secara cukup akurat.

Random Forest merupakan model terbaik dalam penelitian ini. Dengan parameter yang telah dioptimalkan, model menghasilkan:

Akurasi: 93.56%

Recall Win: 95.73%

Recall Loss: 91.38%

AUC: 0.98
RF menunjukkan performa paling seimbang dan akurat dalam memproses variabilitas data performa pemain.

Feature importance dari Random Forest menunjukkan tiga metrik paling berpengaruh terhadap peluang kemenangan tim:

Kills per Round (KPR): 28.4%

Damage per Round (ADR): 22.7%

Kill/Death Ratio (K:D): 13.2%
Ketiganya berperan lebih dari 64% dalam prediksi, menegaskan bahwa agresivitas dan efektivitas pertempuran merupakan indikator utama kemenangan.

Evaluasi visual seperti confusion matrix, ROC Curve, dan distribusi ACS menunjukkan bahwa pendekatan median split terhadap ACS valid dan stabil, dengan bias prediksi yang rendah dan tidak ekstrem.

Tidak terjadi overfitting, dibuktikan oleh selisih akurasi train–test yang kecil (sekitar 1.5%) serta hasil cross-validation yang konsisten dengan deviasi antar fold yang rendah.
