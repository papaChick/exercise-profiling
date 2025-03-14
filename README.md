# Profiling

<details>
  <summary><h2>Before optimization</h2></summary>
  
  <details><summary><h3>/all-students endpoint</h3></summary>
    
  ![test-plan-1-tree](https://github.com/user-attachments/assets/e78ad1db-da27-4053-96ea-ef12c1fbd1b9)
  ![test-plan-1-table](https://github.com/user-attachments/assets/21260a57-2d13-4ef8-a90c-f4b93992ff01)
  ![test-plan-1-report](https://github.com/user-attachments/assets/326b7fcc-bcd1-41b6-97ac-1589f43b87f0)
  ![test-plan-1-graph](https://github.com/user-attachments/assets/aad2c2a5-baaa-40cc-a323-34a5340fd03e)
  ![image](https://github.com/user-attachments/assets/4ad4ab9d-1e33-4bcb-9779-afabd3f08eaf)
  
  </details>

  <details><summary><h3>/all-students-name endpoint</h3></summary>
    
  ![test-plan-2-tree](https://github.com/user-attachments/assets/6f556d11-2885-4c63-bf81-71cd32883c63)
  ![test-plan-2-table](https://github.com/user-attachments/assets/a99d64df-f69d-43d4-aa1f-cddd56425d8c)
  ![test-plan-2-report](https://github.com/user-attachments/assets/b90251a0-0cba-40eb-a937-4ed676ca45ae)
  ![test-plan-2-graph](https://github.com/user-attachments/assets/c61c67c6-b07b-458c-8b7f-76eaa77cb380)
  ![image](https://github.com/user-attachments/assets/17ca74ab-c77e-4024-8fa1-a881009ab275)

  </details>

  <details><summary><h3>/highest-gpa endpoint</h3></summary>

  ![test-plan-3-tree](https://github.com/user-attachments/assets/be2436e3-3d14-43cf-9292-aaa316e79a73)
  ![test-plan-3-table](https://github.com/user-attachments/assets/a695deae-90f6-4c2c-92a9-613d467597a7)
  ![test-plan-3-report](https://github.com/user-attachments/assets/9a8b8e8e-e9a1-4e82-ac4d-8749066114d3)
  ![test-plan-3-graph](https://github.com/user-attachments/assets/5cc86814-c813-4ecd-9d81-bd162a1881c6)
  ![image](https://github.com/user-attachments/assets/e94e6c0a-f8b4-49ed-9b2c-fa6773b98bdd)

  </details>
</details>



<details>
  <summary><h2>After optimization</h2></summary>

  <details><summary><h3>/all-students endpoint</h3></summary>
    
  ![image](https://github.com/user-attachments/assets/4fe85091-78e1-4f44-9d54-fc67d808cd0c)
  ![image](https://github.com/user-attachments/assets/c8da66ed-9252-4a50-945e-bda84923cd64)
  ![image](https://github.com/user-attachments/assets/d7c99517-fc6e-450f-add1-448c27e79c03)
  ![image](https://github.com/user-attachments/assets/027ce7b5-7702-4b8a-b8d5-fbe05a00006d)
  ![image](https://github.com/user-attachments/assets/793456a4-1360-4d04-b362-f8246982861d)

  </details>

  <details><summary><h3>/all-students-name endpoint</h3></summary>

  ![image](https://github.com/user-attachments/assets/b4f05198-80c9-486c-a11c-7aa3c2f13cfa)
  ![image](https://github.com/user-attachments/assets/9133c418-43ac-4e22-9ead-37f5d096c17f)
  ![image](https://github.com/user-attachments/assets/17419e05-7d4e-482f-ba5e-e63d0d58e26a)
  ![image](https://github.com/user-attachments/assets/8422ae31-92e1-4ac2-8c4d-aea3db7e0ed5)
  ![image](https://github.com/user-attachments/assets/574a3ae8-c142-4344-9362-e66931b59ad0)

  </details>

  <details><summary><h3>/highest-gpa endpoint</h3></summary>

  ![image](https://github.com/user-attachments/assets/d3a66c6f-b158-4243-8f95-ba1d63b63230)
  ![image](https://github.com/user-attachments/assets/e17c717f-e20a-422d-bd57-47e2c4abe8dd)
  ![image](https://github.com/user-attachments/assets/b22f8afb-379e-40fd-be25-15e05812d0ed)
  ![image](https://github.com/user-attachments/assets/7adcb9f5-48ed-49e0-947d-4ae0629d4686)
  ![image](https://github.com/user-attachments/assets/fa9ba82f-1c10-4527-9fbd-b58e726a3ca4)

  </details>
</details>

## Conclusion
Dilihat dari gambar diatas, dapat disimpulkan bahwa terdapat kemajuan drastis setelah kode dioptimisasi.
Jika digeneralisasikan, proses pengambilan data pada setiap endpoint mengalami percepatan sebesar 50% hingga 92%.
Hal tersebut menunjukan bahwa proses optimisasi menggunakan profiling berdampak besar pada performa dari sistem untuk mengurangi bottleneck dan waktu kinerja.

### 

# Reflection
1. **What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?**  
   JMeter mensimulasikan pengguna dalam jumlah tertentu, menghasilkan *load*, dan menghitung waktu response, throughput, dan perilaku sistem dibawah tekanan. _Approach_ ini membantu mengidentifikasi masalah skalabilitas dan konkurensi.
   Sedangkan, IntelliJ Profiler digunakan untuk memberikan informasi mendalam mengenai penggunaan CPU, konsumsi memori, dan aktivitas _thread_ pada kode. _Approach_ ini membantu mendeteksi kelemahan kinerja pada kode agar dapat dioptimisasi secara efektif.
2. **How does the profiling process help you in identifying and understanding the weak points in your application?**  
   Profiling menyediakan metrik waktu tentang waktu eksekusi metode, alokasi memori, dan perilaku thread.
   Hal tersebut memungkinkan analisis mendalam terhadap kelemahan kinerja, seperti loop yang tidak efisien, pembuatan objek yang tidak perlu, atau keterlambatan pada kueri basis data.
   Dengan menganalisis flame graph dan data CPU sampling, kita dapat mengidentifikasi masalah dalam kode yang mempengaruhi kinerja.
3. **Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?**  
   _Bottlenecks_ umumnya disebabkan oleh proses yang membutuhkan CPU dan memori yang berlebih, namun dibatasi oleh kapasitas kinerja komputer. IntelliJ Profile dalam memberikan _insight_ terhadap penggunaan CPU dan memori, yang memungkinkan _developer_ dapat memahami bagaimana aplikasi mengonsumsi sumber daya.
   Namun, perlu disari bahwa IntelliJ profiler tidak selalu mencerminkan masalah beban dunia nyata, sehingga JMeter dapat dijadikan pelengkap dalam pengujian kinerja.
4. **What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?**  
   Performance testing dan profiling menjadi tantangan utama saya daat melakukan identifikasi bottleneck. Saya kebingungan untuk memahami bagian dari kode yang menjadi bottleneck. Hal ini disebabkan oleh banyaknya data yang dihasilkan, dan antarmuka yang tidak biasa saya jumpai.
   Cara saya menanganinya adalah dengan mencoba memahami hasil output tools, sehingga dapat menyimpulkan hasil yang didapat dari tools tersebut untuk mengoptimisasi program.
5. **What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?**  
   IntelliJ Porfiler memampukan kita sebagai developer untuk mengindentifikasi kelemahan kinerja melalui penggunaan CPU, konsumsi meomri, dan aktivitas _thread_. Selain itu, melalui hasil, kita dapat langsung diarahkan kepada source code yang menyebabkan masalah kinerja tersebut, sehingga tidak butuh untuk navigasi codebase lagi.
6. **How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?**  
   Disaat dihadapi situasi ketidakkonsistenan seperti diatas, perlu kita sadari bahwa kedua tools memiliki _approach_ yang berbeda. Intellij mengukur konsumi memori dan CPU sedangkan JMeter mengukur perilaku sistem dibawah tekanan. Ketidakkonsistenan ini dapat diatas dengan menguji program yang diisolasi pada suatu container. Contoh container yang dapat digunakan adalah docker.
7. **What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?**  
   Strategi saya dalam optimisasi kode dimulai dengan memahi alur kerja blok kode yang bermasalah. Kemudian, mengidentifikasi kode yang terkesan redundan dan dapat diganti dengan kode yang lebih efektif. Kode tersebut divalidasi lagi untuk memastikan tetap bekerja sesuai tujuan dan kinerjanya mengalami peningkatan. Unit test dapat digunakan untuk meminimalisir usaha dalam melakukan test yang secara berulang untuk memastikan kode berjalan seperti tujuan.