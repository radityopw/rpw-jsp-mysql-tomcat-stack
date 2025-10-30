# RPW JSP-MySQL-Tomcat Stack

Template (boilerplate) sederhana untuk memulai proyek aplikasi web Java menggunakan **JSP (JavaServer Pages)**, **MySQL**, dan **Tomcat 11**.

Proyek ini dirancang untuk mempercepat proses setup awal dengan menyertakan pustaka (library) esensial yang umum dibutuhkan untuk aplikasi web modern, sehingga Anda bisa langsung fokus pada logika bisnis.

## Tumpukan Teknologi (Tech Stack)

* **Server:** Apache Tomcat 11
* **Backend:** JavaServer Pages (JSP)
* **Database:** MySQL

## Fitur Utama (Pustaka yang Disertakan)

Template ini sudah menyertakan file `.jar` yang diperlukan di dalam direktori `WEB-INF/lib` untuk fungsionalitas umum:

* **[MySQL JDBC Driver](https://dev.mysql.com/downloads/connector/j/)**: Untuk menghubungkan aplikasi Java Anda ke database MySQL.
* **[Apache Commons IO](https://commons.apache.org/proper/commons-io/)**: Pustaka utilitas untuk mempermudah operasi I/O (Input/Output).
* **[Apache Commons FileUpload](https://commons.apache.org/proper/commons-fileupload/)**: Solusi tangguh untuk menangani `multipart/form-data` (upload file) dalam JSP/servlet.
* **[Apache Commons CSV](https://commons.apache.org/proper/commons-csv/)**: Pustaka untuk membaca dan menulis file CSV dengan mudah dan efisien.

## Persyaratan Sistem

Sebelum Anda memulai, pastikan Anda telah menginstal perangkat lunak berikut di sistem Anda:

* [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/downloads/) (Versi 11 atau yang lebih baru, sesuai kebutuhan Tomcat 11).
* [Apache Tomcat 11](https://tomcat.apache.org/download-11.cgi) (atau server kontainer servlet lain yang kompatibel).
* [MySQL Server](https://dev.mysql.com/downloads/mysql/).
* IDE Java (opsional, namun disarankan): [Apache NetBeans](https://netbeans.apache.org/), [IntelliJ IDEA](https://www.jetbrains.com/idea/), atau [Eclipse](https://www.eclipse.org/).

## Cara Menggunakan

1.  **Clone atau Unduh Repositori:**
    ```bash
    git clone [https://github.com/radityopw/rpw-jsp-mysql-tomcat-stack.git](https://github.com/radityopw/rpw-jsp-mysql-tomcat-stack.git)
    ```
    Atau unduh proyek ini sebagai file `.zip`.

2.  **Buka Proyek di IDE atau Text Editor Anda:**
    Buka proyek ini di IDE favorit Anda (misalnya, NetBeans, IntelliJ, Eclipse) sebagai "Web Project" atau impor dari folder yang ada. Tapi saya sarankan tidak usah pakai IDE, pakai text editor biasa saja.

3.  **Konfigurasi Database:**
    * Buat database baru di server MySQL Anda.
    * Sesuaikan konfigurasi koneksi database (URL, username, password) langsung di dalam file JSP Anda yang relevan (misalnya, di dalam skrip koneksi database).


Setelah di-deploy, Anda dapat mengakses aplikasi web Anda melalui browser.

## Struktur Proyek (Umum)

1.	**WEB-INF/lib**
    lokasi .jar untuk library yang dibutuhkan, jika menambah file di sini, maka restart apache tomcat anda.

2.	**(root)**
	lokasi semua JSP anda, JSP dibuat per halaman.

3.	**part**
	lokasi framgent JSP, yaitu JSP yang diinclude di halaman JSP lain.
	
4.	**classes**
	lokasi JSP yang hanya berisi definisi class yang dibutuhkan sebagai business logic. file khusus yang bernama load.jsp melakukan include semua file jsp di classes ini, dan akan diinclude oleh JSP utama di root.
	
5.	**img**
	lokasi image yang dibutuhkan di web 
	
6.	**js**
	lokasi javascript yang digunakan di web 
	
7.	**css**
	lokasi css yang dibutuhkan di web 

## Lisensi

Proyek ini tersedia untuk digunakan di bawah [Lisensi MIT](LICENSE). Silakan gunakan sebagai titik awal untuk proyek Anda!