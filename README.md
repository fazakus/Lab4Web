# Lab4Web

## Tugas Praktikum 4

Nama    : Faza Ardan Kusuma <br>
NIM     : 312010001<br>
Kelas   : TI 20 B1

<hr>

## Membuat Box Element

Buat file html dengan nama file <b>lab4_box.html</b>. Lalu disiapkan seperti biasa dan tambahkan syntax untuk membuat box element beserta CSSnya, maka berikut syntaxnya :<br>
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Box Element</title>
</head>
<body>
    <header>
        <h1>Box Element</h1>
    </header>
    <section> 
        <div class="div1">Div 1</div> 
        <div class="div2">Div 2</div> 
        <div class="div3">Div 3</div> 
    </section>
    <style> 
        div {
            float:left; 
            padding: 10px; 
        } 
        .div1 { 
            background: red; 
        } 
        .div2 { 
            background: yellow; 
        } 
        .div3 { 
            background: green; 
        } 
    </style>
</body>
</html>
```
Tampilan :<br>
![Membuat Box](Pic/boxelement1.png)<br>

Disini saya mencoba dengan mengubah <b>Clear</b> dan <b>float</b> dengan nilai lainnya, berikut saya rubah syntaxnya menjadi : <br>
```
    <style> 
        div {
            padding: 10px; 
            float: none;
        } 
        .div1 { 
            background: red;
            clear: left;
            float: right 
        } 
        .div2 { 
            background: yellow;
            clear: right;
            float: left;
        } 
        .div3 { 
            background: green;
            clear: both;
            float: none;
        }
        .div4 { 
            background-color: blue; 
            clear: right;
            float: left 
        }
    </style>
```

Tampilannya menjadi :<br>
![Box Element 2](Pic/boxelement2.png)<br>

Dari hasil percobaan tersebut, ketika float diisi dengan nilai <b>left</b> maka kolom warna posisinya akan ada di sebelah kiri(<i>Div 1</i>), bila dengan nilai <b>right</b> maka kolom warna akan ada di sebelah kanan (<i>Div 2</i>), bila diisi dengan <b>none</b> maka kolom warna menjadi sepanjang line tersebut (<i>Div 3</i>). 

## Membuat Layout Sederhana

### Membuat file HTML

Saya akan membuat layout sederhana seperti berikut : <br>
![Layout Sederhana](Pic/latihanlayoutweb.png)<br>

Pertama, buat folder baru dengan nama <b>Lab4_Layout</b>. Lalu buat file html baru didalamnya dengan dengan nama <b>home.html</b> dan buat kerangka layout dengan semantics element seperti berikut.<br>
![Semantics](Lab4_Layout/Pic/semantics.png)<br>
Maka syntaxnya seperti berikut :<br>
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header> 
            <h1>Layout Sederhana</h1> 
        </header> 
        <nav> 
            <a href="home.html" class="active">Home</a> 
            <a href="artikel.html">Artikel</a> 
            <a href="about.html">About</a> 
            <a href="kontak.html">Kontak</a> 
        </nav> 
        <section id="hero"></section> 
        <section id="wrapper"> 
            <section id="main"></section> 
            <aside id="sidebar"></aside> 
        </section> 
        <footer> 
            <p>&copy; 2021 - Universitas Pelita Bangsa</p> 
        </footer>
    </div>
    
</body>
</html>
```
Hasil dari syntax terserbut :<br>
![Layout Sederhana](Lab4_layout/Pic/layoutsederhana1.png)<br>

### Menambahkan File CSS
Untuk membuat tampilan menjadi lebih bagus, maka tambahkan CSS. Buat file CSS dengan nama <b>Style.css</b>.<br>
Lalu masukan syntax berikut.<br>
```
/* import google font */ 
@import 
url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap'); 
@import 
url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap'); 

/* Reset CSS */ 
* { 
    margin: 0; 
    padding: 0; 
} 
body { 
    line-height:1; 
    font-size:100%; 
    font-family:'Open Sans', sans-serif; 
    color:#5a5a5a; 
} 
#container { 
    width: 980px; 
    margin: 0 auto; 
    box-shadow: 0 0 1em #cccccc; 
} 

/* header */ 
header { 
    padding: 20px; 
} 
header h1 { 
    margin: 20px 10px; 
    color: #b5b5b5; 
}
```
Maka tampilannya akan berubah menjadi seperti berikut :<br>
![Add CSS](Lab4_layout/Pic/addcss.png)<br>

### Membuat Navigasi

Kemudian, saya akan buat navigasinya agar lebih enak dilihat dengan menambahkan CSS berikut :<br>
```
/* header */ 
header { 
    padding: 20px; 
} 
header h1 { 
    margin: 20px 10px; 
    color: #b5b5b5; 
}

/* navigasi */ 
nav { 
    display: block; 
    background-color: #1f5faa; 
} 
nav a { 
    padding: 15px 30px; 
    display: inline-block; 
    color: #ffffff; 
    font-size: 14px; 
    text-decoration: none; 
    font-weight: bold; 
} 
nav a.active, 
nav a:hover { 
    background-color: #2b83ea; 
}
```

Tampilan outputya :<br>
![Add CSS Nav](Lab4_Layout/Pic/addcssnav.png)<br>

### Membuat Hero Panel
Selanjutnya saya akan membuat hero panel. Tambahkan syntax berikut kedalam file html.<br>
```
<section id="hero">
    <h1>Hello World!</h1> 
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p> 
    <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
    </section>
```

Tampilan outputnya menjadi seperti berikut :<br>
![Add Hero Panel](Lab4_Layout/Pic/addheropanel.png)<br>

Lalu rapikan dengan menambahkan CSS. Tambahkan syntax berikut kedalam file CSS.<br>
```
/* Hero Panel */ 
#hero { 
    background-color: #e4e4e5; 
    padding: 50px 20px; 
    margin-bottom: 20px; 
} 
#hero h1 { 
    margin-bottom: 20px; 
    font-size: 35px; 
} 
#hero p { 
    margin-bottom: 20px; 
    font-size: 18px; 
    line-height: 25px; 
}
```

Maka tampilannya akan berubah menjadi :<br>
![Add CSS Hero Panel](Lab4_Layout/Pic/addcssheropanel.png)<br>

### Mengatur Layout Main dan Sidebar

