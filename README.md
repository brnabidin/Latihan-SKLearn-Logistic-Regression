# Latihan-SKLearn-Logistic-Regression

**Tahapan Latihan**

Tahapan yang dilalui dalam latihan kali ini adalah sebagai berikut:

- Ubah dataset menjadi Dataframe.

- Hapus kolom 'User ID'.

- Pisahkan atribut dan label.

- Latih model Logistic Regression.

- Evaluasi akurasi model.


**Codelab**

Dataset untuk latihan bisa Anda unduh pada tautan https://www.kaggle.com/dragonheir/logistic-regression berikut. Seperti biasa, unggah dataset Social_Network_Ads pada session storage Google Colab.

Setelah kita mengunggah berkas data pada Colab kita akan mengubah dataset menjadi dataframe Pandas. Jangan lupa untuk mengimpor library dasar dan menyesuaikan path/lokasi datanya ya.

![1](https://github.com/brnabidin/Latihan-SKLearn-Logistic-Regression/assets/67081096/724464d5-22c9-40ce-ba8d-1913d4739809)

Pada cell selanjutnya gunakan fungsi head() pada dataframe untuk melihat 5 baris pertama dari dataset.

![2](https://github.com/brnabidin/Latihan-SKLearn-Logistic-Regression/assets/67081096/99907f66-1f65-4823-ac18-fa214fe020f1)

Hasil dari fungsi df.head() seperti di bawah ini.

![202004302238474d62c7da27d447baa0b8d30b89f3e4bc](https://github.com/brnabidin/Latihan-SKLearn-Logistic-Regression/assets/67081096/6baa07fc-8899-4f7e-a533-4e00192514d8)

Kita juga perlu melihat apakah ada nilai yang kosong pada setiap atribut dengan menggunakan fungsi info(). Dapat dilihat bahwa nilai pada semua kolom sudah lengkap.

![3](https://github.com/brnabidin/Latihan-SKLearn-Logistic-Regression/assets/67081096/dd60ad41-a536-46e9-81ca-45e43b1e3f6b)

Sedangkan tampilan hasil dari fungsi df.info() sebagai berikut.

![20200430223940c9aee990b8a1763c632e1362f5f26a2c](https://github.com/brnabidin/Latihan-SKLearn-Logistic-Regression/assets/67081096/4b733b3a-0767-47bd-84ea-1d699e072b9c)

Pada dataset terdapat kolom ‘User ID’. Kolom tersebut merupakan atribut yang tidak penting untuk dipelajari oleh model sehingga perlu dihilangkan. Untuk menghilangkan kolom dari dataframe, gunakan fungsi drop. Jangan lupa panggil fungsi get_dummies() untuk melakukan proses One-Hot Encoding karena label pada dataset kita merupakan data kategorikal.

![4](https://github.com/brnabidin/Latihan-SKLearn-Logistic-Regression/assets/67081096/0f12d12f-d9ae-4a35-a2ce-10b4a7d81618)

Ketika kode di atas dijalankan hasilnya seperti di bawah ini.

![202004302240572131844a873e8b6bf9f7605bae936cd0](https://github.com/brnabidin/Latihan-SKLearn-Logistic-Regression/assets/67081096/32c104dc-b097-4ea2-bed7-0857e73f8dc5)

Kemudian kita pisahkan antara atribut dan label.

![5](https://github.com/brnabidin/Latihan-SKLearn-Logistic-Regression/assets/67081096/38405468-dd5b-4379-9e63-c879c1761c29)

Sebelum kita membagi data menjadi train dan test set, kita perlu melakukan standardisasi data

![6](https://github.com/brnabidin/Latihan-SKLearn-Logistic-Regression/assets/67081096/1b864de7-f107-42d3-8a71-bb76f6692574)

Sekarang, kita akan membagi data menjadi train dan test set dengan fungsi train_test_split yang disediakan SKLearn.

![7](https://github.com/brnabidin/Latihan-SKLearn-Logistic-Regression/assets/67081096/914131ea-74e5-484b-bd04-63a8d3cda0f6)

Setelah membagi data, kita buat model dengan membuat sebuah objek logistic regression. Setelah model dibuat, kita bisa melatih model kita dengan train set menggunakan fungsi fit().

![8](https://github.com/brnabidin/Latihan-SKLearn-Logistic-Regression/assets/67081096/1cfacfcc-b48b-4b96-bea5-fa36313e6dd0)

Setelah model dilatih, kita bisa menguji akurasi model pada test set dengan memanggil fungsi score() pada objek model.

![9](https://github.com/brnabidin/Latihan-SKLearn-Logistic-Regression/assets/67081096/2254573e-a2c3-46e8-af2e-ba92ec39ad1c)

Sehingga hasilnya sebagai berikut.

![202010261403083dff36fc0eb4f15b7e9ce67d682731bb](https://github.com/brnabidin/Latihan-SKLearn-Logistic-Regression/assets/67081096/121bfd49-19a2-48a4-946a-55bd9b45a5f9)
