**Nama : Nisrina Annaisha Sarnadi  
NPM : 2306275960  
Kelas : B**
***
## Test Plan
### Before Optimizing
#### /all-student
<img width="960" alt="before-1" src="https://github.com/user-attachments/assets/d5fc2504-ce51-4ad4-9b79-e7dae43cb002" />
<img width="960" alt="before-1-1" src="https://github.com/user-attachments/assets/cd54c670-4278-474a-bc31-a865f3f3c550" />

#### /all-student-name
<img width="960" alt="before-2" src="https://github.com/user-attachments/assets/907bf9c6-df22-4494-9e6f-b559e6396d39" />
<img width="960" alt="before-2-1" src="https://github.com/user-attachments/assets/14204946-9212-4904-9c79-8ef5e228208d" />

#### /highest-gpa
<img width="960" alt="before-3" src="https://github.com/user-attachments/assets/179ef280-0179-4d60-8003-6138090ee3be" />
<img width="960" alt="before-3-1" src="https://github.com/user-attachments/assets/180c8a2d-d595-4fec-afb4-229a5bcda465" />

### After Optimizing
#### /all-student
<img width="960" alt="after-1" src="https://github.com/user-attachments/assets/54cbcda2-77c0-4e0d-9f90-1823262734dc" />
<img width="960" alt="Screenshot 2025-03-14 201456" src="https://github.com/user-attachments/assets/98ddfbf7-4d14-4ff2-91c7-3a679941ecb9" />

#### /all-student-name
<img width="960" alt="Screenshot 2025-03-14 201456" src="https://github.com/user-attachments/assets/18fe84e1-28db-43d6-b0c4-cc9d680d9dba" />
<img width="960" alt="Screenshot 2025-03-14 203805" src="https://github.com/user-attachments/assets/937ad00f-e464-4785-96f3-ebbe2337421a" />

#### /highest-gpa
<img width="960" alt="after-3" src="https://github.com/user-attachments/assets/05896fbb-486d-46cc-9c94-3507b72f1d72" />
<img width="960" alt="Screenshot 2025-03-14 204019" src="https://github.com/user-attachments/assets/4c7604c0-ccb5-470d-85c2-86e6eaea3378" />

### Conclusion
#### /all-student
Sebelum optimasi, waktu sampel berada di atas 50.000 ms. Setelah dilakukan optimasi, waktu sampel menurun secara signifikan menjadi kurang lebih 2.000 ms, menunjukkan peningkatan performa sebesar 96%.

#### /all-student-name
Sebelum optimasi, waktu sampel berada di kisaran 1.000 ms. Setelah optimasi, waktu sampel berkurang drastis hingga mencapai sekitar 60 ms, dengan peningkatan performa sebesar 94%.

#### /highest-gpa
Sebelum optimasi, waktu sampel berkisar antara 50 hingga 60 ms. Setelah optimasi, waktu sampel menurun menjadi sekitar 10-20 ms, menghasilkan peningkatan performa hingga 66,67%.

## Reflection

**1. Difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler**  
JMeter adalah alat untuk menguji performa suatu program dengan mensimulasikan aktivitas dengan beban pengguna tertentu. JMeter ini menguji program dari sisi eksternal, termasuk analisis waktu respons API, kecepatan pemrosesan, serta kemungkinan terjadinya error. 
Sementara itu, IntelliJ Profiler adalah alat untuk menganalisis performa aplikasi secara internal dengan memantau penggunaan CPU, memori, dan thread, serta mengidentifikasi bottleneck dalam kode melalui alur eksekusi yang mendetail.  
   
**2. How does the profiling process help me in identifying and understanding the weak points in your application?**  
Profiling membantu mengidentifikasi method atau fungsi yang banyak menggunakan CPU atau memori, serta mengevaluasi alokasi objek yang tidak efisien yang dapat menyebabkan garbage collection berlebihan. Selain itu, profiling mendeteksi deadlock atau thread terblokir yang memperlambat eksekusi. Dengan visualisasi alur eksekusi, proses ini mempermudah menemukan dan menganalisis penyebab utama penurunan performa aplikasi.

**3. Do I think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?**  
Ya, IntelliJ Profiler efektif karena menyediakan analisis mendalam terkait performa kode. Fitur ini memungkinkan kita untuk melihat method yang paling banyak menggunakan CPU, penggunaan memori heap, serta aktivitas thread. Dengan adanya fitur visualisasi seperti flame graph dan call tree, kita dapat dengan cepat mengidentifikasi bagian kode yang perlu dioptimalkan.

**4. Main challenges I face when conducting performance testing and profiling, and how do you overcome these challenges?**  
Tantangan dalam performance testing dengan JMeter mencakup penyusunan skenario realistis, menjaga stabilitas server dan jaringan, serta pengelolaan sumber daya agar hasil uji tetap akurat. Sementara itu, profiling dengan IntelliJ Profiler menghadapi kendala seperti kompleksitas data, risiko overhead, dan penentuan perubahan kode yang benar-benar efektif.  
Tantangan ini dapat diatasi dengan menggunakan environment uji yang mendekati kondisi pengembangan, menganalisis profiling secara bertahap untuk mengisolasi masalah, serta mengombinasikan JMeter dan IntelliJ Profiler guna memperoleh gambaran performa aplikasi secara menyeluruh dan melakukan optimasi yang lebih tepat.

**5. What are the main benefits I gain from using IntelliJ Profiler for profiling your application code?**  
- Menemukan bagian kode atau metode yang menjadi penyebab bottleneck.  
- Memberikan visualisasi performa seperti flame graph dan call tree untuk analisis yang lebih jelas.  
- Membantu menganalisis penggunaan CPU dan memori secara mendalam.  
- Dapat digunakan bersamaan dengan debugging untuk memahami eksekusi kode secara real-time.
  
**6. How do I handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?**  
Jika hasil dari IntelliJ Profiler dan JMeter tidak sama, langkah pertama saya adalah mengecek apakah keduanya dijalankan dalam kondisi yang sama, seperti beban sistem dan konfigurasi server. Perbedaan hasil bisa terjadi karena faktor eksternal, seperti koneksi jaringan atau proses lain yang berjalan di latar belakang. Untuk memastikannya, pengujian bisa diulang dengan lebih terkontrol. Jika masih ada perbedaan, data dari kedua alat bisa dibandingkan untuk mencari pola yang paling mungkin menjadi penyebab masalah, lalu dilakukan perbaikan yang sesuai.

**7. What strategies do I implement in optimizing application code after analyzing results from performance testing and profiling? How do I ensure the changes you make do not affect the application's functionality?**  
Strategi saya untuk mengoptimalkan kode aplikasi setelah menganalisis hasil pengujian performa dan profiling sebagai berikut:  
- Mengoptimalkan Algoritma dan Struktur Data: Mengganti algoritma yang kurang efisien dengan yang lebih optimal serta menggunakan struktur data yang sesuai untuk meningkatkan efisiensi pemrosesan.
- Memanfaatkan Caching: Menyimpan hasil yang sering digunakan untuk mengurangi beban pemrosesan dan meningkatkan kecepatan respons aplikasi.
- Memperbaiki Query Database: Mengoptimalkan query SQL, menambahkan indeks yang diperlukan, dan menghindari query yang terlalu kompleks agar interaksi dengan database lebih efisien.
  
Saya memastikan setiap perubahan tidak memengaruhi fungsionalitas aplikasi dengan melakukan pengujian menyeluruh, termasuk unit test, dan integration test, agar fitur yang sudah ada tetap berfungsi dengan baik. Selain itu, pemanfaatan CI/CD pipeline membantu mengotomatiskan proses pengujian dan penerapan perubahan. Sebelum diterapkan ke sistem utama, aplikasi juga diuji di lingkungan staging yang menyerupai kondisi produksi untuk memastikan stabilitasnya.
