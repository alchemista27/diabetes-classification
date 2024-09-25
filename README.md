# Diabetes Classification
Project ini adalah sebuah pengembangan model untuk melakukan klasifikasi terhadap gejala yang dialami pengidap beberapa jenis Diabetes. Dataset yang digunakan dalam pengembangan model ini diperoleh dari [sini](https://www.kaggle.com/datasets/ankitbatra1210/diabetes-dataset).

***

## Karakteristik Data
Dataset terdiri 70000 baris - *entries* dengan jumlah kolom sebanyak 34. Daftar kolom pada dataset adalah sebagai berikut:
| Kolom | Data Types |
|-------|------------|
| Target | object |
| Genetic Markers | object|
|Autoantibodies | object|
|Family History|object|
|Environmental Factors|object|
|Insulin Levels| int64| 
|Age  |int64| 
|BMI |int64| 
|Physical Activity | object|
|Dietary Habits | object|
|Blood Pressure| int64 |
|Cholesterol Levels| int64 |
|Waist Circumference| int64 |
|Blood Glucose Levels|  int64| 
|Ethnicity | object|
|Socioeconomic Factors |object|
|Smoking Status |object|
|Alcohol Consumption |object|
|Glucose Tolerance Test|object|
|History of PCOS |object|
|Previous Gestational Diabetes |object|
|Pregnancy History| object|
|Weight Gain During Pregnancy|int64| 
|Pancreatic Health |int64 |
|Pulmonary Function |int64 |
|Cystic Fibrosis Diagnosis|object|
|Steroid Use History|object|
|Genetic Testing|object|
|Neurological Assessments | int64 |
|Liver Function Tests|object|
|Digestive Enzyme Levels |int64 |
|Urine Test |object|
|Birth Weight |int64 |
|Early Onset Symptoms |object|

***

## Tahapan Pengembangan Model
Pengembangan model klasifikasi yang digunakan pada project ini dimulai dengan tahapan sebagai berikut:
1. Pembersihan data dari *missing value*
2. Memastikan integritas data pada setiap kolom
3. Memisahkan `target` dan `features` dalam dua dataframe berbeda
4. Menggunakan modul `LabelEndoder()` dari sklearn untuk memproses tipe data `object` menjadi angka
5. Menggunakan modul `StandardScaler()` dari sklearn untuk mentandarisasi tipe data `int64`
6. Melakukan spliting set untuk train dan test dengan menggunakan modul `train_test_split()` dari sklearn
7. Menjalankan klasifikasi dengan menggunakan modul `RandomForestClassifier()`
8. Melakukan klasifikasi dengan model lain seperti:
   * Support Vector Machine
   * KNearest Neighbors
   * Decision Tree
***

## Hasil dan Kualitas model
Kualitas model diukur dengan menggunakan skor akurasi. Berdasarkan prediksi yang dilakukan pada set test dari data yang dimiliki diperoleh hasil akurasi model sebagai berikut:

| Model | Accuracy Score |
|-------|----------------|
|Random Forest | 0.90 |
|Support Vector Machine | 0.78 |
| KNN | 0.49 |
| Decision Tree | 0.86 |
***
## Peluang Pengembangan
Dalam model yang dikembangkan ini diketahui bahwa Random Forest masih menjadi model dengan akurasi paling tinggi `0.90`, hal ini diperoleh hanya dengan mengubah parameter `n_estimators` menjadi 300. Pengujian terhadap kombinasi parameter lainnya perlu dilakukan dengan menggunakan teknik Cross Validation.