###PENDAHULUAN
Penetration Testing (disingkat pentest) adalah suatu kegiatan dimana seseorang mencoba mensimulasikan serangan yang bisa dilakukan terhadap jaringan organisasi / perusahaan tertentu untuk menemukan kelemahan yang ada pada sistem jaringan tersebut. Orang yang melakukan kegiatan ini disebut penetration tester (disingkat pentester). Penetration Testing mempunyai standar resmi sebagai acuan dalam pelaksanaannya. 

Penetration Testing memiliki standar (PTES) yang digunakan sebagai acuan dalam pelaksanaanya yang dibagi ke dalam beberapa tahap :

- **Pre-engagement Interactions**

Tahap dimana seorang pentester menjelaskan kegiatan pentest yang akan dilakukan kepada client (perusahaan). Disini seorang pentester harus bisa menjelaskan kegiatan-kegiatan yang akan dilakukan dan tujuan akhir yang akan dicapai.

- **Intelligence Gathering**

Tahap dimana seorang pentester berusaha mengumpulkan sebanyak mungkin informasi mengenai perusahaan target yang bisa didapatkan dengan berbagai metode dan berbagai media. Hal yang perlu dijadikan dasar dalam pengumpulan informasi adalah : karakteristik sistem jaringan, cara kerja sistem jaringan, dan metode serangan yang bisa digunakan.

- **Threat Modeling**

Tahap dimana seorang pentester mencari celah keamanan (vulnerabilities) berdasarkan informasi yang berhasil dikumpulkan pada tahap sebelumnya. Pada tahap ini seorang pentester tidak hanya mencari celah keamanan, tetapi juga menentukan celah yang paling efektif untuk digunakan.

- **Vulnerability Analysis**

Tahap dimana seorang pentester mengkombinasikan informasi mengenai celah keamanan yang ada dengan metode serangan yang bisa dilakukan untuk melakukan serangan yang paling efektif.

- **Exploitation**

Tahap dimana seorang pentester melakukan serangan pada target. Walaupun demikian tahap ini kebanyakan dilakukan dengan metode brute force tanpa memiliki unsur presisi. Seorang pentester profesional hanya akan melakukan exploitation ketika dia sudah mengetahui secara pasti apakah serangan yang dilakukan akan berhasil atau tidak. Namun tentu saja ada kemungkinan tidak terduga dalam sistem keamanan target. Walaupun begitu, sebelum melakukan serangan, pentester harus tahu kalau target mempunyai celah keamanan yang bisa digunakan. Melakukan serangan secara membabi-buta dan berharap sukses bukanlah metode yang produktif. Seorang pentester profesional selalu menyempurnakan analisisnya terlebih dahulu sebelum melakukan serangan yang efektif.

- **Post Exploitation**

Tahap dimana seorang pentester berhasil masuk ke dalam sistem jaringan target dan kemudian melakukan analisis infrastruktur yang ada. Pada tahap ini seorang pentester mempelajari bagian-bagian di dalam sistem dan menentukan bagian yang paling critical bagi target (perusahaan). Disini seorang pentester harus bisa menghubungkan semua bagian-bagian sistem yang ada untuk menjelaskan dampak serangan / kerugian yang paling besar yang bisa terjadi pada target (perusahaan).

- **Reporting**

Reporting adalah bagian paling penting dalam kegiatan pentest. Seorang pentester menggunakan report (laporan) untuk menjelaskan pada perusahaan mengenai pentesting yang dilakukan seperti : apa yang dilakukan, bagaimana cara melakukannya, resiko yang bisa terjadi dan yang paling utama adalah cara untuk memperbaiki sistemnya.

Penetration testing biasanya menggunakan sebuah tools khusus yang memang dirancang untuk menemukan kelemahan pada sebuah sistem. Tools yang umum digunakan adalah metasploit. Metasploit adalah sebuah framework yang berisi tools-tools yang diperlukan untuk melakukan penetration testing.
