# TUTORIAL - 5
### ScreenShoot JMeter Test Plans Before Profiling
#### /all-student
![all-student-before-profiling-jmeter.png](Screenshot_Tutorial_5%2FBefore_Profiling%2Fall-student-before-profiling-jmeter.png)

![all-student-before-profiling-jtl.png](Screenshot_Tutorial_5%2FBefore_Profiling%2Fall-student-before-profiling-jtl.png)

#### /all-student-name
![all-student-name-before-profiling-jmeter.png](Screenshot_Tutorial_5%2FBefore_Profiling%2Fall-student-name-before-profiling-jmeter.png)

![all-student-name-before-profiling-jtl.png](Screenshot_Tutorial_5%2FBefore_Profiling%2Fall-student-name-before-profiling-jtl.png)

#### /highest-gpa
![highest-gpa-before-profiling-jmeter.png](Screenshot_Tutorial_5%2FBefore_Profiling%2Fhighest-gpa-before-profiling-jmeter.png)

![highest-gpa-before-profiling-jtl.png](Screenshot_Tutorial_5%2FBefore_Profiling%2Fhighest-gpa-before-profiling-jtl.png)


### ScreenShoot JMeter Test Plans Before Profiling
#### /all-student
![all-student-after-profiling.png](Screenshot_Tutorial_5%2FAfter_Profiling%2Fall-student-after-profiling.png)

#### /all-student-name
![all-student-name-after-profiling.png](Screenshot_Tutorial_5%2FAfter_Profiling%2Fall-student-name-after-profiling.png)

#### /highest-gpa
![highest-gpa-after-profiling.png](Screenshot_Tutorial_5%2FAfter_Profiling%2Fhighest-gpa-after-profiling.png)

### Analisis dan Kesimpulan
Berdasarkan hasil dari Jmeter didapat bahwa:
1. `all-student`

    - Waktu yang dibutuhkan untuk melaksanakan operasi (sebelum profiling) adalah ~55000 ms

    - Waktu yang dibutuhkan untuk melaksanakan operasi (setelah profiling) adalah ~2500 ms

  Dengan dilakukannya profiling, kode berjalan sekitar 95% lebih cepat. Sehingga dapat dikatakan bahwa profiling berhasil


2. `all-student-name`

   - Waktu yang dibutuhkan untuk melaksanakan operasi (sebelum profiling) adalah ~800 ms

   - Waktu yang dibutuhkan untuk melaksanakan operasi (setelah profiling) adalah ~70 ms

Dengan dilakukannya profiling, kode berjalan sekitar 91% lebih cepat. Sehingga dapat dikatakan bahwa profiling berhasil



3. `highest-gpa`

   - Waktu yang dibutuhkan untuk melaksanakan operasi (sebelum profiling) adalah ~70 ms

   - Waktu yang dibutuhkan untuk melaksanakan operasi (setelah profiling) adalah ~12 ms

Dengan dilakukannya profiling, kode berjalan sekitar 82% lebih cepat. Sehingga dapat dikatakan bahwa profiling berhasil


## Refleksi
1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?  
   Jawab: Pengujian kinerja menggunakan JMeter melibatkan simulasi perilaku pengguna untuk mengukur respons aplikasi, fokus pada waktu respons, throughput, dan penggunaan sumber daya. Ini membantu mengidentifikasi titik-titik lemah untuk perbaikan. Namun, pendekatan ini hanya memperhatikan respons tanpa memperhatikan detail cara kerja aplikasi. Di sisi lain, profiling dengan IntelliJ Profiler menganalisis perilaku aplikasi secara detail, memungkinkan kita untuk mengetahui bagian program mana yang memakan waktu lebih lama dan memahami kinerja aplikasi secara lebih rinci dengan pola penggunaan memori dan waktu CPU bekerja. Dengan informasi dari profiling, kita dapat mengoptimalkan bagian-bagian kode yang mempengaruhi kinerja aplikasi secara signifikan

2. How does the profiling process help you in identifying and understanding the weak points in your application?  
   Jawab: Proses profiling membantu mengidentifikasi dan memahami bagaimana alur kode dalam aplikasi berjalan dengan memantau perilaku saat aplikasi berjalan, termasuk penggunaan CPU, alokasi memori, pemanggilan metode, dan aktivitas thread. Dengan menganalisis data ini, kita dapat mengungkap ketidak-efisienan, bottlenecks, atau penggunaan sumber daya yang berlebihan. Alat-alat profiling juga memberikan representasi visual dari alur runtime aplikasi, memudahkan kita mengidentifikasi bagian kode yang perlu diperbaiki dan memungkinkan pengoptimalan yang lebih terarah

3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?  
   Jawab: Ya, IntelliJ Profiler dapat sangat efektif dalam membantu pengembang menganalisis dan mengidentifikasi bottlenecks dalam kode aplikasi. Sebagai contoh, dalam tutorial dan exercise pada modul 5, kita dapat melihat bahwa ada beberapa metode yang memiliki kinerja lebih lambat. Dengan mengetahui baris kode mana yang menjadi bottlenecks melalui profiling, kita dapat dengan mudah mengidentifikasi bagian program yang mempengaruhi kinerja aplikasi

4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?  
   Jawab: Dalam melakukan pengujian kinerja dan profiling, ada beberapa tantangan utama yang harus dihadapi. Salah satunya adalah memahami hasil output dan membandingkannya dengan output sebelumnya. Pada profiling, banyak informasi yang harus diperhatikan, sehingga kita perlu mencari dengan cermat. Selain itu, kita juga perlu merekam output sebelumnya, misalnya dengan mengambil screenshot atau kembali ke profil sebelumnya. Namun, yang paling penting adalah melakukan perbandingan side by side antara sebelum dan sesudah melakukan optimasi. Untuk mengatasi tantangan ini, kita perlu terbiasa menggunakan alat-alat tersebut dan selalu berhati-hati untuk mendapatkan informasi yang kita butuhkan

5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?  
   Jawab: Dengan menggunakan IntelliJ Profiler, kita tidak perlu mengandalkan aplikasi pihak ketiga, dan fitur profiling sudah terintegrasi dengan keseluruhan IDE. Hal ini memudahkan kita dalam melihat bagian kode yang mempengaruhi kinerja aplikasi, termasuk bottlenecks

6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?  
   Jawab: Dalam pengalaman saya sebelumnya, saya belum menemukan ketidaksesuaian antara hasil profiling menggunakan IntelliJ Profiler dan temuan dari pengujian kinerja dengan JMeter. Namun, jika terjadi perbedaan hasil antara keduanya, langkah pertama yang harus diambil adalah memeriksa kembali metode pengujian dan skenario yang digunakan dalam kedua alat tersebut. Selain itu, perbandingan metrik yang diukur oleh kedua alat dapat membantu mengidentifikasi perbedaan fokus atau ruang lingkup, seperti perbedaan perangkat keras atau perangkat lunak yang digunakan.

7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?  
   Jawab: Setelah menganalisis hasil dari pengujian kinerja dan profil, ada beberapa strategi yang dapat diterapkan untuk mengoptimalkan kode aplikasi. Langkah pertama yang saya lakukan adalah memeriksa durasi program menggunakan JMeter. Jika saya menemukan bahwa waktu eksekusi terlalu lama, saya akan mengidentifikasi bagian kode yang menyebabkan masalah tersebut dan mengoptimalkannya. Selain itu, saya selalu memastikan bahwa perubahan yang saya lakukan tidak memengaruhi fungsionalitas aplikasi dengan membandingkan output sebelum dan sesudah perubahan.