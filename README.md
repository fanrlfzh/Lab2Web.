#membuat dokumen HTML
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CSS Dasar</title>
</head>
<body>
<header>
<h1>CSS Internal dan <i>Inline CSS</i></h1>
</header>
<nav>
<a href="lab2_css_dasar.html">CSS Dasar</a>
<a href="lab2_css_eksternal.html">CSS Eksternal</a>
<a href="lab1_tag_dasar.html">HTML Dasar</a>
</nav>
<!-- CSS ID Selector -->
<div id="intro">
<h1>Hello World</h1>
<p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman
Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat
adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML
dan CSS.</p>
<!-- CSS Class Selector -->
<a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>
</div>
</body>
</html>
![membuat file html](https://github.com/user-attachments/assets/03887c25-ed7b-4749-ab7f-335b2357ee58)


#mendeklarasikan CSS Internal
<head>
    <title>CSS Dasar</title>
    <style>
    body {
    font-family:'Open Sans', sans-serif;
    }
    header {
    min-height: 80px;
    border-bottom:1px solid #77CCEF;
    }
    h1 {
    font-size: 24px;
    color: #0F189F;
    text-align: center;
    padding: 20px 10px;
    }
    h1 i {
    color:#6d6a6b;
    }
    </style>
    </head>
![mendeklarasikan css](https://github.com/user-attachments/assets/dbf5e09f-2ef1-4ca2-9a1b-b9ec10a8a8a1)

#menambahkan Inline CSS
<p style="text-align: center; color: #ccd8e4;">
![menambahkan inline](https://github.com/user-attachments/assets/35e44e9c-353e-44df-83a8-f74cf4e66e46)

#membuat CSS Eksternal
nav {
    background: #20A759;
    color:#fff;
    padding: 10px;
    }
    nav a {
    color: #fff;
    text-decoration: none;
    padding:10px 20px;
    }
    nav .active,
    nav a:hover {
    background: #0B6B3A;
    }
![membuat css](https://github.com/user-attachments/assets/f7cefbda-c9ae-4191-a090-331a90d63889)

#menambahkan CSS Selector
/* ID Selector */
#intro {
    background: #418fb1;
    border: 1px solid #099249;
    min-height: 100px;
    padding: 10px;
    }
    #intro h1 {
    text-align: left;
    border: 0;
    color: #fff;
![css selector](https://github.com/user-attachments/assets/cc2ad243-7194-420d-82d7-4dd9834b0c54)

Pertanyaan dan Tugas
1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS
dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
h1 {
    color: blue;
    font-size: 24px;
    text-align: center;
}

#intro h1 {
    color: red;
    font-size: 30px;
}

p {
    font-size: 18px;
    color: green;
}

p {
    font-size: 16px;
    color: black;
}
![Screenshot (221)](https://github.com/user-attachments/assets/55738bbc-8473-4f23-bee3-2b0ef510648b)


2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan
penjelasannya!
h1 {...}:

Ini adalah aturan CSS yang mengubah semua elemen <h1> di halaman.

#intro h1 {...}:

Ini adalah aturan CSS yang hanya mengubah elemen <h1>yang berada di dalam elemen dengan ID intro . Hanya elemen <h1>di dalam elemen yang ID-nya "intro" yang dipengaruhi oleh aturan ini.

Kesimpulan:
h1 {...}: Mempengaruhi semua <h1> .
#intro h1 {...}: Mempengaruhi hanya <h1> di dalam elemen dengan ID intro.


3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada
elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan
penjelasan dan contohnya!
misalkan memiliki elemen HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <link rel="stylesheet" href="styles.css"> <!-- CSS Eksternal -->
  <style> <!-- CSS Internal -->
    p {
      color: green;
    }
  </style>
</head>
<body>
  <p style="color: red;">Ini paragraf contoh.</p> <!-- CSS Inline -->
</body>
</html>

1. CSS Eksternal :
Di dalam berkas styles.css:
p {
  color: blue;
}
Ini adalah gaya eksternal yang akan memberikan warna biru untuk elemen <p>.

2.CSS Internal :
Di dalam tag <style>:
p {
  color: green;
}
Ini memberikan warna hijau untuk elemen <p>, namun karena ini lebih spesifik daripada eksternal, warna dari internal CSS akan diterapkan jika tidak ada inline CSS .

3. CSS Sebaris :
Pada elemen <p>:
<p style="color: red;">Ini paragraf contoh.</p>
Ini secara langsung memberikan gaya pada elemen <p>dan memiliki prioritas tertinggi dibandingkan eksternal atau internal.

elemen <p>akan berwarna merah di browser karena inline CSS memiliki prioritas tertinggi. Meski ada deklarasi eksternal (biru) dan internal (hijau), browser akan menampilkan warna dari inline CSS.


4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut
terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser?
Berikan penjelasan dan contohnya! ( <p id="paragraf-1" class="text-paragraf"> )
Pemilih ID ( #paragraf-1) a<p>karena memiliki prioritasPemilih Kelas ( .text-paragraf)
Hasil akhir adalah elemen warna teks<p>aliasbiru .





    
