---
theme: default
title: 'Praktikum PBO Pertemuan 1'
highlighter: shiki
lineNumbers: false
info: |
  ## Praktikum PBO Pertemuan 1
  Pengenalan dasar pemrograman Java.

  Asisten Praktikum Pemrograman Berbasis Objek 2022.
  Teknik Informatika Universitas Padjadjaran.
drawings:
  persist: false
css: unocss
title: Welcome to Slidev
---

# Praktikum Pemrograman Berbasis Objek

**Pertemuan 1**

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Getting Started <carbon:arrow-right class="inline"/>
  </span>
</div>

---
class: text-center
css: unocss
---

# Asisten Praktikum PBO 2022

<div grid="~ cols-3 gap-2" m="-t-2">
  <span>Ariq</span>
  <span>Varo</span>
  <span>Muaz</span>
</div>

<div grid="~ cols-2 gap-2" m="-t-2">
  <span>Dicky</span>
  <span>Fahrio</span>
</div>

---

# Rules Praktikum 📃

1. Praktikan wajib mengikuti praktikum sesuai jadwal kelas masing-masing yaitu:
  - **Kelas A : Hari Selasa pukul 10.45 - 12.45**
  - **Kelas B : Hari Rabu pukul 08.00 - 10.00**
  <br>
  Apabila ada yang bentrok dengan jadwal yang lain harap menghubungi asprak.
2. Praktikan yang tidak mengikuti praktikum lebih dari **3 kali** tidak diperkenankan untuk mengikuti UAS.
3. Platform yang digunakan untuk praktikum PBO adalah Discord dan Github Classroom.
4. Absensi akan dibuka **15 menit** sejak awal pertemuan dimulai, diharapkan praktikan absen pada waktu tersebut. (baik discord maupun pertemuan secara hybrid/offline)
5. Praktikan diharap dapat mengikuti praktikum dengan baik, tidak menyontek, dan menjaga kerja sama yang sehat.
6. Untuk peraturan mendatang khusus mengenai Discord dan Github Classroom dapat dipantau di channel announcement Discord Praktikum PBO 2022.
7. Setiap akhir pertemuan praktikan diharap on-cam untuk dokumentasi. (online/hybrid)

---
layout: image-right
image: /img/penilaian.png
---

# Penilaian 📈

Presentase nilai yang diambil adalah:
- 30% dari tugas 
- 15% dari kuis
- 25% dari UTS
- 30% dari project UAS.

---

# Apa yang akan dipelajari?

<div grid="~ cols-2 gap-32" style="margin-bottom: 32px; margin-top:64px">
  <div>
    <h3>01</h3>
    <b>Konsep PBO</b>
    <p>Memahami konsep PBO terutama dalam bahasa Java</p>
  </div>
  <div>
    <h3>02</h3>
    <b>Pemrograman dalam Java</b>
    <p>Memahami struktur kode dan penerapan PBO dalam Java</p>
  </div>
</div>
<div grid="~ cols-2 gap-32">
  <div>
    <h3>03</h3>
    <b>Konsep PBO</b>
    <p>Memahami konsep PBO terutama dalam bahasa Java</p>
  </div>
  <div>
    <h3>04</h3>
    <b>Pemrograman dalam Java</b>
    <p>Memahami struktur kode dan penerapan PBO dalam Java</p>
  </div>
</div>

---

# Materi Pertemuan 1
<br>
<br>

<div grid="~ cols-2 gap-2" style="margin-bottom: 32px">

### 1. Struktur Kode Java
### 2. Membuat Objek dari Class

</div>

<div grid="~ cols-2 gap-2" style="margin-bottom: 32px">

### 3. Input & Output
### 4. Statements dalam Java

</div>

<div grid="~ cols-2 gap-2">

### 5. Compile & Run Kode Java
### 6. Built-in Methods

</div>


<div class="pt-12" style="margin-top: 96px">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Lanjut <carbon:arrow-right class="inline"/>
  </span>
</div>

---
highlighter: shiki
---

# Struktur Code Java (1)

```java {all|1|2-4|all}
public class HelloWorld {
    public static void main(String args[]){
      System.out.println("Hello World from Java!");
    }
}
```
<br>
<div grid="~ cols-2 gap-2">

  <div>

  ## Class 
  <br>

  - `public` : Access Modifier
  - `class` : Class keyword
  - `HelloWorld`: Name of Class

  </div>

  <div>

  ## Method 
  <br>

  - `static` : Static keyword
  - `void`: Return type
  - `main` : Method
  - `String args[]` : Parameter.

  `String args[]` as default parameter for method `main`

  </div>


</div>

---

# Struktur Code Java (2)

```java {all|2-3|5-8|10-13|15-18|all}
public class Ship {
  // Variable
  private int crew;

  // Constructor: Method yang dilakukan saat instansiasi class menjadi object
  public Ship(){
    this.crew = 24;
  }

  // Setter method: Method untuk assign variable dalam class
  public void setCrew(int crew){
    this.crew = crew;
  }

  // Getter method: Method untuk mengambil nilai variable suatu class
  public int getCrew(){
    return this.crew;
  }
}
```

---

# Membuat Object dari Class

<br>
<br>

```java {all|3|all}
public class Test {
  public static void main(String args[]){
    Ship ferry = new Ship();

    if (ferry.getCrew() < 30){
      ferry.setCrew(30);
    }

    System.out.println("The following ship has ", ferry.getCrew(), " crew.");
  }
}
```

Instantiasi class menjadi object dilakukan dengan keyword `new` diikuti dengan class yang akan dijadikan object

---

# Input dan Output

```java {all|1-2|6-7|9-11|13-15|17-18|all}
// import class Scanner dari pakcage java.util
import java.util.Scanner;

public class Test {
  public static void main(String args[]){
    // Instansiasi objek scanner
    Scanner sc = new Scanner(System.in);

    //Input dengan objek scanner
    String name = sc.nextLine();
    int age = Integer.parseInt(sc.nextLine());

    // Output dengan System.out
    System.out.println("Thy shall know i as " + name);
    System.out.println("for i ame " + age + " years old.");

    // Menutup objek scanner supaya tidak terjadi memory leak
    sc.close();
  }
}
```

---

# Statement dalam Java

Contoh if dan loop statement :
```java {all|3-8|all}
public class Loop{
  public static void main(String args[]){
    for(int i = 1; i <= 10; i++){
      if(i > 7){
        break;
      }
      System.out.println("Loop no. " + i);
    }
  }
}
```

Statement **if**, **else**, **for**, **while**, **do-while**, dan **switch** dalam bahasa pemrograman Java memiliki cara penulisan yang sama dengan bahasa pemrograman C++.

Berikut adalah contoh looping dan if for saat menggunakan Java, silahkan coba-coba statement lainnya.


---

# Compile and Run

## - Compile File Java
Untuk compile file java run command berikut di terminal:
```
javac FileName.java
```
Command diatas akan menghasilkan file baru dengan nama `FileName.java`

## - Run File Java
Untuk menjalankan file hasil compile run command berikut di terminal:
```
java FileName
```
Command diatas akan menjalankan hasil compile tanpa membawa type class-nya

---

# Important Things About Compile and Running Java

<br>
<br>

- Nama file `.java` harus sama dengan nama **class**-nya.

contoh : HelloWorld.java harus memiliki class bernama HelloWorld

- Dalam satu file `.java` dapat memiliki banyak class namun hanya diperbolehkan memiliki **satu** public class

- Disarankan unutk class yang bersifat public untuk memiliki filenya sendiri-sendiri

---

# Built-in Methods (1)

<div>
Dalam bahasa pemrograman Java, ada banyak built-in method dari class seperti String, Integer, Character, dll. yang dapat digunakan untuk mempermudah membuat suatu program. Contohnya :
</div>

<div style="margin-top: 16px">
  <div>
    <h3>string.isEmpty()</h3>
    <span>⮤	Mengecek apakah String kosong</span>
    <p>Contoh penggunaan : IF string.isEmpty() THEN …</p>
  </div>

  <div>
    <h3>string1.equals(string2)</h3>
    <span>⮤	Membanding string dengan output true atau false</span>
    <p>Contoh penggunaan : IF string1.equals(string2) THEN …</p>
  </div>

  <div>
    <h3>string1.concat(string2)</h3>
    <span>⮤	Menggabungkan dua string</span>
    <p>Contoh penggunaan : string3 = string1.concat(string2)</p>
  </div>
</div>
	
---

# Built-in Methods (2)

<br>
<div>
Contoh penggunaan Built-in Methods:
</div>

```java {all|5|all}
public class Test{
  public static void main(String args[]){
    String word1 = "Blood";
    String word2 = "Moon";
    System.out.println(word1.concat(word2));
  }
}
```

Untuk method lainnya dapat dicek melalui google atau documentation dari oracle pada link : 
https://docs.oracle.com/en/java/javase/16/docs/api/index.html

---
layout: center
class: text-center
---

# Exercise!
Seperti biasa akan setiap selesai praktikum pasti ada tugas

---
layout: center
class: text-center
---

# Teknis Pengumpulan
Pengerjaan dan pengumpulan tugas akan dilakukan di **Github Classroom**

<div grid="~ cols-2 gap-2" style="margin-top: 48px">
  <div>

  #### Kelas A:
  [Link Tugas Kelas A](https://google.com)

  </div>
  <div>

  #### Kelas B:
  [Link Tugas Kelas B](https://google.com)
  
  </div>
</div>

<br>
Accept assignment terlebih dahulu lalu link akun Github dengan slot nama yang sesuai di Github Classroom

---

# Teknis Pengumpulan

<div>
Format setiap file `.java` didahulukan dengan Nama, NPM, Kelas, Tanggal, dan Deskripsi
</div>

Cara menambah comment di java
```java {all}
// untuk single line
/* untuk multiple line */
```

Contoh Format
```java {all}
/*	
  Nama	: Jane Doe
  NPM		: 99
  Kelas		: A
  Tanggal	: 1 September 2021
  Deskripsi	: Class jawaban exercise-01 soal-01
*/

```

---
layout: center
class: text-center
---

# Deadline Pengumpulan

<div grid="~ cols-2 gap-32" style="margin-top: 48px">
  <div>

  #### Kelas A:
  12 September 2022, 23:59 WIB
  
  </div>
  <div>

  #### Kelas B:
  13 September 2022, 23:59 WIB
  
  </div>
</div>

<br>

**Waktu yang dilihat adalah waktu last commit.** Jika ada yang commit melewati deadline walaupun sudah commit sebelumnya akan dianggap telat

---
layout: center
class: text-center
---

# Terima Kasih!

Do you have any questions?
Please use respective class discussion channel on Discord.

Semangat terus menjalani kuilahnya!! 🔥🔥🔥
